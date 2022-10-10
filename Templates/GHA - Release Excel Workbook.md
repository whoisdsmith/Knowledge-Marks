---
Date: 2022-08-06
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/GHA", "#Topic/Dev/VBA", "#Topic/Tools/Excel"]
Alias: []
---



# GHA - Release Excel Workbook

*Source: [release-excel-workbooks/main.yml at master · xlwings/release-excel-workbooks · GitHub](https://github.com/xlwings/release-excel-workbooks/blob/master/.github/workflows/main.yml)*

```yaml
name: Release Pipeline

on:
  release:
    types:
      - created

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Upload Excel file to GitHub Release Page
        if: github.event_name == 'release'
        uses: actions/upload-release-asset@v1.0.1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          upload_url: ${{ github.event.release.upload_url }}
          asset_path: ./mybook.xlsx
          asset_name: mybook-${{ github.event.release.tag_name }}.xlsx
          asset_content_type: application/zip
```

***

## Appendix: Links and References

- [[_README 3|Code]]
- [[Developer/Development]]
- [[Templates/GitHub Actions/_README|GitHub Actions]]
- [[Templates/VBA/_README|VBA]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022