Task Overview
Build a Shopify app that enables merchants to configure VIP customers and VIP products, and automatically applies discounts based on defined eligibility rules.

Admin Dashboard Configuration
The admin dashboard must provide two configuration sections:
1. VIP Customer Configuration <br>
	•	During app installation, create a customer-level metafield named vip_tag.<br>
	•	The merchant will manually assign a tag value (e.g., VIP) to a customer.<br>
	•	Any customer with this tag value should be treated as a VIP Customer.

  <img width="1199" height="564" alt="Screenshot 2026-01-30 at 5 45 55 PM" src="https://github.com/user-attachments/assets/c204cf40-e1b7-4137-a18a-11e72d5e7caf" />
  
2. VIP Product Configuration<br>
	•	During app installation, create a product-level metafield named vip_tag.<br>
	•	The merchant will manually assign a tag value (e.g., VIP) to a product.<br>
	•	Any product with this tag value should be treated as a VIP Product.

  <img width="1192" height="354" alt="Screenshot 2026-01-30 at 5 43 04 PM" src="https://github.com/user-attachments/assets/4e33d8a2-11be-4957-9503-325ae70a8633" />

Order Processing Logic<br>
	•	When a customer logs in and adds products to the cart (one VIP product and one non-VIP product):<br>
	•	The app must first verify whether the customer placing the order is a VIP Customer.<br>
	•	If the customer is a VIP, the app must then check whether the cart contains at least one VIP Product.<br>
	•	Only when both conditions are met:<br>
	•	The customer is a VIP customer, and<br>
	•	The cart contains at least one VIP product, the Shopify Discount Function should apply a 10% discount to each VIP product in the cart.

Important Rules<br>
	•	The 10% discount must not be applied if:<br>
	•	The customer is not a VIP customer, or<br>
	•	The cart does not contain any VIP products.<br>
	•	The discount should be applied only when both conditions are satisfied.

<img width="1430" height="700" alt="Screenshot 2026-01-30 at 5 42 45 PM" src="https://github.com/user-attachments/assets/69555cb2-17d4-473c-a037-65185a685207" />
