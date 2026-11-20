# Meter Reader Tools

A small browser-based toolkit for preparing and completing meter-reading routes. The landing page links to the classic planner and the Special Reader.

## Special Reader

The Special Reader (`special_reader.html`) is designed to help prepare a prioritized list of meter reads, arrange them into a practical route, and track completion during the day.

### Planning workflow

1. **Prepare the worklist in Bright Forms.** Open Bright Forms and filter the work to the required date (use the date filter, then confirm the results are for the correct day). This filtering happens in Bright Forms; the Special Reader does not connect to Bright Forms or filter its data itself.
2. **Copy the addresses.** Copy the address lines from the filtered Bright Forms results. Review them for missing or ambiguous address details before planning.
3. **Add addresses to the Special Reader.** Open **Special Reader** from the landing page. Paste urgent work into **Urgent reads** and other work into **Normal reads**. Multiple addresses can be pasted as separate lines. Add them to the list. You can also import a CSV/TXT file or add entries individually.
4. **Plan and auto-sort.** Select **Auto-sort** if you want the tool to arrange located reads into a suggested order, then choose **Plan route**. The app locates addresses and presents the route on a map. Auto-sort uses geographic distance and read priority as a planning heuristic; it is a suggested order, not a guarantee of the fastest real-world route. Review the result.
5. **Adjust the list.** Drag rows or use the row controls and bulk-adjust tools to make changes. You can move selected reads, change priority, reverse a range, and undo recent changes. Plan again after edits if you need the map route refreshed.
6. **Use it on the day.** Keep the reader open on your device. The Current read panel shows the next unfinished address. After completing a read, use **Clear this read · Next address** to mark it done and advance. The map and remaining count help you keep track. If you mark something done by mistake, use **Undo**.

### Before you start

- Use a modern browser with JavaScript enabled and an internet connection for address lookup and route planning.
- Google Maps services are used for address lookup and driving directions; a valid Google Maps API key with the required services enabled must be configured in the app. Follow any instructions shown in the app if Maps is unavailable. The map tiles are provided by OpenStreetMap.
- The read list is stored in this browser's local storage. It is not automatically synchronized with Bright Forms or across devices/browsers. Export a backup from **Import / export** if you need to keep a copy or transfer the list.
- Check the addresses and generated order before setting out. Geocoding can fail or match an unintended place when an address is incomplete or ambiguous. Reads without a confirmed location cannot be included in the plotted route.

## Import and export

The Special Reader supports CSV/TXT import and CSV export. Keep an export as a backup before making major changes. A copied list from Bright Forms can also be pasted into the urgent or normal address box, one address per line.

## Files

- `index.html` — landing page linking to the tools and the planning guide.
- `meter_reader.html` — classic meter route planner.
- `special_reader.html` — prioritized read list, bulk adjustments, map, route planning, and completion tracking.
- `special_reader_guide.html` — in-app planning and day-of-use guide.

## Running the app

These are static HTML files. Open `index.html` in a browser or host the files on a static web server. Route planning depends on the external Google Maps services and a configured API key; the map uses Leaflet and OpenStreetMap tiles.
