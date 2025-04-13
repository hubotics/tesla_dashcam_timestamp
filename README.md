# TeslaDashcam

**Version: v0.1.0**

TeslaDashcam is a Python application designed to process Tesla dashcam video files by overlaying timestamps using FFmpeg. It provides a user-friendly GUI built with PySide6, allowing users to select input directories, view grouped video files, and convert them in parallel with real-time progress updates.

## Features

- **Directory Selection**: Select an input directory containing Tesla dashcam videos.
- **File Grouping**: Groups video files by timestamp (e.g., `yyyy-mm-dd_hh-mm-ss`), ignoring non-matching files.
- **Parallel Conversion**: Converts videos from four cameras (`back`, `front`, `left_repeater`, `right_repeater`) in parallel using `multiprocessing`.
- **Progress Monitoring**: Displays full file names, progress bars, and percentage labels for each camera.
- **Missing File Handling**: Marks non-existent files as `Missing` without updating their progress.
- **User-Friendly GUI**: Disables file selection during conversion and resets status on new selections.

## Installation

### Prerequisites

- Python 3.10 or higher
- FFmpeg installed on your system
  - macOS: `brew install ffmpeg`
  - Ubuntu: `sudo apt-get install ffmpeg`
  - Windows: Download from [FFmpeg website](https://ffmpeg.org/download.html) and add to PATH

### Python Dependencies

Install the required Python packages using pip:

```bash
pip install PySide6 ffmpeg-progress-yield
