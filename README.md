# Web Scrapping Project

🌍 **Project Focus:**

The script performs web scraping directly from Wikipedia, on the page "List of countries by total wealth." It searches for a specific HTML table (with style text-align: right) and extracts the data.

🔧 **Data Collection Process:**

Uses BeautifulSoup to parse the HTML content.  
Looks inside the table’s <tbody> for <tr> rows.  
For each row, it collects the <td> cells, cleans characters such as the special space '\xa0', and organizes the values.

🚨 **Exception Handling:**

The code checks whether the table was found. If not, it raises an Exception (“Table not found” or “Table body not found”).  
This ensures robustness in case the page layout changes.

📋 **Data Organization:**

For each table row, the script creates a temporary list, accumulates the values, and then builds a general list of countries and their respective economic metrics.

📊 **Use of pandas:**

The extracted data is transformed into a DataFrame, allowing for tabular manipulation, exporting, and later analysis in a simple and efficient way.

📈 **Visualization and Insights:**

The script uses matplotlib to generate charts from the obtained data.  
A chart was created that clearly shows:
- Saudi Arabia (Arábia Saudita), Greece, and Poland are the top 3 in the ranking, presenting very similar levels of total wealth.
- Right behind are Israel, Portugal, and Chile, still with high values but already showing a slight decline compared to the first group.
- Countries such as Ireland, South Africa (África do Sul), and Finland appear in the intermediate group, maintaining a certain economic relevance.
- Further down, there is a sharp decline with Peru, Pakistan (Paquistão), Argentina, and Romania, highlighting significant disparities in wealth distribution.
- The chart clearly reveals this gradual transition and highlights the geographic diversity among the 20 listed countries.

  <img width="1190" height="590" alt="image" src="https://github.com/user-attachments/assets/2ff49c73-39aa-48f0-83ec-30c0126edcbb" />


💡 **Key Learnings from this Project:**

- Targeted extraction (by style or structure) increases precision.
- Text pre-processing is indispensable for cleaning HTML data.
- Handling exceptions during data collection prevents silent failures.
- Using pandas to organize data facilitates analysis and chart generation.
- Chart generation enhances interpretation, highlighting patterns and extremes immediately.
- Even public web data requires constant verification, as page changes can break the pipeline.

🚀 **Conclusion:**

This project exemplifies a robust pipeline:
1) Reading the website.
2) Locating and parsing the table.
3) Cleaning and structuring the data.
4) Exporting and enabling graphical visualization.

Result: a reliable database on countries and their total wealth, ready for future analyses and visualizations.
