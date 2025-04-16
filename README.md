# Revenue-by-Device-and-Continent-with-Sessions
 ## Description
This SQL query calculates key business metrics segmented by continent, with a focus on revenue and user engagement. It combines data from multiple tables to deliver a high-level overview of:

* **Total revenue**, as well as revenue split by **device type** (mobile and desktop)
* **Number of accounts** and **verified accounts**
* **Session count**
* **Revenue share per continent** (as a percentage of total global revenue)

 ## Key Components
1. `revenue_usd` **CTE**
Calculates revenue metrics:

* `revenue`: total revenue per continent

* `revenue_mobile`: revenue from mobile devices

* `revenue_desktop`: revenue from desktop devices

  
2. `account_usd` **CTE**
Computes user engagement metrics:

* `account_cnt`: number of created accounts

* `verified_cnt`: number of verified accounts

* `session_cnt`: number of sessions

  
3. **Final SELECT**
Merges the results to present a unified table with:

* Revenue and device breakdown
* Percentage contribution to total revenue
* Account and session metrics per continent

 ## Data Sources  
  
`order`: contains purchase records  
  
`product`: contains item prices  
  
`session_params`: contains session and device data  
  
`account_session`: maps sessions to accounts  
  
`account`: stores account verification status
