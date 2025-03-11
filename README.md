# video-downloader-in-python
GUI youtube video downloader using python to download videos and audios from youtube.
!pip install customtkinter: This line installs the customtkinter library using pip.

import tkinter as tk: This imports the tkinter module and assigns it the alias tk.

from pytube import YouTube: This imports the YouTube class from the pytube library, which is used for downloading YouTube videos.

import customtkinter: This imports the customtkinter library, which is a custom implementation of tkinter.

from tkinter import filedialog: This imports the filedialog module from tkinter, which provides a dialog box for selecting file paths.

def startDownload(option):: This defines the startDownload function, which is called when the user clicks the download buttons. It takes an option parameter to determine which type of video to download.

The try block in the startDownload function: This block of code is executed when the video download process is successful.

ytLink = link.get(): This retrieves the YouTube video link entered by the user from the link entry field.

ytObject = YouTube(ytLink, on_progress_callback=on_progress): This creates a YouTube object using the provided video link and specifies the on_progress_callback function to track the download progress.

if option == "hq":, elif option == "lq":, elif option == "audio":, else:: These conditional statements check the value of the option parameter and select the appropriate video stream based on the option (highest resolution, lowest resolution, or audio-only).

file_path_hq = filedialog.asksaveasfilename(defaultextension=".mp4", filetypes=[("MP4 files", "*.mp4")]): This opens a file dialog box for the user to choose the file path and name for saving the downloaded video. The selected file path is stored in the file_path_hq variable.

video.download(file_path_hq): This downloads the selected video stream and saves it to the specified file path.

Updating the UI elements: These lines update the title label, finishLabel label, and progressbar based on the download status.

def on_progress(stream, chunk, bytes_remaining):: This defines the on_progress function, which is called during the video download process to track the progress.

Calculating the download progress: This block of code calculates the download progress percentage and updates the progress label and progressbar accordingly.

customtkinter.set_appearance_mode("system"): This sets the appearance mode of the GUI to the system's default.

customtkinter.set_default_color_theme("green"): This sets the default color theme of the GUI to green.

Creating the app frame: This initializes the main application window using customtkinter.CTk() and sets its geometry and title.

Adding UI elements: These lines create various UI elements such as labels, an entry field, a progress bar, and buttons, and pack them into the app frame.

app.mainloop(): This starts the main event loop of the GUI, allowing the user to interact with the application.
