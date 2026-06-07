# Meter Usage Analyzer 📊⚡💧

A browser-based tool to visualize and analyze your energy and water meter consumption patterns in real-time.

**🌐 Live App:** <https://williamgagiano-droid.github.io/meteranalyzer/>

## Features

- **🏠 Overview dashboard**: At-a-glance totals, projected monthly usage & cost, 7-day trend, baseline load and plain-English insights
- **📊 Half-hourly Manhattan charts**: Every 30-min reading as a bar, colour-coded by time of day, with slot-average overlays
- **📈 Daily / Weekly / Monthly trend**: Aggregate usage over time with a 7-day rolling average and best/worst/percentile stats
- **⚖️ Period comparison**: Compare any two date ranges (or weekday vs weekend, week vs week, month vs month) side by side with % change and an overlaid hour-of-day profile
- **🔥 Pattern heatmap**: Day-of-week × hour-of-day intensity grid showing exactly when you consistently use the most
- **📅 Day-of-week analysis**: Average usage per weekday with highest/lowest markers
- **⏰ Peak time detection**: Historical morning and evening peak windows
- **🚨 Anomaly & leak detection**: Flags readings far above their slot average; treats sustained overnight flow as a possible water leak / energy standby load
- **💰 Cost estimation**: Editable per-kWh and per-kL tariffs drive monthly cost projections and baseline-waste estimates
- **⚡ Energy in Watts · 💧 Water in Litres**: Real power and flow, not just cumulative kWh/kL
- **📍 Zero cloud**: All processing in your browser. Optional Supabase load/save so you never re-upload
- **🧪 Sample data**: One-click demo dataset to explore every view

## How to Use

1. **Visit the app:** [Meter Analyzer](https://williamgagiano-droid.github.io/meteranalyzer/)
1. **Prepare your CSV:**
   
   ```
   Meter Number, Register, Date, Reading
   36114629, Energy, 2026-05-26 12:00, 18870.53
   36114629, Energy, 2026-05-26 11:30, 18870.19
   24073525, kL, 2026-05-26 12:00, 689.78
   ```
1. **Upload:** Click “Load & Visualize” and select your CSV
1. **Explore:** Switch between meters, time frames, and dates
1. **Analyze:** Use stats and averages to identify reduction opportunities

## Understanding the Chart

### Color Coding

- 🔵 **Blue** = Night (00:00-06:00)
- 🟠 **Orange** = Morning (06:00-12:00)
- 🔴 **Red** = Afternoon (12:00-18:00)
- 🟢 **Green** = Evening (18:00-24:00)

### Key Metrics

- **Peak Usage**: Highest consumption in any single 30-minute interval
- **Average**: Mean consumption across selected period
- **Variability Ratio**: Peak ÷ Average (higher = more spiky = bigger savings opportunity)
- **Total Usage**: Sum of all consumption in the period

## Unit Conversions

### Energy

- **Input:** kWh (kilowatt-hours)
- **Display:** Watts (average power over 30-min interval)
- **Formula:** (kWh ÷ 0.5 hours) × 1000 = Watts

### Water

- **Input:** kL (kilolitres)
- **Display:** Litres
- **Formula:** kL × 1000 = Litres

## Typical Usage Patterns

### Energy (Watts)

- **Peak hours:** 7-10am and 6-9pm (household/business activity)
- **Off-peak:** 2-5am (minimal consumption)
- **Common spikes:** Heating, cooling, hot water, major appliances

### Water (Litres)

- **Peak hours:** 6-8am (showers, toilets) and 6-8pm (cooking, cleaning)
- **Off-peak:** 11pm-5am (lowest usage)
- **Opportunities:** Leak detection, shorter showers, load shifting

## Optimization Tips

### High Impact (15-25% savings)

1. **Peak shaving** - Shift major loads to off-peak hours
- Run dishwasher, laundry at night
- Schedule irrigation to low-demand periods
1. **Fix leaks** - Check for continuously running water
- Small leak = 20-30 gallons/day

### Medium Impact (5-15% savings)

1. **Baseline reduction** - Eliminate always-on waste
- Unplug idle devices
- Enable power-saving modes
1. **Behavior changes** - Shift usage patterns
- Shorter showers
- Adjust thermostat 2-3°C

### Low Impact (0-10% savings)

1. **Monitor trends** - Weekly tracking for anomalies
1. **Seasonal adjustment** - Modify schedules for summer/winter

## Technical Details

- **Built with:** HTML5, Canvas/SVG, Vanilla JavaScript
- **Data processing:** Client-side only (no server uploads)
- **Browser support:** All modern browsers (Chrome, Firefox, Safari, Edge)
- **File size:** Single ~50KB HTML file
- **Performance:** Handles 100+ data points smoothly

## CSV Format

Your CSV must have these exact column headers:

```
Meter Number, Register, Date, Reading
```

Example:

```
Meter Number,Register,Date,Reading
36114629,Energy,2026-05-26 12:00,18870.53
36114629,Energy,2026-05-26 11:30,18870.19
24073525,kL,2026-05-26 12:00,689.78
```

**Notes:**

- Register should be “Energy” or “kL” (or similar)
- Date format: YYYY-MM-DD HH:MM
- Reading values are cumulative meter readings (app calculates deltas)

## Privacy & Security

✅ **100% Private**

- No data is sent to any server
- No cookies or tracking
- No analytics
- Works completely offline
- You control your data

## Development

To work on this project locally:

```bash
# Clone the repo
git clone https://github.com/williamgagiano-droid/meteranalyzer.git
cd meteranalyzer

# Open in your browser
open index.html
# or
firefox index.html
```

### File Structure

```
meteranalyzer/
├── index.html                      # Landing page
├── meter_half_hourly_chart.html    # Main analyzer app
├── README.md                       # This file
└── .gitignore
```

## Browser Compatibility

|Browser|Version|Status        |
|-------|-------|--------------|
|Chrome |60+    |✅ Full support|
|Firefox|55+    |✅ Full support|
|Safari |11+    |✅ Full support|
|Edge   |79+    |✅ Full support|

## Future Enhancements

- [ ] Historical data trending (week-over-week, month-over-month)
- [ ] Multi-meter comparison
- [ ] Cost calculation (with utility rates)
- [ ] Anomaly detection alerts
- [ ] Data export (CSV, PDF)
- [ ] Dark mode
- [ ] Mobile app version

## License

MIT - Use freely for personal or commercial purposes

## Support

Found a bug or have a suggestion?

- Open an [issue](https://github.com/williamgagiano-droid/meteranalyzer/issues)
- Submit a [pull request](https://github.com/williamgagiano-droid/meteranalyzer/pulls)

## Author

[William Gagiano](https://github.com/williamgagiano-droid)

-----

**Made with ⚡ for smarter energy & water management**