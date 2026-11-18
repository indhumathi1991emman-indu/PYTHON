> **Python DA Capstone project**
>
> **Name : Indumathi.R**
>
> **Title : Marketing campaign Performance Insights**
>
> **Date of submission: 17.11.2026**

- **SYNOPSIS:**

<!-- -->

- Load dataset

- Basic structure and Data Exploration

- Campaign Performance

- Customer segmentation

- Channel Effectiveness

- Time-based Analysis

- Geographic Analysis

<!-- -->

- **Load Dataset:**

  <img src="./media/image23.png"
  style="width:6.26772in;height:3.52778in" />

  **Output:**

  <img src="./media/image16.png"
  style="width:6.26772in;height:3.52778in" />

  **Explanation:**

<!-- -->

- Import libraries of matplotlib,pyplot and pandas are imported to
  handle data visualization and data manipulation.

- Read data pd.read_csv(url) downloads the dataset and loads it into a
  structured table called a DataFrame(df).

- print (df.head()) print the first five rows of the dataset to verify
  that the data loaded properly.

<!-- -->

- **Obtain the number of rows and columns:**

<img src="./media/image17.png"
style="width:6.26772in;height:3.52778in" />

- The code print(df.shape)checks and displays the dimensions of a Pandas
  DataFrame named df.

- The output (22029, 16) shows that your dataset contains 22,029 rows
  and 16 columns.

<!-- -->

- **The Data types and non-null values:**

<img src="./media/image34.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- Data Quality&Types lists each column’s name, confirms there are no
  missing(null) values in the visible columns, and shows their data
  types such as integers(int64),decimal(float64),and text(object).

<!-- -->

- **Statistics for numerical columns:**

<img src="./media/image11.png"
style="width:6.26772in;height:3.52778in" />

> **Explanation:**

- It calculates the total count, mean(average), and standard
  deviation(std)to show typical values and spread out the data for
  metrics like Conversion_Rate and ROI.

- It displays the minimum (min),maximum(max), and quartile values(25%,
  50%median,75%)to help and quickly spot data ranges and potential
  outliers.

<!-- -->

- **Basic structure and Data Exploration:**

- **The number of Unique Campaign ID values:**

<img src="./media/image41.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- The code counts the total number of distinct values in the Campaign_ID
  column and no duplicate entries.

<!-- -->

- **The unique values of the Location and Customer_Segment columns:**

<img src="./media/image3.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- It prints an array of all 9 unique cities and 5 unique customer
  segments.

- It helps and quickly verify what text categories exist in your dataset
  and check for any spelling inconsistencies.

<!-- -->

- **Count & each category in the Campaign_Type and Channel_Used
  column:**

<img src="./media/image24.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- Category Ranking of the 5 campaign types and 6 marketing channels from
  highest to lowest frequency.

- Clean Spacing of the “\n”inside the second print() adds a blank line
  between the two outputs so they are easy to read.

<!-- -->

- **EDA (Exploratory Data Analysis):**

- **Scatter Plot:**

<img src="./media/image45.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image25.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- Chart Setup & Plotting plt.figure(figsize=8, 5) sets the chart
  dimensions, while sns.scatterplot() plots Acquisition_cost on the
  x_axis against ROI on the y-axis.

- Labels & Display of the Title(), xlabel(), and ylabel() functions
  label the chart clearly before plt.show() renders it on screen.

<!-- -->

- **Bar Chart:**

<img src="./media/image51.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image48.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- Grouping Plotting sns.barplot() plots Channel_Used on the x-axis and
  Conversion_Rate on the y-axis, using hue=’Campaign_Type’ to color-code
  the bars and errorbar=None to hide confidence interval lines.

- Formatting & Display of plt.figure(figsize=(figsize=10, 6)) sizes the
  plot.while title(), xlabel(),ylabel(), and legend() label all chart
  elements before plt.show() displays it.

<!-- -->

- **Box Plot:**

<img src="./media/image29.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image39.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- To create a box plot comparing Engagement_Score across different
  Campaign_Type categories.

- It sets the figure dimensions to 10x6 inches,styles the bar using the
  “Set2” color palette, and adds clear chart titles and axis labels
  before displaying.

<!-- -->

- **Using Bar Chart:**

<img src="./media/image8.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image20.png"
style="width:6.26772in;height:3.52778in" />

<img src="./media/image50.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- This code uses Seaborn(sns) and Matplotlib(plt)to create a bar chart
  comparing the average ROI(Return on Investment)across different
  Companies.

