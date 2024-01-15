# Import packages 
import os # confirm file path/structure       
import numpy as np
import pandas as pd 

# List files in the Kaggle input directory
for dirname, _, filenames in os.walk('/kaggle/input/'):
    for filename in filenames:
        print(os.path.join(dirname, filename))



# Import CSV for prices
airbnb_price = pd.read_csv('/kaggle/input/nyc-market-trends/workspace/data/airbnb_price.csv')

# Import Excel file for room types
airbnb_room_type = pd.read_excel('/kaggle/input/nyc-market-trends/workspace/data/airbnb_room_type.xlsx')

# Import TSV for review dates. Specify sep or delimiter parameter. 
airbnb_last_review = pd.read_csv('/kaggle/input/nyc-market-trends/workspace/data/airbnb_last_review.tsv', sep='\t')
