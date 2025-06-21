# Manga Translation Studio - GUI Module

![License](https://img.shields.io/badge/license-GPL%20v3.0-blue.svg)
![Python](https://img.shields.io/badge/python-3.7%2B-blue.svg)

A user-friendly graphical interface for the powerful [manga-image-translator](https://github.com/zyddnys/manga-image-translator) command-line tool.

## 📋 Table of Contents

- [About](#about)
- [Motivation](#motivation)
- [Installation](#installation)
- [Usage](#usage)
- [GUI Overview](#gui-overview)
- [Important Notes](#important-notes)
- [Known Issues & Limitations](#known-issues--limitations)
- [Support](#support)
- [License](#license)

## 🎯 About

This GUI is the result of a collaborative "vibe coding" project:

- **Ideas, Direction & Testing:** [Kostraw](https://github.com/Kostraw)
- **Code Implementation:** AI Assistant

This project provides an intuitive graphical interface for the incredible command-line tool **`manga-image-translator`** created by **zyddnys**.

**🔗 Original Project:** [https://github.com/zyddnys/manga-image-translator](https://github.com/zyddnys/manga-image-translator)

## 💡 Motivation

The original `manga-image-translator` tool is incredibly powerful but requires command-line knowledge. This GUI democratizes that power, making it accessible to everyone who prefers a visual workflow. It transforms a complex tool into an intuitive, user-friendly application.

## 🚀 Installation

> **⚠️ Prerequisites:** This guide assumes you have the main `manga-image-translator` tool already installed according to the [original project's instructions](https://github.com/zyddnys/manga-image-translator).

### Step 1: Create Virtual Environment (Recommended)

Using a virtual environment keeps your Python installation clean and prevents conflicts:

```bash
# Create virtual environment
python -m venv venv

# Activate it (Windows)
.\venv\Scripts\activate

# Activate it (Linux/Mac)
source venv/bin/activate
```

*You should see `(venv)` at the beginning of your terminal prompt.*

### Step 2: Install GUI Dependencies

```bash
pip install customtkinter Pillow tkinterdnd2 CTkToolTip
```

> **Note:** This only installs GUI dependencies. The main manga-image-translator must be installed separately.

## 🖥️ Usage

### Launching the Application

**Do not run the .py script directly.** Use the provided launcher:

1. Double-click `MangaStudioRun.bat`
2. Choose your launch mode:
   - **Normal Mode:** Clean interface without console (recommended for daily use)
   - **Debug Mode:** Visible console for logs and troubleshooting

### File Structure

The GUI files are located within the main manga-image-translator directory:

```
📁 manga-image-translator/     # Main translator tool directory
├── 📄 MangaStudio.py          # GUI application file
├── 📄 MangaStudioRun.bat      # GUI launch script
├── 📁 MangaStudio_Data/       # GUI-generated files (auto-created)
│   ├── 📁 profiles/           # Your preset(s) folder
│   ├── 📁 temp/               # Temporary processing files
│   └── 📄 config.json         # Saved configuration presets
└── ... (other main tool files)
```

The GUI automatically creates its own `MangaStudio_Data/` folder to keep all GUI-generated files organized and separate from the main tool's outputs.

## 🎛️ GUI Overview

### Configuration Tabs
The main control panel for the translation pipeline:

- **General & Translator:** Language selection, translator models, core settings
- **Detector & OCR:** Text detection and recognition fine-tuning
- **Image & Inpainter:** Text removal, upscaling, colorization settings
- **Render & Output:** Font styling, text rendering, file output options

### Visual Compare Tab
Test your settings on a single image before processing large batches. Provides instant visual feedback.

### Model Manager Tab
Download and manage common AI models. 

> **Note:** The underlying tool supports additional models not listed here. Refer to the [original documentation](https://github.com/zyddnys/manga-image-translator) for the complete list.

### Extra Settings Tab
Advanced features for power users:

- **Preset Manager:** Save and load configuration profiles
- **Advanced Debug Mode:** Save intermediate processing steps (⚠️ uses significant disk space)
- **Special Tasks Workshop:** Standalone operations (RAW Output, Upscale, Colorize) independent of the main pipeline

### Live Log Tab
Real-time backend output during operations. Shows identical information to Debug Mode console.

## ⚠️ Important Notes

### Performance
- **First Run:** Initial model loading may take several minutes
- **Subsequent Runs:** Models are cached for faster processing

### System Requirements
- Python 3.7 or higher
- Sufficient RAM for AI model operations
- Adequate storage space (especially with Debug Mode enabled)

## 🚨 Known Issues & Limitations

> **⚠️ Compatibility Warning:** This GUI may experience issues under certain conditions:
> 
> - **Settings Changes:** Some interface elements may not function properly if certain parameters are modified
> - **Version Updates:** Future updates to the underlying manga-image-translator tool may cause compatibility issues with specific GUI components
> - **Model Updates:** Changes to AI model architectures or APIs may affect functionality
> 
> If you encounter unexpected behavior, try reverting to default settings or check for updates.

### Troubleshooting
- Use **Debug Mode** to launch `MangaStudioRun.bat` for detailed error information
- Check the **Live Log Tab** for real-time diagnostics
- Verify that the main manga-image-translator tool is properly installed
- GUI output files are saved in the `GUI_Output/` folder within the main tool directory

## 🛠️ Support

This GUI was created as a passion project and is not officially maintained.

For bugs, feature requests, or support:
1. Check existing issues in the main [manga-image-translator repository](https://github.com/zyddnys/manga-image-translator/issues)
2. Create new issues in the same repository for centralized community support
3. Include detailed information about your system, settings, and the specific problem

## 📄 License

This GUI module, as a derivative work, follows the same license as the original manga-image-translator project.

**License:** [GNU General Public License v3.0](https://www.gnu.org/licenses/gpl-3.0.en.html)

---

## 🙏 Acknowledgments

- **zyddnys** for the original manga-image-translator tool
- **Kostraw** for project direction and testing
- The open-source community for ongoing support and feedback

---

*This GUI was developed in collaboration with an AI assistant.*