- It sets a white grid background, sizes the figure to 10x6 inches, and
  plots the bars using sns.barplot() with “Company” on the x-axis and
  “ROI” on the y-axis.

- Finally, it adds a title,rotates the x-axis labels by 45 degrees so
  they don’t overlap,adjusts the layout spacing, and displays the chart.

<!-- -->

- **Using Heatmap:**

<img src="./media/image26.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image47.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- This code calculates and visualizes the correction matrix between
  Engagement_Score and Conversion_Rate using a heatmap.

- First, .corr() computes the correlation values between the two
  selected columns, and sns.heatmap() plot a color-coded grid displaying
  the exact correlation values from -1 to 1.

<!-- -->

- **Customer Segmentation:**

- **Count Plot:**

<img src="./media/image53.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image28.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- Initialize & Plot sets the chart dimensions(10x5) and uses Seaborn
  (sns.countplot) to count and color-code campaigns for each audience
  for each audience group.

- Label & rotate adds a bolt title, names the x and y axes, and titles
  the bottom segment labels by 30 degrees so they do not overlap

- Adjust Spacing runs plt.tight_layout() to prevent any text from
  getting cut off when rendering the final bar graph.

<!-- -->

- **Bar chart:**

<img src="./media/image27.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image13.png"
style="width:6.26772in;height:3.52778in" />

<img src="./media/image33.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Setup & Plot:** Initializes a 12x6 figure and draws a grouped bar
  chart comparing average conversion rates across languages and customer
  segments without error bars.

- **Labels & Title:** Adds a bold main title and sets font sizes for the
  x-axis ("Language") and y-axis ("Average Conversion Rate").

- **Legend & Display:** Places the legend neatly outside the top-right
  corner, adjusts spacing to prevent overlap, and renders the final
  chart.

<!-- -->

- **Box plot:**

<img src="./media/image1.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image5.png"
style="width:6.26772in;height:3.52778in" />

<img src="./media/image15.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Setup & Boxplot:** Initializes a 12x6 figure and draws a grouped
  boxplot showing the distribution of acquisition costs across customer
  segments and channels.

- **Title & Axis Labels:** Adds a main title to the chart and labels the
  horizontal x-axis ('Customer Segment') and vertical y-axis
  ('Acquisition Cost').

- **Legend & Display:** Adds a legend titled 'Channel Used',
  automatically adjusts spacing to prevent overlap, and renders the
  final plot.

<!-- -->

- **Bar chart:**

<img src="./media/image14.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image21.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Setup & Sorting:** plt.figure(figsize=(10, 5)) sets the chart size,
  while avg_conv_by_lang groups the data by language to find and sort
  the highest average conversion rates (though it is not yet applied to
  the plot).

- **Creating the Bar Chart:** sns.barplot(...) plots Language on the
  horizontal axis and the mean Conversion_Rate on the vertical axis
  without error bars (errorbar=None).

- **Labels & Display:** The plt functions add the title, label both
  axes, adjust the spacing (tight_layout), and display the final graph
  on screen (show).

<!-- -->

- **Bar chart:**

<img src="./media/image49.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image32.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Data Cleaning:** It converts Engagement_Score to numeric values
  (turning invalid entries into NaN) and saves a version without missing
  scores into clean_df.

- **Plotting the Chart:** plt.subplot(4, 1, 2) selects the second slot
  in a 4-row grid, and sns.barplot(...) plots Channel_Used against
  Engagement_Score, using color (hue) to separate each Campaign_Type.

- **Formatting:** The remaining plt lines add axis labels, a legend
  titled "Campaign Type", and the main chart title.

<!-- -->

- **Pie Chart:**

<img src="./media/image9.png"
style="width:6.26772in;height:3.52778in" />

**output:**

> <img src="./media/image40.png"
> style="width:6.26772in;height:3.52778in" />
>
> <img src="./media/image22.png"
> style="width:6.26772in;height:3.52778in" />
>
> **Explanation:**

- **Data Grouping & Pie Chart:** Groups the dataset to calculate total
  ROI per marketing channel and plots a square 8x8 pie chart displaying
  percentage shares with a custom color palette.

- **Title & Aspect Ratio:** Adds a descriptive chart title and forces an
  equal aspect ratio so the pie renders as a true circle rather than an
  oval.

- **Display:** Renders and displays the final pie chart on the screen.

<!-- -->

- **Scatter plot:**

