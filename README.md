# MMM-IndyCarTiming

A [MagicMirror²](https://magicmirror.builders/) module to display live IndyCar race standings.  
The module automatically hides itself when there is no active race.

## Features

- Shows current IndyCar race standings from the official IndyCar live feed.
- Automatically hides when there is no active race and reappears on race day.
- Updates automatically during an active race.

## Installation

1. Clone this repository into your MagicMirror `modules` directory:

   ```sh
   cd ~/MagicMirror/modules
   git clone https://github.com/brmfulasha/MMM-IndyCarTiming.git
   ```

2. No extra dependencies are required; the module uses Node.js built-in modules only.

## Configuration

Add the module to the `modules` array in your `config.js`:

```javascript
{
  module: "MMM-IndyCarTiming",
  position: "top_left", // Or any other region
  config: {
    updateIntervalRaceDay: 60000, // Update interval in ms during race
    dataUrl: "https://example.com/indycar/live-feed.json"
  }
},
```

## How It Works

- On race days, the module fetches live data from the IndyCar feed and displays the standings.
- When there is no active race, the module hides itself automatically.

## Customization

- You can adjust `updateIntervalRaceDay` in the config to change how often the data updates during a race.
- You may style the module via custom CSS (`MMM-IndyCarTiming.css`).

## Troubleshooting

- If the module does not appear, ensure MagicMirror is running and your config is valid.
- Check your internet connection to ensure access to the IndyCar live feed.

## License

MIT

---

**Enjoy live IndyCar standings on your MagicMirror!**
