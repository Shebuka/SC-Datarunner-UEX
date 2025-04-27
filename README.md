# Star Citizen Datarunner for UEX

A lightweight Windows desktop application for Star Citizen players to automate DataRunner tasks for the UEX Corporation website. Capture trading terminal screenshots with a single keypress, extract commodity data using Tesseract OCR, and submit it to the UEX Website with one click, contributing to a shared pool of trading information for the Star Citizen community. Save time and effort with automated screenshot handling and precise data processing, including proper rounding of commodity prices, especially at busy locations with extensive commodity lists.

![Application Usage Screenshot](data/app_usage_screenshot.png)

## Features

- **Automated Screenshot Processing**: Capture commodity kiosk data by pressing <kbd>Print Screen</kbd> in-game, eliminating the need for manual screenshot management.
- **Accurate Data Extraction**: Uses Tesseract OCR to extract terminal names, commodity details (name, SCU, stock level, price), and terminal type (buy/sell) with high accuracy, including proper price rounding.
- **User-Friendly Interface**: Review, edit, and submit data with inline corrections and visual feedback in a list view with collapsible cells.
- **Language Support**: Available in English (🇬🇧), with planned support for German (🇩🇪), Italian (🇮🇹), and others based on community interest.
- **Local Processing**: Screenshot processing is performed locally, ensuring privacy, with only parsed commodity data and a perspective-corrected screenshot sent to the UEX API for verification.
- **Tutorial and Help**: Interactive tutorial on first launch and accessible via the Help menu to guide users through the process.
- **Windows Support**: Optimized for Windows, the only platform supported by Star Citizen.

## Installation

1. Download the [latest release](https://github.com/Shebuka/SC-Datarunner-UEX/releases) `.7z` file from the "Assets" section.
2. Extract the `SC-Datarunner-UEX` folder to any location on your computer.
3. Ensure Star Citizen is installed (LIVE or PTU environment).
4. Obtain your personal UEX Secret Key from [UEXCorp.space](https://uexcorp.space/account/home/tab/account_main#panel-secret-key) by logging into your account and scrolling to the Secret Key section on your account page.

### Uninstalling

1. Delete the `SC-Datarunner-UEX` folder wherever you extracted it.
2. Optionally, remove the `config.ini` file from `%APPDATA%\SC-Datarunner-UEX` to fully clear settings.

## Usage

1. **Launch the Application**:
   - Double-click `SC-Datarunner-UEX.exe` in the extracted folder to start the application.
   - On first launch, complete the onboarding wizard to enter your personal UEX Secret Key (from [UEXCorp.space](https://uexcorp.space/account/home/tab/account_main#panel-secret-key)) and select your Star Citizen screenshot folder.
   - Follow the interactive tutorial to learn how to capture screenshots, select the game environment (LIVE/PTU), and use the app.

2. **Capture Screenshots**:
   - In Star Citizen, navigate to the trading terminal you want to update.
   - Access the terminal, under 'Your Inventories' select the terminal's inventory, identifiable by the cargo deck image at the center and a list of commodities with their Available Cargo Sizes (SCU).
   - Press <kbd>Print Screen</kbd> to capture the screen. Scroll and repeat to capture all commodities, ensuring the first commodity is fully visible.
   - Follow [Best Practices](#best-practices-for-screenshot-capture) for optimal OCR results.

3. **Review and Submit Data**:
   - Switch to the application to view extracted data in a list.
   - Check the terminal name and the fields highlighted in red/orange (indicating errors or low confidence) and correct them if needed.
   - Click "Send" to submit individual entries or "Send All" to submit all entries at once to the UEX Website, associating submissions with your UEX account.
   - Screenshots are saved to the `/screenshots` folder within the application directory.

4. **Access Help**:
   - Revisit the tutorial anytime via the "Help > Show Tutorial" menu.

### Best Practices for Screenshot Capture

- **Minimize Glare**: Position your character to reduce screen glare, or try a different terminal with better lighting.
- **Align Closely**: Stand as close and straight to the terminal as possible for maximum clarity.
- **Disable Hints**: Turn off in-game hints (Options > Game Settings > Show Hints, Control Hints) to avoid text overlap.
- **Avoid Overlays**: Ensure `r_DisplayInfo` or other overlays do not obscure the commodity list.
- **Scroll Carefully**: When scrolling, ensure the first commodity is fully visible to avoid partial data extraction.

![In-Game Terminal Screenshot](data/terminal_screenshot.jpg)

## Frequently Asked Questions (FAQ)

### Why Use Star Citizen Datarunner?
This application streamlines the process of scraping commodity kiosk data, saving time and effort for Star Citizen players. It automates screenshot capture and data extraction, properly rounds commodity prices, and simplifies submission to the UEX Website, making it ideal for busy trading locations with extensive commodity lists. Contribute valuable trading information to the UEX community with minimal hassle.

### Where Are My Screenshots Processed?
All processing is performed locally on your computer, ensuring privacy and security.

### Is Any Data Shared with Third Parties?
Only the parsed commodity data (terminal name, commodity details) and a perspective-corrected screenshot are sent to the UEX API for data submission verification, associated with your UEX account. These are published on [UEXCorp.space](https://uexcorp.space/data/home). No personal data or raw screenshots are shared.

### What If I Encounter Issues?
Check the [Known Issues](https://github.com/Shebuka/SC-Datarunner-UEX/issues?q=is%3Aopen+is%3Aissue+label%3Abug) page or file a new issue on the [GitHub repository](https://github.com/Shebuka/SC-Datarunner-UEX/issues).

![Application icon](data/icon@512.png)

## Disclaimer

All rights are reserved. Star Citizen Datarunner for UEX is not officially affiliated with UEX Corporation or Roberts Space Industries, the developers of Star Citizen.

## Acknowledgments

- [UEX Corporation](https://uexcorp.space/) for providing the API and community platform.
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) for enabling robust text recognition.
- The Star Citizen community for inspiring this tool and providing valuable feedback.
