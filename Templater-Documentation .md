# Templater



[Templater](https://github.com/SilentVoid13/Templater) is a template language that lets you insert **variables** and **functions** results into your notes. It will also let you execute JavaScript code manipulating those variables and functions.

With [Templater](https://github.com/SilentVoid13/Templater), you will be able to create powerful templates to automate manual tasks.


The following template file, that is using [Templater](https://github.com/SilentVoid13/Templater) syntax:
    
    
    ---
    creation date: <% tp.file.creation_date() %>
    modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>
    ---
    
    << [[<% tp.date.now("YYYY-MM-DD", -1) %>]] | [[<% tp.date.now("YYYY-MM-DD", 1) %>]] >>
    
    # <% tp.file.title %>
    
    <% tp.web.daily_quote() %>



Will produce the following result when inserted:


    ---
    creation date: 2021-01-07 17:20
    modification date: Thursday 7th January 2021 17:20:43
    ---
    
    << [[2021-04-08]] | [[2021-04-10]] >>
    
    # Test Test
    
    > Do the best you can until you know better. Then when you know better, do better.
    > &mdash; <cite>Maya Angelou</cite>


**You can install this plugin via the Community Plugins tab within Obsidian. Search for "Templater".**

It's a good practice to restart the obsidian app after the installation of [Templater](https://github.com/SilentVoid13/Templater), to make sure everything is working properly.

**To understand how [Templater](https://github.com/SilentVoid13/Templater) works, let's define a few terms:**

* A **template** is a file that contains **[commands](./commands/overview.html)**.

* A text snippet that starts with an opening tag <%, ends with a closing tag %> is what we will call a **[command](./commands/overview.html)**.

* A **function** is an object that we can invoke inside a **command** and that returns a value (the replacement string)

* There are two types of functions you can use:

* [Internal functions](./internal-functions/overview.html). They are **predefined** functions that are built within the plugin. As an example, tp.date.now is an internal function that will return the current date.

* [User functions](./user-functions/overview.html). Users can define their own functions. They are either [system command](./user-functions/system-user-functions.html) or [user scripts](./user-functions/script-user-functions.html).

**The following template contains 2 commands, calling 2 different internal functions:**

  
Yesterday: <% tp.date.yesterday("YYYY-MM-DD") %>
Tomorrow: <% tp.date.tomorrow("YYYY-MM-DD") %>

We'll see in the next part the syntax required to write some commands.

 **[Templater](https://github.com/SilentVoid13/Templater) uses the [Eta](https://eta.js.org/) templating engine syntax to declare a command. You may need a bit of time to get used to it, but once you get the idea, the syntax is not that hard.**


All of Templater's functions are JavaScript objects that are invoked using a **command**.

**A command **must** have both an opening tag <% and a closing tag %>.** 

A complete command using the tp.date.now internal function would be: <% tp.date.now() %>


**All of Templater's functions, whether it's an internal function or a user function, are available under the tp object. You could say that all our functions are children of the tp object. To access the "child" of an object, we have to use the dot notation .**

This means that a Templater function invocation will always start with tp.<something>


### To invoke a function, we need to use a syntax specific to functions calls: appending an opening and a closing parenthesis after the function name. 

As an example, we would use tp.date.now() to invoke the tp.date.now internal function.

A function can have arguments and optional arguments. They are placed between the opening and the closing parenthesis, like so:

tp.date.now(arg1_value, arg2_value, arg3_value, ...)

All arguments must be passed in the correct order.


The arguments of a function can have different **types**. Here is a non-exhaustive list of the possible types of a function:


* A string type means the value must be placed within simple or double quotes ("value" or 'value')

* A number type means the value must be an integer (15, -5, ...)

* A boolean type means the value must be either true or false (completely lower case), and nothing else.

The type of an argument must be respected when calling a function, or it won't work.

### The documentation for the internal functions of Templater are using the following syntax:

tp.<my_function>(arg1_name: type, arg2_name?: type, arg3_name: type = <default_value>, arg4_name: type1|type2, ...)

Where:

* arg_name represents a **symbolic** name for the argument, to understand what it is.
* type represents the expected type for the argument. This type must be respected when calling the internal function, or it will throw an error.

If an argument is optional, it will be appended with a question mark ?, e.g. arg2_name?: type

If an argument has a default value, it will be specified using an equal sign =, e.g. arg3_name: type = <default_value>.

If an argument can have different types, it will be specified using a pipe |, e.g. arg4_name: type1|type2

####  Please note that this syntax is for documentation purposes only, to be able to understand what arguments the function expects. 

You mustn't specify the name nor the type nor the default value of an argument when calling a function. Only the value of the arguments are required, as explained [here](./syntax.html#function-invocation)


##### Let's take the tp.date.now internal function documentation as an example: 

tp.date.now(format: string = "YYYY-MM-DD", offset?: number|string, reference?: string, reference_format?: string)

This internal function has 4 optional arguments: 

* a format of type string, with a default value of "YYYY-MM-DD".

 *I an offset of type number or of type string.

* a reference of type string .

* a reference_format of type string .

That means that **valid invocations** for this internal function are:

* <% tp.date.now() %>

* <% tp.date.now("YYYY-MM-DD", 7) %>

* <% tp.date.now("YYYY-MM-DD", 7, "2021-04-09", "YYYY-MM-DD") %>

* <% tp.date.now("dddd, MMMM Do YYYY", 0, tp.file.title, "YYYY-MM-DD") %> *Assuming the file name is of the format: "YYYY-MM-DD"

On the other hand, **invalid invocations** are:

* tp.date.now(format: string = "YYYY-MM-DD")

* tp.date.now(format: string = "YYYY-MM-DD", offset?: 0)

You can set a Template folder location to tell [Templater](https://github.com/SilentVoid13/Templater) to only check this folder for templates.

You can set a timeout for your system commands with the Timeout option. A system command that takes longer than what you defined will be canceled and considered as a failure.


You can set [Templater](https://github.com/SilentVoid13/Templater) to be triggered on new file creation. It will listen for the new file creation event and replace every command it finds in the new file's content.

This makes Templater compatible with other plugins like the Daily note core plugin, Calendar plugin, Review plugin, Note refactor plugin, ...

## It can be dangerous if you create new files with unknown / unsafe content on creation. Make sure that every new file's content is safe on creation.

#### You can specify a template that will automatically be used on a selected folder and children using the Folder Templates functionality.

**Note**: This setting is hidden by default.  To view it first enable the Trigger Template on new file creation setting.



#### You can enable system commands. This allows you to create [user functions](./user-functions/overview.html) linked to system commands.


#### It can be dangerous to execute arbitrary system commands from untrusted sources. Only run system commands that you understand, from trusted sources.


cmd.exe and powershell on Windows are known to have problems with unicode characters.

You can check https://github.com/SilentVoid13/Templater/issues/15#issuecomment-824067020 for a solution.

Another good solution (probably the best) is to use [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701) and set it as the default shell in Templater's setting.

Another resource containing solutions that could work for you: <https://stackoverflow.com/questions/49476326/displaying-unicode-in-powershell>

The different internal variables and functions offered by [Templater](https://github.com/SilentVoid13/Templater) are available under different **modules**, to sort them. The existing **internal modules** are:
    
    
    
    
    
    
      * [Config module](internal-functions/./internal-modules/config-module.html): tp.config
    
    
      * [Date module](internal-functions/./internal-modules/date-module.html): tp.date
    
    
      * [File module](internal-functions/./internal-modules/file-module.html): tp.file
    
    
      * [Frontmatter module](internal-functions/./internal-modules/frontmatter-module.html): tp.frontmatter
    
    
      * [Obsidian module](internal-functions/./internal-modules/obsidian-module.html): tp.obsidian
    
    
      * [System module](internal-functions/./internal-modules/system-module.html): tp.system
    
    
      * [Web module](internal-functions/./internal-modules/web-module.html): tp.web

If you understood the [object hierarchy](internal-functions/../syntax.html#objects-hierarchy) correctly, this means that a typical internal function call looks like this:  <% tp.<module_name>.<internal_function_name> %>

I invite everyone to contribute to this plugin development by adding new internal functions. More information [here](internal-functions/./contribute.html).

This module exposes Templater's running configuration.

This is mostly useful when writing scripts requiring some context information.

* [Documentation](internal-functions/internal-modules/config-module.html#documentation)
    
        
            * [tp.config.active_file?](internal-functions/internal-modules/config-module.html#tpconfigactive_file)
        
        
            * [tp.config.run_mode](internal-functions/internal-modules/config-module.html#tpconfigrun_mode)
        
        
            * [tp.config.target_file](internal-functions/internal-modules/config-module.html#tpconfigtarget_file)
        
        
            * [tp.file.template_file](internal-functions/internal-modules/config-module.html#tpfiletemplate_file)
        
        


### tp.config.active_file?
    
    
    
    
    The active file (if existing) when launching Templater.
    
    
    
    
    ### tp.config.run_mode
    
    
    
    
    The RunMode, representing the way Templater was launched (Create new from template, Append to active file, ...)
    
    
    
    
    ### tp.config.target_file
    
    
    
    
    The TFile object representing the target file where the template will be inserted.
    
    
    
    
    ### tp.file.template_file
    
    
    
    
    The TFile object representing the template file.
    
    
    
    
    # 
    
    
    
    
    This module contains every internal function related to dates.
    
    
    
    
    
    
      * [Documentation](internal-functions/internal-modules/date-module.html#documentation)
    
        
            * [tp.date.now(format: string = "YYYY-MM-DD", offset?: number⎮string, reference?: string, reference_format?: string)](internal-functions/internal-modules/date-module.html#tpdatenowformat-string--yyyy-mm-dd-offset-numberstring-reference-string-reference_format-string)
        
        
            * [tp.date.tomorrow(format: string = "YYYY-MM-DD")](internal-functions/internal-modules/date-module.html#tpdatetomorrowformat-string--yyyy-mm-dd)
        
        
            * [tp.date.weekday(format: string = "YYYY-MM-DD", weekday: number, reference?: string, reference_format?: string)](internal-functions/internal-modules/date-module.html#tpdateweekdayformat-string--yyyy-mm-dd-weekday-number-reference-string-reference_format-string)
        
        
            * [tp.date.yesterday(format: string = "YYYY-MM-DD")](internal-functions/internal-modules/date-module.html#tpdateyesterdayformat-string--yyyy-mm-dd)
        
        
    
    
    
      * [Moment.js](internal-functions/internal-modules/date-module.html#momentjs)
    
    
      * [Examples](internal-functions/internal-modules/date-module.html#examples)
    
    
    
    
    ## 
    
    
    
    
    Function documentation is using a specific syntax. More information [here](internal-functions/internal-modules/../../syntax.html#function-documentation-syntax)
    
    
    
    
    ### tp.date.now(format: string = "YYYY-MM-DD", offset?: number⎮string, reference?: string, reference_format?: string)
    
    
    
    
    Retrieves the date.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * 
    
    
    format: Format for the date, refer to [format reference](https://momentjs.com/docs/#/displaying/format/)
    
    
    
    
    
      * 
    
    
    offset: Offset for the day, e.g. set this to -7 to get last week's date. You can also specify the offset as a string using the ISO 8601 format
    
    
    
    
    
      * 
    
    
    reference: The date referential, e.g. set this to the note's title
    
    
    
    
    
      * 
    
    
    reference_format: The date reference format.
    
    
    
    
    
    
    
    ### tp.date.tomorrow(format: string = "YYYY-MM-DD")
    
    
    
    
    Retrieves tomorrow's date.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * format: Format for the date, refer to [format reference](https://momentjs.com/docs/#/displaying/format/)
    
    
    
    
    ### tp.date.weekday(format: string = "YYYY-MM-DD", weekday: number, reference?: string, reference_format?: string)
    
    
    
    
    ##### 
    
    
    
    
    
    
      * 
    
    
    format: Format for the date, refer to [format reference](https://momentjs.com/docs/#/displaying/format/)
    
    
    
    
    
      * 
    
    
    reference: The date referential, e.g. set this to the note's title
    
    
    
    
    
      * 
    
    
    reference_format: The date reference format.
    
    
    
    
    
      * 
    
    
    weekday: Week day number. If the locale assigns Monday as the first day of the week, 0 will be Monday, -7 will be last week's day.
    
    
    
    
    
    
    
    ### tp.date.yesterday(format: string = "YYYY-MM-DD")
    
    
    
    
    Retrieves yesterday's date.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * format: Format for the date, refer to [format reference](https://momentjs.com/docs/#/displaying/format/)
    
    
    
    
    ## 
    
    
    
    
    Templater gives you access to the moment object, with all of its functionalities.
    
    
    
    
    More information on moment.js [here](https://momentjs.com/docs/#/displaying/)
    
    
    
    
    ## 
    
    
    
    
    
    Date now: <% tp.date.now() %>
    Date now with format: <% tp.date.now("Do MMMM YYYY") %>
    
    Last week: <% tp.date.now("dddd Do MMMM YYYY", -7) %>
    Today: <% tp.date.now("dddd Do MMMM YYYY, ddd") %>
    Next week: <% tp.date.now("dddd Do MMMM YYYY", 7) %>
    
    Last month: <% tp.date.now("YYYY-MM-DD", "P-1M") %>
    Next year: <% tp.date.now("YYYY-MM-DD", "P1Y") %>
    
    File's title date + 1 day (tomorrow): <% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>
    File's title date - 1 day (yesterday): <% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>
    
    Date tomorrow with format: <% tp.date.tomorrow("Do MMMM YYYY") %>    
    
    This week's monday: <% tp.date.weekday("YYYY-MM-DD", 0) %>
    Next monday: <% tp.date.weekday("YYYY-MM-DD", 7) %>
    File's title monday: <% tp.date.weekday("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
    File's title next monday: <% tp.date.weekday("YYYY-MM-DD", 7, tp.file.title, "YYYY-MM-DD") %>
    
    Date yesterday with format: <% tp.date.yesterday("Do MMMM YYYY") %>
    
    
    
    
    
    # 
    
    
    
    
    This module contains every internal function related to files.
    
    
    
    
    
    
      * [Documentation](internal-functions/internal-modules/file-module.html#documentation)
    
        
            * [tp.file.content](internal-functions/internal-modules/file-module.html#tpfilecontent)
        
        
            * [tp.file.create_new(template: TFile ⎮ string, filename?: string, open_new: boolean = false, folder?: TFolder)](internal-functions/internal-modules/file-module.html#tpfilecreate_newtemplate-tfile--string-filename-string-open_new-boolean--false-folder-tfolder)
        
        
            * [tp.file.creation_date(format: string = "YYYY-MM-DD HH:mm")](internal-functions/internal-modules/file-module.html#tpfilecreation_dateformat-string--yyyy-mm-dd-hhmm)
        
        
            * [tp.file.cursor(order?: number)](internal-functions/internal-modules/file-module.html#tpfilecursororder-number)
        
        
            * [tp.file.cursor_append(content: string)](internal-functions/internal-modules/file-module.html#tpfilecursor_appendcontent-string)
        
        
            * [tp.file.exists(filename: string)](internal-functions/internal-modules/file-module.html#tpfileexistsfilename-string)
        
        
            * [tp.file.find_tfile(filename: string)](internal-functions/internal-modules/file-module.html#tpfilefind_tfilefilename-string)
        
        
            * [tp.file.folder(relative: boolean = false)](internal-functions/internal-modules/file-module.html#tpfilefolderrelative-boolean--false)
        
        
            * [tp.file.include(include_link: string ⎮ TFile)](internal-functions/internal-modules/file-module.html#tpfileincludeinclude_link-string--tfile)
        
        
            * [tp.file.last_modified_date(format: string = "YYYY-MM-DD HH:mm")](internal-functions/internal-modules/file-module.html#tpfilelast_modified_dateformat-string--yyyy-mm-dd-hhmm)
        
        
            * [tp.file.move(new_path: string, file_to_move?: TFile)](internal-functions/internal-modules/file-module.html#tpfilemovenew_path-string-file_to_move-tfile)
        
        
            * [tp.file.path(relative: boolean = false)](internal-functions/internal-modules/file-module.html#tpfilepathrelative-boolean--false)
        
        
            * [tp.file.rename(new_title: string)](internal-functions/internal-modules/file-module.html#tpfilerenamenew_title-string)
        
        
            * [tp.file.selection()](internal-functions/internal-modules/file-module.html#tpfileselection)
        
        
            * [tp.file.tags](internal-functions/internal-modules/file-module.html#tpfiletags)
        
        
            * [tp.file.title](internal-functions/internal-modules/file-module.html#tpfiletitle)
        
        
    
    
    
      * [Examples](internal-functions/internal-modules/file-module.html#examples)
    
    
    
    
    ## 
    
    
    
    
    Function documentation is using a specific syntax. More information [here](internal-functions/internal-modules/../../syntax.html#function-documentation-syntax)
    
    
    
    
    ### tp.file.content
    
    
    
    
    Retrieves the file's content
    
    
    
    
    ### tp.file.create_new(template: TFile ⎮ string, filename?: string, open_new: boolean = false, folder?: TFolder)
    
    
    
    
    Creates a new file using a specified template or with a specified content.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * 
    
    
    filename: The filename of the new file, defaults to "Untitled".
    
    
    
    
    
      * 
    
    
    folder: The folder to put the new file in, defaults to obsidian's default location. If you want the file to appear in a different folder, specify it with app.vault.getAbstractFileByPath("FOLDERNAME")
    
    
    
    
    
      * 
    
    
    open_new: Whether to open or not the newly created file. Warning: if you use this option, since commands are executed asynchronously, the file can be opened first and then other commands are appended to that new file and not the previous file.
    
    
    
    
    
      * 
    
    
    template: Either the template used for the new file content, or the file content as a string. If it is the template to use, you retrieve it with tp.file.find_tfile(TEMPLATENAME)
    
    
    
    
    
    
    
    ### tp.file.creation_date(format: string = "YYYY-MM-DD HH:mm")
    
    
    
    
    Retrieves the file's creation date.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * format: Format for the date, refer to format reference
    
    
    
    
    ### tp.file.cursor(order?: number)
    
    
    
    
    Sets the cursor to this location after the template has been inserted. 
    
    
    
    
    You can navigate between the different tp.file.cursor using the configured hotkey in obsidian settings.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * order: The order of the different cursors jump, e.g. it will jump from 1 to 2 to 3, and so on.
    If you specify multiple tp.file.cursor with the same order, the editor will switch to multi-cursor.
    
    
    
    
    ### tp.file.cursor_append(content: string)
    
    
    
    
    Appends some content after the active cursor in the file.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * content: The content to append after the active cursor
    
    
    
    
    ### tp.file.exists(filename: string)
    
    
    
    
    Checks if a file exists or not. Returns a true / false boolean.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * filename: The filename of the file we want to check existence, e.g. MyFile.
    
    
    
    
    ### tp.file.find_tfile(filename: string)
    
    
    
    
    Search for a file and returns its TFile instance
    
    
    
    
    ##### 
    
    
    
    
    
    
      * filename: The filename we want to search and resolve as a TFile
    
    
    
    
    ### tp.file.folder(relative: boolean = false)
    
    
    
    
    Retrieves the file's folder name.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * relative: If set to true, appends the vault relative path to the folder name.
    
    
    
    
    ### tp.file.include(include_link: string ⎮ TFile)
    
    
    
    
    Includes the file's link content. Templates in the included content will be resolved.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * include_link: The link to the file to include, e.g. [[MyFile]], or a TFile object. Also supports sections or blocks inclusions, e.g. [[MyFile#Section1]]
    
    
    
    
    ### tp.file.last_modified_date(format: string = "YYYY-MM-DD HH:mm")
    
    
    
    
    Retrieves the file's last modification date.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * format: Format for the date, refer to format reference.
    
    
    
    
    ### tp.file.move(new_path: string, file_to_move?: TFile)
    
    
    
    
    Moves the file to the desired vault location.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * new_path: The new vault relative path of the file, without the file extension. Note: the new path needs to include the folder and the filename, e.g. /Notes/MyNote
    
    
    
    
    ### tp.file.path(relative: boolean = false)
    
    
    
    
    Retrieves the file's absolute path on the system.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * relative: If set to true, only retrieves the vault's relative path.
    
    
    
    
    ### tp.file.rename(new_title: string)
    
    
    
    
    Renames the file (keeps the same file extension).
    
    
    
    
    ##### 
    
    
    
    
    
    
      * new_title: The new file title.
    
    
    
    
    ### tp.file.selection()
    
    
    
    
    Retrieves the active file's text selection.
    
    
    
    
    ### tp.file.tags
    
    
    
    
    Retrieves the file's tags (array of string)
    
    
    
    
    ### tp.file.title
    
    
    
    
    Retrieves the file's title.
    
    
    
    
    ## 
    
    
    
    
    
    File content: <% tp.file.content %>
    
    File creation date: <% tp.file.creation_date() %>
    File creation date with format: <% tp.file.creation_date("dddd Do MMMM YYYY HH:mm") %>
    
    File creation: [[<% (await tp.file.create_new("MyFileContent", "MyFilename")).basename %>]]
    
    File cursor: <% tp.file.cursor(1) %>
    
    File cursor append: <% tp.file.cursor_append("Some text") %>
        
    File existence: <% await tp.file.exists("MyFolder/MyFile.md") %>
    
    File find TFile: <% tp.file.find_tfile("MyFile").basename %>
        
    File Folder: <% tp.file.folder() %>
    File Folder with relative path: <% tp.file.folder(true) %>
    
    File Include: <% tp.file.include("[[Template1]]") %>
    
    File Last Modif Date: <% tp.file.last_modified_date() %>
    File Last Modif Date with format: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm") %>
    
    File Move: <% await tp.file.move("/A/B/" + tp.file.title) %>
    File Move + Rename: <% await tp.file.move("/A/B/NewTitle") %>
    
    File Path: <% tp.file.path() %>
    File Path with relative path: <% tp.file.path(true) %>
    
    File Rename: <% await tp.file.rename("MyNewName") %>
    Append a "2": <% await tp.file.rename(tp.file.title + "2") %>
    
    File Selection: <% tp.file.selection() %>
    
    File tags: <% tp.file.tags %>
    
    File title: <% tp.file.title %>
    Strip the Zettelkasten ID of title (if space separated): <% tp.file.title.split(" ")[1] %>
    
    
    
    
    
    # 
    
    
    
    
    This modules exposes all the frontmatter variables of a file as variables.
    
    
    
    
    
    
      * [Documentation](internal-functions/internal-modules/frontmatter-module.html#documentation)
    
        
            * [tp.frontmatter.<frontmatter_variable_name>](internal-functions/internal-modules/frontmatter-module.html#tpfrontmatterfrontmatter_variable_name)
        
        
    
    
    
      * [Examples](internal-functions/internal-modules/frontmatter-module.html#examples)
    
    
    
    
    ## 
    
    
    
    
    ### tp.frontmatter.<frontmatter_variable_name>
    
    
    
    
    Retrieves the file's frontmatter variable value.
    
    
    
    
    If your frontmatter variable name contains spaces, you can reference it using the bracket notation like so: 
    
    
    
    
    
    <% tp.frontmatter["variable name with spaces"] %>
    
    
    
    
    
    ## 
    
    
    
    
    Let's say you have the following file:
    
    
    
    
    
    ---
    alias: myfile
    note type: seedling
    ---
    
    file content
    
    
    
    
    
    Then you can use the following template:
    
    
    
    
    
    File's metadata alias: <% tp.frontmatter.alias %>
    Note's type: <% tp.frontmatter["note type"] %>
    
    
    
    
    
    # 
    
    
    
    
    This module exposes all the functions and classes from the obsidian API.
    
    
    
    
    This is mostly useful when writing scripts. 
    
    
    
    
    Refer to the obsidian API [declaration file](https://github.com/obsidianmd/obsidian-api/blob/master/obsidian.d.ts) for more information.
    
    
    
    
    # 
    
    
    
    
    This module contains system related functions.
    
    
    
    
    
    
      * [Documentation](internal-functions/internal-modules/system-module.html#documentation)
    
        
            * [tp.system.clipboard()](internal-functions/internal-modules/system-module.html#tpsystemclipboard)
        
        
            * [tp.system.prompt(prompt_text?: string, default_value?: string, throw_on_cancel: boolean = false, multiline?: boolean = false)](internal-functions/internal-modules/system-module.html#tpsystempromptprompt_text-string-default_value-string-throw_on_cancel-boolean--false-multiline-boolean--false)
        
        
            * [tp.system.suggester(text_items: string[] ⎮ ((item: T) => string), items: T[], throw_on_cancel: boolean = false, placeholder: string = "", limit?: number = undefined)](internal-functions/internal-modules/system-module.html#tpsystemsuggestertext_items-string--item-t--string-items-t-throw_on_cancel-boolean--false-placeholder-string---limit-number--undefined)
        
        
    
    
    
      * [Examples](internal-functions/internal-modules/system-module.html#examples)
    
    
    
    
    ## 
    
    
    
    
    Function documentation is using a specific syntax. More information [here](internal-functions/internal-modules/../../syntax.html#function-documentation-syntax)
    
    
    
    
    ### tp.system.clipboard()
    
    
    
    
    Retrieves the clipboard's content
    
    
    
    
    ### tp.system.prompt(prompt_text?: string, default_value?: string, throw_on_cancel: boolean = false, multiline?: boolean = false)
    
    
    
    
    Spawns a prompt modal and returns the user's input.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * 
    
    
    default_value: A default value for the input field
    
    
    
    
    
      * 
    
    
    multiline: If set to true, the input field will be a multiline textarea
    
    
    
    
    
      * 
    
    
    prompt_text: Text placed above the input field
    
    
    
    
    
      * 
    
    
    throw_on_cancel: Throws an error if the prompt is canceled, instead of returning a null value
    
    
    
    
    
    
    
    ### tp.system.suggester(text_items: string[] ⎮ ((item: T) => string), items: T[], throw_on_cancel: boolean = false, placeholder: string = "", limit?: number = undefined)
    
    
    
    
    Spawns a suggester prompt and returns the user's chosen item.
    
    
    
    
    ##### 
    
    
    
    
    
    
      * 
    
    
    items: Array containing the values of each item in the correct order.
    
    
    
    
    
      * 
    
    
    limit: Limit the number of items rendered at once (useful to improve performance when displaying large lists)
    
    
    
    
    
      * 
    
    
    placeholder: Placeholder string of the prompt
    
    
    
    
    
      * 
    
    
    text_items: Array of strings representing the text that will be displayed for each item in the suggester prompt. This can also be a function that maps an item to its text representation.
    
    
    
    
    
      * 
    
    
    throw_on_cancel: Throws an error if the prompt is canceled, instead of returning a null value
    
    
    
    
    
    
    
    ## 
    
    
    
    
    
    Clipboard content: <% tp.system.clipboard() %>
    
    Entered value: <% tp.system.prompt("Please enter a value") %>
    Mood today: <% tp.system.prompt("What is your mood today ?", "happy") %>
    
    Mood today: <% tp.system.suggester(["Happy", "Sad", "Confused"], ["Happy", "Sad", "Confused"]) %>
    Picked file: [[<% (await tp.system.suggester((item) => item.basename, app.vault.getMarkdownFiles())).basename %>]]
    
    
    
    
    
    # 
    
    
    
    
    This modules contains every internal function related to the web (making web requests).
    
    
    
    
    
    
      * [Documentation](internal-functions/internal-modules/web-module.html#documentation)
    
        
            * [tp.web.daily_quote()](internal-functions/internal-modules/web-module.html#tpwebdaily_quote)
        
        
            * [tp.web.random_picture(size?: string, query?: string, include_size?: boolean)](internal-functions/internal-modules/web-module.html#tpwebrandom_picturesize-string-query-string-include_size-boolean)
        
        
    
    
    
      * [Examples](internal-functions/internal-modules/web-module.html#examples)
    
    
    
    
    ## 
    
    
    
    
    Function documentation is using a specific syntax. More information [here](internal-functions/internal-modules/../../syntax.html#function-documentation-syntax)
    
    
    
    
    ### tp.web.daily_quote()
    
    
    
    
    Retrieves and parses the daily quote from the API https://api.quotable.io
    
    
    
    
    ### tp.web.random_picture(size?: string, query?: string, include_size?: boolean)
    
    
    
    
    Gets a random image from https://unsplash.com/
    
    
    
    
    ##### 
    
    
    
    
    
    
      * 
    
    
    include_size: Optional argument to include the specified size in the image link markdown. Defaults to false
    
    
    
    
    
      * 
    
    
    query: Limits selection to photos matching a search term. Multiple search terms can be passed separated by a comma ,
    
    
    
    
    
      * 
    
    
    size: Image size in the format <width>x<height>
    
    
    
    
    
    
    
    ## 
    
    
    
    
    
    Web Daily quote:  
    <% tp.web.daily_quote() %>
    
    Web Random picture: 
    <% tp.web.random_picture() %>
    
    Web Random picture with size: 
    <% tp.web.random_picture("200x200") %>
    
    Web random picture with size + query: 
    <% tp.web.random_picture("200x200", "landscape,water") %>
    
    
    
    
    
    # 
    
    
    
    
    You can contribute to [Templater](https://github.com/SilentVoid13/Templater) by developing a new internal function / variable.
    
    
    
    
    The process to develop a new one is really easy.
    
    
    
    
    Keep in mind that only pertinent submissions will be accepted, don't submit a very specific internal variable / function that you'll be the only one using.
    
    
    
    
    ## 
    
    
    
    
    Internal variables / functions are sorted by modules. Each module has a dedicated folder under [src/InternalTemplates](https://github.com/SilentVoid13/Templater/tree/master/src/InternalTemplates). 
    
    
    
    
    Let's take the [date module](https://github.com/SilentVoid13/Templater/tree/master/src/InternalTemplates/date) as an example.
    
    
    
    
    It contains an [InternalModuleDate](https://github.com/SilentVoid13/Templater/blob/master/src/InternalTemplates/date/InternalModuleDate.ts) file where all our internal date's related variables and functions are defined and registered:
    
    
    
    
    
    export class InternalModuleDate extends InternalModule {
        name = "date";
    
        async createStaticTemplates() {
            this.static_templates.set("now", this.generate_now());
            this.static_templates.set("tomorrow", this.generate_tomorrow());
            this.static_templates.set("yesterday", this.generate_yesterday());
        }
    
        async updateTemplates() {}
    
        generate_now() {
            return (format: string = "YYYY-MM-DD", offset?: number, reference?: string, reference_format?: string) => {
                if (reference && !window.moment(reference, reference_format).isValid()) {
                    throw new Error("Invalid title date format, try specifying one with the argument 'reference'");
                }
                return get_date_string(format, offset, reference, reference_format);
            }
        }
    
        generate_tomorrow() {
            return (format: string = "YYYY-MM-DD") => {
                return get_date_string(format, 1);
            }
        }
    
        generate_yesterday() {
            return (format: string = "YYYY-MM-DD") => {
                return get_date_string(format, -1);
            }
        }
    }
    
    
    
    
    
    Every module extends the [InternalModule](https://github.com/SilentVoid13/Templater/blob/master/src/InternalTemplates/InternalModule.ts) abstract class, which means they contain the following attributes and methods:
    
    
    
    
    
    
      * this.app attribute: the obsidian API App object.
    
    
      * this.file attribute: The destination file where the template will be inserted.
    
    
      * this.plugin attribute: The Templater plugin object.
    
    
      * this.static_templates attribute: A map containing all (name; variable/function) that are static. A static variable / function means that it doesn't depend on the file when executed. These type of variables / functions won't be updated each time we insert a new template, to save some overhead.
    
    
      * this.dynamic_templates attribute: Same as static_templates except  that it contains variables / functions dependent on the file when executed.
    
    
      * this.createStaticTemplates() method: Registers all static internal variable / function for that module.
    
    
      * this.updateTemplates() method: Registers every dynamic internal variable / function for that module.
    
    
    
    
    You can use these attributes in your new internal variable / function if you need them.
    
    
    
    
    ## 
    
    
    
    
    Here are the different steps you need to follow, in order to register a new internal variable / function in a module.
    
    
    
    
    **1st step:** Create a method inside the module called generate_<internal_variable_or_function_name>() that will generate your internal variable / function, that means it will return either a lambda function (representing the internal function) or directly the internal variable you want to expose.
    
    
    
    
    All generation methods are ordered by alphabetical order based on the internal variable / function name.
    
    
    
    
    Try to give a good, self-explanatory name for your variable / function.
    
    
    
    
    **2nd step:** Register your internal variable / function in the static_templates or dynamic_templates map depending on whether your internal variable / function on the file when executed. The registration happens either in createStaticTemplates or updateTemplates.
    
    
    
    
    To register your variable / function, use your this.generate_<internal_variable_or_function_name>() method you defined earlier:
    
    
    
    
    
    this.static_templates.set(<internal_variable_or_function_name>, this.generate_<internal_variable_or_function_name>());
    OR
    this.dynamic_templates.set(<internal_variable_or_function_name>, this.generate_<internal_variable_or_function_name>());
    
    
    
    
    
    Internal variable / function registrations are also ordered by alphabetical order based on the variable / function name.
    
    
    
    
    **3rd step:** Add your internal variable / function documentation to Templater's [documentation](https://github.com/SilentVoid13/Templater/tree/master/docs/docs/internal-variables-functions/internal-modules).
    
    
    
    
    And you are done ! Thanks for contributing to [Templater](https://github.com/SilentVoid13/Templater) !
    
    
    
    
    Now, just submit a [pull request](https://github.com/SilentVoid13/Templater/pulls) on Github, I'll try to be as reactive as possible.
    
    
    
    
    # 
    
    
    
    
    You can define your own functions in Templater.
    
    
    
    
    There are two types of user functions you can use:
    
    
    
    
    
    
      * [Script User Functions](user-functions/./script-user-functions.html)
    
    
      * [System Command User Functions](user-functions/./system-user-functions.html)
    
    
    
    
    ## 
    
    
    
    
    You can call a user function using the usual function call syntax: tp.user.<user_function_name>(), where <user_function_name> is the function name you defined. 
    
    
    
    
    For example, if you defined a system command user function named echo, a complete command invocation would look like this:
    
    
    
    
    
    <% tp.user.echo() %>
    
    
    
    
    
    ## 
    
    
    
    
    Currently user functions are unavailable on Obsidian for mobile.
    
    
    
    
    # 
    
    
    
    
    This type of user functions allows you to call JavaScript functions from JavaScript files and retrieve their output.
    
    
    
    
    To use script user functions, you need to specify a script folder in Templater's settings. This folder needs to be accessible from your vault. 
    
    
    
    
    ## 
    
    
    
    
    Let's say you specified the Scripts folder as your script folder in Templater's settings.
    
    
    
    
    Templater will load all JavaScript (.js files) scripts in the Scripts folder.
    
    
    
    
    You can then create your script named Scripts/my_script.js (The .js extension is required) for example.
    
    
    
    
    You will then be able to call your scripts as user functions. The function name corresponds to the script file name.
    
    
    
    
    Scripts should follow the [CommonJS module specification](https://flaviocopes.com/commonjs/), and export a single function.
    
    
    
    
    Let's have an example with our previous script my_script.js.
    
    
    
    
    Note that instead of outputting directly to the console, as we did earlier, a user script needs to return its output:
    
    
    
    
    
    function my_function (msg) {
        return "Message from my script:";
    }
    module.exports = my_function;
    
    
    
    
    
    In our previous example, a complete command invocation would look like this: 
    
    
    
    
    
    <% tp.user.my_script("Hello World!") %>
    
    
    
    
    
    Which would print Message from my script: Hello World! in the console.
    
    
    
    
    ## 
    
    
    
    
    In script user functions, you can still access global namespace variables like app or moment.
    
    
    
    
    However, you can't access Eta scoped variables like tp or tR. If you want to use them, you must pass them as arguments for your function.
    
    
    
    
    ## 
    
    
    
    
    You can pass as many arguments as you want to your function, depending on how you defined it.
    
    
    
    
    You can for example pass the tp object to your function, to be able to use all of the [internal variables / functions](user-functions/../internal-variables-functions/overview.html) of Templater: <% tp.user.<user_function_name>(tp) %>
    
    
    
    
    # 
    
    
    
    
    This type of user functions allows you to execute system commands and retrieve their output.
    
    
    
    
    System command user functions need to be enabled in Templater's settings.
    
    
    
    
    ## 
    
    
    
    
    To define a new system command user function, you need to define a **function name**, associated with a **system command**.
    
    
    
    
    To do that, go to the plugin's settings and click Add User Function.
    
    
    
    
    Once this is done, [Templater](https://github.com/SilentVoid13/Templater) will create a user function named after what you defined, that will execute your system command and return its output.
    
    
    
    
    Just like internal functions, user functions are available under the tp JavaScript object, and more specifically under the tp.user object.
    
    
    
    
    ![user_templates](user-functions/../imgs/templater_user_templates.png)
    
    
    
    
    ## 
    
    
    
    
    You can pass optional arguments to user functions. They must be passed as a single JavaScript object containing properties and their corresponding values: {arg1: value1, arg2: value2, ...}.
    
    
    
    
    These arguments will be made available for your programs / scripts in the form of [environment variables](https://en.wikipedia.org/wiki/Environment_variable).
    
    
    
    
    In our previous example, this would give the following command declaration: <% tp.user.echo({a: "value 1", b: "value 2"}). 
    
    
    
    
    If our system command was calling a bash script, we would be able to access variables a and b using $a and $b.
    
    
    
    
    ## 
    
    
    
    
    You can use internal functions inside your system command. The internal functions will be replaced before your system command gets executed.
    
    
    
    
    For example, if you configured the system command cat <% tp.file.path() %>, it would be replaced with cat /path/to/file before the system command gets executed.
    
    
    
    
    # 
    
    
    
    
    ## 
    
    
    
    
    [Templater](https://github.com/SilentVoid13/Templater) defines 3 types of opening tags, that defines 3 types of **commands**:
    
    
    
    
    
    
      * <%:  Raw display command. It will just output the expression that's inside.
    
    
      * <%~: Interpolation command. Same as the raw display tag, but adds some character escaping.
    
    
      * <%*: [JavaScript execution command](commands/./execution-command.html). It will execute the JavaScript code that's inside. It does not output anything by default.
    
    
    
    
    The closing tag for a command is always the same: %>
    
    
    
    
    ## 
    
    
    
    
    In addition to the 3 different types of commands, you can also use command utilities. They are also declared in the opening tag of the command, and they work with all the command types. Available command utilities are:
    
    
    
    
    
    
      * [Whitespace Control](commands/./whitespace-control.html)
    
    
      * [Dynamic Commands](commands/./dynamic-command.html)
    
    
    
    
    # 
    
    
    
    
    With this command utility, you can declare a command as "dynamic", which means that this command will be resolved when entering preview mode.
    
    
    
    
    To declare a dynamic command add a plus + sign after the command opening tag: <%+
    
    
    
    
    That's it, your command will now be executed only in preview mode.
    
    
    
    
    This is useful for internal functions like tp.file.last_modified_date for example:
    
    
    
    
    
    Last modified date: <%+ tp.file.last_modified_date() %>
    
    
    
    
    
    ## 
    
    
    
    
    One "downside" of the preview mode is that it puts the rendered note in cache, to speed things up.
    
    
    
    
    This means that your dynamic command will be rendered only once, when you open the note, but won't be refreshed after.
    
    
    
    
    If you want to refresh it, you must close the note to clear the cache and open it again.
    
    
    
    
    # 
    
    
    
    
    This type of command allows us to execute JavaScript code.
    
    
    
    
    With a JavaScript Execution command, we can pretty much do everything that JavaScript allows us to do. Some examples are given below.
    
    
    
    
    We can still access the tp object and all the internal variables / functions from this type of command.
    
    
    
    
    JavaScript Execution commands let you access global namespace variables. This means you can access things like app or moment.
    
    
    
    
    ## 
    
    
    
    
    Some internal functions are asynchronous. When calling such functions inside a JavaScript execution command, don't forget to use the await keyword if necessary.
    
    
    
    
    ## 
    
    
    
    
    Sometimes, you may want to output something when using a JS execution command. This is possible although a raw display / interpolation command is preferable.
    
    
    
    
    When the [Eta](https://eta.js.org/) templating engine generates a replacement string using all of our commands results, it is stored in a variable named tR. This is the string that will contain the processed file content. You are allowed to access that variable from a JS execution command.
    
    
    
    
    This means that, to output something from a JS execution command, you just need to append what you want to output to that tR string variable.
    
    
    
    
    For example, the following command: <%* tR += "test" %> will output test.
    
    
    
    
    ## 
    
    
    
    
    Here are some examples of things you can do using JavaScript Execution Commands:
    
    
    
    
    
    <%* if (tp.file.title.startsWith("Hello")) { %>
    This is a hello file !
    <%* } else { %>
    This is a normal file !
    <%* } %>
        
    <%* if (tp.frontmatter.type === "seedling") { %>
    This is a seedling file !
    <%* } else { %>
    This is a normal file !
    <%* } %>
        
    <%* if (tp.file.tags.contains("#todo")) { %>
    This is a todo file !
    <%* } else { %>
    This is a finished file !
    <%* } %>
    
    <%*
    function log(msg) {
        console.log(msg);
    }
    %>
    <%* log("Title: " + tp.file.title) %>
        
    <%* tR += tp.file.content.replace(/stuff/, "things"); %>
    
    
    
    
    
    # 
    
    
    
    
    By default, **commands** in Templater are not removing any newlines. Commands are replaced with their values and that's it.
    
    
    
    
    It can sometimes be useful to have some whitespace control after commands are inserted, which is exactly what this command utility offers.
    
    
    
    
    Let's have an example. The following template:
    
    
    
    
    
    <%* if (tp.file.title == "MyFile" ) { %>
    This is my file!
    <%* } else { %>
    This isn't my file!
    <%* } %>
    Some content ...
    
    
    
    
    
    Will produce the following output if the condition is false (the same happens when it's true), notice the blank lines:
    
    
    
    
    
    This isn't my file!
    
    Some content ...
    
    
    
    
    
    You may want to remove the blank lines produced by the **execution commands**, that do not produce any output.
    
    
    
    
    A specific syntax exists for whitespace control:
    
    
    
    
    
    
      * An underscore _ at the **beginning** of a tag (<%_) will trim **all** whitespace **before** the command
    
    
      * An underscore _ at the **end** of a tag (_%>) will trim **all** whitespace **after** the command
    
    
      * A dash - at the **beginning** of a tag (<%-) will trim **one** newline **before** the command
    
    
      * A dash - at the **end** of a tag (-%>) will trim **one** newline **after** the command.
    
    
    
    
    In our example, to fix our template to remove the blank lines, we would use the following template (notice the dashes - at the end of the tags), to remove the blank newlines **after** the execution commands:
    
    
    
    
    
    <%* if (tp.file.title == "MyFile" ) { -%>
    This is my file!
    <%* } else { -%>
    This isn't my file!
    <%* } -%>
    Some content ...
    
    
    
    
    
    Which would produce the following output:
    
    
    
    
    
    This isn't my file!
    Some content ...
    
    
    
    
                        
    
    
    


___

#article Templater 