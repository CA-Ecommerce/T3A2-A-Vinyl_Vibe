# Vinyl Vibe - T3A2-A

Vinyl Vibe is a sophisticated e-commerce store built using the MERN stack. This platform seamlessly integrates secure payment processing, user authentication, and inventory management into a user-friendly shopping experience.

At its core, the application serves as a bridge between businesses and their customers, offering a modern, responsive interface for browsing products, managing purchases, and processing secure transactions. Built with scalability in mind, it accommodates both small businesses and larger enterprises, providing essential tools for inventory management, order processing, and customer engagement.

The platform combines React's powerful frontend capabilities with Express.js's robust backend, MongoDB's flexible data management, and industry-standard security practices. With features like Stripe integration for payments and automated email notifications through Resend, it delivers a comprehensive solution for modern e-commerce needs.

Key aspects include:

-   Secure user authentication and authorization
-   Comprehensive product management system
-   Streamlined checkout process with Stripe integration
-   Responsive design for all devices
-   Admin dashboard for business operations
-   Real-time inventory tracking
-   Automated email notifications for orders and updates

<br>

## Table of Contents

-   [Features and Functionality](#features-and-functionality)

    -   [MVP Features](#mvp-features)
    -   [Additional Features](#additional-features-post-mvp)

<br>

-   [Packages, Dependencies and Third-Party Services](#packages-dependencies-and-third-party-services)

    -   [Backend](#backend)
    -   [Frontend](#frontend)
    -   [Development](#development)
    -   [Deployment Services](#deployment-services)

<br>

-   [Dataflow & Application Architecture](#dataflow-and-application-architecture)

    -   [Dataflow Diagram](#dataflow-diagram)
    -   [Application Architecture Diagram](#application-architecture-diagram)

<br>

-   [User Stories & Personas](#user-stories-and-personas)

    -   [Persona 1](#persona-1)
    -   [Persona 2](#persona-2)
    -   [Persona 3](#persona-3)
    -   [User Story 1](#user-story-1)
    -   [User Story 2](#user-story-2)
    -   [User Story 3](#user-story-3)

<br>

-   [Task Management and Project Progress](#task-management-and-project-progress)
    -   [Trello Board](#trello-board)
    -   [Key Milestones](#key-milestones)

<br>

## Features and Functionality

### MVP Features

1. **User Authentication and Management**

    - Secure registration and login system
    - JWT-based authentication
    - Password reset via email
    - User profile management
    - Role-based access (Customer/Admin)
    - Order history tracking
    - Address management

2. **Product Management**

    - Product catalog with detailed information
    - Multiple product images
    - Category organization
    - Search functionality
    - Stock level tracking
    - Product availability status
    - Basic sorting options

3. **Shopping Experience**

    - Intuitive shopping cart
    - Real-time stock updates
    - Mobile-responsive design
    - Product image galleries
    - Cart persistence
    - Guest checkout option
    - Basic product filtering

4. **Payment and Checkout**

    - Stripe payment integration
    - Secure checkout process
    - Order confirmation system
    - Email notifications
    - Basic shipping options
    - Order tracking
    - Transaction history

5. **Admin Features**
    - Product CRUD operations
    - Basic inventory management
    - Order processing system
    - Category management

### Additional Features (Post-MVP)

1. **Enhanced Shopping Features**

    - Product reviews and ratings
    - Wishlist functionality
    - Recently viewed products
    - Social sharing

2. **Advanced Commerce Features**

    - Multiple payment methods
    - Discount code system

3. **Advanced Admin Tools**
    - Advanced analytics
    - Bulk product management
    - Advanced user management
    - Sales reports
    - Customer insights
    - Staff accounts

Each feature is designed to enhance the overall shopping experience while providing businesses with powerful tools to manage their online presence effectively.

<br>
<br>

## Packages, Dependencies and Third-Party Services

The E-commerce Store utilises carefully selected technologies that work together to create a robust online shopping experience. Here's a detailed overview of our technology choices and why they're essential for our project:

### Backend

-   `Express.js` (version 4.18.2)
    -   body-parser
    -   cors
    -   compression
        We chose Express.js as our backend framework for its minimalist yet powerful approach. Its middleware system is perfect for our e-commerce needs, allowing us to easily implement authentication, request processing, and error handling. The large ecosystem of middleware packages helps us solve common e-commerce challenges like CORS for secure client-server communication and compression for faster response times.

<br>

-   `MongoDB` (version 6.3.0)

    -   mongodb (version 6.3.0)
    -   mongoose (version 8.1.1)

    MongoDB's flexible schema design is ideal for our e-commerce platform where product attributes can vary significantly. Mongoose adds a crucial layer of structure and validation, ensuring our product data, user profiles, and order information maintain consistency. The schema-based approach helps prevent errors in critical operations like order processing and inventory management.

<br>

-   `JSON Web Token` (version 9.0.2)

    -   jsonwebtoken

    JWT provides a secure and scalable solution for user authentication in our e-commerce platform. It enables stateless authentication, perfect for maintaining user sessions across multiple devices while accessing protected routes like user profiles, order history, and admin functions.

<br>

-   `Stripe` (version 14.14.0)

    For handling payments, Stripe is our go-to choice due to its robust security features and comprehensive API. It manages complex payment flows while ensuring PCI compliance, handling multiple currencies, and providing detailed transaction analytics - crucial features for any modern e-commerce platform.

<br>

-   `Resend` (version 3.2.0)

    Email communication is vital for e-commerce, and Resend provides a modern, developer-friendly solution. We use it for sending order confirmations, shipping updates, password resets, and marketing communications, with excellent delivery rates and easy-to-use templates.

<br>

-   `Jest` (version 29.7.0)

    -   supertest

    Testing is crucial for maintaining reliability in e-commerce systems. Jest provides a comprehensive testing solution for our backend, allowing us to verify critical paths like checkout processes, inventory updates, and user authentication flows with confidence.

<br>

### Frontend

-   `React` (version 18.2.0)

    -   react-dom
    -   react-router-dom (version 6.22.0)

    React forms the foundation of our frontend, chosen for its component-based architecture that perfectly suits our e-commerce UI needs. It enables us to create reusable components for product cards, shopping carts, and checkout forms while maintaining excellent performance through its virtual DOM system.

<br>

-   `Vite` (version 5.1.0)

    -   @vitejs/plugin-react

    Vite significantly improves our development workflow with its lightning-fast hot module replacement and optimised build process. This means faster development cycles and better performance for our customers, crucial for maintaining a competitive e-commerce platform.

<br>

-   `Tailwind CSS` (version 3.4.1)

    -   postcss
    -   autoprefixer

    Tailwind CSS enables us to build a consistent and responsive design system efficiently. Its utility-first approach allows rapid UI development while maintaining a professional look across our product catalog, shopping cart, and checkout process. The built-in responsive design utilities ensure our store looks great on all devices.

<br>

-   `shadcn/ui` (version 0.8.0)

    -   @radix-ui/react-\* (various components)
    -   class-variance-authority
    -   clsx
    -   tailwind-merge

    We leverage shadcn/ui to provide a consistent and accessible component library. Its integration with Tailwind CSS and focus on customization allows us to maintain brand consistency while providing a polished user experience across all interactive elements of our store.

<br>

-   `Vitest` (version 1.2.0)

    -   @testing-library/react
    -   @testing-library/jest-dom

    Vitest ensures our frontend components and user interactions work flawlessly. Its compatibility with Vite makes it perfect for testing critical user flows like add-to-cart functionality, checkout processes, and form validations in a way that mimics real user behaviour.

<br>

-   `Axios` (version 1.6.7)

    For handling API communications, Axios provides a robust solution with features like request/response interceptors and automatic JSON transformation. This is crucial for maintaining smooth communication between our frontend and backend, especially for operations like cart updates and order processing.

<br>

### Development

-   `nodemon` (version 3.0.3)

    During development, nodemon dramatically improves our workflow by automatically restarting the server when code changes are detected. This is particularly valuable when working on API endpoints and backend business logic, ensuring we can quickly test and iterate on features.

<br>

-   `dotenv` (version 16.4.1)

    Security is paramount in e-commerce, and dotenv helps us manage sensitive configuration data like API keys and database credentials safely across different environments. It's essential for maintaining secure configurations between development, testing, and production environments.

<br>

### Deployment Services

-   `Vercel`
    For our e-commerce frontend, Vercel is the ideal choice due to its seamless integration with React applications. Its zero-configuration deployment process means we can focus more on developing features rather than dealing with deployment complexities. The platform's edge network ensures our store loads quickly for customers worldwide, while the automatic preview deployments for each pull request enable our team to confidently review changes before they go live. The built-in analytics help us understand user behaviour and optimise the shopping experience.

<br>

-   `Render`

    We chose Render for our backend deployment because it strikes the perfect balance between simplicity and power for a Node.js/Express API. Unlike more complex platforms like AWS, Render allows us to deploy our API with minimal configuration while still providing enterprise-grade features. Its automatic scaling capabilities ensure our store can handle traffic spikes during peak shopping periods or sales events. The seamless integration with MongoDB Atlas and built-in SSL security makes it ideal for handling sensitive customer data and payment processing through Stripe.

<br>

-   `MongoDB Atlas`

    For an e-commerce platform that needs to handle dynamic product catalogs, user sessions, and order processing, MongoDB Atlas provides the flexibility and scalability we need. Its document-based structure perfectly matches our data models for products, users, and orders, while the ability to perform complex queries helps with features like product filtering and search. The automated backups and security features protect our customer data, while the global distribution ensures fast database access regardless of customer location. The built-in monitoring helps us optimise performance and identify potential issues before they impact the shopping experience.

<br>

These packages and their dependencies work together to provide a robust, secure, and efficient full-stack e-commerce application, handling everything from database operations and payment processing to user interface components and testing.

<br>

## Dataflow & Application Architecture

![Dataflow_Diagram_V3](docs/Dataflow-Diagram/dataflow_diagram_V3.JPG)

### External Entities
External entities represent the User/Admin or systems that interact with the application from the outside. These entities provide input or receive output from the system.

User
-   Represents the customer interacting with the eCommerce store.
-   Actions:
    -   Authenticates to log in or register
    -   Browse products
    -   Add items to shopping cart
    -   Proceed to checkout
    -   Payment

Admin
-   Represents the store administrator who can manage the store and perform CRUD operations.
-   Actions:
    -   Manages Product, Orders and Users via CRUD operations
    -   View the admin dashboard tools

Guest
- Represents a guest browsing the store without logging in.
- Actuons:
    - Browse products
    - Add items to shopping cart
    - Proceed to checkout (Checkout will then require login)

Payment Gateway (Stripe)
-   Third party service used to securely process payments.
-   Actions:
    -   Processes payment details submitted by customer during checkout
    -   Returns a payment confirmation or failure status

Email service (Resend)

-   Third party email service used for sending transactional emails.
-   Actions:
    -   Sends order confirmation emails to the customer upon successful order payment
    -   Sends additional updates related to orders or account activities

### Processes
Processes represent the core operations or functions that process, manipulate, or route data within the system.

User Signup (1)
- Users can signup with a new login to the website
- Inputs: New login credentials (email and password)
- Outputs: User account creation enabling login access

User Login (1.5)
- The standard user login which can access all areas of the website excluding the admin dashboard.
- Inputs: Login credentials (email and password)
- Outputs: Successful JWT token for a User login

Admin Login (1.5)
- Admin role able to access all areas of website including admin dashboard
- Inputs: Login credentials (email and password)
- Outputs: Successful JWT token for Admin login

 User Authentication (2)
- Validates user credentials during login or registration
- Inputs: User credentials (email and password)
- Outputs: Authentication token (JWT) on success or error message on failure

Add to Cart (3)
- Adds products to shopping cart to view and use for checkout
- Inputs: Product data
- Outputs: Adds product data to cart

Shopping cart (4)
- Handles the uesr's shopping cart operations. Shows a list of products that have been added to cart, with product details (Price, SKU, Quantity, etc)
- Inputs: Product selections (add, remove, modify quantities)
- Outputs: List of selected items with quantities and pricing

Checkout and Payment (5)
- Manages the checkout process and interfaces with the payment gateway (via stripe)
- Inputs: Shopping cart details and payment details
- Outputs: Order confirmation on success or error message on failure

Successful Order Page (6)
- Displays a confirmation message and order details upon successful checkout

Continue Shopping (7)
- Allows users to return to browsing and shopping with a reset cart after successfully completing a checkout
- This process ensures users can continue their shopping journey with a refreshed cart, enabling them to explore and add new products

### Processes Cont. (Admin Dashboard) 

Admin Dashboard
- Provides the admin with tools for managing the store via CRUD operations
- Inputs: Admin actions for product, user and order management
- Outputs: Updated product, user and order details displayed and stored

Product Management
- Handles the management of product inventory, including creating, updating, viewing, and deleting products
- Inputs: Product data provided by the admin for CRUD operations (e.g. product name, price, stock quantity)
- Outputs: Updated product records stored in the database and reflected in the store's product listings

Order Management
- Manages the lifecycle of orders, from creation to tracking and fulfillment
- Inputs: Shopping cart details, payment confirmation from the payment gateway and user information
- Outputs: New order records stored in the database and a confirmation email sent to the user via Resend

User Management
- Oversees the management of user accounts within the system, including creating, updating, viewing and deleting user records
- Inputs: User data provided by the admin for CRUD operations (e.g. user profile information)
- Outputs: Updated user records stored in the database and reflected in the admin dashboard

### Data Stores

Where the data is stored in the system and is accessed or updated by the processes.

1. User Database
-   Stores user account information (name, email)
-   Contents:
    -   User Profiles (name, email, address)
    -   Login credentials (hashed passwords)
    -   Order history

2. Products Database
-   Stores product information
-   Contents:
    -   Product details (ID, SKU, name, description, price, stock level)

3. Orders Database
-   Stores records of all orders placed by users
-   Contents:
    -   Order details (items purchased, quantities and total price)
    -   Payment status


<br>

Explanation of application architecture here...

**--IMAGE of Application Architecture Diagram--**

<br>

## User Stories & Personas

<strong>Vinyl Vibe</strong> is an expanding Record Store with a <em>cult following</em>!

After many years of struggling to keep the doors open as <strong>Groovy Records</strong>, the resurgence of the Vinyl Record market in the past 5 years has seen them outgrow the crude, hardcoded, HTML page that owner Norm Gleeson's nephew created in the 90s, attached below (image reference 1).

Norm has a large inventory of rare and hard to find records from both famous and obscure Australian artists, including highly sort after records that never made it into International markets. He is the go to guru for all things Aus Music!

Word of the treasure trove of rare and hard to find records at <strong>Vinyl Vibe</strong> has travelled far and wide through Facebook and Reddit. They've identified a growing market of customers who want buy from Norm, <em>but don't live in the area.</em>

Norm needs an effective modern website that can connect and sell to their customers, be they local, interstate, or international!

### Persona 1

#### Shop Owner

Name: Norm Gleeson

#### Demographic:

-   66 years old
-   Divorced
-   No children
-   Former Musician and Roadie for The Screaming Jets turned Record Store Owner.

#### Goals:

-   Share his passion for music with the expanding community of music lovers, collectors, and audiophiles who purchase records and turntables from his shop.
-   Expand his busisness to provide a more stable income for himself and his staff.
-   Build a brand for his business to allow him to increase the size of his professional network.
-   Expand his professional network to allow him to better serve his customers in the exchanging of hard to find and rare records.

#### Motivations:

-   To help his customers discover the simple joy of listening to a vinyl record. To learn to appreciate the work that has gone into a piece of art. The stories that are shared. The sound quality, the hiss and crackle, and the experience of not being distracted with skip buttons, fast forward and the overwhelm of endless options and advertising on streaming services.

#### Frustrations:

-   His current website (much like most of his fondest memories of being on the road) is stuck in the 90s and is well overdue for an update, but Norm takes a while learning new systems and building a website is well outside his skillset.
-   With an estmiated <strong>80-100 milk crates full of records in his exisiting inventory</strong>, Norm isn't even sure how many records he has at any given moment. It's also difficult for him to keep track of what comes and goes. There are many records that could be getting sold, but aren't even advertised on his website. Not that it would matter, as the SEO for his website is almost non-existent and it gets very little traffic.

<br>

### Persona 2

#### Store Manager/Webmaster

Name: Ruby Harper

#### Demographic

-   38 years old
-   Married
-   3 children
-   Former manager of a JB Hi Fi.
-   Amateur musicain and artist.

#### Goals:

-   To take the organisation of stock out of Norm's hands so that he can focus on what he does best, building relationships with his customers and direct selling.
-   To have a website that at any given time has <strong>EVERY</strong> record they have in boxes and milk creates advertised to buy. Titles should also be searchable.
-   A stremlined process for customers to log onto their website and create a profile to track orders and addresses. This will allow for direct marketing through email, or even traditional postage of newsletters and catalogues.
-   Expand the business so they can move to a larger premises. This will create opportunites for them to add additional income streams, such as:
    -   A cafe with a liquor license,
    -   A small live venue suitable for album launches, listening parties, and signings,
    -   More display space for their existing stock,

#### Motivations:

-   To once again thrive in a store that's main focus is music, and not a "Bing Lee with records" (which is what she believes JB Hi Fi has become.)
-   To feel a sense of pride, ownership, and community in her workplace while nurturing her passion for music.
- To form lifetime connections with local independent musicians, giving them a place to stock and sell their music to the world. 
- To become a destination that touring artists stop for promotions and signings.

#### Frustrations:

-   So much unrealised potential in this business!
-   Incomplete database of stock, orders, and customers.
-   A very outdated website that is quite obnoxious and ineffective.
-   No procedures for marketing or retargeting past customers.

<br>

### Persona 3

Name: Atticus Hastings-Du Toit

#### Demographic

-   29 Years old
-   Single
-   2 x "Furr Children"
-   Record collector, Audiophile, and Coffee Enthusiest.
-   Amateur DJ and Producer.

#### Goals:

-   To have a large and eclectic record collection on display in his house, including every record by Arcade Fire, Bon Iver, and Daft Punk.
-   To create new productions with obscure songs that haven't been sampled before.
-   To have his sound system and turn table working at their optimum at all times.

#### Motivations:

-   Always looking to expand his record collection, especially with rare and hard to find records that he can boast about. The more obscure the better.
-   Obscure records offer him an opportunity to unearth songs that haven't been sampled before when creating beats.

#### Frustrations:

-   Can't make it into Vinyl Vibe in person as often as he would like to.
-   Wants to be able to search a catalogue of Norm's records from home, and purchase online. 
- Has a network of collectors that he would happily refer to Vinyl Vibe, but they don't live in the area.  
    <br>

### Persona 4

#### Shop Owner

Name: Diego Navarro

#### Demographic

-   64 Years old
-   Married
-   4 kids
-   Former roadie for Pearl Jam who became friends with Norm on a Screaming Jets USA tour in the early 90s.
-   Has recently opened <strong>The Needle Drop</strong>, a similar store to Vinyl Vibe in Seatle, Washington, USA.
-   Decades of industry knowledge and another extremely large and mostly uncatalogued collection of rare and hard to find records.
-   Potential customer for a website like the one being made for Vinyl Vibe.

#### Goals

-   Same goals as Norm, but specifically and in addition:
-   Create a website that can reciprocate the service that Vinyl Vibes website will provide for him. 

#### Motivations:

-   Grow his business to the cult like status that Vinyl Vibes has achieved.
-   Much like Norm, share his knowledge and passion for music with the record enthusiest community.
-   Refine a reciprocal agreement with Vinyl Vibe where they share resources. NB: Due to his location, local knowledge, and network, Diego has access to a lot of early Grunge and Alternative Records that didn't make it to Australia. Similarly, Norm has access to a lot of even rarer Pub Rock, New Wave, and Underground records from Australia that have never made it outside of the Southern Hemisphere that have become quite reveered by collectors in Seattle. 

#### Frustrations:
-   Regularly in contact with Norm (by phone call) to trade and find records for his customer base.
-   Would buy from Norm more regularly if it were easier to see his stock levels on an up-to-date and easy to navigate website. Not having to call at 3am would be a bonus too.
<br>

### User Story 1

<strong>As the owner of Vinyl Vibe,</strong>

-   I want to attract new customers from outside my local area with a method of purchasing my stock for shipping.
-   I need branding that reflects my desire to be viewed as a modern business with decades of expertise in my field.
-   I need a method to properly catalogue my ever changing stock of records, turntables, parts, and accessories.

<br>

### User Story 2

<strong>As a Vinyl Vibe's manager,</strong>

-   I want to grow our business through serving our customers much better than we have been.
-   I want a simple to use backend for the website that allows me to catalogue and advertise the vast stock of records, turn tables, parts and accessories we have at any given time.
-   I want to be able to retarget our previous customers to advertise sales,small events, and listening parties that will get people into the store where they're more likely to buy records.
-   We need to be able to effectively advertise to the people outside of our local area chasing very hard to find records that we currently have in stock, but not advertised.

<br>

### User Story 3

As a cutsomer of Vinyl Vibe,

- I want to be able to search their catalogue from my phone and make purchases from wherever I am. 
- I want to be able to recommend them to other people from the record colleting communtiy so the store can thrive. 
- I want Vinyl Vibe to grow even bigger so I can say that I knew about and used to go there before it was mainstream.....

<br>

### User Story 4

As the owner of The Needle Drop in Seattle, 

- I want to see how a modern website works out for Vinyl Vibe before I commit to the investment myself.
- I want a website that is going to allow me to advertise to my potential customer base all over the world.
- I want to keep support the industry that has supported me and enriched my life. 
- I want to expand my business so that I can move to a larger premises and create more product lines and income streams. 
- I want a business that my family can run without me micro managing! I just want to oversee the store, hangout, and sell. 
<br>

---

<details>
  <summary>Image References</summary>

  <br>

-   Reference 1

    <img src="docs/user-stories/reference-1.png" alt="Groovy Records Webpage Reference" width="300">

    <br>

-   Reference 2
    <img src="docs/user-stories/reference-1.png" alt="Groovy Records Webpage Reference" width="300">
    </details>

---

<br>

## Site Map

Our e-commerce platform's structure is designed to provide intuitive navigation for both customers and administrators. The site map illustrates the hierarchical organization of pages and features, ensuring a logical flow from browsing products to completing purchases. We've organised the navigation to minimise the number of clicks required to reach any destination while maintaining a clear separation between customer-facing pages and administrative functions.

The following site map outlines the complete structure of our application:

![Image of the desktop wireframe for all pages](/docs/wireframes/site-map.png)

<br>

## Wire Frames

We designed three breakpoints for the following devices:

-   Mobile
-   Tablet
-   Desktop

You can view the Figma file [here](https://www.figma.com/design/FcoiuafqXz3Ca4uVnaOFhp/%5BCODER-ACADEMY%5D-Ecommerce-App?node-id=14-65499&node-type=canvas).

### **Desktop view**

![Image of the desktop wireframe for all pages](/docs/wireframes/wireframe-desktop.png)

### **Tablet view**

![Image of the desktop wireframe for all pages](/docs/wireframes/wireframe-tablet.png)

### **Mobile view**

![Image of the desktop wireframe for all pages](/docs/wireframes/wireframe-mobile.png)

### **Hi-Fi Wireframe**

![Image of the desktop wireframe for all pages](/docs/wireframes/wireframe-hi-fi.png)
<br>

## Task Management and Project Progress

Throughout the development of this project we utilised Trello as our primary task management tool. This approach allowed us to effectively organise, prioritise, and track the progress of various features and tasks.

### Trello Board

You can view our project's Trello board [here](https://trello.com/b/lGrFjkAu).

The board is organised into the following lists:

-   Backlog
-   To Do
-   In Progress
-   Testing
-   Done

<br>

---

<details>
  <summary>View Trello Board Screenshots ⬇️</summary>
  <br>
  <img src="docs/trello-screenshots/trello-1.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-2.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-3.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-4.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-5.png" alt="Trello Board Screenshot 1" width="300">
  <img src="docs/trello-screenshots/trello-6.png" alt="Trello Board Screenshot 1" width="300">
</details>

---

<br>

### Key Milestones

1. Project Initialisation

    - Task here

2. MVP Features (Frontend)

    - Task here

3. MVP Features (Backend)

    - Task here

4. Stretch Features

    - Task here

5. Documentation and Deployment
    - Write API documentation
    - Prepare deployment scripts
    - Finalize README and user guide

<br>
<br>
