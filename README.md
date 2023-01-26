# Mars_Analysis

## Deliverable 2: Analysis of Mars Weather Data

1. How many months exist on Mars?

There are 12 martian months. This information can be found by identifying the number of unique values in the martian month column.

<img width="505" alt="image" src="https://user-images.githubusercontent.com/114873837/214962650-f1c53e9f-0ac6-4454-8da5-bc66186b2f30.png">


2. How many Martian (and not Earth) days worth of data exist in the scraped dataset?

If each data point represents another day that has elapsed on Mars and there are 1867 observations within the data set, we can assume that 1867 martian days have elapsed. To confirm, there are 1867 unique values in the "sol" column, which represents the martian days - which means that the data set contains 1867 martian days worth of data. 

<img width="934" alt="image" src="https://user-images.githubusercontent.com/114873837/214963027-b2ea6ee6-032e-4563-a2c2-ac9366bcc1b0.png">

3. What are the coldest and the warmest months on Mars (at the location of Curiosity)?

To find the average of the minimum daily temperature for each month on Mars, I began by grouping the weather data by month with a group by function and then calculated the aggregate mean value. The command and results for each month are below:

<img width="691" alt="image" src="https://user-images.githubusercontent.com/114873837/214963593-1c9ec21f-e6be-457f-9153-cb693fc5299b.png">

To display the average minimum temperature by month visually within a bar chart, I used matplotlib to chart the temperature on the y-axis and martian month on the x-axis.

<img width="1084" alt="image" src="https://user-images.githubusercontent.com/114873837/214964011-c7c24766-9ba6-4946-84f0-a097ed615d7b.png">

From this plot and the previous data frame displaying average temperatures, the third month is the coldest, with an average temperature of -83.3, and the 8th month is the warmest, with an average temperature of -68.38.

4. Which months have the lowest and the highest atmospheric pressure on Mars?

Using the dataframe grouped by month that was created for the previous question, I isolated the "pressure" column in order to display the atmospheric pressure of all the martian months.

<img width="651" alt="image" src="https://user-images.githubusercontent.com/114873837/214964663-ab2788d0-7126-4686-b279-3fda23e65925.png">

To display the average pressure by month visually within a bar chart, I used matplotlib to chart the pressure on the y-axis and martian month on the x-axis.

<img width="1135" alt="image" src="https://user-images.githubusercontent.com/114873837/214965125-ebc1a26d-4955-4e59-92a7-29818c514b1e.png">

From this plot and the previous data frame displaying average pressure, the sixth month has the lowest pressure, and the ninth month has the highest pressure.

5. About how many terrestrial (Earth) days exist in a Martian year?

Since the data of interest for this question includes the terrestrial date and the minimum temperature, I used the 'loc' function to create a new data frame isolating those columns.

<img width="746" alt="image" src="https://user-images.githubusercontent.com/114873837/214965596-5c19ec50-c463-43aa-bdac-56cf1695aeae.png">

Then I plotted a line chart of the minimum temperature over time, displaying the terrestrial days on the x axis and temperature on the y-axis.

<img width="1079" alt="image" src="https://user-images.githubusercontent.com/114873837/214965787-cd3d8ddf-d862-494c-8f91-6c8ef184c3b7.png">

On this graph, the first terrestrial day recorded is set at a value of zero, with each increment of 1 representing another day of the earth's calendar. We know that the temperature on mars follows a cyclical pattern throughout the year, so the length of time between the visual dips of the lowest temperature should represent one martian year. I would estimate that the first bottom dip occurs around day 450 and the second around day 1125, so if we subtract that we'd get 675 earth days that have elapsed for the martian year.
