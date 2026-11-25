# IndiaMart-India-PowerBI
Retail Sales and Profitability Analysis using Power BI, DAX, and Star Schema Data Modeling.

**Dax Formulas used to Analyze Data and Find useful insights.**
Total_Sales = sum('Sales Data'[Sales])
Total_Profit = sum('Sales Data'[Profit])
Total_Units = sum('Sales Data'[Quantity])
Profit_Margin% = DIVIDE(sum('Sales Data'[Profit]),[Total_Sales],0)
Avg_Order_Value = [Total_Sales]/DISTINCTCOUNT('Sales Data'[OrderID])
YTD = TOTALYTD([Total_Sales],'Calendar Data'[Date])
High_Margin_Sales = CALCULATE([Total_Sales],FILTER('Sales Data',DIVIDE('Sales Data'[Profit],'Sales Data'[Sales],0)>=0.20))
Sales_Target = ([Total_Sales]*0.2)+[Total_Sales]
