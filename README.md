# Python-based Audiobook Reader

## Overview

The **Python-based Audiobook Reader** is a versatile application that converts text files (such as `.txt`, `.epub`, and `.pdf`) into spoken audio using the `pyttsx3` library. This desktop application provides users with the ability to listen to their favorite books or documents offline, adjust speech settings, manage playback efficiently, and save the spoken text as audio files. With a user-friendly graphical interface built using `Tkinter`, the Audiobook Reader ensures an accessible and seamless experience for all users.

## Prerequisites

Before running the **Python-based Audiobook Reader**, ensure you have the following installed on your system:

- **Python 3.6 or higher**
- **pip** (Python package installer)

### Required Python Libraries

Install the necessary Python libraries using `pip`:

```bash
pip install pyttsx3 ebooklib beautifulsoup4 PyMuPDF
```

Note: If you encounter any installation issues, ensure that your pip is up to date by running pip install --upgrade pip.

## Linux-Specific Requirements

If you're using a Linux system and encounter issues with voice output, install the following dependencies:

```bash
sudo apt update && sudo apt install espeak ffmpeg libespeak1
```

## Installation

### Clone the Repository

Clone the Python-based Audiobook Reader repository from GitHub:

```bash
git clone https://github.com/Aman-Sunesh/Python-based-Audiobook-Reader.git
cd Python-based-Audiobook-Reader
```

### Running the Application

Since the executable is a Jupyter Notebook (Python-based Audiobook Reader.ipynb), you can run it using Jupyter Notebook or JupyterLab.

1. **Install Jupyter Notebook (if not already installed):**

    ```bash
    pip install notebook
    ```

2. **Launch Jupyter Notebook:**

    ```bash
    jupyter notebook
    ```

3. **Open the Notebook:**

    In the Jupyter interface, navigate to the `Python-based Audiobook Reader.ipynb` file and open it.

4. **Run the Notebook:**

    Execute the cells sequentially to launch the application.

Alternatively, you can convert the notebook to a standalone Python script and run it directly:

1. **Convert Notebook to Script:**

    ```bash
    jupyter nbconvert --to script "Python-based Audiobook Reader.ipynb"
    ```

2. **Run the Script:**

    ```bash
    python "Python-based Audiobook Reader.py"
    ```

## Usage

### 1. Loading a File

1. **Launch the Application:**  
   Run the application using Jupyter Notebook or the converted Python script.

    ```bash
    jupyter notebook
    ```

    *Or, if you've converted the notebook to a script:*

    ```bash
    python "Python-based Audiobook Reader.py"
    ```

2. **Load a File:**  
   Click on the "Load File" button to select a `.txt`, `.epub`, or `.pdf` file from your system.

3. **Display Content:**  
   The content of the loaded file will be displayed in the text area within the application.

### 2. Playback Controls

- **Play:**  
  Click the "Play" button to start reading the text aloud.

- **Stop:**  
  Click the "Stop" button to halt the ongoing playback.

- **Save as Audio:**  
  Click the "Save as Audio" button to save the spoken text as an `.mp3` or `.wav` file.

### 3. Speech Settings

Adjust the speech settings to customize your listening experience:

- **Voice Selection:**  
  Choose between available voices (e.g., male, female) from the dropdown menu.

- **Rate:**  
  Adjust the speech rate using the slider to increase or decrease the speaking speed.

- **Volume:**  
  Modify the volume level using the slider to set the desired loudness.

## Features and Functionalities

### 1. Support for Multiple File Formats:

- **.txt:** Plain text files.
- **.epub:** Electronic publication files.
- **.pdf:** Portable Document Format files.

### 2. Text-to-Speech Conversion:

- Utilizes `pyttsx3` for offline speech synthesis.
- Compatible with multiple TTS engines, including SAPI5, NSSS, and eSpeak.

### 3. Adjustable Speech Settings:

- **Voice Selection:** Switch between different voices.
- **Speech Rate:** Control the speed of the spoken text.
- **Volume Control:** Set the volume level for playback.

### 4. Playback Controls:

- **Play:** Start reading the text aloud.
- **Stop:** Stop the ongoing playback.
- **Save to Audio File:** Save the spoken text as an audio file (`.mp3` or `.wav`).

