# 🔐 Locker Register – Branch Locker Allotment Tracker

A Power Apps canvas app with SharePoint Online lists to track locker allotment and release at a co-operative credit society branch, replacing the physical register.

 Problem
Staff checked a paper register every time a customer asked about a locker. This was slow, error-prone and had no history or search.

Solution
- Visual grid of 36 lockers per set (2 sets), green = free, red = allotted
- Allot a locker: operator name, officer, date/time, page no., remarks
- Release a locker with a confirmation step and release remark
- Searchable register with filters (set, size, status, date range)
- Print / save-as-PDF report
- Login with lockout after 5 wrong attempts
- Works on mobile and desktop (responsive layout)

Tech stack
Power Apps (Canvas) · SharePoint Online lists · Power Fx · SVG-generated tiles

Screenshots
| Locker grid | Allot | Register |
|---|---|---|
| ![](Screenshots/02-locker-grid.png) | ![](Screenshots/03-allot-locker.png) | ![](Screenshots/04-register-report.png) |

 Data model
- **LockerEntries**: Title, LockerSet, LockerNo, KeyNo, PageNo, Officer, AllotAt, Remark, ReleasedAt, RelRemark, IsActive
- **LockerUsers**: Title (User ID), FullName, Password, IsActive

How to run
1. Create the two SharePoint lists above.
2. In Power Apps, import `App/Locker_Register.msapp`.
3. Reconnect the data sources to your lists.

Impact
Built and used at the Seloo Branch, Godavari Urban Multistate Credit Co-op Society, Nanded.

Planned improvements
Audit trail (allotted/released by), Microsoft 365 sign-in instead of passwords, delegable register filters, gallery-based tiles.

Author
Akash Ravi Sontakke – [GitHub](https://github.com/aakashsontakke456-pixel)
