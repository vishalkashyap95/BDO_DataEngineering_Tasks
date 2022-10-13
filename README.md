# BDO_DataEngineering_Tasks
## > Please check the Final_submission.ipynb file for the code and assumptions made.

<dl>
  <dt><h3>Task 1</h3></dt>
  <dd><h3>Task 1.1 - Compute the average time on flyer per user.</h3></dd>
  
  ```
  # In the below output we can see that user "4e0521677630b9df7d69717098024419179910e1fff66d24a1affbc084b0c91f" has 
  spent 71.27 secs on an average on 1st Oct 2018 on flyers.
  
  final_events_df.show(5,False)
  +----------------------------------------------------------------+----------+----------------------+
  |user_id                                                         |date      |avg_time_spent_in_secs|
  +----------------------------------------------------------------+----------+----------------------+
  |4e0521677630b9df7d69717098024419179910e1fff66d24a1affbc084b0c91f|01-10-2018|71.27                 |
  |74130f3f5de109961e12f22e8c802dc8fdafda2a045b60556cf2e604bfa98e62|01-10-2018|1560.86               |
  |7b8f402162b5d8012c075cade7c331dc7ceccafc93de5a03bc1c272ef55477e6|01-10-2018|267.00                |
  |a043a79b8262033eade50cd80b31b9c4883a3a77294634d2b91267e90c886c2a|01-10-2018|1525.50               |
  |c104b2e862e69bbd850a7ddfb49e6d6455be36f0bc74774f4057def99ef25715|01-10-2018|497.00                |
  +----------------------------------------------------------------+----------+----------------------+
  only showing top 5 rows
  ```
  
  <dd><h3>Task 1.2 - Next, generate an output that will back a Business Intelligence (Bl) report that will be shared with our merchant partners.</h3></dd>
  
  ```
  # As we would be sharinig the data with merchants. One of the metric can be...
  
  How much time user spent on which flyer by merchants?
  In the below output we can see that, for merchant "2066", user "4e0521677630b9df7d69717098024419179910e1fff66d24a1affbc084b0c91f" 
  has spent total 196 secs and avg 98 secs on flyer "2009693", on 1st oct 2018. 
  This can be use to understand what kind of flyers user spent time on and accordingly we can provide recommendations
  +-----------+--------+--------------------+----------+------------------------+----------------------+
  |merchant_id|flyer_id|             user_id|      date|total_time_spent_in_secs|avg_time_spent_in_secs|
  +-----------+--------+--------------------+----------+------------------------+----------------------+
  |       2432| 1998362|4e0521677630b9df7...|01-10-2018|                   38.00|                 38.00|
  |       2268| 2016316|4e0521677630b9df7...|01-10-2018|                   35.00|                 35.00|
  |       2362| 2009401|4e0521677630b9df7...|01-10-2018|                    3.00|                  3.00|
  |       2066| 2009693|4e0521677630b9df7...|01-10-2018|                  196.00|                 98.00|
  |       2609| 2016439|4e0521677630b9df7...|01-10-2018|                   38.00|                 38.00|
  +-----------+--------+--------------------+----------+------------------------+----------------------+
  only showing top 5 rows
  ```
  
  <dd><h3>Task 1.3 Explain how your algorithm scales for:<br>
  - 1 Million Events (~10 MB of data)<br>
  - 1 Trillion Events (~10 TB of data)</h3></dd>
  
  ```
  Explainiation - As I am using PySpark. Scalability depends on the size of cluster and the resources allocated to the jobs.
  Need to understand the size of the data that we might process and accordingly we can assign resources.
  ```
  
</dl>

## > Definetely, all Python code can be wrapped in classes and methods.
