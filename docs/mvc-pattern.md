# MVC Pattern Implementation
* **Model (Data):** Database schemas for Users, Movies, Theaters, and Bookings.
* **View (UI):** Frontend interfaces rendering movie lists, seat maps, and checkout pages.
* **Controller (Logic):** API routes handling business logic (e.g., verifying seat availability, calculating totals, processing payments).

**`docs/mvc-pattern.md`**
```markdown
# MVC Pattern Architecture

```mermaid
flowchart TD
    User([User / Browser])
    
    subgraph MVC Architecture
        Controller[Controller Layer\nAPI Routing & Logic]
        Model[(Model Layer\nDatabase/Schemas)]
        View[View Layer\nReact UI]
    end

    User -- Interacts with --> View
    View -- Sends Requests --> Controller
    Controller -- Queries/Updates --> Model
    Model -- Returns Data --> Controller
    Controller -- Sends JSON Data --> View
    View -- Updates UI for --> User