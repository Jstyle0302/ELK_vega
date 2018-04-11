if we have more than 2 layers(levels) ,we have to re-create the marked code again and again.

{  
> SET the overview specification of the chart 

data: [  
> **_QUERY ES based on the currently selected time range and filter string_**  
>
> **_SET new key for later lookups - identifies each node  
> CREATE stack and grpId of each row_**
> 
> **_CREATE a sortkey, different for stk1 and stk2 stacks.  
> CALCULATE vertical center point for each node, used to draw edges 
> all nodes into country groups, summing up the doc counts  
> RE-CALCULATE the stacking y0,y1 values_** 
> 
> **_PROJECT y0 and y1 values to screen coordinates_** 
> 
> **_CREATE boolean flag if the label should be on the right of the stack  
> CALCULATE traffic percentage for this country using "y" scale_**  
>     
> **_CREATE a temp lookup table with all the 'stk2' stack nodes  
> FILTER  nodes from the left stack    
> FIND corresponding node from the right stack, keep it as "target"  
> CALCULATE SVG link path between stk1 and stk2 stacks for the node pair_**   
> 
]  

scales: [  
> **_CALCULATE horizontal n-stack positioning_**  
> SET scale goes up as high as the highest y1 value of all nodes  
> USE rawData to the colors  
> **_MAP internal ids (stk1, stk2,stk3,...,stk-n ) to stack names_**  
>
]  
  
axes: [  
> SET x axis custom label formatting to print proper stack names  
>
]  
  
marks: [  
> **_DRAW the connecting line between stacks_**  
> **_DRAW the text of connecting line between stacks_**    
> **_DRAW stack groups (countries)_**  
> **_DRAW country code labels on the inner side of the stack_**  
>	
]  

}
