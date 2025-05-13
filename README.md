# Amazon-sales-dashboard
 # 1. Project Objective
 
The main goal of this project was to provide clear and actionable insights to help retailers and digital marketers better understand and optimize their sales performance and shipping processes on Amazon. 

The dashboards were designed to monitor revenue trends, order fulfillment, and product category performance, enabling data-driven decisions.

# 2. Tools Used

Microsoft Excel 

# 3. Data Challenges & Cleaning Process

# ⚠️ One of the biggest challenges I faced 
was during the data cleaning phase, especially dealing with missing values across many features.

Instead of simply removing blanks, I explored the relationships between columns to identify patterns and hidden logic in the dataset.

That’s when I discovered something unexpected:

The column “Courier Status” had over 12,000 blank rows.

All of these rows had Quantity = 0.

They were fulfilled via “Easy Ship”.

And surprisingly, some still had a positive Amount — meaning the customer had been charged!

This raised critical questions:

Were these cancelled orders? Refunds? Service charges?

Can I safely remove them? Or would that delete meaningful transactions?

# 🔍 Solution
To handle this complexity, I created a new column to classify each case:

Need Review: Qty = 0, but Amount > 0 → may represent refunds, fees, or system errors. Requires manual check.

Safe to Delete: Qty = 0 and Amount = 0 → clearly incomplete or canceled orders. Can be deleted.

Keep: All valid orders with quantity and amount.

This segmentation helped me clean the data without losing potentially important business records.

Later, I discovered that 100% of the “Need Review” cases were fulfilled by “Merchant”, not Amazon — revealing a possible fulfillment issue or inconsistency in merchant-side operations.




# Additional data cleaning steps:

*  Removed unnecessary columns like "postal code" and "SKU" for clarity.

*  Deleted 8,150 duplicate orders to ensure accuracy in analysis.

 # 4. Key Insights from Dashboard:
# KPIs
*  Total Revenue: $78.6M ( only 1% from B2B) 

*  Total Orders: 113K (dropped by 17% in may)

*  Average Monthly Orders: 37.7K  (dropped by 12% in Jun)

*  Top Performing Categories: Saree (49.9%), Kurta (27.1%), Western Dresses (14.3%)

   # insights

*  April was the peak month in sales while dropped in Jun.

*  90% of orders were successfully shipped

*  Major shipping partners: Amazon (64%), Merchant (26%)

*  Top 5 States by Revenue: Maharashtra, Karnataka, Uttar Pradesh, Telangana, Tamil Nadu

*  Top 5 Cities: Bengaluru, Hyderabad, Mumbai, Delhi, Chennai.



#  5. Recommendations
*  Investigate root causes of declining orders in May and June.

*  Optimize fulfillment with Amazon as it shows higher shipping success rate.

*  Focus marketing efforts on high-performing regions and categories (e.g. Saree, Kurta).

*  Review and address orders labeled as “Need Review” to prevent revenue leakage.


here is the link of dataset in kaggle.com : 
https://www.kaggle.com/datasets/thedevastator/unlock-profits-with-e-commerce-sales-data





 

 

