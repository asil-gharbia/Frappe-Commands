# <img src="https://archive.org/download/github.com-frappe-erpnext_-_2021-10-23_15-35-28/cover.jpg" alt="Frappe Logo" width="30" height="30"> Frappe Commands - Quick Reference

This README provides a concise guide to essential Frappe commands for managing applications, sites, and development workflows. These commands are primarily executed within the Frappe Bench environment.

---

## **🚀** General Commands

### 1. **Start the Bench**
```bash
bench start
```
Starts the development server for the Frappe framework.

### 2. **Apply Database Migrations**
```bash
bench migrate
```
Executes pending database migrations for all installed apps.

### 3. **Build Frontend Assets**
```bash
bench build
```
Compiles and builds frontend assets for all apps.

To build assets for a specific app:
```bash
bench build --app APP_NAME
```

### 4. **Clear Cache**
```bash
bench clear-cache && bench clear-website-cache
```
Clears server-side and website caches for the current bench.

### 5. **Enable Developer Mode**
```bash
bench set-config developer_mode 1
```
Enables developer mode by updating the configuration in `site_config.json`.

### 6. **Export Fixtures**
```bash
bench export-fixtures
```
Exports all fixtures defined in the app's `hooks.py` file.

### 7. **Interactive Python Console**
```bash
bench console
```
Opens an interactive Python console within the Frappe environment.

### 8. **Open VS Code**
```bash
code .
```
Opens the current directory in Visual Studio Code.

---

## **🏗️** Site Management

### 1. **Create a New Site**
```bash
bench new-site SITE_NAME 
```
Creates a new Frappe site.

### 2. **Switch Active Site**
```bash
bench use SITE_NAME
```
Sets the specified site as the active site for the current bench session.

### 3. **Remove a Site**
```bash
bench drop-site SITE_NAME
```
Deletes the specified site along with its database.

---

## **🧩** App Management

### 1. **Create a New App**
```bash
bench new-app APP_NAME
```
Creates a new Frappe app.

Alternatively, fetch an app from a Git repository:
```bash
bench get-app https://github.com/REPO_URL
```

### 2. **Install an App**
```bash
bench --site SITE_NAME install-app APP_NAME
```
Installs the specified app on a given site.

### 3. **List Installed Apps**
```bash
bench --site SITE_NAME list-apps
```
Displays all apps installed on the specified site.

---

Feel free to use these commands as a quick reference for your Frappe development and management tasks.
