# Mysql-Task

## create a database namme ecommerce
```SQL
CREATE DATABASE ecommerce;
```

### create a table products
```SQL
create table customers ( 
    id INT AUTO_INCREMENT, 
    name CHAR(50),
    email VARCHAR(100),
    address VARCHAR(200),
    PRIMARY KEY (id)
);
```

### INSERT a sample data to the table products

```SQL
INSERT INTO customers (name, email, address) VALUES
('Alice Smith', 'alice.smith@example.com', '123 Maple Street'),
('Bob Johnson', 'bob.johnson@example.com', '456 Oak Avenue'),
('Charlie Davis', 'charlie.davis@example.com', '789 Pine Road'),
('David Wilson', 'david.wilson@example.com', '101 Cedar Lane'),
('Eva Clark', 'eva.clark@example.com', '234 Elm Boulevard'),
('Frank Harris', 'frank.harris@example.com', '567 Birch Drive'),
('Grace Lewis', 'grace.lewis@example.com', '890 Spruce Street'),
('Henry Young', 'henry.young@example.com', '135 Walnut Circle'),
('Isabella Green', 'isabella.green@example.com', '246 Willow Avenue'),
('Jack Baker', 'jack.baker@example.com', '357 Redwood Road'),
('Katie Adams', 'katie.adams@example.com', '468 Cherry Lane'),
('Liam Nelson', 'liam.nelson@example.com', '579 Sycamore Drive'),
('Mia Turner', 'mia.turner@example.com', '680 Poplar Street'),
('Noah White', 'noah.white@example.com', '791 Maplewood Avenue'),
('Olivia Scott', 'olivia.scott@example.com', '802 Oakwood Drive'),
('Paul Walker', 'paul.walker@example.com', '913 Pinehurst Lane'),
('Quincy Moore', 'quincy.moore@example.com', '124 Cedar Court'),
('Rachel Brown', 'rachel.brown@example.com', '235 Birch Street'),
('Samuel Martin', 'samuel.martin@example.com', '346 Spruce Circle'),
('Tina Thompson', 'tina.thompson@example.com', '457 Walnut Boulevard'),
('Ulysses King', 'ulysses.king@example.com', '568 Willow Drive'),
('Victoria Hall', 'victoria.hall@example.com', '679 Redwood Avenue'),
('William Lee', 'william.lee@example.com', '780 Elm Circle'),
('Xavier Parker', 'xavier.parker@example.com', '891 Maple Street'),
('Yasmin Allen', 'yasmin.allen@example.com', '902 Oak Lane'),
('Zachary Evans', 'zachary.evans@example.com', '103 Cedar Avenue'),
('Amanda Brooks', 'amanda.brooks@example.com', '214 Birch Drive'),
('Brian Carter', 'brian.carter@example.com', '325 Spruce Boulevard'),
('Chloe Fisher', 'chloe.fisher@example.com', '436 Walnut Court'),
('Daniel Rivera', 'daniel.rivera@example.com', '547 Willow Road'),
('Emma Simmons', 'emma.simmons@example.com', '658 Redwood Street'),
('Finn Roberts', 'finn.roberts@example.com', '769 Elm Lane'),
('George Wright', 'george.wright@example.com', '870 Maplewood Drive'),
('Hannah Collins', 'hannah.collins@example.com', '981 Pine Circle'),
('Ian Russell', 'ian.russell@example.com', '192 Cedar Boulevard'),
('Julia Watson', 'julia.watson@example.com', '203 Birch Avenue'),
('Kevin Griffin', 'kevin.griffin@example.com', '314 Spruce Drive'),
('Linda Ortiz', 'linda.ortiz@example.com', '425 Walnut Street'),
('Mark Diaz', 'mark.diaz@example.com', '536 Willow Lane');
```


### creating a second table orders
```SQL
CREATE TABLE orders (
    id INT AUTO_INCREMENT,
    customer_id INT,
    order_date DATE,
    total_amount INT,
    PRIMARY KEY (id),
    FOREIGN KEY (customer_id) REFERENCES customers(id)
);
```

