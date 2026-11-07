# CommerceIQ — E-commerce Analytics Dashboard

A responsive static dashboard for Vercel. It reads the actual 46-column project CSV in the browser and provides interactive Year, Region, Sales Channel and Order Status slicers.

## Deploy to Vercel
1. Add `index.html` to the **root** of your GitHub repository (same level as README.md).
2. Commit the change to `main`.
3. In Vercel, set Root Directory to `./`, Framework Preset to `Other`, and leave Build Command and Install Command empty.
4. Set Output Directory to `.` and deploy. If Vercel redeploys automatically after the GitHub commit, use that deployment.
5. Open the site and click **Upload CSV dataset** to select the real `ecommerce_sales_customer_analytics_150k.csv`.

## Important: Git LFS
The CSV currently uploaded in this chat is only a Git LFS pointer file (two text lines), not the 48.7 MB dataset. Download the real file from your local Git LFS checkout or use `git lfs pull` after cloning with Git LFS installed. Do not upload the two-line pointer as the dataset.

## Data
The dashboard expects these fields from the full flat file: `order_id`, `order_date`, `order_status`, `sales_channel`, `customer_id`, `customer_country`, `region`, `marketing_channel`, `net_sales`, and `profit`. It calculates KPIs and charts from the imported rows. The CSV is parsed locally in the visitor's browser and is not sent to a server.

The portfolio baseline shown before data import is taken from the repository README: $177,134,263.74 net revenue, $76,146,395.76 profit, 138,116 orders, 24,911 purchasing customers, and $1,282.50 AOV. Filters and detailed charts become live after importing the full CSV.
