## Accessibility

- 403: Provide a 403 - Access denied page.
- 404: Provide a 404 - Page not found page.
- [Custom Search](https://developers.google.com/structured-data/slsb-overview) - With Google Sitelink search box, people can reach your content more quickly.
- File not found: Avoid `404 FILE_NOT_FOUND` errors.
- Layout: Use `divs` instead of `tables` for layout. Using `tables` is not semantically correct.
- Moving a website: Redirect all your links to the new location via `.htaccess`.
- [Pagination](https://support.google.com/webmasters/answer/1663744) - Implement the `rel="next"` and `rel="prev"` attributes to links.
- [Performance](https://developers.google.com/webmasters/mobile-sites/mobile-seo/common-mistakes/slow-mobile-pages) - Performance and loading time is important.
- Redirects: Avoid redirects if possible. Use 301 redirect instead of 302.
- [RichSnippets](https://schema.org/) - Markup your code with rich snippets, they show up on the search results page.
- [Robots](https://en.wikipedia.org/wiki/Robots_exclusion_standard) - Block pages which should not be indexed via the `robots.txt` file or
  `<meta name="robots" content="">`.
- Validation: Write valid code ([HTML Validator](https://validator.w3.org/) [CSS Validator](https://jigsaw.w3.org/css-validator/)).
- [WAI-Aria](https://www.w3.org/TR/wai-aria/) - Use WAI-Aria tags to help machines understand your code.