### INSERT a sample data to the orders table 
```SQL
INSERT INTO orders (customer_id, order_date, total_amount) VALUES
(5, '2024-08-05', 150),
(8, '2024-08-10', 300),
(12, '2024-08-12', 95),
(3, '2024-08-15', 220),
(10, '2024-08-20', 180),
(7, '2024-08-25', 320),
(14, '2024-08-28', 275),
(12, '2024-09-01', 621),
(1, '2024-09-02', 400),
(9, '2024-09-05', 260),
(6, '2024-09-10', 150),
(4, '2024-09-15', 520),
(11, '2024-09-18', 125),
(2, '2024-09-22', 340),
(15, '2024-09-25', 90),
(18, '2024-10-01', 500),
(28, '2024-10-02', 258),
(38, '2024-10-03', 753),
(8, '2024-10-04', 951),
(13, '2024-10-05', 200),
(11, '2024-10-06', 180),
(15, '2024-10-07', 265),
(19, '2024-10-08', 245),
(17, '2024-10-09', 235),
(18, '2024-10-10', 300),
(10, '2024-10-11', 180),
(20, '2024-10-12', 175),
(3, '2024-10-13', 705),
(23, '2024-10-14', 963),
(15, '2024-10-15', 200),
(29, '2024-10-16', 548),
(15, '2024-10-17', 365),
(22, '2024-10-18', 150),
(1, '2024-10-19', 255),
(16, '2024-10-20', 420),
(25, '2024-10-21', 555),
(17, '2024-10-22', 210),
(12, '2024-10-23', 544),
(2, '2024-10-24', 180),
(20, '2024-10-25', 200),
(18, '2024-10-26', 900),
(31, '2024-10-27', 260),
(12, '2024-10-28', 700),
(22, '2024-10-29', 110),
(19, '2024-10-30', 350),
(33, '2024-11-01', 500),
(24, '2024-11-02', 215),
(35, '2024-11-03', 350),
(30, '2024-11-03', 586),
(26, '2024-11-04', 125),
(37, '2024-11-04', 280),
(28, '2024-11-04', 75),
(39, '2024-11-05', 450),
(30, '2024-11-05', 600);
```

### creating a third table products
```SQL
CREATE TABLE products (
    id INT AUTO_INCREMENT,
    name CHAR(50),
    price DECIMAL(10, 2),
    description VARCHAR(300),
    PRIMARY KEY (id)
);
```

### INSERT a sample data to the products table 
```SQL
INSERT INTO products (name, price, description) VALUES
('Product A', 49.99, 'High-quality product A with excellent features.'),
('Product B', 120.00, 'Reliable and durable product B for everyday use.'),
('Product C', 75.50, 'Affordable product C with great value.'),
('Product D', 89.99, 'Versatile product D for multiple purposes.'),
('Product E', 55.45, 'Product E with advanced functionality.'),
('Product F', 150.75, 'Premium product F for professionals.'),
('Product G', 42.15, 'Product G designed for convenience.'),
('Product H', 199.99, 'Exclusive product H with unique benefits.'),
('Product I', 65.90, 'Compact and efficient product I.'),
('Product J', 36.80, 'Budget-friendly product J with essential features.'),
('Product K', 95.25, 'Product K optimized for performance.'),
('Product L', 78.45, 'Product L with innovative technology.'),
('Product M', 130.60, 'Product M for specialized applications.'),
('Product N', 37.00, 'Eco-friendly product N.'),
('Product O', 175.30, 'Product O with high-end specifications.'),
('Product P', 38.20, 'Cost-effective product P.'),
('Product Q', 45.00, 'Product Q for home and office use.'),
('Product R', 56.30, 'Product R with reliable performance.'),
('Product S', 200.00, 'Top-of-the-line product S with premium features.'),
('Product T', 110.50, 'Well-rounded product T with balanced specs.');
```

# Queries to Write:

