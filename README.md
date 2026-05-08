# Book Log Shortcuts

Apple Shortcuts that make recording my reading data easier. 
[See how i'm using it](https://github.com/ericsmoore/reading-analysis).

## Installation

Download both `.shortcut` files and import them into Apple Shortcuts. 

Create an output directory for logs and adjust the file paths in the shortcut to match.

Also create the helper files in the output directory:

- `current-book.txt`
- `last-page.txt`

## Usage

### Start

Run the **session-start** shortcut

- Writes the current date and time to a new line in `reading-log.txt`
- Starts a stopwatch to track active reading time
  - Can be paused and reset as needed


### Stop

Run the **session-stop** shortcut

- Stops the stopwatch if it is running
- Records start and end pages to `reading-log.txt`
  - Default start page is read from `last-page.txt`
  - Updates `last-page.txt` to the session's end page
- Records stopwatch time
- Records current book
  - Default is read from `current-book.txt`
  - Updates `current-book.txt` to the session's book

<br>

### Output Format

Each session is written to a new line in `reading-log.txt`:

`YYYY-MM-DD 15:24 | 'start pg' | 'end pg' | 'active time' | 'book'`

