# KEDEN Data System

A comprehensive platform for dynamic form management, field data collection, and automated Google Drive cloud synchronization.

---

## Project Overview

KEDEN Data System is a web application and backend system designed for field data collection via customizable dynamic forms. The platform handles the complete workflow: from form field design and mobile data entry with attachments, to supervisor review, status tracking, and exporting comprehensive reports.

The system features an automated cloud storage engine that syncs images and attachments directly to Google Drive into structured folders organized by form and submission IDs.

---

## Technology Stack

### Backend & API Framework
- **PHP 8.4** - Runtime environment.
- **Laravel 13** - Web application framework.
- **Laravel Sanctum** - API token authentication for mobile and web clients.
- **Laravel Boost** - Developer tooling and workflow optimization.

### Cloud Storage & Integrations
- **Google Drive API** (`masbug/flysystem-google-drive-ext` and `google/apiclient`) - Automated attachment upload and synchronization.
- **Google OAuth 2.0** - Secure authentication with Google Cloud Services.

### Frontend & UI
- **Blade Components** - Admin and supervisor web dashboard templates.
- **Tailwind CSS v4** - Modern responsive user interface styling.
- **Vite** - Asset bundling and compilation.

### Reporting & Data Export
- **Maatwebsite Excel** - Exporting submission data to Excel spreadsheets.
- **mPDF & DomPDF** - Generating formatted PDF reports.

### Testing & Code Quality
- **Pest PHP 4 / PHPUnit 12** - Automated feature and unit testing suite.
- **Laravel Pint** - Code style formatting and PSR-12 compliance.

---

## Key Features

1. **Dynamic Form Generator**:
   - Supports diverse field types including short text, long text, single choice, multiple choice, image uploads, video files, and document attachments.
   - Configurable field validation rules, allowed MIME types, and file size limits.

2. **Automated Google Drive Sync**:
   - Stores field attachments in organized folder structures on Google Drive (`Keden_Data_System/form_{id}/submission_{id}`).
   - Resolves direct, secure Google Drive view URLs for persisted attachments.

3. **Role-Based Access Control (RBAC)**:
   - **Admin**: Complete system control, form builder, user management, form-to-user assignment, batch deletion, and global data export.
   - **Supervisor**: Access to assigned forms, submission review workflow (approve, reject, pending), and adding feedback comments.
   - **Data Entry**: Access to assigned forms via API/mobile client, field data submission, attachment uploading, and editing user-submitted entries.

4. **Reporting & Data Export**:
   - Export form submission data into Excel spreadsheets or printable PDF files.

5. **App Versioning Engine**:
   - API endpoints (`/api/latest-version`) for mobile app update notifications and forced upgrade management.

---

## User Interfaces & Screenshots

### 1. Admin Dashboard
Allows system administrators to manage users, build dynamic forms, define field types, and assign permissions.
<img width="1920" height="1041" alt="333333" src="https://github.com/user-attachments/assets/0a4cd4f7-e825-423a-b997-b87f1588c01e" />
<img width="1915" height="1036" alt="1111" src="https://github.com/user-attachments/assets/b8152f18-7488-4416-b4f1-72ba5d64ad20" />
<img width="1920" height="1042" alt="2222222" src="https://github.com/user-attachments/assets/07f50354-7d41-46ba-87b1-68b7959c4747" />


---

### 2. Supervisor Portal
Dedicated portal for supervisors to inspect submitted field data, update submission statuses (approved, rejected, pending), and attach reviewer notes.

<img width="5304" height="2778" alt="kdn-supers" src="https://github.com/user-attachments/assets/f3cbcca4-c37b-4de0-a376-d1dfc72b01c4" />


---

### 3. Data Entry & Field User Interface
Streamlined interface for field personnel to complete forms, capture photos/attachments, and track submission progress.

<img width="5304" height="2778" alt="kdn-users" src="https://github.com/user-attachments/assets/4891887b-edf6-43da-8393-5a0ea7be9658" />

---

## License

This project is open-sourced software licensed under the [MIT License](LICENSE).
