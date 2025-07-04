# Salesforce File Import — PowerShell CLI

This repository contains a CLI-ready PowerShell script to bulk upload `.pdf` files into Salesforce using the ContentVersion object, with metadata matching, logging, and duplicate handling.

---

## 🔧 Features

- Upload files as ContentVersion via Salesforce REST API
- Match files with external metadata (CSV)
- Create ContentDocumentLinks automatically
- Control file visibility (`InternalUsers`)
- Detect and defer duplicates to a manual review batch
- Log every action and error during processing

---

## 🗂 File Structure

- `upload.ps1` – main PowerShell script
- `config.json` – configuration file (instance URL, token, paths)
- `batch_manual_review.csv` – output queue for files requiring human review
- `.gitignore` – excludes logs and review outputs
- `README.md` – you're reading it 😄

---

## 🚀 How to Run

1. Fill in `config.json` with:
   - Your Salesforce access token
   - Folder path for `.pdf` files
   - Path to metadata CSV file

2. Launch PowerShell and run:
```powershell
.\upload.ps1
