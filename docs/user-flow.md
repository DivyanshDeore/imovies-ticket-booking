# User Flow
1. User lands on the home page and browses movies.
2. User clicks on a movie to view details and available theaters/times.
3. User logs in or registers.
4. User selects a theater, showtime, and available seats.
5. User proceeds to checkout and completes payment.
6. System generates a ticket and sends a confirmation email.

**`docs/user-flow.md`**
```markdown
# User Flow Diagram

```mermaid
flowchart TD
    A([User Visits Homepage]) --> B[Browse Movies]
    B --> C[View Movie Details]
    C --> D{Is User Logged In?}
    
    D -- No --> E[Login / Signup]
    E --> F
    D -- Yes --> F[Select Theater & Showtime]
    
    F --> G[Interactive Seat Selection]
    G --> H[Proceed to Checkout]
    H --> I[Payment Gateway]
    I --> J[Generate Ticket & Confirmation]
    J --> K([End])