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

### Cart Management

#### Get Cart Total
**GET** `/cart/total?newItemPrice={price}&cartTotal={total}`
- Returns the updated cart total after adding a new item.

#### Apply Discount
**GET** `/cart/discount?cartTotal={total}&isMember={true/false}`
- Applies a 10% discount if the user is a member.

#### Get Tax Amount
**GET** `/cart/tax?cartTotal={total}`
- Applies a 5% tax on the cart total.

### Shipping & Delivery

#### Get Delivery Estimate
**GET** `/delivery/estimate?shippingMethod={standard/express}&distance={km}`
- Returns the estimated delivery time based on the shipping method and distance.

#### Get Shipping Cost
**GET** `/shipping/cost?weight={kg}&distance={km}`
- Calculates shipping cost using the formula: `weight * distance * 0.1`.

### Loyalty Program

#### Get Loyalty Points
**GET** `/loyalty/points?purchaseAmount={amount}`
- Returns loyalty points as `2 points per $1 spent`.

## Demo

### Live Preview
- **StackBlitz:** [Live Demo](https://stackblitz.com/edit/stackblitz-starters-9jvouk?file=index.js)
- **Vercel Deployment:** [Live Site](https://basice-commerceproject-akshay-arellis-projects.vercel.app/)

### Video Demo

<div>
    <a href="https://www.loom.com/share/1fa588995fd54f17b3d1644e308408dd">
      <p>Basic-E-commerce-Project-LiveDemo - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/1fa588995fd54f17b3d1644e308408dd">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/1fa588995fd54f17b3d1644e308408dd-0ba118e5ea0ab7a2-full-play.gif">
    </a>
  </div>
  
## Deployment

To deploy, follow these steps:

1. Deploy your backend to Vercel or another hosting provider.
2. Copy the deployed URL.
3. Configure the front end to use this back end by updating the API base URL in the front end settings.

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
   node index.js
   ```

## Tech Stack

- Node.js
- Express.js
- CORS

## License

This project is licensed under the MIT License.

