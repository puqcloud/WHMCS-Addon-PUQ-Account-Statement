# Generate Statement

### Account Statement addon **[WHMCS](https://puqcloud.com/link.php?id=77)**
#####  [Order now](https://puqcloud.com/store/whmcs-addon-modules) | [Download](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/) | [FAQ](https://community.puqcloud.com/)

The Generate page is available at: **Addons** > **PUQ Account Statement** > **Generate**

This is the main page for creating individual account statements for a specific client.

![Generate Statement — parameters and preview](img/03-generate.png)
*03-generate.png*

---

## Statement Parameters

### Client Selection

Use the search field to find a client by name or email. The field uses Select2 with AJAX search — start typing at least 2 characters to see results.

> **Tip:** You can navigate here from the Dashboard's Quick Generate feature, which pre-selects the client.

### Date Range

Set the date range for the statement using:

- **Date From / Date To** — manual date inputs
- **Quick Period** buttons — one-click presets:
  - **This Month** — first to last day of current month
  - **Last Month** — first to last day of previous month
  - **This Year** — January 1 to December 31 of current year
  - **Last Year** — January 1 to December 31 of previous year

### Include Options

Select which financial data to include in the statement:

| Option | Description |
|--------|-------------|
| **Paid** | Include paid invoices |
| **Unpaid** | Include unpaid/outstanding invoices |
| **Refunded** | Include refunded invoices |
| **Transactions** | Include payment transactions |
| **Credits** | Include credit entries |

### Advanced Filters

| Filter | Description |
|--------|-------------|
| **Payment Methods** | Filter invoices by payment gateway (multi-select). Leave empty for all |
| **Product Groups** | Filter invoices by product group (multi-select). Leave empty for all |

---

## Actions

### View Statement

Click **View Statement** to generate and display the statement preview inline on the page. The preview shows the rendered HTML statement with all sections.

### Download PDF

Click **Download PDF** to generate and download the statement as a PDF file. The PDF uses the template configured in the Settings page.

### Download CSV

Click **Download CSV** to generate and download the statement data as a CSV file for import into spreadsheets or accounting software.

---

## Statement Preview Actions

After viewing a statement, additional action buttons appear in the preview header:

| Action | Description |
|--------|-------------|
| **Save to Archive** | Save the statement to the saved statements archive for future reference |
| **Send to Client** | Send the statement to the client via email with PDF attachment |
| **Generate Link** | Generate a public shareable link (copied to clipboard automatically) |

![Statement preview with action buttons](img/04-generate-preview.png)
*04-generate-preview.png*
