# FlipFlash

FlipFlash is a Flipper Zero flashcard app that reads flashcards from a text file. 

## Deck format

The flashcard deck files are stored on the Flipper at:

`/ext/apps_data/FlipFlash/flashcardFile.txt`

Each card uses one line in the form:

`front|back`

Blank lines and lines starting with `#` are ignored.

Example:

```
hola|hello
adios|goodbye
```

<!-- ## State storage

The app stores the current mode and removed-card list in:

`/ext/apps_data/FlipFlash/flashflash_state.txt` -->

## Controls

- `OK`: flip front/back, then advance to the next card when the back is shown
- `RIGHT`: go to the next card
- `UP`: open settings
- `DOWN`: remove the current card
- `BACK`: cancel, return to previous screen or exit the app

## Sample deck

On first launch, FlipFlash creates two small Spanish test decks automatically if the deck file does not exist. 

## Installation

### 1. Install with uv

#### a). Install uv
If you do not have `uv` installed yet, install it following the link: [Installing uv](https://docs.astral.sh/uv/getting-started/installation/). 


#### b). Install Project Dependencies
Run the following command in the project root. `uv` will automatically create a virtual environment (`.venv`) and install all required packages listed in `pyproject.toml`: 
```bash
uv sync
```

#### c). Build
```
uv run ufbt
```
The `.fap` file is stored at `dist/`

Or run
```
uv run ufbt launch
```
Whe a flipper zero is connected, it will automatically install. 

### 2. Install directly ufbt

#### a). Install ufbt
```bash
python3 -m pip install --upgrade ufbt
```

#### b). Build
```bash
ufbt
```
The `.fap` file is stored at `dist/`

Or run
```
ufbt launch
```
Whe a flipper zero is connected, it will automatically install. 