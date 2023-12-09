# Ebook

A compilation of PDFs

## Instructions

Pull pdfs:

```
wget --execute="robots = off" --mirror --convert-links --no-parent --wait=0.1 http://mileswmathis.com/
```

Compile document

```
pdflatex ebook.tex
```

Compress document

```
gs \
  -sDEVICE=pdfwrite \
  -sOutputFile=compressed.pdf \
  -dCompatibilityLevel=1.4 \
  -dPDFSETTINGS=/screen \
  -dNOPAUSE \
  -dQUIET \
  -dBATCH \
  -dDownsampleColorImages=true \
  -dDownsampleGrayImages=true \
  -dDownsampleMonoImages=true \
  -dColorImageResolution=72 \
  -dGrayImageResolution=72 \
  -dMonoImageResolution=72 \
  -dDetectDuplicateImages=true \
  -dEmbedAllFonts=false \
  -dSubsetFonts=true \
  -dConvertCMYKImagesToRGB=true \
  -dCompressFonts=true \
  "ebook.pdf"

```
