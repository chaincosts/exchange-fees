# ChainCosts exchange fee datasets

Cited, machine-readable snapshots of cryptocurrency **exchange withdrawal fees** and related venue facts.

Live explorer and human-readable tables: **https://chaincosts.com/data**

Raw files on the site (same series, updated in place):

- https://chaincosts.com/facts.csv
- https://chaincosts.com/data/withdrawal-fees.json

This repository is a citable mirror. Numbers come from each venue's own public fee page or public API. A missing venue is a venue that does not publish the number without a login, not a zero.

## Files

| File | What it is |
| --- | --- |
| `withdrawal-fees.json` | Per-chain withdrawal fee, minimum, enabled flag, source URL, `verified_at`. Venues that publish: Binance, Bitget, CoinEx, HTX, KuCoin. Venues that withhold a public table (OKX, MEXC, Bybit, Coinbase, Kraken, Gate.io) are listed as withholding, not invented. |
| `facts.csv` | Entity facts used on ChainCosts pages: fees, licensing, rails. Columns include `source_url` / `human_source_url` and `verified_at`. |

## License

[CC BY 4.0](LICENSE). Facts themselves are not copyrightable; the compilation, schema, and documentation are. Attribution: cite **ChainCosts** and link to https://chaincosts.com/data

## Methodology

- Harvest only from a venue's public fee page or unauthenticated public API.
- Keep disabled / paused networks in the file. A paused route is not a missing number.
- `verified_at` is the harvest date of that row, not a promise the venue has not changed it since.
- Do not fill gaps with secondary blogs, app-store screenshots, or login-walled tables.

## Citation

```
ChainCosts. Exchange withdrawal fee snapshot. https://chaincosts.com/data
```

See `CITATION.cff`.
