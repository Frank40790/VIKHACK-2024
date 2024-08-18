# Ease Event

## Overview

EaseEvent is an app that makes managing your calendar events easier than ever. If you have a photo or image of a calendar event, EaseEvent converts it into a calendar file. This simplifies the tedious process of adding events to your digital calendar, saving you time and effort. Say goodbye to manual data entry and let EaseEvent handle the details for you!

## Installation

Setting up the server

1. Put your API key in `.env.example` and rename the file to `.env`
2. Install the dependencies by running `pip install -r requirements.txt `
3. Run the server using the command `uvicorn api_server:app --reload --host 0.0.0.0 --port 8000 `

Get result from the server

1. Put a img.png under current directory
2. Run the following command

```
curl -X POST "http://localhost:8000/image/" \                                                                                    ─╯
     -H "Content-Type: application/json" \
     -d '{"image": "'"$(cat  sample_img.png | base64 )"'"}' > sample_img.ics
```
