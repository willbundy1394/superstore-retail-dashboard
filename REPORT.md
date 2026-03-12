### Business Analytics Project Report Template
Will Bundy
### Project Title: Business Analytics Project Report For Superstore Retail
### Part 1: Business Problem and Objectives
Business Domain: Sales & Operations (Retail Analytics)
### Problem Statement: 
The superstore is making decent sales, but profits are all over the place, some stuff makes money, a lot of stuff loses money. Management doesn’t really know which products, regions, or customers are dragging profits down or which ones are worth pushing harder. Right now, they’re kind of lost with discounts and inventory decisions, so the main goal of this project is to figure out what’s killing or boosting profit and give them clear recommendations.
### Business Questions:
1.	Which categories and sub categories are profitable vs. total money losers?
2.	Which regions/states/cities are performing the best and worst?
3.	How much discounting is too much, when do discounts start eating all the profit?
4.	Which customer segment (Consumer, Corporate, Home Office) brings in the most profit?
5.	Are there any obvious seasonal patterns we can use for planning promotions and stock?
### Why This Matters: 
Pretty much every retail company lives or dies by its margins. If you keep pushing heavy discounts on stuff that’s already low margin, or you keep stocking things nobody wants in certain states, you can have huge sales numbers but still end up barely breaking even or even worse. Figuring this out with data is way better than guessing.
### Part 2: Data Source and Preparation
### Data Source(s): 
The data comes from a file called “Store Dataset for Project.xlsx” that was provided with the assignment. It contains real looking transactional records of a U.S. based superstore chain covering four years of actual orders. Even though it’s a sample file, the numbers, product mix, regional differences, and loss making items all are like what you’d see in a real retail company, so it’s reliable for analysis.
### Dataset Summary:
•	9,994 rows each row is one line item from a customer order 
•	21 columns
•	Time range: January 2014 through December 2017
•	Key fields: Order Date, Ship Date, Ship Mode, Customer Segment (Consumer/Corporate/Home Office), Region, State, City, Category (Furniture, Office Supplies, Technology), Sub-Category, Product Name, Sales, Quantity, Discount, Profit, etc.
### Data Cleaning & Preparation: 
•	Before I could build anything solid, I had to fix a couple of small things in Tableau.
•	Created a relationship between Sales Data/Zip Codes/Regional Manager
•	Converted the necessary columns to strings
•	Order Date and Ship Date were being read as text instead of actual dates so I changed them to proper date format so I could group by month, year, etc.
•	I created Calculated Fields such as Total Sales, Total Profit, Total Costs, Current Year Sales, Current Year Profit, Current Year Quantity Sold, Previous Year Sales, Previous Year Profit, Previous Year Quantity Sold, Adjusted Profit, Adjusted Sales Price Per Item, Adjusted Total Sales, Change of Profit, Profit Margin Change %, Profit Change %, Quantity Sold Change % and Sales Change %
•	I created Parameters such as Category Parameter, Discount Rate %, Select Current Year and Region by Region Manager
### Part 3: Descriptive, Diagnostic, Predictive & Prescriptive Analytics
### Chart 1: KPI Card - Total Yearly Sales
 
### Insights: 
The dual line chart shows that 2023 Current Year (CY) sales (blue line) finished the year at $732K, a solid 19.9% increase over Previous Year (PY) sales (grey line). 
### Why It Matters: 
The 19.9% sales jump in 2023 looks great, but almost all of it came from bigger holiday spikes instead of steady growth, the rest of the year was just as choppy as always. This means we still have zero reliable base business, and everything still depends on Q4.
### Business Interpretation: 
While CY sales were volatile month to month with big spikes in the middle of the year and a huge peak toward the end. Overall, the trend ended strongly upward compared to the much flatter and gradually declining PY performance

### Chart 2: KPI Card - Total Yearly Profit
 
### Insights: 
The dual line chart shows that 2023 Current Year profit ended at $94K, a solid 14.9% jump over Previous Year. 
### Why It Matters: 
Profit grew 14.9% to $94K, but the 2023 monthly profit line is a rollercoaster compared to last year’s slow decline, meaning the extra money came from a few big months, while a lot of months were worse.
### Business Interpretation: 
The blue CY line is super erratic with huge peaks and deep drops every couple month, while the gray PY line just gently drifts downward the whole year, so we made more money overall, but monthly profits were way less stable than last year.

