# PDF Thumbnailer for Gramps

PDF Thumbnailer is a Gramps addon that generates thumbnail images for PDF media files.

Instead of displaying a generic document icon, Gramps can display a thumbnail of the first page of a PDF document.

## Features

- Generates a PNG thumbnail from the first page of a PDF.
- Supports normal and large thumbnail sizes used by Gramps.
- Uses Poppler's `pdftoppm` utility for PDF rendering.
- Automatically searches for Poppler.
- Caches the discovered executable path to avoid repeated searches.
- Supports Gramps 5.2 and 6.0.

## Requirements

- Gramps 5.2 or 6.0.
- Poppler, installed separately.

**Poppler is not included with this addon.**

## Installing Poppler

Poppler is a free, open-source PDF rendering library and collection of utilities used to read, process and convert PDF documents. PDF Thumbnailer uses its pdftoppm utility to generate thumbnail images.

### Windows

Poppler is available as a prebuilt Windows package from the following GitHub repository:

**[Poppler for Windows — Latest Release](https://github.com/oschwartz10612/poppler-windows/releases/latest)**

To install Poppler:

1. Open the link above and download the ZIP archive from the latest release.
2. Extract the archive to a suitable directory, such as `C:\Poppler` , or one of the locations listed below.
3. Locate `pdftoppm.exe`, normally found in the `Library\bin` subdirectory.
4. Restart Gramps.

PDF Thumbnailer automatically searches several common installation directories, including `C:\Poppler`, `C:\Program Files\Poppler`, `C:\Program Files (x86)\Poppler`, `C:\Tools\Poppler`, and `%LOCALAPPDATA%\Poppler`.

Both direct installations and version-numbered subdirectories are supported. The addon also searches the system `PATH`.

If Poppler is installed elsewhere and cannot be found automatically, see **Optional configuration** below.

### Linux

Install Poppler using your distribution's package manager. Ensure that `pdftoppm` is available on the system `PATH`.

### macOS

Install Poppler using a suitable package manager and ensure that `pdftoppm` is available on the system `PATH`.

*Linux and macOS support has not yet been tested.*

## Optional configuration

Advanced users can specify the full path to the Poppler executable using the environment variable:

`PDFTHUMBNAILER_PDFTOPPM`

This is normally unnecessary when Poppler can be found automatically.

## Installing PDF Thumbnailer

PDF Thumbnailer is available for Gramps 5.2 and Gramps 6.0 and can be installed through the Gramps Addon Manager.

To install:

1. Open Gramps and select **Edit → Addon Manager**.

2. Add a new addon project (you could name it Gramps-Addons) and use the URL appropriate to your Gramps version:

   **Gramps 5.2**

   `https://raw.githubusercontent.com/johnvitlin/Gramps-Addons/main/gramps52`

   **Gramps 6.0**

   `https://raw.githubusercontent.com/johnvitlin/Gramps-Addons/main/gramps60`

   Note: If you have already configured the Gramps-Addons project for another addon, you do not need to add it again.

3. Ensure the addon project is enabled and refresh the available addons.

4. Find **PDF Thumbnailer** in the addon list and install it.

5. Restart Gramps to activate PDF Thumbnailer.

PDF Thumbnailer is an independent addon and does not require Dynamic Web Extended (DWE) or any other third-party Gramps addon to be installed.

## Using PDF Thumbnailer

PDF Thumbnailer is registered as a startup addon, and is activated when Gramps starts.  Once the addon and Poppler are installed, restart Gramps.

PDF Thumbnailer runs automatically when Gramps requests a thumbnail for a PDF media object. No additional activation is required.

If Poppler cannot be found, PDF Thumbnailer cannot generate a thumbnail. Gramps can continue displaying its normal document icon.

## Licence

PDF Thumbnailer is free software distributed under the GNU General Public License, version 2 or later (GPL-2.0-or-later).

Copyright (C) 2026 John Vitlin.
