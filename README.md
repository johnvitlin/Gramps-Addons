# Gramps Addons

This repository provides independently developed addons for Gramps, together with their user documentation and installation instructions.

## Available addons

| Addon | Description | Supported Gramps versions |
|---|---|---|
| [PDF Thumbnailer](PDFThumbnailer/README.md) | Generates thumbnails of PDF media objects using Ghostscript or Poppler. | 5.2 and 6.0 |

## Installing addons

1. Open Gramps and select **Edit → Addon Manager**.

2. Add a new addon project (you could name it Gramps-Addons) using the URL appropriate to your Gramps version:

   **Gramps 5.2**

   `https://raw.githubusercontent.com/johnvitlin/Gramps-Addons/main/gramps52`

   **Gramps 6.0**

   `https://raw.githubusercontent.com/johnvitlin/Gramps-Addons/main/gramps60`

3. Ensure the addon project is enabled and refresh the available addons.

4. Select and install the required addon.

5. Follow the instructions in the individual addon's documentation, including any additional software requirements.

Only one addon project needs to be configured for your Gramps version to access all compatible addons distributed through this repository.

## Source code

The development source code, build instructions and shared development tools are maintained in the separate [Gramps-Addons-Source](https://github.com/johnvitlin/Gramps-Addons-Source) repository.

## Related project

[Dynamic Web Extended (DWE)](https://github.com/johnvitlin/DWE-Addons) is maintained and distributed separately. It is not required to use PDF Thumbnailer.

## Licensing

Licence information is provided in the individual addon documentation and downloadable addon packages.