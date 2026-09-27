# Scroll Receipt

An itemised receipt for the time you've spent on TikTok.

Drop in the data export TikTok gives you and the page adds up every video in your
watch history: total hours, average per day, your peak hour, your longest sitting,
zero-video days, and what that time could have paid for instead.

**Live:** https://m041997.github.io/scroll-receipt/

## Privacy

Your export is read inside your browser tab and never leaves it. There is no server,
no account, no analytics, and no tracking. The page only fetches its fonts from
Google Fonts and [JSZip](https://stuk.github.io/jszip/) (to open the .zip) from cdnjs;
your file is never sent anywhere.

## Getting your data

1. In TikTok, go to **Profile** and tap the **☰** menu.
2. Open **Settings and privacy → Account → Download your data**.
3. Select **All data**, set the format to **JSON**, and tap **Request data**.
4. When it's ready (usually a few days), download the .zip and drop it on the page.

## How time is estimated

The export has a timestamp for each video, not a watch duration. A gap of under
5 minutes before the next video counts as watching; a longer gap counts as 15 seconds.
TikTok stores times in UTC; the page converts them to your local time zone.

## Development

It's one static file, `index.html`. Open it in a browser — no build step.
