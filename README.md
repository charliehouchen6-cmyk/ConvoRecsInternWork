# ConvoRecs website metadata drafts

This repository contains draft website crawl and structured-data files for review. The files are not proof that the live websites have been updated; review and deploy them to the intended sites separately.

## Repository contents

| Repository file | Purpose / coverage | Intended production URL or use |
|---|---|---|
| `README.md` | Repository guide and review checklist | — |
| `convorecs.ai/robots.txt` | Allows crawling for the wildcard group and 25 named bot groups; points to the ConvoRecs sitemap | `https://convorecs.ai/robots.txt` |
| `convorecs.ai/sitemap.xml` | Lists the ConvoRecs homepage, Team page, and Values page | `https://convorecs.ai/sitemap.xml` |
| `convorecs.ai/structured-data.html` | JSON-LD describing the ConvoRecs organization and website | Review for placement on the ConvoRecs site before deployment |
| `arbiter.convorecs.ai/robots.txt` | Allows crawling for the wildcard group and 25 named bot groups; points to the Arbiter sitemap | `https://arbiter.convorecs.ai/robots.txt` |
| `arbiter.convorecs.ai/sitemap.xml` | Lists the Arbiter homepage only | `https://arbiter.convorecs.ai/sitemap.xml` |
| `arbiter.convorecs.ai/structured-data.html` | JSON-LD describing Arbiter as a software application | Review for placement on the Arbiter site before deployment |
| `sugoi.ai/index.html` | Short draft page heading and description for Sugoi | The file does not specify a production URL; confirm the intended domain before deployment |
| `sugoi.ai/structured-data.html` | JSON-LD describing Sugoi as a software application | Its `url` property currently names `https://sugoi.convorecs.ai`; confirm this matches the intended production URL before deployment |

## Crawl settings

Both robots files include `User-agent: *` and the same 25 explicitly named bot groups. Each group has `Allow: /`; there are no `Disallow` rules. Each file points to the sitemap on its corresponding host. These are draft settings and do not confirm the deployed robots files have the same contents.

## Sitemap coverage

- ConvoRecs: `https://convorecs.ai/`, `/team`, and `/values`.
- Arbiter: `https://arbiter.convorecs.ai/` only.

Only add sitemap entries for real, public, indexable URLs. Buttons, tabs, and application states do not automatically represent separate URLs. Do not include private account pages. Add `lastmod` only when reliable significant page-update dates are available.

## Structured data and Sugoi notes

The two ConvoRecs-related structured-data files are JSON-LD scripts wrapped in HTML `<script>` tags. Check their content and placement against the live pages before deployment. The Sugoi folder contains a short `index.html` fragment and a structured-data script, but does not contain a robots file or sitemap. The Sugoi structured data names `https://sugoi.convorecs.ai`, while the repository folder is `sugoi.ai`; confirm the intended public host and update the metadata or mapping if necessary.

## Review checklist

- Confirm the repository file inventory and intended production destinations before deploying.
- Parse both XML sitemap files and verify the sitemap namespace, expected URL counts (three for ConvoRecs and one for Arbiter), unique URLs, and correct hostnames.
- Confirm both robots files contain the wildcard group, all 25 named bot groups, `Allow: /` for every group, no `Disallow` rules, and the correct sitemap pointer.
- Validate the JSON-LD syntax and check every organization, application, and URL detail for accuracy; confirm where each script should be placed.
- Resolve the Sugoi production-host discrepancy before using its structured data.
- Review the repository diff for unintended file changes.

## Official references

- [Google robots.txt guide](https://developers.google.com/crawling/docs/robots-txt/create-robots-txt)
- [Google sitemap guide](https://developers.google.com/search/docs/crawling-indexing/sitemaps/build-sitemap)
- [Schema.org](https://schema.org/)