<img src="./media/image46.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image37.png"
style="width:6.26772in;height:3.52778in" />

<img src="./media/image31.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Chart Setup:** plt.figure(figsize=(10, 6)) initializes a blank
  canvas measuring 10 by 6 inches for the visualization.

- **Plotting the Data:** sns.scatterplot(...) maps Impressions (x-axis)
  against Clicks (y-axis), coloring the points by Channel_Used with
  slight transparency (alpha=0.7) to reveal overlapping data.

- **Formatting & Display:** The plot lines add the chart title, label
  both axes, display the channel legend, and render the final graph on
  screen.

<!-- -->

- **Histogram:**

<img src="./media/image30.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image44.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Chart Setup:** plt.figure(figsize=(8, 5)) sets the width and height
  of the plot to 8 by 5 inches.

- **Plotting the Histogram:** sns.histplot(...) divides Duration into 20
  sky-blue bars (bins=20) and overlays a smooth density curve (kde=True)
  to highlight the data's overall shape.

- **Labels & Display:** plt.xlabel and plt.ylabel name the horizontal
  and vertical axes, while plt.show() displays the final chart on
  screen.

<!-- -->

- **Line chart:**

<img src="./media/image52.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image4.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Data Prep & Line Plot:** Converts the date column to datetime
  format, calculates the average conversion rate per company over time,
  and plots a 12x6 multi-line chart.

- **Labels & Formatting:** Sets the main title, axis labels, and legend
  title, while rotating the x-axis date ticks by 45 degrees for
  readability.

- **Layout & Display:** Automatically adjusts spacing to prevent
  overlapping text and renders the final chart.

<!-- -->

- **Line Chart:**

  <img src="./media/image36.png"
  style="width:6.26772in;height:3.52778in" />

  **output:**

  <img src="./media/image38.png"
  style="width:6.26772in;height:3.52778in" />

  <img src="./media/image19.png"
  style="width:6.26772in;height:3.52778in" />

  **Explanation:**

<!-- -->

- **Date Formatting & Grouping:** It converts the Date column into a
  standard datetime format and calculates the average Engagement_Score
  for each date into eng_trend.

- **Plotting the Line:** plt.figure sets a 12x6 canvas, and sns.lineplot
  draws a teal trend line with circular data markers (marker='o')
  tracking Date against Engagement_Score.

- **Styling & Display:** The remaining plt lines add titles, rotate the
  date labels by 45 degrees for readability, add a faint dashed grid,
  and display the chart.

<!-- -->

- **Using Bar Chart:**

<img src="./media/image42.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image12.png"
style="width:6.26772in;height:3.52778in" />

<img src="./media/image43.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Data Loading & Grouping:** It reads the CSV data into a DataFrame,
  sums Acquisition_Cost by Location, and sorts the totals from highest
  to lowest.

- **Plotting the Bars:** cost_by_location.plot(...) draws a 10x6 bar
  chart with sky-blue bars and black outlines.

- **Styling & Display:** The plt functions add the title, label both
  axes, rotate city names by 45 degrees, and display the chart.

<!-- -->

- **Using Bar Chart:**

<img src="./media/image2.png"
style="width:6.26772in;height:3.52778in" />

**Output:**

<img src="./media/image6.png"
style="width:6.26772in;height:3.52778in" />

<img src="./media/image10.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Creating the Pivot Table:** df.pivot_table(...) calculates the
  average (mean) Conversion_Rate with Location as rows and
  Target_Audience groups as separate columns.

- **Plotting the Grouped Bars:** pivot_conv.plot(...) generates a 12x6
  bar chart with black-outlined bars representing each audience segment
  side by side.

- **Styling & Display:** The plot functions add the chart title, label
  both axes, display the audience legend, rotate city names by 45
  degrees, and render the graph.

<!-- -->

- **Using Pie Chart:**

<img src="./media/image35.png"
style="width:6.26772in;height:3.52778in" />

**output:**

<img src="./media/image18.png"
style="width:6.26772in;height:3.52778in" />

<img src="./media/image7.png"
style="width:6.26772in;height:3.52778in" />

**Explanation:**

- **Data Grouping & Pie Chart:** Groups the dataset to sum total ROI by
  location and plots an 8x8 pie chart displaying percentage shares using
  the Set3 color palette.

- **Title & Aspect Ratio:** Adds a descriptive title and enforces an
  equal aspect ratio so the pie renders as a true circle.

- **Layout & Display:** Adjusts spacing to prevent clipping and renders
  the final chart on screen.
