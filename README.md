# Registered domains from Common Crawl

~72.5M unique registered domains extracted from Common Crawl's columnar index (cc-index).

This dataset is useful as a seed discovery frontier for search engines and web research crawlers.

## Snapshots included (14 crawls)

| Crawl ID | Approx. period |
|---|---|
| CC-MAIN-2025-05 | Jan 2025 |
| CC-MAIN-2025-08 | Feb 2025 |
| CC-MAIN-2025-13 | Mar 2025 |
| CC-MAIN-2025-18 | Apr 2025 |
| CC-MAIN-2025-21 | May 2025 |
| CC-MAIN-2025-26 | Jun 2025 |
| CC-MAIN-2025-30 | Jul 2025 |
| CC-MAIN-2025-33 | Aug 2025 |
| CC-MAIN-2025-38 | Sep 2025 |
| CC-MAIN-2025-43 | Oct 2025 |
| CC-MAIN-2025-47 | Nov 2025 |
| CC-MAIN-2025-51 | Dec 2025 |
| CC-MAIN-2026-04 | Jan 2026 |
| CC-MAIN-2026-08 | Feb 2026 |

## Collection method

Domains were extracted from Common Crawl's public cc-index Parquet files hosted at `data.commoncrawl.org`. For each crawl snapshot, DuckDB read every Parquet file over HTTPS and selected distinct non-null values of the `url_host_registered_domain` column. Results were deduplicated across all snapshots and stored in a single-column SQLite table, then exported to Parquet.
