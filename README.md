# LocalConnect

## Overview
LocalConnect is a local marketplace web application built with **ASP.NET Core MVC**. It connects local store owners with customers by allowing owners to create stores, upload products, and manage their listings, while customers can browse stores, search/filter stores, add products to cart, and complete checkout.

The uploaded code is primarily a full-stack web system. It does **not** include a trained AI model inside the current codebase. However, the project structure is suitable for future AI features such as recommendation systems, smart search, demand prediction, and product moderation.

## Current Project Type
- Full-stack web application
- Local marketplace platform
- Store and product management system
- Shopping cart and order workflow

## AI Positioning
This project should be presented as **AI-ready**, not as a finished AI system. Claiming that it already contains AI would be wrong. The correct AI-focused framing is:

> LocalConnect is a marketplace platform that can be extended with AI features such as personalized product recommendations, store ranking, search intelligence, and sales forecasting.

## Main Features
- User registration and login.
- Role-based user flow: customer and store owner.
- Store creation and management.
- Product creation, editing, deletion, and image upload.
- Customer store browsing.
- Store search and price-range filtering.
- Product browsing inside store pages.
- Shopping cart management.
- Checkout and order creation.
- Entity Framework Core migrations.
- SQL Server database integration.

## Database Entities
The project includes the following main entities:

### UsersProp
Stores user registration data including name, email, password, confirmation password, and role.

### Stores
Represents a local shop with name, description, image, location, price range, phone number, website/social link, owner user ID, and products.

### Product
Represents a store product with name, description, price, image, and store relationship.

### CartItem
Stores cart products linked to a user.

### Order
Represents a customer order with total amount, date, status, and order items.

### OrderItem
Stores product name, price, quantity, and order relationship at purchase time.

## Technology Stack
- ASP.NET Core MVC
- C#
- Entity Framework Core 8
- SQL Server
- Razor Views
- HTML / CSS / JavaScript
- Bootstrap-style frontend structure

## Project Structure
```text
LocalConnect1/
├── Controllers/
│   ├── CartController.cs
│   ├── HomeController.cs
│   ├── ProductsController.cs
│   ├── StoresController.cs
│   └── WelcomeController.cs
├── DataBase/
│   └── DBbridge.cs
├── Models/
│   ├── CartItem.cs
│   ├── Order.cs
│   ├── OrderItem.cs
│   ├── Product.cs
│   ├── Stores.cs
│   └── UsersProp.cs
├── Migrations/
├── Views/
├── wwwroot/
└── Program.cs
```

## Core Workflow
1. Store owner signs up and logs in.
2. Owner creates a store profile.
3. Owner adds products with images and prices.
4. Customer browses stores.
5. Customer filters/searches stores.
6. Customer views store products.
7. Customer adds products to cart.
8. Customer checks out.
9. System creates an order and order items.

## Suggested AI Extensions
These are realistic AI improvements that fit the current system:

### 1. Product Recommendation System
Recommend products based on:
- User cart history
- Similar stores
- Product category behavior
- Price preferences

Possible models:
- Collaborative filtering
- Content-based filtering
- Hybrid recommender

### 2. Smart Store Ranking
Rank stores based on:
- Customer behavior
- Order conversion
- Location relevance
- Price range similarity
- Popularity

### 3. Search Intelligence
Improve search using NLP:
- Typo-tolerant search
- Semantic search
- Product synonym matching
- Arabic/English mixed search support

### 4. Demand Forecasting
Predict demand for store products using historical orders.

Possible models:
- Random Forest Regression
- XGBoost
- Prophet
- LSTM for time-series sales

### 5. Product Image Moderation
Use computer vision to detect inappropriate or low-quality product images.

### 6. Fraud / Suspicious Activity Detection
Detect abnormal checkout or account behavior.

## AI Results / Model Performance
LocalConnect does not contain a trained AI model in the submitted codebase. It is an AI-ready marketplace system, not an already AI-powered model.

| Item | Value |
|---|---|
| Accuracy / F1 / Precision / Recall | Not applicable |
| Dataset size for AI training | Not included |
| Images/videos for AI training | Product/store images exist as app assets/uploads, but no AI dataset is prepared |
| Epochs | Not applicable |
| Train/test split | Not applicable |
| Benchmark / baseline | Not applicable |

The AI value here is future extension potential: recommendations, smart search, store ranking, demand forecasting, and image moderation. Claiming existing AI results would be false.

## Running the Project
Restore packages:

```bash
dotnet restore
```

Apply migrations:

```bash
dotnet ef database update
```

Run the app:

```bash
dotnet run
```

## Strengths
- Clean MVC separation.
- Database-backed marketplace workflow.
- Product and store image upload support.
- Owner/customer role concept.
- Real shopping cart and checkout logic.

## Limitations
- No real AI model is currently implemented.
- Password handling should be upgraded to ASP.NET Core Identity or secure hashing.
- Authorization should be hardened.
- More validation and error handling are needed for production.
- Payment integration is not included.

## Summary
LocalConnect is a solid marketplace web application. Its current value is full-stack development, database modeling, and business workflow implementation. For an AI-focused portfolio, it should be described as an **AI-ready marketplace platform** with clear future AI extensions, not as an already AI-powered project.
