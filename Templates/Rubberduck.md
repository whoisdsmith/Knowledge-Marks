---
Date: 2022-08-14
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: []
Alias: []
---

# Rubberduck

[[Rubberduck]] is probably the most prominent free [[VBA]] add-in. It covers a lot of functionality with the most important ones being:

-   **Refactoring**: You can easily rename functions and add, remove and reorder function arguments.
-   **Indentation**: Automatically indent your code either on function, module or project level.
-   **Navigation**: Rubberduck’s Code Explorer is a modern replacement for the built-in Project Explorer. It doesn’t stop at the module level but allows to quickly jump to a specific function or variable declaration. Very useful if you have modules with a lot of code and many functions!
-   **Code Inspection**: Rubberduck has multiple categories of code inspection that point out possible issues and allow you to improve your code quality with usually a single click. For example, it shows you if you use a variable that is not assigned, if you have unused procedures or if a parameter is implicitly passed by reference. Rubberduck also has a `Find all references` functionality that makes it easy to see where a certain function is called from.
-   **Bulk import and export of all VBA modules**: Without Rubberduck, you have to export/import each VBA module separately. In Rubberduck’s Code Explorer, you can use `Import...` and `Export Project...` respectively. Alternative: If bulk import/export is all you need, you can also use the [Excel VBA Developer Tools](http://vbatools.sourceforge.net/).

**Tip**: By default, Rubberduck shows a splash screen every time you startup the VBA editor. You can disable that by going to `Rubberduck` > `Settings` > `General Settings`, then un-check `Show splash screen at startup`.

The following screenshot shows Rubberduck’s `Refactor > Reorder Parameters` dialog:

![rubberduck reorder arguments](https://d33wubrfki0l68.cloudfront.net/a266d34576e8acf34670e794028e361a60073ea1/89df9/assets/images/blog/vba_tools/rubberduck.png)

***

## Appendix: Links and References

- [[Microsoft Excel]]
- [[Excel Developer Resources List]]
- [[Templates/VBA/_README|VBA]]
- [[Developer/Development]]
- [[Tools]]
- [[Developer Tools]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022