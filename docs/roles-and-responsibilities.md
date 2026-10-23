# Roles and Responsibilities
* **Admin:** Add/remove movies, manage theaters and showtimes, view booking statistics.
* **Customer (User):** Browse movies, select seats, make payments, manage booking history.

**`docs/roles-and-responsibilities.md`**
```markdown
# Roles and Responsibilities

```mermaid
flowchart LR
    Admin([Admin])
    Customer([Customer])

    Admin --> |Manages| M1[Movies & Theaters]
    Admin --> |Schedules| M2[Showtimes]
    Admin --> |Monitors| M3[Booking Statistics]

    Customer --> |Browses| U1[Movie Listings]
    Customer --> |Selects| U2[Theaters & Seats]
    Customer --> |Completes| U3[Payments]
    Customer --> |Receives| U4[E-Tickets]