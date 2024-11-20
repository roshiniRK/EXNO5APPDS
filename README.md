# EXNO5APPDS

# AIM:

      To implement Dashboards creation with Plotly and Dash using python.
      

# About Dash and Plotly tools:

Dash is a Python framework for building analytical web applications. Dash helps in building responsive web dashboards that is good to look at and is very fast without the need to understand complex front-end frameworks or languages such as HTML, CSS, JavaScript. Let’s build our first web dashboard using Dash.

Plotly library in Python is an open-source library that can be used for data visualization and understanding data simply and easily. Plotly supports various types of plots like line charts, scatter plots, histograms, box plots, etc.


# ALGORITHM:

Step 1: Import Necessary Library like dash and plotly.
Step 2: Load the dataset.
Step 3: Add dropdown using layout function and include the necessary options.
Step 4: Display the necessary visualization tools and include the necessary parameters.
Step 5: Display the output.


# CODING AND OUTPUT:
```
pip install dash plotly pandas

import dash
from dash import dcc, html
from dash.dependencies import Input,Output
import plotly.express as px
import pandas as pd
import plotly.graph_objects as px
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df = sns.load_dataset('tips')
```

```
plot=px.Figure(data=[px.Scatter(x=df['day'],y=df['tip'],mode='markers')])
plot.update_layout(updatemenus=[dict(buttons=list([dict(args=["type","scatter"],label="Scatter Plot",method="restyle"),dict(args=["type","bar"],label="Bar Chart",method="restyle")]),direction="down",)])
plot.show()

```
```
import plotly.express as px
df=px.data.tips()fig = px.scatter_3d(df, x="total_bill",y="sex",z="tip",color='day',size='total_bill',symbol='time')
fig.show()
```

```
import plotly.express as px
df=px.data.tips()
fig = px.bar(df, x='day',y='total_bill',color='sex',facet_row='time',facet_col='sex')
fig.show()
```

```
import plotly.express as px
df=px.data.tips()
fig = px.histogram(df, x='total_bill',color='sex',nbins=50,histnorm='percent',barmode='overlay')
fig.show()
```

```
import plotly.express as px
df=px.data.tips()
fig = px.pie(df, values='total_bill',names='day')
fig.show()

```

# OUTPUT :

![image](https://github.com/user-attachments/assets/02b2c967-3618-4981-8169-3d70eb037f5c)

<table>
<tr>
<td>
      
![image](https://github.com/user-attachments/assets/474beebd-a86d-4607-bfe0-fa0e69162c50)

</td>

<td>
      
![image](https://github.com/user-attachments/assets/6763a720-64fa-4f52-b938-b3a25c2177a4)


</td>
            
</tr>
</table>

![image](https://github.com/user-attachments/assets/0fedad7b-78f3-4895-b7dc-f51c0f66e0aa)

![image](https://github.com/user-attachments/assets/194b3ceb-a74a-469f-979f-bcdde16695f0)

![image](https://github.com/user-attachments/assets/202f68e4-f58f-4fa4-8dcc-8f55293351a5)

# RESULT:
Thus , To implement Dashboards creation with Plotly and Dash using python is successfully done.
