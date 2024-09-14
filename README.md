# JavaScript Shopping Cart Project

This project is a simple shopping cart application built with JavaScript. It includes features such as increasing/decreasing product quantities, removing products, and calculating the total price of the cart. It also calculates VAT (tax) and shipping fees, and uses `localStorage` to store some constants.

## Project Summary

- Calculates total cart price based on product prices and quantities.
- Automatically includes VAT (tax) and shipping fees in the calculation.
- Uses `localStorage` and DOM manipulation to update the user interface dynamically.
- Users can add, remove, or update the quantity of products in the cart.
- All calculations are updated as soon as the page is loaded.

## Used Methods

### 1. **Event Listeners**
The project uses various event listeners to capture user interactions:

- `window.addEventListener("load", ...)`: Automatically executes certain actions (like price calculation) when the page is loaded.
- `navbarList.addEventListener("click", ...)`: Captures button clicks in the navigation bar to update the cart content.
- `productList.addEventListener("click", ...)`: Captures button clicks on products to increase, decrease, or remove items in the cart.

### 2. **DOM Manipulation**
Various changes are made directly to the DOM:

- **`document.querySelector()` and `document.querySelectorAll()`**: Used to select HTML elements, such as product prices and cart details.
- **`Element.innerText`**: Used to get or set the text content of an HTML element.
- **`Element.closest()`**: Finds the closest parent element of a specific item. This is useful for identifying which product's button was clicked.
- **`Element.remove()`**: Removes a product from the cart.

### 3. **LocalStorage**
The project uses `localStorage` to store constant values (like tax rate and shipping fee) that persist even after the page is refreshed.

- **`localStorage.setItem()`**: Saves data to `localStorage`.
- **`localStorage.getItem()`**: Retrieves data from `localStorage`.

### 4. **Conditional Statements**
Conditional logic is used to decide actions based on user interactions and product status.

- For example, when a user decreases the product quantity, and it goes below 1, a confirmation prompt is shown before removing the product from the cart.

### 5. **Array and NodeList Operations**
Loops and operations are performed on **NodeLists** and **Arrays** to process multiple DOM elements:

- **`forEach()`**: Loops through each item in a NodeList or Array to process it.
- **`reduce()`**: Used to calculate the total cart price by summing up individual product prices.

### 6. **Mathematical Calculations**
Mathematical operations are used to calculate the cart total, including taxes and shipping fees:

- **`parseFloat()`**: Converts string values (from the DOM) to floating-point numbers for calculation.
- **Tax and Shipping Calculations**: Adds VAT and shipping fees to the product subtotal.

### 7. **User Confirmation with `confirm()`**
Before removing a product from the cart, the user is prompted with a confirmation message using `confirm()`. If the user confirms, the product is removed.

### 8. **Functions**
To keep the code modular and reusable, common tasks are placed into functions:

- **`calculateProductPrice(btn)`**: Updates the product price when its quantity changes.
- **`calculateCartPrice()`**: Calculates the total cart price, including VAT and shipping fees, and updates the UI.

## Project Flow

1. **Page Load**: When the page is loaded, constants like the tax rate and shipping fee are retrieved from `localStorage`, and the total cart price is calculated.
2. **Changing Product Quantity**: When the user clicks `-` or `+`, the quantity is updated, and the product price is recalculated.
3. **Removing a Product**: When the user clicks the remove button, a confirmation prompt is shown. If confirmed, the product is removed from the cart.
4. **Updating Cart Information**: After each product modification, the total price, tax, and shipping fees are recalculated and updated on the screen.

## Setup

1. Download or clone the project files.
2. Open the `index.html` file in your browser.

## Project Link

You can access the project using this link: [Your Project Link](https://okan87.github.io/checkoutApp/)