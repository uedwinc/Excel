Drinko - Soft Drink Producer

Operates in FMCG - Fast Moving Consumer Goods industry involved in the production and sales of non-durable goods such as toiletries, soft drinks, processed goods and other consumable goods. Volume is usually very high with relatively low margins and large product portfolios.
There are lots of firms competing for market share hence the need for financial transparency and insights.

Metrics - 
- Most profitable products
- Packages of these products that are most prefered by clients
- Optimal size clients prefer to buy
- What drives clients to pick one product over another

Drinko operates with mostly key clients

Goal - 
- Build a model that will allow the management see the volume sold, the revenue and margins obtained
- Provide a breakdown of client, client type, brand, size and pack.

Dataset - 
The data used was extracted from SAP's Business Objects application. The excel file contains specific descriptive and financial information.
* The descriptive fields include:
	- Material Number
	- Material description
	- Period (yearmonth)
	- Brand
	- Size
	- Pack
	- Client
	- Client Type
* The Financial Fields include:
	- Volume
	- Gross Sales
	- Discount
	- Net Sales
	- Cost of Goods Sold
	- Distribution
	- Warehousing


ANALYSIS/REPORT

1. Mapping - I first separated the period field into two different columns of month and year using the RIGHT and LEFT function

2. Structure - Created another sheet called Analysis where I outlined all the metrics that will be calculated.

3. Formating and Formulars - I customized the layout and appearance of the table and inserted the various formulars so that as soon as I reference my data source, the values auto-populate.

4. Pivot Table - I created a pivot table from the data source in a new sheet. Then I populated it with the columns showing years and months and the rows showing brands. The values in the cells include the sum of all the values from the financial fields of the data source.

5. GETPIVOTDATA - The GETPIVOTDATA is the excel function I used and customized to extract relevant and specific information from the pivot table into the analysis sheet.

6. Slicers - With the report ready, I inserted slicers to help customize or narrow down the information displayed on the table. Slicers inserted were for months, brand, size, pack, client and client type.
I then formatted the slicers to taste.



DASHBOARD

I went on to build a dashboard to visialize client preferences as well as sales data. Even though Drinko is a B2B enterprise, we will need to see what clients prefer in terms of brand, size. It will also need to see how much sales volume each of it's clients make.

I will build 3 charts - 
- A bar and line chart to track monthly net sales and gross profit development.
- An inverted columns chart showing volume by size of product
- Another inverted columns chart showing volume by client type

Then there will be 2 KPIs. One for the average dstribution cost and the other for average discount given to clients.

The process for creating our dashboard include:

1. We'll insert 4 new columns in our data. These are date, current year, Year-to-date (YTD) and Last twelve months (LTM). YTM is a sort protocol inserted to help visualize how well the company is performing since the beginning of the current year. LTM will help the company visualize data for the past year.

2. After populating the date field using excel date function, we created a new sheet named references where we referenced distinct date fields. This help us create the "Current Period" dropdown validation on the dashboard sheet.

3. From the Developers tab of excel, we added radio buttons to reflect YTD and LTM. These were then linked to the references sheet.

4. Inorder to have a dashboard that allows us to choose from 2 distinct reference periods, we need to add columns that will auto-update our data set anytime these reference periods are selected. 

- First we populated the newly created current year field on our data with fixed reference from the current period of the report sheet. By fixing the reference, only the particular current period selected will be reflected in our data, and the dashbaord accordingly.

- Next we populated the newly created LTM and YTD fields of our data. Using the IF-AND function, referencing the EOMONTH function of our current period, we obtained data to reflect the last twelve months and year to date of any selected period.

- Then we modified our pivot table to include client type and size

5. I created a new sheet named tables where I will calculate a few key values that will then be transformed into KPIs.

- I created month, year and selected dates field to reflect any given period of YTD and LTM months and populated them with functions to reflect any given reference period selected.

- Then I added net sales and gross profit development table where I calculated all the financial variables using excels GETPIVOTDATA

6. In the table's sheet, I created the volume by size table. This is to help us track the volume of the firm's sales based on the size of the packaging that was used.

7. We also created a volume by client type table.

***
Chart

1. We'll create a bar and line chart. It will track monthly net sales and gross profit margins. These will give us an idea on how the firm's business is growing or developing. The trend of revenues shows whether the business is expanding and at what pace. GP margins will give us an idea of profitability.

2. Using rows from the net sales and gross profit development table, we created a bar and line chart combo. The bars represent monthly net sales while the line represent GP%. This is perfectly connected to the YTD and LTM radio buttons so that it adjusts according to which ever period is selected in our current period drop-down.

3. Next we create a clustered bar chart (inverted columns chart) showing the volume of purchases by the size of the drinks containers. We use the volume by size table. Also, we only use the totals column.

4. Next, we add another inverted columns chart to show volume by client type. This will help us determine the best performing client and which clients are failing. This knowledge will help improve targeting and client retention.

5. Next we'll add some KPIs. These will be related to the average discount and the average distribution cost. Since the dashboard is centered around sales and orders, these 2 metrics makes sense to know how much percentage of net sales the firms spends for customer satisfaction and retention.



Report

With this report, you can track the monthly, quarterly and yearly development of the company.

With the brand slicer, we can determine
- Who are the top performers
- Are there brands that are losing us money
- Are there brands that aren't growing fast enough


This report would help us come up with new strategy on company or brand level and help improve our numbers in the months to come.


