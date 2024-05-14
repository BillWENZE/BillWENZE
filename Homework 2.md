```
import pandas as pd

data = pd.read_csv('hw2_data.csv')
```

# Filter data where label is between -1 and 2

```
filtered_data = data[data['label'].between(-1, 2)]
```

# Split the data based on the fiscal year
```
train_data = filtered_data[filtered_data['fyear'] == 2018].drop('label', axis=1)
train_labels = filtered_data[filtered_data['fyear'] == 2018]['label']

validation_data = filtered_data[filtered_data['fyear'] == 2019].drop('label', axis=1)
validation_labels = filtered_data[filtered_data['fyear'] == 2019]['label']

test_data = filtered_data[filtered_data['fyear'] == 2020].drop('label', axis=1)
test_labels = filtered_data[filtered_data['fyear'] == 2020]['label']

(train_data.shape, train_labels.shape, validation_data.shape, validation_labels.shape, test_data.shape, test_labels.shape)
```
