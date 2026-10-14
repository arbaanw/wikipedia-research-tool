# Wikipedia Research Tool

A simple Python CLI tool that automates Wikipedia research and saves introductory notes in Markdown format.

## Features

- **Automated search:** Search Wikipedia for any topic directly from the terminal.
- **Content extraction:** Extracts introductory paragraphs from the selected article.
- **Citation removal:** Removes Wikipedia's inline citation markers.
- **Markdown output:** Saves extracted text to `notes.md` for easy reference.
- **Browser automation:** Uses Selenium to interact with Wikipedia through Chrome.

## Tech Stack

- Python
- Selenium
- Beautiful Soup 4
- Google Chrome
- ChromeDriver

## Prerequisites

Make sure you have the following installed:

- Python 3.9+
- Google Chrome
- ChromeDriver compatible with your installed Chrome version

## Installation

**1. Clone the repository**

```bash
git clone https://github.com/arbaanw/wikipedia-research-tool.git
cd wikipedia-research-tool
```

**2. Create a virtual environment (recommended)**

```bash
python -m venv .venv
```

Activate it:

Linux/macOS:

```bash
source .venv/bin/activate
```

Windows:

```powershell
.venv\Scripts\activate
```

**3. Install dependencies**

```bash
pip install selenium beautifulsoup4
```

**4. Configure ChromeDriver**

Download the ChromeDriver version compatible with your installed Chrome browser.

Place the executable named `chromedriver` in the same directory as `main.py`.

On Linux/macOS, ensure it has executable permissions:

```bash
chmod +x chromedriver
```

## Usage

Run the program from your terminal:

```bash
python main.py
```

Enter the topic you want to research when prompted:

```text
Enter topic to search
>> Artificial Intelligence
```

The tool will open Wikipedia in Chrome, search for the topic, extract the introductory paragraphs, and save the results to `notes.md`.

## Output

The extracted notes are saved to:

```text
notes.md
```

The file is created in the current working directory. Each run overwrites the existing notes file.

## Project Structure

```text
wikipedia-research-tool/
├── main.py
├── chromedriver
├── notes.md          # Generated output
└── README.md
```

`chromedriver` is a local browser-driver executable and may not be tracked in the repository.

## Limitations

- Requires an internet connection.
- Requires Chrome and a compatible ChromeDriver installation.
- Extracts introductory content rather than the entire article.
- The output is plain text in Markdown format; headings and other article formatting are not preserved.
- Search results and extracted content depend on Wikipedia's page structure.

## Future Improvements

- [ ] Support multiple articles in a single session.
- [ ] Allow users to specify the output filename.
- [ ] Preserve headings and formatting in the extracted notes.
- [ ] Add support for exporting research to PDF.
- [ ] Improve error handling for missing pages and browser setup issues.
- [ ] Add configurable extraction depth.

