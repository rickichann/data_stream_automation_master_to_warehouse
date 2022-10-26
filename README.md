# data_stream_automation_master_to_warehouse
Data Stream, Master to WH (Data Stream, insert & update)


1. Fetch the last date in the updated_at / write_date column, and edit date in load_date_update_csv.csv using that data.
2. Database configuration
3. Create new table "cron_activity" for activity check


   <img width="295" alt="Screen Shot 2022-10-26 at 11 32 10" src="https://user-images.githubusercontent.com/53082147/197947894-3e37cf1b-d0bd-4614-93c1-ddf0ca7c113f.png">
   
   
   Notes : 
   
   - id (Auto increment, index)
   - table_name (Manual insert, fill with the name of the warehouse table ex: transactions_activity_warehouse )
   - status (Update, auto from cron)
   - interval(Manual insert, ex: 1 minutes, 2 minutes, etc)
   - last_processing_time (Update, auto from cron)
   - description (Manual insert, ex: insert_and_update)
   - updated_at (Update, auto from cron)
   
   <img width="687" alt="image" src="https://user-images.githubusercontent.com/53082147/197949164-5cf09d54-1356-4937-b900-26a7e658d8a5.png">

4. Convert ipynb to py, run jupyter nbconvert --to python data_stream_master_to_wh.ipynb
5. Save in cron tab, run once a minute. 