### Chart 3: KPI Card - Total Yearly Quantity Sold 
 
Insights: The dual line chart shows total quantity sold in 2023 came in at 12K units, a nice 25.6% increase over Previous Year. 
Why it Matters: We moved 25.6% more units in 2023, but volume was uneven with huge spikes and deep drops vs. last year’s flat line. This means higher fulfillment costs, bigger inventory swings, and zero predictable base load, everything still comes down to a couple peak months.
Business Interpretation: The blue CY line shows way more dramatic ups and downs throughout the year (big spikes mid-year and late year) while the grey PY line stays flat and slightly declining, so we moved a lot more product this year, but volume was super inconsistent month to month. We should focus on trying to figure out how we can sell units year-round or else one bad month could really put us in a hole. 



### Chart 4: Pareto Chart
 
Insights: This Pareto chart proves the 80/20 rule is basically alive and well. Just the top four subcategories (Phones, Chairs, Storage, and Tables) make up over 80% of total sales, with Phones and Chairs alone at almost $600K combined.
Why This Matters: Revenue growth will come almost exclusively from these four any resources spent on the rest are largely wasted.
Business Interpretation: Everything after Tables drops off hard, so if we want to boost revenue fast, we should probably just pay more attention to those big four and not sweat the tiny stuff like labels and fasteners.





### Chart 5: Dual Chart vs. Total Profit
 
Insights: This dual axis chart shows monthly sales (blue) and profit (green) from 2020 through early 2023, and honestly sales are a rollercoaster with huge spikes and crashes every year while profit stays way more relaxed and basically flat the whole time.
Why This Matters: Sales swing quite a bit, profit barely moves, even $120K months only yield around $20K profit. Most extra volume is low to no margin, more revenue without pricing fixes just adds cost, not profit.
Business Interpretation: Even when sales jump to $120K in a month, profit barely moves above $20K, so it looks like higher revenue isn’t really translating into much extra profit.




### Chart 6: Order Segmentation Chart
 
Insights: This scatter plot segments every order by price per item and total profit, and it’s obvious we have three clear clusters Circle/Square/Addition Symbol. A large red/green cluster on the left with tons of low-price orders that make very minimal profits/losses, a green cloud in the middle making decent profit on mid-price stuff, and then a thin trail of high price orders on the right that mostly break even or barely win.
Why This Matters: The scatter plot shows that most orders are low ticket items that collectively deliver almost no profit (or even lose money), while the truly profitable middle cluster is relatively small and the high price orders, we probably spend the most time chasing barely make a difference.
Business Interpretation:  Basically, selling a bunch of cheap items is killing our margins, while the expensive stuff isn’t profitable enough to make up for it.



### Chart 7: Profit and Sales Distribution Across the States
 
Insights: Okay, so looking at this map, it’s super obvious that almost all the money is coming from just California ($458k) and New York ($311k). Those two alone are crushing it while every other state is basically pocket change. Texas is third with $170k, then there’s a bunch of other states in the $50k–$139k range, but most of the country is either barely breaking even or losing money (all those red/pink states).
Why This Matters: Basically, the whole company is riding on Cali and NY. If something bad happens in either of those states (new taxes, competition, etc.), profits would be destroyed. Meanwhile, we’re losing money or making almost nothing in 40+ states.
Business Interpretation: Either we figure out how to make money there or just stop wasting time and money on places that clearly aren’t working.



### Chart 8: Tree map
 
Insights: The tree map shows extreme profit concentration: Labels (44.4%), Envelopes (42.3%), Paper (43.4%), and Copiers (37.2%) together drive virtually 100% of company profit. The remaining 13 categories are essentially profit-neutral or negative, with Tables (-8.6%), Bookcases (-3.0%), and Supplies (-2.5%) being the clearest underperformers.
Why This Matters: The whole company is living off four products while dragging around a ton of dead weight that eats inventory, warehouse space, and sales effort for zero profit. 
Business Interpretation: Smart move would be to consider exiting furniture and supplies entirely. Keep treating all 17 categories as equals and we are voluntarily losing profit every day. 



