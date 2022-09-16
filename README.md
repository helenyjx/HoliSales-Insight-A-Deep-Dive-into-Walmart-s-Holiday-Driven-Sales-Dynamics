[![Python application test with Github Actions](https://github.com/nogibjj/Project-1-Jiaxin-Ying-/actions/workflows/main.yml/badge.svg)](https://github.com/nogibjj/Project-1-Jiaxin-Ying-/actions/workflows/main.yml)

# Project-1-Jiaxin-Ying-
This is a repository about my project 1.

## Demo Video Link:
https://teams.microsoft.com/l/message/19:9e5856d19b4f42eaa8d38f159d93a640@thread.tacv2/1663199207426?tenantId=cb72c54e-4a31-4d9e-b14a-1ea36dfac94c&groupId=428262e3-7a97-45de-8ed6-eb751b9cb87c&parentMessageId=1663199207426&teamName=IDS.706.01.F22&channelName=Week%203%20Demo_Project%201&createdTime=1663199207426&allowXTenantAccess=false

## Key Objectives of Project:
I use Databricks to upload my dataset and connect it with VS Code by using a microservice(FastAPI) and command-line tool(click). The goal of my project is showing Walmart weekly sales of holidays and non-holidays. It will help managers to check weekly sales based on holiday element. 

## Dataset Source:
Walmart, one of the leading retail stores in the US, it is also my favorite supermarket since I was a kid. Therefore, for my project 1, I chose a dataset from Kaggle called Walmart (https://www.kaggle.com/datasets/yasserh/walmart-dataset), which is about 45 Walmart stores’ historical data that covers sales from 2010-02-05 to 2012-11-01. There are seven main variables:Date, Weekly_Sales, Fuel_Price, CPI, Temperature, Holiday_Flag and Unemployment rate. My project will focus on exploring the effect of holidays on weekly sales for Walmart. After analyzing this data, managers could update or fix sales strategies according to the weekly sales in each week which has holidays or non-holidays.

<img width="1064" alt="Screen Shot 2022-09-16 at 12 20 56 PM" src="https://user-images.githubusercontent.com/112274822/190724905-1fcf07c8-8764-4272-89f0-acd94733c324.png">

## Connect Codespace and Databricks
We need to create four secrets for codespace depository by copying link from databricks (DATABRICKS_HOST, DATABRICKS_HTTP_PATH, DATABRICKS_SERVER_HOSTNAME and DATABRICKS_TOKEN)

<img width="926" alt="Screen Shot 2022-09-16 at 12 19 26 PM" src="https://user-images.githubusercontent.com/112274822/190724999-f68b0cc7-2f5f-4455-9150-ffa6f9b9a546.png">

After that, we need to check whether databricks and codespace has been connected by typing following code in terminal.

Then test the following code in Codespaces to check the connection.

## Function of hi_query_sql_db
My sql query will return the weekly sales of Walmart according to weeks which have holidays or non-holidays. Once we call the querydb function, it shows the weekly sales that includes holidays when type 1, anor not include holidays when type 0. Also, it will sort the weekly sales by descending order, so that mangers can find the week which have relatively high sales quickly.

<img width="804" alt="Screen Shot 2022-09-16 at 3 48 02 PM" src="https://user-images.githubusercontent.com/112274822/190725080-6732c08d-5bf1-4132-b98d-97a15ca578c3.png">

## Fastapi App for Web 
Now, if we type the following code in terminal, and click "open in browser":

<img width="651" alt="Screen Shot 2022-09-16 at 3 54 48 PM" src="https://user-images.githubusercontent.com/112274822/190725166-a56973c7-6008-4eae-ab5a-c75e05f677a6.png">

After that, a new web page will come up and shows a sentence below: 

<img width="469" alt="Screen Shot 2022-09-16 at 4 02 01 PM" src="https://user-images.githubusercontent.com/112274822/190724682-7a590678-b510-47dc-abed-c588a87c77bf.png">
<img width="1009" alt="Screen Shot 2022-09-16 at 3 57 24 PM" src="https://user-images.githubusercontent.com/112274822/190725170-e169bca1-745a-4244-83c1-027c2fbcc9ff.png">

Then, if we type "/query" at the end of the url address, it will return the weekly sales for weeks with holidays automatically:

<img width="1499" alt="Screen Shot 2022-09-16 at 3 53 30 PM" src="https://user-images.githubusercontent.com/112274822/190725216-f6b52b9f-5766-4e53-9da6-7cce3999b8e2.png">
