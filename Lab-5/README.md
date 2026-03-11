# ARTI 308 – Lab 5: Feature Engineering (Classification)
### Task 1
Create one new engineered feature that you believe will help predict `Order_Status`.  
Write one paragraph justifying your choice.

A dist_price_ratio feature was added.
It will determine how efficient it would be to fulfill an order. If the distance is high with a low price, there would be a potentially low revenue earned at a high time and cost investment, which makes the order less attractive for delivery drivers to accept. Should the opposite occur, in which the price is very high with a short distance, the restaurant may not have enough time to prepare the large order before the driver arrives, which can cause long wait times or order cancellations. By creating this feature, the model would understand the delivery effort vs reward concept, which is a stronger predictor of potential cancellations or delays over viewing price or distance alone.

### Task 2
Try a different rule for `is_peak_hour` and discuss whether performance changes.

| rule | accuracy | top feature 1 | top feature 2 | top feature 3 |
|-------|----------|---------------|---------------|---------------|
| original rule  | 0.8519 | price_per_item (0.066192) | Driver_Lon (0.065526) | Customer_Lat (0.065284) |
| new rule | 0.8519 | price_per_item (0.065589) | Driver_Lon (0.064978) | Driver_Lat (0.064933) |


The top features have changed while the accuracy has remained unaffected

### Task 3
Change `top_k` in `Item_Name_reduced` (for example 10, 30, 50) and compare:
- accuracy
- top feature importances

| top_k | accuracy | top feature 1 | top feature 2 | top feature 3 |
|-------|----------|---------------|---------------|---------------|
|20  | 0.8519 | price_per_item (0.065589) | Driver_Lon (0.064978) | Driver_Lat (0.064933) |
| 5 | 0.8519 | price_per_item (0.067059) | Driver_Lon (0.066686) | Driver_Lat (0.066800) |
| 30 | 0.8519 | price_per_item (0.065589) | Driver_Lon (0.064978) | Driver_Lat (0.064933) |
| 50 | 0.8519 | price_per_item (0.065589) | Driver_Lon (0.064978) | Driver_Lat (0.064933) |


### Task 4
Run the optional feature selection section and explain whether it was beneficial in your case.

There was no difference in the results
