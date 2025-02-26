# Basic E-commerce Project

## Overview
This project is a backend implementation for an e-commerce cart system, providing APIs to manage cart operations, discounts, taxes, shipping, and loyalty points.

## Features
- Add products to the cart
- Apply membership discounts
- Calculate tax and shipping costs
- Estimate delivery time
- Calculate loyalty points earned from purchases

## API Endpoints

### 1. Calculate Cart Total
**GET** `/cart-total?newItemPrice={price}&cartTotal={total}`  
Returns the updated cart total after adding a new item.

### 2. Apply Membership Discount
**GET** `/membership-discount?cartTotal={total}&isMember={true/false}`  
Applies a 10% discount if the user is a member.

### 3. Calculate Tax
**GET** `/calculate-tax?cartTotal={total}`  
Applies a 5% tax on the cart total.

### 4. Estimate Delivery Time
**GET** `/estimate-delivery?shippingMethod={standard/express}&distance={km}`  
Returns the estimated delivery time based on the shipping method and distance.

### 5. Calculate Shipping Cost
**GET** `/shipping-cost?weight={kg}&distance={km}`  
Calculates shipping cost using the formula: `weight * distance * 0.1`.

### 6. Calculate Loyalty Points
**GET** `/loyalty-points?purchaseAmount={amount}`  
Returns loyalty points as `2 points per $1 spent`.

## Deployment
To deploy, follow these steps:
1. Deploy your StackBlitz project to Vercel.
2. Copy the deployed Vercel URL.
3. Configure the frontend to use this backend by pasting the URL in the frontend settings.

## Installation & Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/AkshAI-2030/Basic-E-commerce-Project.git
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   npm start
   ```

## Tech Stack
- Node.js
- Express.js
- CORS

## License
This project is licensed under the MIT License.

