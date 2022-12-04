# online-boutique application

Cloud Native Application consists of 11 Microservices developed using Java, Python, C#, Go and Node.js


1. Frontend: Go Language, Exposes an HTTP server to serve the website. Does not require signup/login and generates session IDs for all users automatically.

2. Cart Service: C# Language, Stores the items in the user's shopping cart in Redis and retrieves it.

3. Product Catalog Service: Go Language, Provides the list of products from a JSON file and ability to search products and get individual products.

4. Currency Service: Node.js, Converts one money amount to another currency. Uses real values fetched from European Central Bank. It's the highest QPS service.

5. Payment Service: Node.js, Charges the given credit card info (mock) with the given amount and returns the transaction ID.

6. Shipping Service: Go Language, Gives shipping cost estimates based on the shopping cart. Ships items to the given address (mock)

7. Email Service: Python Language, Sends users an order confirmation email (mock).

8. Checkout Service: Go Language, Retrieves user cart, prepares order and orchestrates the payment, shipping and the email notification.

9. Recommendation Service: Python Language, Recommends other products based on what's given in the cart.

10. Ad Service: Java Language, Provides text ads based on given context words.

11. Load Generator: Python/Locust Language, Continuously sends requests imitating realistic user shopping flows to the frontend.
