# AI Article Summarizer Chrome Extension

**AI Article Summarizer** is a Chrome extension that uses Google Gemini AI to generate concise, detailed, or bullet-point summaries of any article or web page you visit. It extracts the main content from the page and provides a summary directly in your browser popup.

---

## Features

- **Summarize Any Web Page:** Get a brief, detailed, or bullet-point summary of articles and web content.
- **Customizable Summary Type:** Choose between brief, detailed, or bullet-point formats.
- **Copy to Clipboard:** Easily copy the generated summary for sharing or note-taking.
- **API Key Management:** Securely store your Gemini API key using the extension's options page.

---

## Installation

1. **Clone or Download the Repository**
   ```
   git clone https://github.com/yourusername/AI_Article_Summarizer.git
   ```
   Or download and extract the ZIP.

2. **Load the Extension in Chrome**
   - Go to `chrome://extensions/`
   - Enable **Developer mode** (top right)
   - Click **Load unpacked**
   - Select the `AI_Article_Summarizer` folder

3. **Set Your Gemini API Key**
   - After installation, the options page will open automatically.
   - Paste your [Gemini API key](https://makersuite.google.com/app/apikey) and save.

---

## Usage

1. **Navigate to Any Article or Web Page**
2. **Click the Extension Icon**
3. **Choose Summary Type**
   - Brief Summary
   - Detailed Summary
   - Bullet Points
4. **Click "Summarize This Page"**
5. **Copy the Summary** (optional) using the "Copy Summary" button.

---

## File Structure

```
AI_Article_Summarizer/
│
├── manifest.json         # Chrome extension manifest (permissions, scripts)
├── popup.html            # Extension popup UI
├── popup.js              # Popup logic (UI, messaging, API calls)
├── content.js            # Content script (extracts article text)
├── background.js         # Handles first-run logic
├── options.html          # Options page for API key
├── options.js            # Logic for saving API key
├── icon.png              # Extension icon
└── config.js             # (Optional) Configuration file
```

---

## How It Works

- **Content Script (`content.js`):** Extracts the main text from the current page (using `<article>` or `<p>` tags).
- **Popup (`popup.html` & `popup.js`):** UI for selecting summary type, displaying results, and copying to clipboard.
- **API Integration:** Sends the extracted text to the Gemini API for summarization.
- **Options Page:** Lets you securely save your Gemini API key.

---

## Troubleshooting

- **"Could not extract article text from this page."**
  - The page may not contain extractable text (e.g., PDFs, some web apps).
  - Try on a standard news or blog article.

- **"Cannot access this page. Try another website."**
  - Content scripts cannot run on Chrome Web Store, `chrome://` pages, or some special URLs.

- **No summary generated / API errors**
  - Ensure your Gemini API key is valid and has quota.
  - Check your internet connection.

---

## Privacy

- Your API key is stored locally using Chrome's `storage.sync` and is **never shared** with anyone except the Gemini API endpoint.

---

## Credits

- Built with [Google Gemini API](https://ai.google.dev/).
- Extension icon from [Flaticon](https://www.flaticon.com/).

---

## License

MIT License

---

## Contributing

Pull requests and suggestions are welcome! Please open an issue for bugs or feature requests.
