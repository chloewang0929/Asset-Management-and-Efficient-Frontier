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

# Plotting the Efficient Frontier

1.  Using PIL and tkinter packages: Create a GUI window, background, and input-output list fields.<br>
2. Establish two functions:<br>
• One function to list the individual stocks selected by the user.<br>
• Another function to delete the individual stocks selected by the user.<br>