### Retrieve all customers who have placed an order in the last 30 days.
```SQL
SELECT 
    customers.id, 
    customers.name, 
    customers.email, 
    customers.address, 
    orders.order_date, 
    orders.total_amount
FROM 
    customers
INNER JOIN 
    orders ON customers.id = orders.customer_id
WHERE 
    orders.order_date BETWEEN '2024-10-06' AND '2024-11-05';
```

### Get the total amount of all orders placed by each customer.
```SQL
SELECT 
    customers.id,
    customers.name,
    sum(orders.total_amount) as total_spent
FROM
    customers
INNER JOIN
    orders ON customers.ID = orders.customer_id
GROUP BY
    customers.id,customers.NAME;
```

### Update the price of Product C to 45.00.
```SQL
UPDATE products SET price = 45.00 WHERE name = 'Product C';
```

### Add a new column discount to the products table.
```SQL
ALTER TABLE products ADD discount int;
```

### Retrieve the top 3 products with the highest price.
```SQL
SELECT * FROM products ORDER BY price DESC LIMIT 3;
```
### Get the names of customers who have ordered Product A.

after Normalization
```SQL
SELECT 
    customers.name
FROM 
    customers
JOIN 
    orders ON customers.id = orders.customer_id
JOIN 
    order_items ON orders.id = order_items.order_id
JOIN 
    products ON order_items.product_id = products.id
WHERE 
    products.name = 'Product A';
```

### Join the orders and customers tables to retrieve the customers name and order date for each order. 
```SQL
SELECT 
    customers.name,
    orders.order_date
FROM
    customers
INNER JOIN
    orders ON customers.id = orders.customer_id;
```
### Retrieve the orders with a total amount greater than 150.00.
```SQL
SELECT * 
FROM
    orders
WHERE
    total_amount > 150.00;
```
### Normalize the database by creating a separate table for order items and updating the orders table to reference the order_items table.

```SQL
CREATE TABLE order_items (
    id INT AUTO_INCREMENT PRIMARY KEY,
    order_id INT,
    product_id INT,
    quantity INT,
    price DECIMAL(10, 2),
    FOREIGN KEY (order_id) REFERENCES orders(id),
    FOREIGN KEY (product_id) REFERENCES products(id)
);
```
INSERTING data in te order_items table
```SQL
INSERT INTO order_items (order_id, product_id, quantity, price)
VALUES
(1, (SELECT id FROM products WHERE name = 'Product A'), 2, 49.99),
(1, (SELECT id FROM products WHERE name = 'Product B'), 1, 120.00),
(2, (SELECT id FROM products WHERE name = 'Product D'), 2, 89.99),
(2, (SELECT id FROM products WHERE name = 'Product F'), 1, 150.75),
(2, (SELECT id FROM products WHERE name = 'Product S'), 2, 200.00),
(3, (SELECT id FROM products WHERE name = 'Product T'), 1, 110.50),
(3, (SELECT id FROM products WHERE name = 'Product A'), 2, 49.99),
(3, (SELECT id FROM products WHERE name = 'Product M'), 1, 130.60),
;
```
updating the orders table on two option one we can drop the total_amount column in orders table or update the total_amount of the order 

option one 
```SQL
ALTER TABLE orders
DROP COLUMN total_amount;
```
option two 
```SQL
UPDATE orders SET total_amount = 60000 WHERE customer_id = '5';
```

```SQL
SELECT 
    orders.id AS order_id,
    customers.name AS customer_name,
    products.name AS product_name,
    order_items.quantity,
    order_items.price,
    (order_items.quantity * order_items.price) AS total_price
FROM 
    orders
JOIN 
    customers ON orders.customer_id = customers.id
JOIN 
    order_items ON orders.id = order_items.order_id
JOIN 
    products ON order_items.product_id = products.id
WHERE 
    orders.id = 1;
```
### Retrieve the average total of all orders.

after Normalization
```SQL
SELECT 
    AVG(order_items.quantity * order_items.price) AS average_order_total
FROM 
    order_items;
```
before Normalization 
```SQL
SELECT 
    AVG(total_amount) AS average_total
FROM 
    orders;
```
