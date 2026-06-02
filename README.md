# i-harmonium

A web-based harmonium that uses your laptop's lid angle to control the bellows. Press keys on your keyboard and move the lid to play notes.

## What It Does

- Plays harmonium-style notes from your keyboard
- Uses the MacBook lid angle as a bellows control
- Sends live lid angle data from Python to the browser over WebSockets
- Renders the instrument in a single HTML page

## Requirements

- Python 3.7+
- A MacBook with a working lid angle sensor
- A web browser such as Chrome, Firefox, or Safari
- Python packages: `websockets` and `pybooklid`

## Setup

Clone the repository and enter the project folder:

```bash
git clone https://github.com/USMAN1626/Mac_Harmonium.git
cd Mac_Harmonium
```

Create and activate a virtual environment:

```bash
python3 -m venv venv
source venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Run

1. Start the Python backend:

```bash
python harmonium.py
```

You should see:

```text
Bridge active! Waiting for your web app on port 8765...
```

2. Open the frontend in your browser:

```bash
open harmonium.html
```

## How To Play

- Click the page once to enable audio
- Hold any of these keys: A, W, S, E, D, F, T, G, Y, H, U, J, K
- Partially close your laptop lid to pump air into the bellows
- The sound gets stronger as the bellows fill up

## Key Mapping

White keys:

- A = C
- S = D
- D = E
- F = F
- G = G
- H = A
- J = B
- K = C (octave)

Black keys:

- W = C#
- E = D#
- T = F#
- Y = G#
- U = A#

## Troubleshooting

- No sound: click the page to activate audio and check system volume
- WebSocket not connecting: make sure `harmonium.py` is running first
- Lid angle not changing: confirm `pybooklid` is installed and the sensor works on your MacBook

## Stop

- Stop the backend with `Ctrl+C` in the terminal running `harmonium.py`
- Close the browser tab to stop the frontend

## Project Files

- `harmonium.py` - Python WebSocket backend that streams lid angle data
- `harmonium.html` - Browser-based harmonium interface
- `README.md` - Setup and usage instructions

## License

Feel free to use and modify this project as you wish.
