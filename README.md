# ConvoRecs crawl drafts

This repository contains draft crawl files for **Yves to review and apply** to ConvoRecs and Arbiter. These drafts do not establish that the live websites have changed.

## File mapping

| Repository file | Intended production URL |
|---|---|
| `convorecs.ai/robots.txt` | `https://convorecs.ai/robots.txt` |
| `convorecs.ai/sitemap.xml` | `https://convorecs.ai/sitemap.xml` |
| `arbiter.convorecs.ai/robots.txt` | `https://arbiter.convorecs.ai/robots.txt` |
| `arbiter.convorecs.ai/sitemap.xml` | `https://arbiter.convorecs.ai/sitemap.xml` |

## Crawl settings

Both robots files retain `User-agent: *` and explicit groups for all named bots, with `Allow: /` in every group and no exclusions or `Disallow` rules.

## Sitemap coverage

The ConvoRecs sitemap lists the homepage, Team page, and Values page. The Arbiter sitemap lists only the Arbiter homepage.

Additional Arbiter entries require identifying actual public, indexable page URLs. Buttons, tabs, and application states do not automatically represent additional URLs, and private account pages or personal resume/assessment results should not be added.

Do not add `lastmod` unless reliable significant page-update dates are available.

## Review checks

- Parse both XML files and verify the sitemap namespace.
- Confirm exactly three ConvoRecs URLs and one Arbiter URL, with no duplicates or incorrect hostnames.
- Confirm both robots files contain the wildcard group, all 25 named bot groups, `Allow: /` for every group, no `Disallow` rules, and the correct sitemap pointer.
- Review the repository diff for unintended file changes.

Official references: [Google robots.txt guide](https://developers.google.com/crawling/docs/robots-txt/create-robots-txt) and [Google sitemap guide](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap).
