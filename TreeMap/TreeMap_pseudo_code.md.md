{   
> SET the overview specification of the chart 

"signals": [

> SET the adjustable bottom for users to resize the chart  

],



"data": [
 
> QUERY ES based on the currently selected time range and filter string  
>
> SET new key for later lookups - identifies each node  
> USE **stratify** to transform the dataset into the desired data format  
> CREATE **nodes, leaves and first_nodes table** 

],

"scales": [

> SET the color, size, opacity and fontWeight reference values

],

"marks": [
> SET the properties of the first layer   
> SET the properties of the leaves and set the tooltips   
> SET the texts which we want to show on the chart     

]

}