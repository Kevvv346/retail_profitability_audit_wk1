Analysis is being done on Big Query

# 1. Summary per State
select state,
    SUM(sales) AS total_sales
from `salesanalysis.sales`
GROUP BY
    state
ORDER BY
    total_sales DESC

# 2. Summary per Region
select Region,
    SUM(sales) AS total_sales
from `salesanalysis.sales`
GROUP BY
    Region
ORDER BY
    total_sales DESC

# 3. Summary per Categories & Sub Categories
select Category, `Sub-Category`,
    SUM(sales) AS total_sales
from `salesanalysis.sales`
GROUP BY
    Category, `Sub-Category`
ORDER BY
    Category,`Sub-Category`,total_sales DESC
