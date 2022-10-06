# Custom Search Engines in Firefox
---
[Ready2Search](https://ready.to/search/en/#) is a website that generates the [OpenSearch](https://developer.mozilla.org/en-US/docs/Web/OpenSearch) XML file for Firefox.

1. Navigate to https://ready.to/search/en/# in Firefox.
2. Enter a descriptive name.
3. Enter everything before the search term (`%s` in the README.md examples) in the `Url-template(prefix)` textbox.
4. Enter everything after the search term in the `Url-template(suffix)` textbox.
5. (Optional) Enter a description for the search engine
6. (Optional) Download the favicon.ico for the website, upload it, and select `original color`.
7.  Press `Make Search Plug-in` to generate the XML.
8. Press `OpenSearch plug-in` to add it to Firefox.
9. Navigate to `about:preferences#search` and add the keyword that will trigger the search. Optionally, uncheck the box to remove it as a suggested search engine in the address bar.
10. Open a new tab, type the keyword, hit space, and then your search.\
---