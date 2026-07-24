readme_content = """# FadCode Generator 🚀

**FadCode Generator** is a powerful, lightweight, and 100% free web application designed to generate and scan static QR Codes and Barcodes. Say goodbye to intermediary links and annoying ads! With FadCode, your generated codes point directly to your destination securely and instantly.

---

## 🌟 Key Features

### 🎨 General
* **Clean & Modern UI**: Built with Tailwind CSS for a sleek, responsive design that looks great on both desktop and mobile.
* **Dark/Light Mode**: Fully supports user-preferred color schemes with an easy toggle button.
* **Ad-Free & Static**: Generates raw, static codes. No dynamic redirects, no hidden subscriptions, and no inserted advertisements. 100% free.

### 🪄 Generator
* **QR Code Generation**: 
  * Create custom QR codes for text, URLs, or hidden messages.
  * Customize foreground and background colors.
  * Select resolution sizes (Small, Medium, Large).
  * **Logo Support**: Upload a custom image or logo (supports transparent PNGs) to be embedded directly into the center of the QR code.
* **Barcode Generation**:
  * Generate high-quality CODE128 barcodes.
  * Toggle the display of text below the barcode.
  * Customize colors and sizes.
* **Instant Export**: Preview your generated code and download it instantly as a high-quality PNG file.
* **Size Estimation**: View the estimated file size of your generated image before downloading.

### 🔍 Scanner
* **Dual Mode Detection**: Specifically tuned modes for scanning either QR Codes (multiple results supported) or Barcodes.
* **Scan via Camera**: 
  * Real-time camera scanning.
  * Smart camera selection automatically attempts to use the primary rear camera while filtering out ultra-wide lenses (0.5x) for better focus.
* **Scan via Image Upload**:
  * Upload existing images (PNG, JPG, JPEG) to extract codes.
  * **Smart Crop Tool**: Includes an integrated image cropper (`Cropper.js`). If your uploaded image has too much clutter, you can crop the exact area of the code before scanning to improve accuracy.
  * Fallback to modern `BarcodeDetector` API when available for lightning-fast local processing.
* **Result Management**: 
  * View scanned results in a clean list.
  * One-click "Copy to Clipboard" functionality.
  * Automatically detects URLs and provides a clickable link to open them in a new tab.

---

## 🛠️ Tech Stack & Libraries

This project is built purely with Frontend technologies (HTML, CSS, JavaScript) and relies on robust open-source libraries via CDN:

* **[Tailwind CSS](https://tailwindcss.com/)** - For rapid, utility-first UI styling and dark mode.
* **[FontAwesome](https://fontawesome.com/)** - For beautiful vector icons.
* **[EasyQRCodeJS](https://github.com/ushelp/EasyQRCodeJS)** - Core engine for generating QR codes with logo support.
* **[JsBarcode](https://lindell.me/JsBarcode/)** - Core engine for generating Barcodes.
* **[HTML5-QRCode](https://github.com/mebjas/html5-qrcode)** - Core engine for the scanning camera and image file processing.
* **[Cropper.js](https://fengyuanchen.github.io/cropperjs/)** - For the image cropping modal during file uploads.

---

## 🚀 Getting Started

Since FadCode Generator is entirely client-side, no complex server setup or installation is required.

1. **Clone or Download** this repository.
2. Open the `index.html` file directly in any modern web browser (Chrome, Firefox, Safari, Edge).
3. Ensure you have an active internet connection on the first load so the CDN libraries can be fetched.

*(Note: For the camera scanning feature to work properly due to browser security policies, the app should be served over HTTPS or accessed via `localhost` / `127.0.0.1` if you are hosting it).*

---

## 💡 How to Use

### Generating a Code
1. Switch to the **Generator** tab.
2. Select your desired type: **QR Code** or **Barcode**.
3. Enter your Text or URL in the text area.
4. Customize the colors and resolution. 
5. *(Optional for QR)* Check "Tambahkan Gambar di Tengah" to upload a central logo.
6. Click **Generate** and then click **Download PNG** to save your code.

### Scanning a Code
1. Switch to the **Scanner** tab.
2. Choose what you want to scan (QR Code or Barcode).
3. Choose your method:
   * **Camera**: Click "Mulai Kamera", grant permissions, and point it at the code.
   * **Upload**: Select an image file. You can either click "Scan Langsung" to scan it immediately, or "Edit Area" to crop the image around the code for better results.
4. View your results at the bottom of the page, click the URL to open it, or click "Salin" to copy the text.

---

## 👨‍💻 Author & Credits

Created with ❤️ by **Fadkun10**. 
If you like this project, feel free to check out my [Instagram](https://www.instagram.com/fadkun.10/).

Enjoy generating and scanning without limits!
"""

with open('README.md', 'w', encoding='utf-8') as f:
    f.write(readme_content)
    
print("README.md generated successfully.")
