# 📄 Filely

**Filely** is a lightweight Windows desktop utility that extracts key identifiers from delivery PDFs using OCR and renames the files for streamlined archiving. It’s designed for logistics teams, warehouse admins, and anyone who needs to organize scanned packing lists or delivery notes.

---

## 🚀 Features

- ✅ Extracts **Delivery Number** and **Shipment Number** from scanned PDFs
- ✅ Uses **Tesseract OCR** (open-source) for text recognition
- ✅ Automatically renames the original PDF to:  
  `DeliveryNumber-ShipmentNumber-XXXXX.pdf`
- ✅ Deletes temporary OCR output after processing
- ✅ Handles messy OCR formatting with regex-based resilience
- ✅ No paid dependencies — fully deployable with free libraries

---

## 🛠️ How It Works

1. **Upload a PDF**  
   Filely reads the first page and converts it to an image using ImageMagick.

2. **Run OCR**  
   Tesseract extracts text from the image.

3. **Parse Identifiers**  
   Regex scans for 9+ digit Delivery and Shipment Numbers.

4. **Rename PDF**  
   The file is renamed using the extracted values and a random 5-digit suffix.

5. **Cleanup**  
   Temporary `.txt` and image files are deleted.

---

## 📦 Dependencies

- [.NET Framework or .NET Core](https://dotnet.microsoft.com/)
- [Tesseract OCR](https://github.com/charlesw/tesseract)
- [ImageMagick](https://imagemagick.org/)
- [PdfPig (optional)](https://github.com/UglyToad/PdfPig) — if you want to avoid Ghostscript

---

## 🧰 Setup Instructions

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/filely.git
