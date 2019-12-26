# qtpdf - Qt-based PDF viewing based on pdfium

[See here for some background](https://www.qt.io/blog/2017/01/30/new-qtpdf-qtlabs-module).

QPdfDocument can render a PDF page to a QImage, and there is QPdfBookmarkModel which can be used for a bookmarks view. There is an example application: a widget-based PDF viewer.

If you want to try it out, here's how to get started:

```bash
git clone git://code.qt.io/qt-labs/qtpdf

cd qtpdf
git submodule update --init --recursive
qmake
make

cd examples/pdf/pdfviewer
qmake
make

./pdfviewer /path/to/my/file.pdf
```
