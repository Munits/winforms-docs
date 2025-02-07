---
title: Overview
page_title: PDF417 | BarcodeView
description: PDF417 is a stacked linear barcode symbol format used in a variety of applications, primarily transport, identification cards, and inventory management. 
slug: barcodeview-barcode-types-2d-barcodes-pdf417-overview 
tags: barcode, pdf417
published: True
position: 0 
---

# Overview

PDF417 is a stacked linear barcode symbol format used in a variety of applications, primarily transport, identification cards, and inventory management. PDF stands for Portable Data File. The 417 signifies that each pattern in the code consists of 4 bars and spaces, and that each pattern is 17 units long. The PDF417 symbology was invented by Dr. Ynjiun P. Wang at Symbol Technologies in 1991. (Wang 1993) It is represented by ISO standard 15438.

>caption Figure 1. PDF417 RadBarcodeView

![winforms/barcode-2d-barcodes-pdf417-overview 001](images/barcode-2d-barcodes-pdf417-overview001.png)

## Visual Structure

The code is divided into rows and columns, which accommodate all the encoded data, the error correction code words, as well as any additional format information, such as start and stop sequences.

The PDF417 barcode has the following structure:


>caption Figure 2. PDF417 RadBarcodeView's structure

![winforms/barcode-2d-barcodes-pdf417-overview 002](images/barcode-2d-barcodes-pdf417-overview002.png)

The Data codewords are located in the middle section of the barcode and include the following sections:

1. The length indicator cluster (each cluster contains 17 modules), which signifies the total length of the data code words.
2. The actual data, which represents the data entered by the user initially, encoded.
3. The error correction cluster(s), which help the decoder in recovering any data from the code.
4. Padding cluster(s) – since a rectangular matrix is allocated for the data code words, it may become necessary to pad the data, and add one or more clusters, in order to fill any gaps in the available matrix.

The Left Row Indicator codewords, as well as the Right Row Indicator codewords help the decoder locate each row. Essentially the row indicators represent an encoding of the row number.

The Start and Stop patterns are present on each row in the PDF417. The signal when the data and row indicators start and end. Each start/stop cluster is identical for each row.

Additionally, there is a minimum of two modules on each side of the PDF417 barcode, dedicated to the quiet zone. This gives space and separates the barcode from other visual elements on the page, allowing the reader to more reliably detect it.
 
