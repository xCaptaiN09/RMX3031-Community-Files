<div align="center">

# RMX3031 Community Files

**Centralized repository for Realme X7 Max (RMX3031) and GT Neo Flash (RMX3350) modifications.**

[![Deployment](https://img.shields.io/badge/Cloudflare_Pages-Deployed-F38020?style=for-the-badge&logo=cloudflare)](https://rmx3031-community-files.pages.dev)
[![Maintainer](https://img.shields.io/badge/Maintainer-xCaptaiN09-blue?style=for-the-badge&logo=github)](https://github.com/xCaptaiN09)
[![Storage](https://img.shields.io/badge/Hosted_on-Internet_Archive-CCCCCC?style=for-the-badge&logo=internetarchive)](https://archive.org/details/@xcaptain09)


</div>

<hr>

## Infrastructure Access

| Node | Target URL |
| :--- | :--- |
| **Frontend Portal** | [rmx3031-community-files.pages.dev](https://rmx3031-community-files.pages.dev) |
| **Admin Panel** | [rmx3031-community-files.pages.dev/admin](https://rmx3031-community-files.pages.dev/admin) |
| **Storage Archive** | [Archive.org: @xcaptain09](https://archive.org/details/@xcaptain09) |

## System Architecture

Static site deployment managed via Cloudflare Pages. Data layer relies on JSON objects rendering categorical arrays to frontend tabs.

* **Frontend (`index.html`):** Dynamic DOM population, custom cursor tracking UI, horizontal overflow navigation.
* **Database (`index.json`):** Categorical arrays defining physical file parameters (ROMs, Kernels, Modules, OTA, Firmware, SP Tool FW, Recovery).
* **Administration (`admin.html`):** GUI utilizing GitHub REST API. Executes atomic commits to append JSON nodes and dynamically expand HTML tab architecture.

## Supported Hardware

* **RMX3031**: Realme GT Neo (China) / Realme X7 Max (India)
* **RMX3350**: Realme GT Neo Flash Edition (China)
* *Note: RMX3357 (GT Neo 2T) explicitly excluded from current scope.*

## Administration Protocol

Access the Admin Panel to inject database entries. Requires GitHub Personal Access Token (PAT) with `repo` scope.

1. Generate PAT via GitHub Developer Settings.
2. Authenticate within Admin Panel (token persists locally).
3. Configure payload parameters via GUI. URL generation supports automated ID/filename concatenation and manual override mapping.
4. Execute API commit. Cloudflare redeploys automatically (~30s execution time).
