# eCommerce Events History in Cosmetics Shop
## About
This file contains behavior data for 5 months (Oct 2019 – Feb 2020) from a medium cosmetics online store.

Each row in the file represents an event. All events are related to products and users. Each event is like many-to-many relation between products and users.

Data collected by Open CDP project. Feel free to use open source customer data platform.

Source: https://www.kaggle.com/datasets/mkechinov/ecommerce-events-history-in-cosmetics-shop
## How to read it

There are different types of events. See below.

## Semantics (or how to read it):

User user_id during session user_session added to shopping cart (property event_type is equal cart) product product_id of brand brand of category category_code (category_code) with price price at event_time

## File structure

| Property |	Description |
| --- | --- |
| **event_time** | Time when event happened at (in UTC). |
| **event_type** | Only one kind of event: purchase. |
| **product_id** | ID of a product |
| **category_id** |	Product's category ID |
| **category_code** |	Product's category taxonomy (code name) if it was possible to make it. Usually present for meaningful categories and skipped for different kinds of accessories. |
| **brand** |	Downcased string of brand name. Can be missed. |
| **price** |	Float price of a product. Present. |
| **user_id** |	Permanent user ID. |
| **user_session** |	Temporary user's session ID. Same for each user's session. Is changed every time user come back to online store from a long pause. |

## Event types
### Events can be:

| Property |	Description |
| --- | --- |
| **view** | a user viewed a product |
| **cart** | a user added a product to shopping cart |
| **remove_from_cart** | a user removed a product from shopping cart |
| **purchase** | a user purchased a product |

## Multiple purchases per session
A session can have multiple purchase events. It's ok, because it's a single order.

----
# Questions I'm trying to solve from provided information:
1. What are the most frequently purchased products/categories in the cosmetics online store?
2. What is the average price of a product in the cosmetics online store?
3. What are the most popular brands in the cosmetics online store?
4. How often do users add items to their shopping cart but not complete a purchase?
5. What is the conversion rate from cart to purchase?
6. How long do users typically spend in a single session on the cosmetics online store?
7. What is the distribution of user sessions across different times of day and days of the week?
8. How do product/category popularity and purchase patterns vary across different user demographics (e.g. age, gender, location)?
9. What is the average order value in the cosmetics online store?
10. What is the customer retention rate over time?
