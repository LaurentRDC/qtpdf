# qtpdf - Qt-based PDF viewing based on pdfium

[See here for some background](https://www.qt.io/blog/2017/01/30/new-qtpdf-qtlabs-module).

QPdfDocument can render a PDF page to a QImage, and there is QPdfBookmarkModel which can be used for a bookmarks view. There is an example application: a widget-based PDF viewer.

If you want to try it out, here's how to get started:

```bash
git clone https://github.com/LaurentRDC/qtpdf

cd qtpdf
git submodule update --init --recursive
qmake
make

cd examples/pdf/pdfviewer
qmake
make

./pdfviewer /path/to/my/file.pdf
```

## Installing manually on Windows

Changes are, you don't have the right build environment on Windows. In order to install on Windows, you can do the following:

1. Download the source and prepare the submodules:

    ```bash
    git clone https://github.com/LaurentRDC/qtpdf
    cd qtpdf
    git submodule update --init --recursive
    ```

2. Open the `qtpdf.pro` file in Qt Creator. Configure the projects using the kits with which you will use QtPdf.

3. Run qmake. This is important because some files are created during this phase.

4. Build all subprojects. Make sure Debug and Release are both built. 

5. Copy the resulting files in `bin`, `include`, `lib`, and `mkspecs` to the equivalent folders in the appropriate version of Qt (e.g. C:/Qt/5.14.0/msvc2017_64/). 

After this, you can use the classes defined herein by adding the following to your `.pro` file:

```
QT += pdf pdfwidgets
```

After this, the example shown in this repository will work properly.