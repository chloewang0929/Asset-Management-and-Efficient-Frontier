# Asset-Management-and-Efficient-Frontier

# Motivation and Purpose

1. Different asset allocation ratios based on varying risk tolerance levels.<br>
2. Users can select desired individual stocks to invest in and input expected returns.<br>
3. Python calculates the efficient frontier and exports expected risk and asset allocation.<br>
4. Excel is used for Monte Carlo analysis, exporting both the best and worst-case scenarios.<br>
5. Related research: There are many studies on the efficient frontier and Monte Carlo analysis available online, but none provide a complete, user-oriented design with an interactive window for analysis.<br>

# Method

1. Create a GUI using tkinter and its related packages.<br>
2. Obtain individual stock lists and interact with users through the ssl package.<br>
3. Scrape information of listed stocks from the stock exchange.<br>
4. Draw the efficient frontier after calculations using Python.<br>
5. Conduct Monte Carlo analysis using Excel.<br>

```python
import scipy.optimize as solver
import matplotlib.pyplot as plt
import tkinter.font as tkFont
import tkinter.messagebox
import tkinter as tk
import pandas as pd
import numpy as np
import requests
import random
import string
import time
import json
import ssl
from pathlib import Path
from functools import reduce
from PIL import Image, ImageTk
from bs4 import BeautifulSoup
from pandas.core.frame import Dataframe
from datetime import datetime
from dateutil.relativedelta import relativedelta
```


# Plotting the Efficient Frontier

1.  Using PIL and tkinter packages: Create a GUI window, background, and input-output list fields.<br>
2. Establish two functions:<br>
• One function to list the individual stocks selected by the user.<br>
• Another function to delete the individual stocks selected by the user.<br>

__After scraping the list of codes from the Taiwan Stock Exchange, display it in the left column of the window and create a drop-down menu for user selection.__

```python
import requests
from bs4 import BeautifulSoup
all_stock =[]

res = requests.get("https://www.twse.com.tw/zh/stockSearch/stockSearch")
html = BeautifulSoup(res.text, "html.parser")

st_list = html.findAll("td")

row = 2
for name in st_list:
  names = name.text
  row += 1
  all_stock.append(names)
print(all_stock)
```
