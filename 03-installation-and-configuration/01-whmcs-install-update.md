# WHMCS Module Installation and Update

### PUQ Account Statement module **[WHMCS](https://puqcloud.com/link.php?id=77)**
##### [Order now](https://puqcloud.com/whmcs-addon-puq-account-statement.php) | [Download](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/) | [Community](https://community.puqcloud.com/)

## System Requirements

| Requirement | Minimum          |
|-------------|------------------|
| WHMCS       | 8.x or higher |
| PHP         | 7.4, 8.1, 8.2, 8.3, 8.4 |
| ionCube Loader | v15+  |

> **Note:** The module is encrypted with ionCube. Ensure that the correct ionCube Loader version is active on your web server.

---

## Download

The module can be ordered and downloaded from PUQ Cloud:

- **Order Module:** [https://puqcloud.com/whmcs-addon-puq-account-statement.php](https://puqcloud.com/whmcs-addon-puq-account-statement.php)
- **Documentation:** [https://doc.puq.info/books/account-statement-whmcs-addon](https://doc.puq.info/books/account-statement-whmcs-addon)
- **All Versions / Download:** [https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/)
- **Support:** [https://puqcloud.com/submitticket.php?step=2&deptid=1](https://puqcloud.com/submitticket.php?step=2&deptid=1)
- **Community:** [https://community.puqcloud.com/](https://community.puqcloud.com/)
- **Direct download link for the latest version:**

```bash
wget https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/PUQ_WHMCS-Account-Statement-latest.zip
```

> All versions can be found at this link:
> [https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Account-Statement/)

---

## Installation

### Step 1: Unzip the Archive
On your WHMCS server (or locally):
```bash
unzip PUQ_WHMCS-Account-Statement-latest.zip
```

### Step 2: Copy the Module Files
Copy the extracted module directory directly to your WHMCS directory:

```bash
# For addon modules:
cp -r PUQ_WHMCS-Account-Statement/puq_account_statement /var/www/html/whmcs/modules/addons/
```

### Step 3: Activate and Configure the Addon Module
1. Log in to the WHMCS admin area.
2. Navigate to **System Settings > Addon Modules** (or **Setup > Addon Modules** in older WHMCS versions).
3. Find **PUQ Account Statement** in the list and click **Activate**.
4. Click **Configure**, enter your **License Key**, and select the admin groups allowed to access the module.
5. Click **Save Changes**.

---

## File Structure

Structure of files after a successful installation:
```
whmcs/
└── modules/
    └── addons/
        └── puq_account_statement/          # Module files
```

---

## Update Procedure

To update the module to a newer version:
1. **Deactivate** the addon module in **Setup > Addon Modules** (System Settings > Addon Modules).
2. Make a backup of your WHMCS files and database.
3. Download the latest version archive.
4. Extract the ZIP and overwrite the existing files in the `modules/` directories.
5. **Reactivate** the addon module in **Setup > Addon Modules** (this will trigger database migrations). All settings and client data are safe during this process.