### Predictive & What-If Analysis:
### Chart 9: Sales & Profit Distribution Across the Product Categories & Sub-Categories
 
Insights: This chart shows the distribution across the product categories and sub-categories as a Drill Down chart. It shows that technology is the leading bread winner where furniture is the loser in this scenario. In the right corner you can use the parameter to see each sub-category and where profit and loss occur. 
Why this Matters: We’re leaving massive money on the table by letting a high-volume category like Furniture destroy margins while Technology carries the profits; treating all three categories equally in pricing, promotions, and sales incentives is costing us heavily
Business Interpretation: Even though Furniture brings in solid sales too, its darker red color shows it has the lowest profit contribution of the three categories. We need to stop treating all categories the same, furniture needs urgent attention. This gives us an opportunity to re-evaluate prices for the future. 

### Chart 10: Sales Forecast
 
 
 
Interpretation: The 2024 forecast shows almost zero growth (+0.7% trend) and the same huge holiday spike every November/December, with sales crashing right after. The 99% confidence band is massive. MASE is 0.32 anything under 1.0 means the forecast beats a simple “same as last year” guess by a lot. This model is solid and captures the crazy seasonality well.
Why It Matters: One bad holiday season tanks the whole year, there’s nothing else propping up sales. The wide band means we must plan inventory and load up big for Q4, stay super lean the rest of the year.
Business Interpretation: We’re a seasonal business pretending to be year-round. Treat Q4 like life or death, cut costs in the off season, and stop lying to ourselves about steady growth because we don’t have. The $121K monthly target isn’t happening without a real plan.




### Chart 11: What If Scenario Analysis – Prescriptive Analytics
 
Insights: This chart shows a what if scenario if we added a discount to our categories. Eliminating all discounts adds $30K - $50K profit in Copiers, Phones, Accessories, Paper and Binders, flips Tables from loss to break even, and barely moves already high margin items like Labels/Envelopes.
Why This Matters: Discounting would destroy over $200K in potential profit annually, concentrated in just the top 6–7 categories. Not having discounts on Copiers, Phones, Accessories, Paper, and Binders alone would deliver a massive profit boost with zero additional sales volume required.
Business Interpretation: These categories are price sensitive and should be carefully monitored during promotions.
Part 4: Dashboard Overview
 
 
I built the dashboard in two pages
### Page 1 – Performance
•	Top-line KPIs: $732K sales (+20% YoY), $94K profit (+15%), units +25%
•	Big forecast chart with the Q4 spike
•	Dual axis sales vs. profit chart so you can see they track together

### Page 2 – The Real Problems
•	Profit tree map: only Copiers, Paper, Accessories, and Phones make real money
•	Pareto: 4-5 products carry basically the whole company
•	What if analysis chart: we would be throwing away $200K + a year on discounts
•	U.S. map: California and New York make up most of the profit, the rest of the country barely breaks even
•	Order Segmentation: most orders are small and make almost nothing
Red = bad, green = good, everything has region/category filters. The flow is simple: Page 1 shows we grew, Page 2 shows we’re still fragile and one bad move can destroy the company.
Part 5: Project Conclusions
### Key Findings:
1.	80% of profit = 4 products and 2 states 
2.	Furniture & Supplies lose money every year
3.	Discounts cost us a lot of money do not discount the big four, upsell instead.
4.	No real growth outside Q4, run it like seasonal retail, focus on holidays
5.	Tiny orders kill profit
### Reflection: 
This project was way more real world than I expected. Spent forever cleaning data, but once that was done everything was easy. Tableau went from I don’t know what I’m doing to second nature. The best part was seeing six figure profit leaks pop out in minutes just by navigating the data right. Honestly this is the first school project that didn’t feel like school, this felt like I built something a company would pay for. Solid preparation for a real job and I’m excited for what’s next.

<img width="432" height="618" alt="image" src="https://github.com/user-attachments/assets/8a73a43d-a5b4-49d2-880c-5f2e482b9586" />
