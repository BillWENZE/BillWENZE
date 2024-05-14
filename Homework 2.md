```
import pandas as pd

data = pd.read_csv('hw2_data.csv')
```

# Filter data where label is between -1 and 2

```
filtered_data = data[data['label'].between(-1, 2)]
```

"""Split the data based on the fiscal year"""
