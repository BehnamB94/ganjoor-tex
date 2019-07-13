# Ganjoor-TeX

Ganjoor-TeX is a set of scripts to convert the content of the ganjoor.net (a Persian poetry) website into LaTeX files.

## Getting started

### Html to Text

The script `html2txt.py` reads the content of the ganjoor.net and creates text files.

```
usage:   ./html2txt.py <ganjoor link> <txt directory>

example: ./html2txt.py https://ganjoor.net/moulavi/masnavi/daftar1/ moulavi/masnavi/daftar1/
```

### Text to TeX

The script `txt2tex.py` reads the content of text files generated by `html2txt.py` and creates TeX files.

```
usage:   ./txt2tex.py <txt directory> <tex directory>

example: ./txt2tex.py ../txt/moulavi/masnavi/daftar1/ moulavi/masnavi/daftar1/
```

### TeX to PDF

Using `xelatex` the TeX files generated by `txt2tex.py` are converted into PDF files. 

```
usage:   xelatex <tex file>

example: xelatex daftar1.tex
```

The [Persian fonts](https://github.com/ganjoor/persian-fonts-linux) must have been installed before compiling the TeX files.

```
git clone https://github.com/ganjoor/persian-fonts-linux.git

./farsifonts.sh
```