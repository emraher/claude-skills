---
name: posit-news
description: |
  Fetch and display the 5 latest blog posts from the Posit's blogs.
  Use when the user wants to see recent Posit news, blog updates, or company announcements.

---

# Posit News

Fetch the latest blog posts from Posit blogs and present them to the user.

## Blogs to Fetch

| Blog | URL | Posts |
|------|-----|-------|
| Posit | https://posit.co/feed/ | 5 |
| Tidyverse | https://www.tidyverse.org/blog/ | 5 |
| Shiny | https://shiny.posit.co/blog/ | 5 |
| Quarto | https://quarto.org/docs/blog/ | 5 |

## Instructions

1. Use WebFetch to retrieve each URL in parallel. For each, use this prompt:
   "Extract the [N] most recent blog posts with title, date, brief description, and URL."

2. For relative URLs, prepend the blog's base URL to form complete links.

3. Present the results grouped by blog in this format:
   ```
   ## Posit Blog (5 latest)

   - (YYYY-MM-DD) **Post Title**: Brief description. URL

   ## Tidyverse Blog (5 latest)

   - (YYYY-MM-DD) **Post Title**: Brief description. URL

   ## Shiny Blog (5 latest)

   - (YYYY-MM-DD) **Post Title**: Brief description. URL

   ## Quarto Blog (5 latest)

   - (YYYY-MM-DD) **Post Title**: Brief description. URL
   ```

4. If a URL cannot be retrieved, note the limitation and continue with other blogs.

## Example Output

## Posit Blog (5 latest)

- (2025-01-10) **Announcing Positron 1.0**: Posit releases version 1.0 of Positron, the next-generation IDE for data science. https://posit.co/blog/announcing-positron-1-0/

## Tidyverse Blog (5 latest)

- (2025-01-08) **dplyr 1.2.0**: New features in dplyr including improved joins and better error messages. https://tidyverse.org/blog/2025/01/dplyr-1-2-0/

## Shiny Blog (5 latest)

- (2025-01-05) **Shiny for Python 1.0**: Shiny for Python reaches 1.0 with production-ready features. https://shiny.posit.co/blog/shiny-python-1-0/

## Quarto Blog (5 latest)

- (2025-01-03) **Quarto 1.5 Release**: New features for scientific publishing and improved PDF output. https://quarto.org/docs/blog/posts/2025-01-03-quarto-1.5/
