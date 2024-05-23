# Windows Print Spooler Service

Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.

The Windows Print Spooler is a popular target because it is running as SYSTEM and can easily be interacted with from a standard user via Win32 APIs over RPC.

It has drawn people to perform all sorts of interesting attacks, such as:
- Printing to a file in a privilege location, hoping Spooler will do that
- Loading a “printer driver” that’s actually malicious
- Dropping files remotely using Spooler RPC APIs
- Injecting “printer drivers” from remote systems
- Abusing file parsing bugs in EMF/XPS spooler files to gain code execution

### Covered issues:
- CVE-2020-1048
- CVE-2020-1337
- CVE-2020-17001
- CVE-2010-2729
- CVE-2020-1030


### Resources:
- [Printing (Documents and Printing)](https://learn.microsoft.com/en-us/windows/win32/printdocs/printdocs-printing)
- [Print Spooler API](https://learn.microsoft.com/en-us/windows/win32/printdocs/print-spooler-api)
- [Security Advisory: MSRPC Printer Spooler Relay (CVE-2021-1678)](https://www.crowdstrike.com/blog/cve-2021-1678-printer-spooler-relay-security-advisory/)
- [VoidSecs CVE-2020-1337 PoC](https://github.com/VoidSec/CVE-2020-1337)
- [BlackHat talk - Printing is still stairway to heaven](https://i.blackhat.com/USA-20/Thursday/us-20-Hadar-A-Decade-After-Stuxnet-Printer-Vulnerability-Printing-Is-Still-The-Stairway-To-Heaven.pdf)
- [PrintDeamon by Yarden Shafir & Alex Ionescu](https://windows-internals.com/printdemon-cve-2020-1048/)
- https://blog.ismaelvalenzuela.com/wp-content/uploads/2009/11/my_erp_got_hacked_1.pdf (Page 24)
