# Page Patterns

## MASTER 1Q2026 Workbook Patterns

Common sheets:

- `Home`
- `Financial Highlights`
- `Business Overview`

Homepage values usually come from `Home`:

- As-of date: `As of 31 March 2026` / `ข้อมูล ณ วันที่ 31 มีนาคม 2569`
- Our doctors / จำนวนแพทย์: `53`
- Our customers / จำนวนลูกค้าทั้งหมด: `162388`
- Number of main procedures / บริการของเรา: `101`
- Foreign customers / จำนวนลูกค้าต่างประเทศ: `22040`
- Customer circles: `2025 = 19855`, `1Q/2026 = 3054`
- Surgery hours: `2025 = 46005`, `1Q/2026 = 11080`
- Home chart Total Revenue: `2023 = 1948.93`, `2024 = 2162.66`, `2025 = 1899.28`, `1Q/2026 = 441.16`
- Home chart Net Profit: `2023 = 416.30`, `2024 = 522.45`, `2025 = 198.40`, `1Q/2026 = 61.03`

Financial Highlights chart summary rows can differ from detailed table rows:

- Chart Total Revenue 2024 may be `2162.66`.
- Detailed table Total Revenue 2024 may be `2156.52`.
- Chart Net Profit 2025 may be `198.40`.
- Detailed table Net Profit 2025 may be `198.00`.

For the detailed table, use the detailed table rows, not the summary rows:

- Periods EN: `2023`, `2024`, `2025`, `1Q/2026`
- Periods TH: `2566`, `2567`, `2568`, `1Q/2569`
- Total Assets: `3637.23`, `4505.67`, `4286.13`, `4326.52`
- Liabilities: `646.05`, `1010.94`, `834.85`, `814.22`
- Equity: `2991.18`, `3509.43`, `3451.28`, `3512.30`
- D/E: `0.22`, `0.29`, `0.24`, `0.23`
- ROA: `23.34`, `16.12`, `6.31`, `6.32`
- ROE: `24.52`, `16.11`, `5.70`, `5.75`
- Cash Cycle: `-20.79`, `-15.13`, `12.31`, `14.26`
- Revenues from hospital operations: `1916.76`, `2135.08`, `1884.83`, `436.35`
- Cost from hospital operations: `784.87`, `855.48`, `868.56`, `211.25`
- Gross Profit: `1131.90`, `1279.60`, `1016.26`, `225.10`
- Other Income: `26.82`, `21.45`, `14.46`, `3.91`
- SG&A: `633.92`, `702.23`, `756.50`, `169.95`
- Finance Income: `4.30`, `2.10`, `4.38`, `0.90`
- Interest / Finance cost: `13.88`, `18.46`, `29.29`, `6.22`
- Income tax expense: `104.73`, `115.35`, `50.08`, `10.88`
- Total Revenue table row: `1948.93`, `2156.52`, `1899.28`, `441.16`
- Net Profit table row: `416.30`, `522.45`, `198.00`, `61.03`
- Fully Diluted: `1.59`, `1.73`, `0.83`, `0.20`

## SKR Financial Highlight Patterns

For SKR-style annual-to-quarter updates:

- Update titles from FY/year to `Quarter 1/2026` / `ไตรมาส 1/2569`.
- `Revenue from Operation` pie values can come from rows under the revenue operation section:
  - Medical treatment: `98.88`
  - Food and beverage: `0.54`
  - Other revenue: `0.58`
- Put quarter values in chart `quarterly` arrays and set `QoQ: true`.
- Keep annual values in `yearly` arrays.

SKR detailed table example periods:

- EN: `Y/E '22 31/12/2022`, `Y/E '23 31/12/2023`, `Y/E '24 31/12/2024`, `Y/E '25 31/12/2025`, `Quarter 1/2026 31/03/2026`
- TH: `งบปี 65 31/12/2565`, `งบปี 66 31/12/2566`, `งบปี 67 31/12/2567`, `งบปี 68 31/12/2568`, `ไตรมาส 1/2569 31/03/2569`

Common SKR quarter values:

- Assets: `9671.30`
- Liabilities: `1648.51`
- Equity: `7930.22`
- Paid-up Capital: `1028.91`
- Revenue: `1404.22`
- Net Profit: `125.47`
- EPS: `0.06`
- ROA: `9.01`
- ROE: `8.50`
- Net Profit Margin: `8.94`
