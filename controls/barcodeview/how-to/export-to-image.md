---
title: Export to Image
page_title: Export to Image | BarcodeView
description: RadBarcode is a set of components that can be used to create, show and read barcodes. 
slug: barcodeview-export-to-image 
tags: barcode
published: True
position: 0 
---

# Export to Image

**RadBarcodeView** supports export to image functionality.

You can export the **RadBarcodeView** content by using one of the following overloads of the **ExportToImage** method:

* **ExportToImage()** - Exports the barcode with the current dimentions of the control.
ExportToImage(int width, int height) 	Layouts the barcode using the provided dimentions and exports it to an image.

* **ExportToImage(Stream stream, Size size)** - Layouts the barcode using the provided size and exports it to the specified stream.

* **ExportToImage(string filePath, Size size)** - Layouts the barcode using the provided size and exports it to the specified file location.

* **ExportToImage(Stream stream, Size size, ImageFormat imageFormat)** - Layouts the barcode using the provided size and exports it to the specified stream in the specified image format.

* **ExportToImage(string filePath, Size size, ImageFormat imageFormat)** - Layouts the barcode using the provided size and exports it to the specified file location in the specified image format.

#### Export to Image

{{source=..\SamplesCS\BarcodeView\BarcodeViewGettingStarted.cs region=ExportToImage}} 
{{source=..\SamplesVB\BarcodeView\BarcodeViewGettingStarted.vb region=ExportToImage}} 

````C#

using (SaveFileDialog saveFileDialog = new SaveFileDialog())
{
    saveFileDialog.Filter = "Png (*.png)|*.png";
    saveFileDialog.FileName = "QRCode";
    if (saveFileDialog.ShowDialog() == DialogResult.OK)
    {
        Image img = radBarcodeView1.ExportToImage();
        img.Save(saveFileDialog.FileName, System.Drawing.Imaging.ImageFormat.Png);
    }
}           

````
````VB.NET

Using saveFileDialog As SaveFileDialog = New SaveFileDialog()
    saveFileDialog.Filter = "Png (*.png)|*.png"
    saveFileDialog.FileName = "QRCode"

    If saveFileDialog.ShowDialog() = DialogResult.OK Then
        Dim img As Image = radBarcodeView1.ExportToImage()
        img.Save(saveFileDialog.FileName, System.Drawing.Imaging.ImageFormat.Png)
    End If
End Using

````

{{endregion}} 

>caption Figure 1: Exported Barcode

![barcode-how-to-export-to-image 001](images/barcode-how-to-export-to-image001.png)

If you need to export the barcode data to a document, you can use a __RadDocument__ and [insert the exported image]({%slug winforms/richtexteditor-/document-elements/inline-image%}) into it. Afterwards, you can use the __RadRichTextEditor__ 's [export]({%slug winforms/richtexteditor/import-export/overview%}) functionality.

 
        
