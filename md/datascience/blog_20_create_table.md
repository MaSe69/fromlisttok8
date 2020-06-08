---
layout: page_public
title: From Lists to K8s
meta: Overview Meta
permalink: /create_table/
---

# Create Table

In this first technical part, I create some tables.

For the accounting scenario, typically, there are numbers in a period of time, e.g. months. These numbers could be revenue or costs in various accounts.
Step 1: A First Table For Accounting
I intend to create a table with months as columns and accounts as rows. At first, I create a list for the acconts, then a list for the months. The point is to use the pandas command to create the dataframe using the accounts as index and the months as columns. Finally, I fill the values of the cells with zeros.
accounts = ["Account_A", "Account_B", "Account_D", "Account_X"]
months = ["January", "February", "March"]
df = pd.DataFrame(index=accounts, columns=months) 
df = df.fillna(0)
As intended, the outcome looks like:
           January  February  March
Account_A        0         0      0
Account_B        0         0      0
Account_D        0         0      0
Account_X        0         0      0

Step 2: Make the columns more dynamic 
Adding months to a list should be automated. Using pandas’ period_range, the start, the increment and the repetition can be easily defined.
months = pd.period_range(start="2020-01-01", periods=8, freq="M")
Further, the cell values should reflect values in a currency. Random numbers with 2 digits would be nice.
This can be achieved as follows:
cellValues = np.random.rand(4, 8) * 1000
cellValues = cellValues.astype(float).round(2)
df = pd.DataFrame(cellValues, index=accounts, columns=months)

Now the result looks much more like an interesting accounting table.
           2020-01  2020-02  2020-03  2020-04  2020-05  2020-06  2020-07  2020-08
Account_A   351.16   982.01   241.13   422.12   499.90   721.31   525.59    59.76
Account_B   690.57    82.52   194.08    54.63   460.64   901.15   303.77   699.62
Account_D   555.01   591.41   825.60   403.47   856.62   485.57   716.13   602.52
Account_X   506.24   197.62   912.49   717.87   988.16   585.67   957.28   112.60



Step 3: Define a Function for Table Creation
The column should represent any time interval, e.g. days, weeks, months, years, and certainly should start at any time to cover a many iterations as we like.
The number of accounts should also be flexible and determined by the number of accounts that we provide in the list. 
Re-use is typically done by defining a function. Function have parameters. Providing the required mandatory input parameters can be painful, because it requires all interfaces to be adapted at the same time to avoid syntax errors. Luckily, a single parameter when defined as a dictionary can do the trick in Python. I call that general purpose parameter for short ‘para’. 
Functions need to be defined before they are called. Here is a possible general implementation for the purpose described.
def pdDFFromListsCreate(para):
    dfl = pd.DataFrame(para["CellValues"], index=para["Index"], columns=para["Columns"])
    return dfl
The parameterization is chosen to be 
para["StartDate"] = "2020-06-01"
para["TimeInterval"] = "D"
para["NrColumns"] = 10
para["Columns"] = myMonthsPD = pd.period_range(
    start=para["StartDate"], periods=para["NrColumns"], freq=para["TimeInterval"]
)
# Rows
accounts = ["Account_A", "Account_B", "Account_D", "Account_F", "Account_X"]
para["Index"] = accounts
para["NrRows"] = len(accounts)
# Values
cellValues = np.random.rand(para["NrRows"], para["NrColumns"]) * 1000
cellValues = cellValues.astype(float).round(2)
para["CellValues"] = cellValues


The result is a larger table
           2020-06-01  2020-06-02  2020-06-03  2020-06-04  2020-06-05  2020-06-06
Account_A      496.62      578.81      730.94      697.60      967.98       64.05
Account_B      177.26      942.11      604.33      103.91      513.84      455.17
Account_D       32.24      629.63      442.73      916.11      827.24      314.53
Account_F      444.54      298.93       39.16      600.06      674.27      175.03
Account_X      792.80      289.78      189.62      560.98      407.42      468.28
