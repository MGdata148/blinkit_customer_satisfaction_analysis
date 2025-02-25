# Blinkit Customer Satisfaction Analysis

### Background
In the fast-growing world of e-commerce, customer satisfaction and feedback play a crucial role in shaping the success of online shopping and delivery platforms. Satisfied customers are more likely to become repeat buyers, recommend the service to others, and contribute to positive brand reputation. Feedback, both positive and negative, provides valuable insights into customer preferences, service quality, and areas for improvement. By actively listening to customer reviews and addressing concerns, businesses can enhance user experience, build trust, and maintain a competitive edge in the dynamic online marketplace.

### Project aim
The objective of this project is to analyze customer feedback on shopping and delivery in an online grocery store to identify areas for improvement.

### About dataset
[Blinkit Sales Dataset](https://www.kaggle.com/datasets/akxiit/blinkit-sales-dataset) was obtained from [Kaggle](https://www.kaggle.com/) and containes sales transaction data from Blinkit, an online grocery delivery platform. It provides valuable insights into customer purchasing behavior, product demand, revenue trends, and sales performance over time. For the purpose of this analysis 4 out of 11 files were used:

1. `blinkit_customer_feedback` containing:
   - `feedback_id`
   - `order_id`
   - `customer_id`
   - `rating`
   - `feedback_text`
   - `feedback_category`
   - `sentiment`
   - `feedback_date`

2. `blinkit_delivery_performance` containing:
   - `order_id`
   - `delivery_partner_id`
   - `promised_time`
   - `actual_time`
   - `delivery_time_minutes`
   - `distance_km`
   - `delivery_status`
   - `reasons_if_delayed`

3. `blinkit_order_items` containing:
   - `order_id`
   - `product_id`
   - `quantity`
   - `unit_price`

4. `blinkit_products` containing:
   - `product_id`
   - `product_name`
   - `category`
   - `brand`
   - `price`
   - `mrp`
   - `margin_percentage`
   - `shelf_life_days`
   - `min_stock_level`
   - `max_stock_level`

Research questions
How have foodborne disease outbreaks evolved over time?
Which foods and locations pose the highest risk for foodborne disease contamination?
Which pathogens present the greatest threat to public health?
Data analysis and visualisation
Data was analyzed using PostgreSQL and visualised in Tableau.

Data cleaning and analysis
Results
Visualisation
Conclusions
Foodborne disease outbreaks occured more frequently and had higher rates of hospitalizations and fatalities from April to June, which can be related to warm temperatures favoring the growth of microorganisms.
Both number of reported foodborne disease outbreaks and total number of cases showed a tendency to decrease over the years, what may indicate raising awareness and improvement in food supply chain.
Meat, fish and seafood, and vegetables were food categories most frequently causing foodborne diseases, respectively. This probably results from their high consumption rates combined with short shelf life and susceptibility to the development of microorganisms.
The type of meat responsible for the most of registered foodborne diseases was poultry, which is a common source of dangerous bacteria, e.g. Salmonella, Campylobacter.
Restaurants were the most common location for foodborne disease outbreaks, however the average number of cases was much higher in public utility facilities, where many people eat the same meals. The most dangerous foodborne disease outbreaks took place at assisted livig facilities and hospitals probably due to comorbid conditions of patients. Private homes and farms also showed high rates of hospitalizations and fatalities, which may be due to lack of compliance with food storage standards.
Foodbore disease outbreaks were most commonly caused by viruses and bacteria with Norovirus, Salmonella, and Clostridium occuring the most frequently.
The deadliest cause of foodborne disease outbreakes was Listeria monocytogenes, which is known for its high mortality rate of up to 30%.
