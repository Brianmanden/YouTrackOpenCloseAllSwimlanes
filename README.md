# YouTrackOpenCloseAllSwimlanes

Two bookmark scripts to open / close all swimlanes on a YouTrack Board

## Open all swimlanes

1. Add a Bookmark in your browser and name it OPEN
2. In the URL field of the bookmark paste the following:
```JavaScript
javascript:(function () { const toggles = document.querySelectorAll('.yt-agile-table__row-title__summary__text'); toggles.forEach((toggle, i) => { const lane = toggle.closest('.yt-agile-table__row'); if (!lane) return; const isOpen = !!lane.querySelector('.yt-agile-table__row__cell'); if (!isOpen) { toggle.click(); } });})();
```
3. Navigate to your YouTrack Board
4. Click the OPEN bookmark and all swimlanes opens

## Close all swimlanes

1. Add a Bookmark in your browser and name it CLOSE
2. In the URL field of the bookmark paste the following:
```JavaScript
javascript:(function () { const toggles = document.querySelectorAll('.yt-agile-table__row-title__summary__text'); toggles.forEach((toggle, i) => { const lane = toggle.closest('.yt-agile-table__row'); if (!lane) return; const isOpen = !!lane.querySelector('.yt-agile-table__row__cell'); if (isOpen) { toggle.click(); } });})();
```
3. Navigate to your YouTrack Board
4. Click the CLOSE bookmark and all swimlanes closes
