# 📩 Dynamic DL Filter Updater

A PowerShell utility designed for IT administrators to **manage Dynamic Distribution Lists (DDLs)** in Exchange Online. It enables you to **generate reports**, **bulk update recipient filters**, and **preview (dry-run) which users would match those filters**, all via CSV.

---

## 🎯 Features

- ✅ **Generate Report**: Export all DDLs with current filters, readable summaries, and email addresses.
- ✏️ **Edit and Re-Upload**: Modify recipient filters directly in the generated CSV and apply updates in bulk.
- 🔍 **Dry Run**: Simulate filter results and export matching recipients per DDL.
- 🧑‍💼 UPN fallback logic: If `UserPrincipalName` is missing, it falls back to `PrimarySmtpAddress`.

---

## 📂 Output Overview

| File / Folder | Description |
|---------------|-------------|
| `DynamicDL_RecipientFilters_YYYY-MM-DD.csv` | Main report and editable source for updates |
| `DryRun_Results/` | One CSV per DDL showing members matching its filter |

---

## 🧰 Prerequisites

- Windows OS with PowerShell 5.1+
- Exchange Online Management Module  
  ```powershell
  Install-Module ExchangeOnlineManagement -Scope CurrentUser
  ```
