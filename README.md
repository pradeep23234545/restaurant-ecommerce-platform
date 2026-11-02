# The Zaika Loft — Restaurant Website

A responsive, single-page restaurant website concept for **The Zaika Loft**. It presents a food menu, lets visitors add items to a shopping cart, calculates the order total, and demonstrates Cash on Delivery and UPI checkout selections.

> **Project type:** Front-end demonstration  
> **Built with:** HTML, CSS and vanilla JavaScript  
> **Backend:** Not included

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [How the Website Works](#how-the-website-works)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Run Locally](#run-locally)
- [Deployment](#deployment)
- [Important Notes and Limitations](#important-notes-and-limitations)
- [Customization](#customization)
- [Author](#author)

---

## Overview

**The Zaika Loft** is a restaurant website designed to showcase a variety of food and beverage options in an attractive menu layout. The page uses a dark gradient background, gold/orange accents, food imagery, and responsive CSS styling.

The menu is divided into six categories:

- **Breakfast**
- **Lunch**
- **Dinner**
- **Desserts**
- **Beverages**
- **Chef's Specials**

Visitors can add menu items to a cart, see quantities and prices, view the running total, choose a checkout option, and complete the front-end order demonstration.

## Features

### Restaurant menu

- Six food and beverage categories.
- Menu item names, descriptions and prices.
- Food images used as category backgrounds.
- Hover effects and visual styling for menu items.

### Shopping cart

- Add menu items using the **Order** button.
- Add the same item more than once to increase its quantity.
- View each selected item and its subtotal.
- Automatically calculate the cart total.

### Checkout selection

- Choose **Cash on Delivery (COD)** or **UPI / Online Payment**.
- Selecting UPI displays fields for a UPI ID and account-holder name.
- The UPI fields are checked before the demonstration order is accepted.
- A browser alert displays the order/checkout result.

### Responsive layout

- CSS media queries adjust the menu layout for smaller screens.
- Menu sections stack vertically on narrow screens.
- The cart summary moves into the normal page flow on mobile.

## How the Website Works

### 1. Open the website

Open the page in a web browser. The restaurant title and menu are displayed on the page.

### 2. Browse the menu

Explore the six categories and read the descriptions and displayed prices.

### 3. Add food items to the cart

Select **Order** beside a menu item.

- The selected item is added to the cart.
- Selecting the same item again increases its quantity.
- The cart displays the item quantity and its calculated subtotal.
- The total amount is recalculated whenever an item is added.

### 4. Select a checkout method

The cart provides two options:

| Method | Current behaviour |
|---|---|
| Cash on Delivery | Displays an order-placed confirmation alert when the cart contains items. |
| UPI / Online Payment | Displays UPI ID and account-holder name fields. Both fields must be filled before the demo checkout confirmation appears. |

### 5. Place the order

Select **Place Order**.

The page checks that the cart is not empty. For UPI, it also checks that both input fields contain text. It then displays a browser alert with the result.

**Note:** This is a front-end demonstration only. The alert is not proof of a real payment or a real restaurant order. See [Important Notes and Limitations](#important-notes-and-limitations).

---

## Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure and menu content |
| CSS3 | Layout, gradients, responsive styling, hover effects and background images |
| Vanilla JavaScript | Cart operations, total calculation, checkout selection and browser alerts |

The current project does not use a JavaScript framework, package manager, database, or external payment SDK.

## Project Structure

The repository is intentionally simple and does not require a build step.

~~~text
restaurant-ecommerce-platform/
│
├── index.html
│
├── Artisan Lemonade.jpeg
├── Molten Chocolate Volcano.jpg
├── Paneer Tikka Masala.jpeg
├── Poha with Jalebi.jpg
├── Rajma Chawal.jpeg
├── Seafood Paella Valenciana.jpg
│
└── README.md
~~~

**File details:**

- **index.html** — Contains the page markup, CSS styles and JavaScript functionality.
- **Image files** — Used as the background visuals for the menu categories.
- **README.md** — Project documentation and setup instructions.

Keep the image files in the same directory as **index.html**. The CSS refers to them using relative file paths.

## Run Locally

### Requirements

- A modern web browser such as Google Chrome, Microsoft Edge, or Firefox.
- The project files downloaded or cloned to your computer.
- A code editor such as Visual Studio Code is optional.

No Node.js, npm, Python, database, or dependency installation is required for the current version.

### Option 1: Download from GitHub

1. Open the repository: [restaurant-ecommerce-platform](https://github.com/pradeep23234545/restaurant-ecommerce-platform).
2. Click **Code → Download ZIP**.
3. Extract the ZIP file.
4. Open the extracted project folder.
5. Double-click **index.html** to launch the website in your default browser.

### Option 2: Clone using Git

Open a terminal and run:

~~~bash
git clone https://github.com/pradeep23234545/restaurant-ecommerce-platform.git
cd restaurant-ecommerce-platform
~~~

Then open **index.html** in your browser.

### Option 3: Run through Visual Studio Code

1. Open Visual Studio Code.
2. Select **File → Open Folder** and choose the cloned project folder.
3. Open the Extensions panel and install **Live Server** if it is not already installed.
4. Right-click **index.html**.
5. Select **Open with Live Server**.

The website will open in your browser. Live Server is optional; opening the HTML file directly also works.

## Deployment

Because this is a static HTML/CSS/JavaScript project, it can be hosted using GitHub Pages.

1. Open the repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the **main** branch and the **/(root)** folder.
5. Save the settings.
6. After GitHub Pages finishes publishing, use the website URL shown in the Pages settings.

Make sure **index.html** and all six image files remain in the repository root so the relative image paths continue to work.

## Important Notes and Limitations

This repository currently demonstrates the **front-end flow** of a restaurant ordering website. It is not yet a production-ready e-commerce or restaurant order-management system.

- **No backend:** The project does not send orders to a server.
- **No database:** Cart items are stored in a JavaScript object in the browser and are lost when the page is refreshed or closed.
- **No real payment processing:** The UPI option only checks that the two fields contain text and then displays a success-style alert. It does not connect to a UPI app, payment gateway, or bank. No money is transferred.
- **COD is a demonstration:** The COD option displays a confirmation alert; it does not notify restaurant staff or create a stored order.
- **No user accounts:** Login, registration and customer profiles are not implemented.
- **No reservation system:** The navigation includes a Reservations item, but a reservation form or booking workflow is not implemented.
- **Navigation placeholders:** Some navigation links refer to page sections that are not currently implemented with matching section targets.
- **Sample restaurant details:** The address, contact information, opening hours and menu prices in the HTML are demonstration content. Replace them with verified details before using the website publicly.

**Safety and privacy:** Do not enter real payment credentials or sensitive financial information into this demo. The UPI fields are not connected to a payment provider.

## Customization

### Change menu items and prices

Open **index.html** and find the relevant menu category. Update the item name, description, displayed price, and the values passed to the JavaScript **addToCart()** function together.

For example, the displayed item price and the numeric price used by the cart should match.

### Replace food images

Replace an image while keeping its existing filename, or update the corresponding CSS background URL and keep the new image in the same folder.

The current image mappings are:

| Menu category | Image file |
|---|---|
| Breakfast | Poha with Jalebi.jpg |
| Lunch | Rajma Chawal.jpeg |
| Dinner | Paneer Tikka Masala.jpeg |
| Desserts | Molten Chocolate Volcano.jpg |
| Beverages | Artisan Lemonade.jpeg |
| Chef's Specials | Seafood Paella Valenciana.jpg |

### Update restaurant information

Search in **index.html** for the contact section and replace the sample address, phone number, email address, and operating hours with the correct restaurant details.

### Extend the project

Possible next steps for turning this demonstration into a fuller restaurant platform include:

- Add a backend API and database to store orders.
- Add customer details, delivery address and order history.
- Integrate a trusted payment gateway with server-side payment verification.
- Add a working reservation form.
- Implement the missing navigation sections.
- Add cart removal, quantity controls and cart persistence.
- Add order validation, confirmation pages and restaurant-side order management.

These are future improvements and are not part of the current implementation.

---

## Author

**Pradeep Yedage**

- GitHub: [@pradeep23234545](https://github.com/pradeep23234545)
- Project repository: [The Zaika Loft — Restaurant Website](https://github.com/pradeep23234545/restaurant-ecommerce-platform)
- LinkedIn: [Pradeep Yedage](https://www.linkedin.com/in/pradeep-yedage-b474a0325/)

---

<p align="center">
  <sub>Built as a front-end restaurant website project. Explore, learn, and keep building.</sub>
</p>
