# DO Staffing Executive Dashboard

Static executive dashboard for DO Staffing Excel data. It can read an Excel file from:

- A local upload using the `เลือกไฟล์ Excel` button
- A SharePoint / OneDrive / Excel link address, if the link allows browser download
- A URL query, for example `?link=https%3A%2F%2F...`

## GitHub Pages Deployment

1. Create a new GitHub repository.
2. Upload everything in this folder to the repository root.
3. In GitHub, go to `Settings` -> `Pages`.
4. Set `Source` to `Deploy from a branch`.
5. Select branch `main` and folder `/root`.
6. Open the published GitHub Pages URL.

## Important Notes

- Do not commit real staffing Excel files to a public repository.
- `.xlsx`, `.xls`, and `.csv` files are ignored by default in `.gitignore`.
- SharePoint / OneDrive links may fail in the browser if Microsoft blocks direct download with authentication or CORS.
- If the link fails, either set the file permission to allow direct download or use a backend/Microsoft Graph proxy with proper Microsoft 365 authentication.

## Local Preview

From this folder:

```bash
python3 -m http.server 8124
```

Then open:

```text
http://127.0.0.1:8124/
```

