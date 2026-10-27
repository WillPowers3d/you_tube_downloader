# YouTube Downloader

A small desktop app that downloads a YouTube video or every video in a playlist at the highest available resolution.

The window has two fields and two buttons:

- **Enter Video Link** + **Download Video** — downloads that video
- **Enter Playlist Link** + **Download Playlist** — downloads each video in the playlist

Files are saved to `G:/Downloads` (hardcoded in `you_tube_download.py`). Success or error is shown in the window; exceptions are also printed to the console.

## Tech stack

- Python 3
- [tkinter](https://docs.python.org/3/library/tkinter.html) (standard library) for the GUI
- [pytube](https://pypi.org/project/pytube/) (`YouTube`, `Playlist`) — the source comment also cites [pytube3](https://pypi.org/project/pytube3/)

## Install

```bash
python3 -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

tkinter ships with most Python installs. On some Linux distros you may also need the system package (for example `python3-tk`).

## Run

```bash
python you_tube_download.py
```

A Tk window titled **Youtube Video Downloader** opens.

## Example usage

1. Start the app as above.
2. Paste a YouTube watch URL into **Enter Video Link** and click **Download Video**.
3. Or paste a playlist URL into **Enter Playlist Link** and click **Download Playlist**.
4. When a download finishes, the label under that button turns green and says `Success!`. On failure it turns red (`Error` or `Playlist Error`).

The download directory must exist (`G:/Downloads` on the machine that runs the app).