### 5. User-Friendly GUI:

- Built with `Tkinter` for an intuitive and responsive interface.
- Text display area with scrollbar for easy navigation through the content.
- Progress bar to indicate the reading progress.

### 6. Threading for Smooth Operation:

- Implements threading to handle speech playback without freezing the GUI.

## Detailed Features

### Loading and Displaying Files

- **Supported Formats:**  
  The application can load `.txt`, `.epub`, and `.pdf` files.

- **Content Extraction:**
  - **.txt:** Reads plain text directly.
  - **.epub:** Uses `ebooklib` and `BeautifulSoup` to extract text from EPUB files.
  - **.pdf:** Utilizes `PyMuPDF` (`fitz`) to extract text from PDF documents.

- **Error Handling:**  
  Provides error messages for unsupported file types or failed file loading attempts.

### Speech Playback

- **Threaded Playback:**  
  Speech synthesis runs on a separate thread to keep the GUI responsive.

- **Chunk-Based Reading:**  
  Breaks the text into manageable chunks to update the progress bar accurately.

- **Stop Functionality:**  
  Allows users to stop the playback at any time, resetting the progress.

### Saving Audio Files

- **File Formats:**  
  Supports saving spoken text as `.mp3` or `.wav` files.

- **Dependencies:**  
  On Linux, ensure that `espeak` and `ffmpeg` are installed for audio file generation.

- **User Feedback:**  
  Notifies users upon successful saving or in case of errors during the process.

### Speech Settings

- **Voice Selection:**  
  Users can select from available voices installed on their system.

- **Rate Adjustment:**  
  Sliders allow users to increase or decrease the speech rate for a comfortable listening speed.

- **Volume Control:**  
  Users can set the desired volume level for the speech output.

## Screenshots

*(Include screenshots of the application interface here)*

## Troubleshooting

### 1. Installation Errors:

- **Ensure all required libraries are installed using `pip`.**
- **Upgrade `pip` if necessary:**

    ```bash
    pip install --upgrade pip
    ```

### 2. Voice Output Issues:

- **On Linux, install `espeak`, `ffmpeg`, and `libespeak1` as mentioned in the prerequisites.**

    ```bash
    sudo apt update && sudo apt install espeak ffmpeg libespeak1
    ```

- **Verify that the selected voice is available and compatible with your system.**

### 3. Saving Audio Files Fails:

- **Ensure that `ffmpeg` is installed and accessible in your system's PATH.**
- **Check write permissions for the directory where you intend to save the audio file.**

### 4. GUI Freezes or Becomes Unresponsive:

- **Ensure that threading is properly handled. Avoid making blocking calls on the main thread.**

### 5. Unsupported File Formats:

- **The application currently supports `.txt`, `.epub`, and `.pdf`. Convert other formats to one of these for compatibility.**

## Contributing

Contributions are welcome! Whether it's improving existing features, adding new functionalities, or enhancing the documentation, your input is valuable. Please follow these steps to contribute:

1. **Fork the Repository:**

    Click the "Fork" button on the repository page to create your own copy.

2. **Create a Branch:**

    ```bash
    git checkout -b feature/YourFeatureName
    ```

3. **Commit Your Changes:**

    ```bash
    git commit -m "Add your message here"
    ```

4. **Push to Your Fork:**

    ```bash
    git push origin feature/YourFeatureName
    ```

5. **Create a Pull Request:**

    Navigate to the original repository and click on "Compare & pull request" to submit your changes.


## Acknowledgments

- **pyttsx3:** [https://pyttsx3.readthedocs.io/en/latest/](https://pyttsx3.readthedocs.io/en/latest/)
- **EbookLib:** [https://github.com/aerkalov/ebooklib](https://github.com/aerkalov/ebooklib)
- **BeautifulSoup:** [https://www.crummy.com/software/BeautifulSoup/bs4/doc/](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- **PyMuPDF (fitz):** [https://pymupdf.readthedocs.io/en/latest/](https://pymupdf.readthedocs.io/en/latest/)
- **Tkinter Documentation:** [https://docs.python.org/3/library/tkinter.html](https://docs.python.org/3/library/tkinter.html)
- **Python Community:** For continuous support and resources.
