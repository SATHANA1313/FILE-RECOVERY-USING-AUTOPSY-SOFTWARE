# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Install and launch autospy
<img width="1920" height="1200" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/7b4a2fec-2b3d-4747-b331-6a7e781494ec" />

case information
<img width="1920" height="1200" alt="Screenshot (50)" src="https://github.com/user-attachments/assets/a1d2ec63-9301-44e3-8c2a-54864b54361e" />

select data source type
<img width="1920" height="1200" alt="Screenshot (53)" src="https://github.com/user-attachments/assets/fada8c12-b63a-4c87-bbc1-c0694c67c7c9" />


<img width="1920" height="1200" alt="Screenshot (54)" src="https://github.com/user-attachments/assets/d41c323c-0b67-434e-a34d-b4ffdc618bd1" />

Add data source 
<img width="1920" height="1200" alt="Screenshot (56)" src="https://github.com/user-attachments/assets/fdd32376-e9f7-40a3-94ff-a4d4f2948184" />

File system analysis
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/74e83b83-b851-4219-955f-f6dd1fbcc2fb" />
Select file to exract
<img width="1920" height="1200" alt="image" src="https://github.com/user-attachments/assets/3e3368c7-68a6-402a-a47f-07338312d9e0" />
file exracted
<img width="1920" height="1200" alt="Screenshot (71)" src="https://github.com/user-attachments/assets/f79edd1c-a297-4a4a-8c13-37c27c9dc461" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
