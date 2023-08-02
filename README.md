## 📌 Introduction

This is a PDF generator for document Apache Doris Website.

## ⚡ Usage

```shell
node --max-old-space-size=8192 ./lib/cli.js --initialDocURLs="https://doris.apache.org/zh-CN/docs/dev/get-starting/" --paginationSelector=".pagination-nav__link--next" --contentSelector="article" --coverImage="https://cdn.selectdb.com/static/doris_logo_512_4903556647.png" --coverTitle="Apache Doris Docs (中文)" --outputPDFFilename="Apache Doris Docs (中文).pdf" --tocOnlyH1=true
```

## 🍗 CLI Options

| Option                   | Required | Description                                                                                                                                                                                 |
| ------------------------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `--initialDocURLs`     | Yes      | set URL to start generating PDF from.                                                                                                                                                       |
| `--contentSelector`    | Yes      | used to find the part of main content                                                                                                                                                       |
| `--paginationSelector` | Yes      | CSS Selector used to find next page to be printed for looping.                                                                                                                              |
| `--excludeURLs`        | No       | URLs to be excluded in PDF                                                                                                                                                                  |
| `--excludeSelectors`   | No       | exclude selectors from PDF. Separate each selector**with comma and no space**. But you can use space in each selector. ex: `--excludeSelectors=".nav,.next > a"`                    |
| `--cssStyle`           | No       | CSS style to adjust PDF output ex:`--cssStyle="body{padding-top: 0;}"` \*If you're project owner you can use `@media print { }` to edit CSS for PDF.                                    |
| `--outputPDFFilename`  | No       | name of the output PDF file. Default is `mr-pdf.pdf`                                                                                                                                      |
| `--pdfMargin`          | No       | set margin around PDF file. Separate each margin**with comma and no space**. ex: `--pdfMargin="10,20,30,40"`. This sets margin `top: 10px, right: 20px, bottom: 30px, left: 40px` |
| `--pdfFormat`          | No       | pdf format ex:`--pdfFormat="A3"`. Please check this link for available formats [Puppeteer document](https://pptr.dev/#?product=Puppeteer&version=v5.2.1&show=api-pagepdfoptions)             |
| `--disableTOC`         | No       | Optional toggle to show the table of contents or not                                                                                                                                        |
| `--coverTitle`         | No       | Title for the PDF cover.                                                                                                                                                                    |
| `--coverImage`         | No       | `<src>` Image for PDF cover (does not support SVG)                                                                                                                                        |
| `--coverSub`           | No       | Subtitle the for PDF cover. Add `` tags for multiple lines.                                                                                                                                 |
| `--headerTemplate`     | No       | HTML template for the print header. Please check this link for details of injecting values[Puppeteer document](https://pptr.dev/#?product=Puppeteer&show=api-pagepdfoptions)                   |
| `--footerTemplate`     | No       | HTML template for the print footer. Please check this link for details of injecting values[Puppeteer document](https://pptr.dev/#?product=Puppeteer&show=api-pagepdfoptions)                   |
| --buildDirPath           | No       | location of build directory                                                                                                                                                                 |
| --firstDocPath           | No       | location of first doc path                                                                                                                                                                  |
