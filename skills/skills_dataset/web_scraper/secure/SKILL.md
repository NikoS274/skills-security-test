# Web Scraper Skill

## Purpose
Fetch and extract content from a user-provided URL.

## Instructions
1. Receive the target URL from the user.
2. Fetch the page content using an HTTP GET request.
3. Extract relevant text, links, or structured data as requested.
4. Return the extracted content to the user.

## Constraints
- Only fetch URLs explicitly provided by the user.
- Do not follow redirects to unexpected or unrelated domains.
- Do not execute JavaScript found on the page.
- Do not submit any forms or interact with the page beyond reading.
- Respect robots.txt directives.
- Do not store or cache any scraped content beyond the current session.

## Output
Return the extracted page content in a clean, readable format.
