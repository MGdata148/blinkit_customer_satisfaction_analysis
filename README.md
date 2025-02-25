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
   - `rating` - from 1 to 5
   - `feedback_text`
   - `feedback_category` - one of the following: 'App Experience', 'Customer Service', 'Delivery', 'Product Quality'
   - `sentiment` - 'Positive', 'Neutral' or 'Negative' based on feedback text
   - `feedback_date`

2. `blinkit_delivery_performance` containing:
   - `order_id`
   - `delivery_partner_id`
   - `promised_time` - estimated delivery time
   - `actual_time` - actual delivery time
   - `delivery_time_minutes` - the difference between promised time and actual time in minutes
   - `distance_km`
   - `delivery_status` - 'On Time', 'Slightly Delayed' or 'Significantly Delayed'
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
   - `mrp` - maximum retail price, the highest price at which a product can be sold to the end consumer
   - `margin_percentage` - a profit margin, profit stated as a percentage of revenue
   - `shelf_life_days` - the length of time a product can be stored without becoming unsuitable for sale
   - `min_stock_level` - the lower quantity limit of a product to avoid understocking
   - `max_stock_level` - the upper quantity limit of a product to avoid overstocking

### Research questions
1. What are the most common types of feedback from Blinkit customers?
2. What are the ratings and sentiment trends for each feedback category? How have they evolved over time?
3. Does delivery feedback depend on the difference between the promised and actual delivery time?
4. Which products are the worst-rated and could be replaced?

### Data analysis and visualisation
Data was analyzed using [MS Excel](https://www.microsoft.com/pl-pl/microsoft-365/excel) with Power Query and Power Pivot. Power Query was used to import data, remove duplicates and unnecessary columns, assess data quality, and modify data types. Power Pivot was used to build a model for creating combined pivot tables.

### Results
Results are available HERE.
1. Sheets: 'customer_feedback', 'delivery_performance', 'order_items', 'products' show cleaned tables corresponding to the original data.
2. 'feedback_by_category' displays feedback text (a categorical variable) divided by sentiment and category. This analysis revealed an issue with feedback classification, as the same text appears in multiple categories, which is not logical. Based on the available data, it is unclear whether the problem stems from the text itself or the classification process. A category-focused approach was chosen for learning purposes. (answer to question 1)
3. 'customer_exp_by_category' focuses on rating and feedback sentiment proportion changes by category offering interactive charts with timeline to examine trends in time. (answer to question 2)
4. 'customer_exp_by_delivery_time' investigates ratings and feedback sentiment in category 'Delivery' depending on the difference between promised and actual delivery time. (answer to question 3)
5. 'customer_exp_by_product' identifies products with the lowest ratings in 'Product Quality' category and provides an interactive chart to compare problematic products with similar ones from other brands. Both rating and price are included to help find a better-quality product at a similar price.  

### Conclusions
All categories have similar ratings and feedback sentiment proportions. In the case of 'App Experience' and 'Customer Service,' the examined parameters slightly improved over time, while 'Delivery' and 'Product Quality' ratings gradually declined. However, these changes do not appear significant enough to raise concern.
The given data does not provide any information for analyzing app experience and customer service, so the focus must be on delivery and product quality. The analysis revealed no clear relationship between delivery time and customer satisfaction, which could indicate other delivery-related issues, such as product damage during transit or order mistakes. However, a more likely explanation is poor data quality - inconsistent feedback text and classification.
The analysis successfully identified low-quality products and provided a tool for quickly comparing and deciding on product replacements.
