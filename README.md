# Nirnayasindu2

A PDF and companion-document catalogue based on Nyayapustika.

Website: https://shivaprasadacharya.github.io/nirnayasindu2/

## Add documents

Use **Add files**, upload to this repository, and commit to `main`. PDFs and `.doc`, `.docx`, `.rtf`, and `.txt` documents are supported, including files inside ordinary subfolders. Keep their original filenames; Nepali filenames and spaces are supported. This repository starts empty, ready for its own documents.

GitHub Pages rebuilds the catalogue after every commit. Wait for **pages build and deployment** to succeed, then refresh the website. `catalogue.json` is a Jekyll template: the deployed JSON is generated from the same files as the website, so it does not depend on GitHub API quotas or a manually maintained index. Do not add `.nojekyll` or remove the front matter from `catalogue.json`. Use ordinary folder names rather than names beginning with a dot or underscore, which Jekyll may exclude.

## Matching companions

- Give the PDF and companion the same filename before the extension: `Judgment.pdf` and `Judgment.docx`, for example.
- Any of DOC, DOCX, RTF or TXT can be a companion. When several formats exist, all are available in the PDF's row with their own **Open** and **Download** links.
- Matching ignores letter case and normalizes Unicode. A PDF in the same folder takes priority. Across folders, a companion attaches only when there is exactly one matching PDF.
- Ambiguous matches remain standalone, so no document disappears. Move a companion beside its intended PDF to resolve ambiguity.
- Unpaired PDFs and unpaired companion documents remain visible as standalone rows.

## Browse, search and download

The five-column table retains serial number, folder, filename, links and remarks. It includes Nepali-normalized and advanced search, match navigation, sorting, fullscreen previews, floating top/bottom buttons, and page sizes of 100 (default), 150, 200, 250, 300 or All. Filtering by a companion extension also shows PDF rows containing that format. Search covers names, categories and remarks, not document contents.

Counts show PDFs with at least one companion, total PDFs, total companion documents (paired and standalone), standalone PDFs, and standalone companions. A PDF with several companion formats counts once in the paired-PDF total.

PDFs and TXT open in the built-in preview; TXT can be copied. DOC/DOCX open through Microsoft's Office web viewer, which requires publicly reachable files and may not preview every document. RTF opens as the original file and may download depending on your browser. Every format has a direct download link. PDF preview guidance remains available when the browser cannot display a PDF.

## Verification

The verification screen uses the same configured mobile number as Nyayapustika. After that check, either the current Nepal-time **HHMM** or the master code **1234** opens the catalogue. For example, 09:05 is `0905`; 18:30 is `1830`. The analog clock runs in `Asia/Kathmandu`, based on the device clock. No digital time or code hints are shown on the page.

Session behaviour is retained: six-hour expiry and reuse within one hour after leaving. The entered number and code are not transmitted or saved. Only session timestamps are stored, under this site's own key.

This is a browser-side convenience check, not secure authentication or proof of phone ownership. No SMS is sent. The repository, documents, code and direct document URLs are public.

## Hosting

GitHub Pages publishes from `main` / root using its default Jekyll build. Keep `index.html` and `catalogue.json` at the repository root. No additional packages, API keys or server are needed. A plain local HTTP server can show the interface, but a Jekyll build is needed to generate the catalogue JSON from uploaded files.

Adapted from https://github.com/ShivaPrasadAcharya/nyayapustika.
