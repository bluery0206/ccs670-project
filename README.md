# Read Me: Online Shopping / E-Commerce System

This UML Class Diagram represents an Online Shopping / E-Commerce System similar to Shopee or Lazada. It illustrates the classes, attributes, methods, and relationships involved in managing users, products, shopping carts, orders, inventory, payments, and deliveries.

## 1. Classes

The diagram consists of the following classes:

- User: Stores user account information, including username, password, and mobile number. Serves as the parent class for different user types.
- Customer: Represents customers who can add products to their cart, check out, track orders, and review products.
- Seller: Represents sellers who manage products and track orders.
- Courier: Represents couriers responsible for delivering orders.
- Product: Stores product information, including its name and price.
- Stock: Manages product inventory and available quantities. Provides methods to increase or decrease stock.
- Cart: Holds the items selected by the customer and provides methods to add or remove orders.
- Order: Represents an order containing a product and its quantity. Allows the quantity to be increased or decreased.
- Payment: Stores payment information, including the payment amount.
- Shipment: Tracks shipment information, payment details, and delivery status.

## 2. Attributes and Methods

Each class contains attributes and methods relevant to its responsibilities.

- Attributes represent the data stored by an object, such as a product's name, price, or stock quantity.
- Methods represent the actions an object can perform, such as adding an order, updating stock, or changing shipment status.

The symbols indicate visibility:

- `+` Public: accessible from outside the class.
- `-` Private: accessible only within the class.

The data types specify the kind of value an attribute stores or a method returns, such as `String`, `int`, `double`, or `void`.

## 3. Class Relationships

The diagram uses relationships to represent how the classes interact.

- Inheritance: Customer, Seller, and Courier inherit common account information from User.
- Association: Classes interact with or reference other classes, such as Customer and Cart, or Order and Product.
- Product and Stock: Stock records the available quantity of a product.
- Cart and Order: The cart manages the orders or items selected for purchase.
- Order and Payment: Payment represents the transaction associated with an order.
- Order and Shipment: Shipment represents the delivery process for an order.
- Courier and Shipment: The courier is responsible for delivering shipments.

## 4. System Process

The general process of the e-commerce system follows this sequence:

1. The customer browses available products.
2. The customer adds selected products to the cart.
3. The customer checks out and creates an order.
4. The customer completes the payment.
5. The seller prepares the order for fulfillment.
6. The courier handles the shipment and delivery.
7. The customer tracks the order and may review the product after receiving it.

## 5. Additional Classes

The `Stock` class is an additional class beyond the six class concepts specified in the requirements. It is included to represent inventory management, making the model more detailed.

Other classes may also be added when necessary, provided that they contribute meaningfully to the system's functionality.

## 6. Notes for Improvement

The diagram provides a conceptual representation of the system. A few details could be refined for better UML accuracy:

- Add an `Admin` class inheriting from `User`, since A  dmin is listed as an actor in the requirements.
- Consider changing `Cart.orders: Order[]` to a collection of products or introducing a `CartItem` class.
- Associate `Payment` directly with `Order` rather than storing it as an attribute of `Shipment`.
- Consider using `String` for `Shipment.status` instead of `int` for this simplified model.
- Replace placeholder methods such as `method(type): type` with meaningful operations.
- Review the connectors and multiplicities to ensure each relationship clearly represents the intended interaction.

These refinements are suggestions for improving the model, rather than additional requirements imposed by the original scenario.