# JSON

A collection of JSON mock/sample data files for development, testing, and prototyping.

## Contents

### `random`

A large JSON file containing sample data across six domains:

| Section | Description |
|---|---|
| `users` | User profiles with names, emails, addresses, phone numbers, and preferences |
| `products` | Product listings with names, prices, categories, stock info, and ratings |
| `orders` | Customer orders with items, payment details, shipping info, and status |
| `events` | Events with location, organizer, speakers, schedule, and sponsors |
| `weather` | City weather data with forecasts, temperatures, wind, and alerts |
| `financialTransactions` | Financial transactions with accounts, amounts, merchants, and payment methods |

## Usage

The data can be used directly in any project that needs realistic mock data:

```js
// Node.js
const fs = require('fs');
const raw = fs.readFileSync('random', 'utf8');
const data = JSON.parse(raw);

console.log(data.users);
console.log(data.products);
console.log(data.orders);
```

```python
# Python
import json

with open('random') as f:
    data = json.load(f)

print(data['users'])
print(data['products'])
```

## Data Structure

<details>
<summary><strong>users</strong></summary>

```json
{
  "id": 1,
  "username": "johndoe",
  "email": "john.doe@example.com",
  "firstName": "John",
  "lastName": "Doe",
  "age": 32,
  "active": true,
  "role": "admin",
  "dateJoined": "2023-01-15T08:30:00Z",
  "address": { "street": "...", "city": "...", "state": "...", "zipCode": "...", "country": "..." },
  "phoneNumbers": [{ "type": "home", "number": "..." }],
  "preferences": { "theme": "dark", "notifications": true, "language": "en-US" }
}
```
</details>

<details>
<summary><strong>products</strong></summary>

```json
{
  "id": 1,
  "name": "...",
  "description": "...",
  "price": 29.99,
  "currency": "USD",
  "category": "...",
  "tags": ["..."],
  "inStock": true,
  "stockQuantity": 150,
  "manufacturer": "...",
  "ratings": { "average": 4.5, "count": 120 },
  "dimensions": { "height": 10, "width": 5, "depth": 3, "unit": "cm" }
}
```
</details>

<details>
<summary><strong>orders</strong></summary>

```json
{
  "orderId": "ORD-001",
  "userId": 1,
  "orderDate": "2024-01-10T10:00:00Z",
  "status": "delivered",
  "items": [{ "productId": 1, "quantity": 2, "pricePerUnit": 29.99, "totalPrice": 59.98 }],
  "shippingAddress": { "street": "...", "city": "..." },
  "paymentMethod": "credit_card",
  "subtotal": 59.98,
  "tax": 5.99,
  "shippingCost": 4.99,
  "total": 70.96
}
```
</details>

<details>
<summary><strong>events</strong></summary>

```json
{
  "id": 1,
  "title": "...",
  "startDate": "2024-06-01T09:00:00Z",
  "endDate": "2024-06-03T18:00:00Z",
  "location": "...",
  "organizer": "...",
  "capacity": 500,
  "registered": 320,
  "ticketPrice": 199.99,
  "speakers": [{ "name": "...", "bio": "...", "topic": "..." }],
  "schedule": [{ "day": 1, "sessions": [{ "time": "09:00", "title": "...", "speaker": "..." }] }]
}
```
</details>

<details>
<summary><strong>weather</strong></summary>

```json
{
  "cityId": 1,
  "cityName": "...",
  "date": "2024-01-15",
  "forecasts": [{
    "temperature": 22,
    "feelsLike": 20,
    "humidity": 65,
    "windSpeed": 15,
    "windDirection": "NW",
    "precipitation": 0,
    "condition": "Sunny",
    "summary": "..."
  }],
  "alerts": [{ "type": "...", "severity": "low", "issuedAt": "...", "expiresAt": "..." }]
}
```
</details>

<details>
<summary><strong>financialTransactions</strong></summary>

```json
{
  "transactionId": "TXN-001",
  "accountId": "ACC-001",
  "userId": 1,
  "type": "debit",
  "category": "groceries",
  "description": "...",
  "amount": 45.67,
  "currency": "USD",
  "date": "2024-01-15T14:30:00Z",
  "status": "completed",
  "merchant": "...",
  "paymentMethod": "card"
}
```
</details>

## License

This repository is open for use in personal and commercial projects.
