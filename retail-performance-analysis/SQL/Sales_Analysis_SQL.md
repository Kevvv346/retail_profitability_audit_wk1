Analysis is being done on Big Query

# 1. Summary per State
select state,
    SUM(sales) AS total_sales
from `salesanalysis.sales`
GROUP BY
    state
ORDER BY
   state, total_sales DESC

# 2. Summary per Region
select Region,
    SUM(sales) AS total_sales
from `salesanalysis.sales`
GROUP BY
    Region
ORDER BY
    Region,total_sales DESC

# 3. Summary per Categories & Sub Categories
select Category, `Sub-Category`,
    SUM(sales) AS total_sales
from `salesanalysis.sales`
GROUP BY
    Category, `Sub-Category`
ORDER BY
    Category,`Sub-Category`,total_sales DESC

# 4. Summary per State
select State, 
    SUM(sales) AS total_sales
from `salesanalysis.sales`
GROUP BY
    State, `Sub-Category`
ORDER BY

# 5. Monthlys Sales Analysis
SELECT
    DATE_TRUNC(`Order Date`, MONTH) AS sales_month,
    SUM(Sales) AS monthly_sales
FROM
    `salesanalysis.sales`
GROUP BY
    sales_month
ORDER BY
    sales_month;
    State,total_sales DESC

