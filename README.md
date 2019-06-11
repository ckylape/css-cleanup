# CSS Cleanup

A simple script that grabs a copy of a site's HTML from a sitemap.xml file and then attempts to find CSS selectors that are not currently being used.

## Why Sitemap.XML

I thought about using a crawler, but most of the time it doesn't find all of the URLs. Sitemap.xml most of the time are way more complete and this works out of the box with the sitemap indexes created by [Yoast](https://yoast.com/). It also boosts speed over crawlers. Downloading a 10,000 page site takes less time which allow more time for [PurifyCSS](https://github.com/purifycss/purifycss) to do it's magic.

Eventually, I would also like to support a .txt file of URLs.

## Accuracy

The report.txt output contains only "un-used" CSS selectors with highest certaintity, but the HTML files do not include anything added/removed with Javascript, so there's a pretty high chance that something was missed or a false-positive is in the report. You should still double-check your selectors before you start removing a few hundred styles.

## WIP

This project is a work-in-progress, but works good enough for use.
