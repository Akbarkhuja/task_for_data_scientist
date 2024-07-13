# task_for_data_scientist

# A test from UZUM Market! 🛒
### Task
Returns of goods pose a serious problem for online marketplaces. Statistics show that approximately 15% to 40% of all online purchases are returned, which not only creates financial difficulties for businesses, but also entails serious environmental problems due to the huge number of goods ending up in landfills. To reduce the number of refunds, it is critically important for sellers to be able to identify the reasons for the refund as early as possible. However, this information often becomes available only after a significant number of product returns. Understanding the reasons for the return of goods and predicting them can greatly help reduce this problem.
### Goal
To develop a machine learning model that will solve the problem of multiclass classification and predict the probability distribution of the reasons for the return of goods based on a variety of factors, including textual customer reviews.
### Input data format
There are 5 files on the link to google drive: https://drive.google.com/drive/folders/1c9ABGWtH5xgJFIPSANEJusIxTMuwIuFD?usp=sharing
#### return_reasons.parquet is a dictionary file with unique reasons for returning an item. Each reason has an id and description. There are 5 unique ones in total - [DEFECTED, WRONG_ITEM, BAD_QUALITY, PHOTO_MISMATCH, WRONG_SIZE]
#### reviews.parquet - a file with reviews of purchases on the marketplace.
 Each review has:
• order_item_id - the unique identifier of the order

• product_id - the unique identifier of the product

• customer_id - the unique identifier of the buyer

• review_text - the customer's text review of the product

• shop_id - the unique identifier of the store

• rating - rating on a scale from 1 to 5

• date_created - timestamp for creating

### a returns.parquet review - a file with product returns on the marketplace.
• id - the unique identifier of the return of the product

• product_id - the unique identifier of the product

• cause - one of the 5 reasons for a refund

• comment - no refund required

• date_created - timestamp for making a refund

• order_item_id - the unique identifier of the product order

• customer_id - the unique identifier of the customer

• purchase_price - the price of the order of the goods

#### products.parquet - a file with a description of the goods in Russian and Uzbek languages
• product_id - the unique identifier of the product

• category_id ****- product category id

• category_title ****- name of the product category

• product_description ****- product description in Russian and Uzbek

#### test.parquet is a file containing the same as returns.parquet, except for the reason for the return. That's what you have to predict.
❗️❗️❗️ All files are presented in parquet format, in which we expect to receive the output file from you. You can read more and get acquainted with parquet here
### Metrics
To evaluate the classification model model, we chose Macro Average Precision:

• Average Precision is a metric that takes into account the accuracy for each class individually and then averages them. It is suitable for cases where both accuracy and completeness are important for each class.

• Macro Average Precision - calculates the accuracy for each class separately, and then averages them, treating all classes equally regardless of their frequency or imbalance in the dataset.
Requirements for the solution

### ❗️❗️❗️ The solution must be downloaded via the link in the form of a zip archive, which contains at the root:

• the **solution** folder with all *.py and *.ipynb files

• file **result.parquet**

Good luck!
