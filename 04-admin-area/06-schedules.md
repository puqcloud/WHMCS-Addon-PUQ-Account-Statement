# Schedules

### PUQ Account Statement module **[WHMCS](https://puqcloud.com/link.php?id=77)**
##### [Order now](https://puqcloud.com/whmcs-addon-puq-account-statement.php) | [Download](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/) | [Community](https://community.puqcloud.com/)

The Schedules page is available at: **Addons** > **PUQ Account Statement** > **Schedules** > **All Schedules**

This page manages automated statement generation schedules. Schedules run automatically via WHMCS cron.

![Schedules — list of configured schedules](../img/07-schedules.png)
*07-schedules.png*

---

## Schedules Table

The table lists all configured schedules with the following columns:

| Column | Description |
|--------|-------------|
| **Name** | Schedule name for identification |
| **Frequency** | How often it runs: Daily, Weekly, Monthly, Quarterly, Yearly |
| **Client Filter** | Target clients: All, By Group, By Country, or With Unpaid Invoices |
| **Next Run** | Date and time of the next scheduled execution |
| **Last Run** | Date and time of the most recent execution |
| **Status** | Badge: **Active** (green) or **Inactive** (gray) |
| **Actions** | Action buttons (see below) |

---

## Actions Per Schedule

| Button | Icon | Description |
|--------|------|-------------|
| **Edit** | edit | Open the schedule editor to modify settings |
| **Run Now** | play | Execute the schedule immediately without waiting for the next scheduled time |
| **Toggle** | power-off | Enable or disable the schedule |
| **Delete** | trash | Delete the schedule (requires confirmation) |

---

## Creating a New Schedule

Click the **Add New** button at the top or go to **Schedules** > **Add Schedule** in the navigation menu.

See the [Schedule Editor](https://doc.puq.info/books/account-statement-whmcs-addon/page/schedule-editor) page for details on configuring a schedule.

---

## Sending All Outstanding Unpaid Invoices

To configure a recurring schedule that automatically sends statements with **all unpaid invoices** (regardless of the year the invoice was issued):

1. Click **Add New** (or edit an existing schedule).
2. In **General Settings**:
   - Enter a **Name** (e.g., `Weekly Outstanding Invoices Reminder`).
   - Select your desired **Frequency** (e.g., `Weekly` or `Monthly`).
   - Select **Period Type** as **All Unpaid Invoices** (or **All Time**).
3. In **Client Filter**:
   - Select **With Unpaid Invoices**. This ensures only clients with unpaid balances are selected.
4. In **Include Options**:
   - Check **Unpaid** only.
   - Uncheck **Paid**, **Refunded**, **Transactions**, and **Credits** so the statement focuses strictly on the unpaid balance and does not include historical paid items.
5. In **Output**:
   - Check **Send Email** (and optionally **Save to Archive**).
6. Click **Save Schedule**.

> [!TIP]
> When using **All Unpaid Invoices**, the module inspects all invoices from `1970-01-01` to the current date, ensuring unpaid invoices from prior years (2025, 2026, 2027, etc.) are never missed. If a client has zero unpaid invoices, the module automatically skips them and does not send empty emails.

---

## How Schedules Work

Schedules are executed by the WHMCS cron job. When a schedule's next run time is reached:

1. The module identifies matching clients based on the schedule's client filter
2. For each client, a statement is generated for the configured period
3. Depending on the schedule's output settings, statements are saved to archive and/or emailed to clients
4. The schedule's next run time is updated based on its frequency
5. Execution details are logged for reference
