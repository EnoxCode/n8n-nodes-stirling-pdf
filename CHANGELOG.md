# Changelog

## Unreleased

### Added

- **Security → Verify Standards Compliance**: validate a PDF against the standards declared in its XMP metadata (PDF/A, PDF/UA-1, PDF/UA-2, WTPDF). Returns JSON.

## 0.2.0 - 2026-10-22

### Added

- **General** resource with **Merge** (several PDFs from one item into one, in the order of _Input Data Field Names_) and **Split Pages** (cut a PDF after the given pages).

### Fixed

- Binary results with a generic `application/octet-stream` content type now get their type and extension from the response's `Content-Disposition` file name, or else from the file's first bytes (ZIP, PDF, PNG, JPEG, GIF, WebP). ZIP results (e.g. PDF to Image with one image per page) previously came out as `.octet-stream` files that the Compression node could not unpack.
