# Entity-Relationship (ER) Diagram
* **User:** UserID, Name, Email, Password, Phone
* **Movie:** MovieID, Title, Genre, Duration, Language
* **Theater:** TheaterID, Name, Location, TotalScreens
* **Showtime:** ShowID, MovieID, TheaterID, StartTime, Price
* **Booking:** BookingID, UserID, ShowID, SeatNumbers, TotalAmount, Status
*(Insert an image or link to your actual ER diagram here once generated via tools like draw.io or Lucidchart).*

# Entity-Relationship (ER) Diagram

```mermaid
erDiagram
    USER ||--o{ BOOKING : makes
    MOVIE ||--o{ SHOWTIME : has
    THEATER ||--o{ SHOWTIME : hosts
    SHOWTIME ||--o{ BOOKING : includes

    USER {
        int UserID PK
        string Name
        string Email
        string Password
        string Phone
    }
    MOVIE {
        int MovieID PK
        string Title
        string Genre
        int Duration
        string Language
    }
    THEATER {
        int TheaterID PK
        string Name
        string Location
        int TotalScreens
    }
    SHOWTIME {
        int ShowID PK
        int MovieID FK
        int TheaterID FK
        datetime StartTime
        float Price
    }
    BOOKING {
        int BookingID PK
        int UserID FK
        int ShowID FK
        string SeatNumbers
        float TotalAmount
        string Status
    }