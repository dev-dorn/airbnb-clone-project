# airbnb-clone-project

## 📌 Team Roles

**Backend Developer**  
Builds and maintains the server-side logic, APIs, and business rules of the application. Integrates the database, handles authentication, and ensures performance and scalability.

**Frontend Developer**  
Implements the user interface, consuming the backend APIs and creating an intuitive experience. Works with frameworks (e.g., React) to ensure the app is responsive and accessible.

**Database Administrator (DBA)**  
Designs, implements, and maintains the database structure. Ensures data integrity, optimizes queries, manages backups, and monitors database performance.

**UI/UX Designer**  
Creates wireframes, mockups, and prototypes to define the product’s look and feel. Focuses on user experience, accessibility, and visual consistency.

**QA Engineer**  
Designs and executes tests to catch bugs before release. Ensures each feature meets the acceptance criteria and that regression tests are run when changes are made.

**Project Manager / Scrum Master**  
Coordinates timelines, team communication, and task prioritization. Ensures deliverables align with requirements and manages scope changes.

---

## 🛠 Technology Stack

- **Django** – Backend web framework for building robust APIs and handling server-side logic.  
- **PostgreSQL** – Relational database for storing structured application data.  
- **GraphQL** – Query language for more efficient and flexible API data fetching.  
- **React** – Frontend library for building interactive user interfaces.  
- **Docker** – Containerization for consistent dev/test/prod environments.  
- **Nginx** – Reverse proxy and static file serving in production.  
- **Redis** – In-memory store for caching and session management.  
- **Celery** – Task queue for handling asynchronous jobs like sending emails.

---

## 🗄 Database Design

**Entities & Key Fields**

- **User**: `id`, `name`, `email`, `password_hash`  
- **Property**: `id`, `owner_id`, `title`, `description`, `price_per_night`  
- **Booking**: `id`, `user_id`, `property_id`, `start_date`, `end_date`  
- **Review**: `id`, `user_id`, `property_id`, `rating`, `comment`  
- **Payment**: `id`, `booking_id`, `amount`, `status`, `payment_date`

**Relationships**
- A **User** can own multiple **Properties**.
- A **Property** can have many **Bookings**.
- A **Booking** belongs to one **User** and one **Property**.
- A **Property** can have many **Reviews** from different **Users**.
- A **Payment** is linked to a **Booking**.

---

## ⚙ Feature Breakdown

**User Management**  
Registration, login, and profile management. Provides secure authentication and personalized access.

**Property Management**  
Owners can create, edit, and delete property listings, including uploading images and setting pricing/availability.

**Booking System**  
Users can browse properties, select dates, and book stays. Includes availability checks and booking confirmation.

**Review System**  
Users can leave ratings and comments after their stay, contributing to property reputation.

**Payment Processing**  
Secure payment gateway integration for handling transactions, ensuring smooth booking completion.

---

## 🔐 API Security

- **Authentication** – Verify user identity using secure methods (e.g., JWT or OAuth). Protects against unauthorized access.  
- **Authorization** – Role-based access control to ensure users can only perform permitted actions.  
- **Rate Limiting** – Prevents abuse by limiting the number of API requests per time window.  
- **Input Validation & Sanitization** – Prevents SQL injection, XSS, and other injection attacks.  

Security here protects **user data**, **transactions**, and **business integrity**.

---

## 🚀 CI/CD Pipeline

**Definition**  
CI/CD (Continuous Integration / Continuous Deployment) automates code building, testing, and deployment, ensuring quick, reliable releases.

**Importance**  
- Detect bugs early through automated tests.  
- Deploy updates faster and more consistently.  
- Reduce human error in deployment processes.

**Tools**  
- **GitHub Actions** for automated builds/tests.  
- **Docker** for consistent packaging.  
- **AWS/GCP/Azure Pipelines** for production deployment.
## UI/UX Design Planning

### Design Goals
- Provide a simple and intuitive booking experience.  
- Ensure responsiveness across devices (desktop, tablet, mobile).  
- Prioritize accessibility (clear typography, sufficient contrast, alt text for images).  
- Maintain visual consistency (color palette, spacing, component styles).  

### Key Features
- Browse property listings with filtering and sorting options.  
- View detailed information for a property (photos, description, reviews, pricing).  
- Simple checkout flow to complete a booking with minimal friction.  

### Primary Pages
| Page | Description |
|------|-------------|
| **Property Listing View** | Displays a grid/list of available properties with filters (location, price, date range). Shows property cards with images, price, and rating. |
| **Listing Detailed View** | Provides in-depth information for a property: full image gallery, amenities, location map, reviews, and a booking button. |
| **Simple Checkout View** | Guides the user through the booking process (selecting dates, confirming guest info, reviewing cost, payment). |

### Importance of a User-Friendly Design
A booking system must be seamless because users are making **time-sensitive and financial decisions**.  
- A clear design reduces cognitive load and prevents abandonment.  
- Consistent navigation builds trust in the platform.  
- Fast, mobile-friendly UI improves conversions.  
- Visual hierarchy ensures the most important information (price, availability) is immediately visible.  
### Figma Design Properties

**Color Styles**
- Primary: #FF5A5F (Airbnb red/pink)  
- Secondary: #00A699 (teal)  
- Background: #FFFFFF  
- Text: #484848  
- Neutral shades for borders/dividers  

**Typography**
- Font Family: Sans-serif (e.g., Circular, Airbnb Cereal, or system fonts like Inter/Roboto)  
- Font Weights: Regular (400), Medium (500), Bold (700)  
- Font Sizes:  
  - Heading: 24px–32px  
  - Subheading: 18px–20px  
  - Body: 14px–16px  
  - Small/Caption: 12px  

### Why Identify Design Properties?
Design properties (colors, typography, spacing) act as a **design system**. They ensure:  
- Consistency across all pages and components.  
- Easier collaboration between designers and developers.  
- Faster iterations when making changes (update one style, propagate everywhere).  
- Scalability as the project grows.  
## UI Component Patterns

Planned reusable components include:  

- **Navbar**  
  - Contains logo, search bar, navigation links, user profile/login.  
  - Sticky on scroll for accessibility.  

- **Property Card**  
  - Displays image, title, price, rating, location.  
  - Clickable to navigate to the property’s detailed view.  

- **Footer**  
  - Includes links (About, Help, Terms, Privacy).  
  - Social media icons and contact info.  

Future components to explore:  
- Date Picker  
- Booking Summary Widget  
- Review Card  
- Filter/Sort Controls  
