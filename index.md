## About Me

Welcome to my GitHub portfolio dedicated to data analysis and data science! I'm a junior at San Francisco State University majoring in Computer Science. I'm also a mentor for DataJam at Pittsburgh DataWorks. My passion for data is unwavering, and I'm actively seeking opportunities to break into the field of Data Science and Analytics. Feel free to reach out to me via email or mobile for any opportunities or collaborations.

## Skills
- **Programming**: Python (NumPy, Pandas), R, SQL
- **Visualization**: Tableau, Python (Matplotlib, Seaborn), R

## Projects

### Data Exploration: Car Break-ins in San Francisco
[![View on GitHub](https://img.shields.io/badge/GitHub-View_on_GitHub-blue?logo=GitHub)](https://github.com/cmeddata/sf-car-breakins-analysis/blob/main/README.md)

- With the rising number of car break-ins here in San Francisco, I decided to do some data exploration using the reported crimes data given by DataSF
  
- The dataset originally had 700k+ reported crimes, in order to suit the needs of this project, I had to find a way to clean the data up to only show what i needed. I ended up using the pandas library in python in order to filter out unnessecary data from the dataset.
  
- The Following code is what i used to filter out the data in python.
  
```break
#reads csv file
Police_Report_df = pd.read_csv("Police_Report.csv")

#filters the csv file to Larceny Theft with Subcategory of Larceny from vehicle. then sets it to Police_Report_df
condition = (Police_Report_df['Incident Category'] == 'Larceny Theft') & (Police_Report_df['Incident Subcategory'] == 'Larceny - From Vehicle')
Police_Report_df = Police_Report_df[condition]
```

- With that out of the way, I was curious as to which neighbourhoods in SF have the most number of Car breakins. In order to Figure that out, I used the code below.


```break
#Analysis by Neighborhood
def Analysis_by_Neighborhood(data):
    # Count the number of incidents for each neighborhood
    neighborhood_counts = Police_Report_df['Analysis Neighborhood'].value_counts()

    # Create a bar plot
    plt.figure(figsize=(10, 5))  # Adjust the figure size as needed
    neighborhood_counts.plot(kind='bar', color='lightcoral')
    plt.title('Car Break-ins by Neighbourhood')
    plt.xlabel('Neighborhood')
    plt.ylabel('Frequency')
    plt.xticks(rotation=90)  # Rotate x-axis labels for better readability
    plt.grid(axis='y', linestyle='--', alpha=0.7)
    plt.show()
```

- This code visualized the data which resulted into this graph.

 ![Neighbourhood](https://github.com/cmeddata/cmeddata.github.io/assets/124543750/2b34a2f0-846d-42be-bf8a-e1fd25908f86)

- If you want to see my full data analysis on this subject, click on either my github profile or this link here. [![View on GitHub](https://img.shields.io/badge/GitHub-View_on_GitHub-blue?logo=GitHub)](https://github.com/cmeddata/sf-car-breakins-analysis/blob/main/README.md)





<center>© 2023 Carlos De Leon. Powered by Jekyll and the Minimal Theme.</center>

