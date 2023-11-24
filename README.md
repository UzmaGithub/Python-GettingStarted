
# Data Loading

Data loading in Python and loading top 1000 records in a separate .csv file in SQL


## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.
## Prerequisites 
The following are required in order to run this code in Python:

Set up Anaconda.
Set up Jupiter notebook.
Set up MSQL.
Create a new userid and password in MySQL.


## Installing
We use Jupiter notebook from the Anaconda package to work with Python. Post that we will install the required Python libraries to interact with MYSQL database and execute SQL queries. Then we will import the necessary libraries including Pandas, which is used to convert tables into dataframe and perform various operations. We will also import pymysql, to interact with MYSQL database.
## Running the tests
First we read the youtube_dataset csv file by creating a dataframe in pandas. 

Then we run tests to display the rows and columns, df.head(), get information about the type of dataset, df.info() function.

Then iloc is used to choose rows and columns from a DataFrame or Series based on their integer location rather than their labels.

results_table is used to return the output of the dataframe.

Then top_1000 and df.iloc are used, and we select rows from position 0 (inclusive) to 1000 (exclusive), which means selecting the first 1000 rows of the total 4000 rows of the DataFrame.

Lastly the create_engine function is used, to create a database engine, which will establish a connection to the specified MySQL database.

## Breakdown of end to end steps

First we read the youtube_dataset csv file by creating a dataframe in pandas. 

Post that we display all the information related to the dataframe, using df.info() function. 

The output of the df.info() function will display the Columns, Column number, the data types (integer, object etc.) and if the Columns have any values; it will also display if any Column has a null value. The memory usage of the dataframe is displayed as well.

Then we input a command to display the number of rows and columns, which essentially shows the shape of the dataframe.

Df.head() is used to display the top five rows of the dataframe.

#### Calculating the distribution of Channel type
To calculate the distribution of channel type, a function channeltype() is used. This function takes ‘data’ as an argument. Then iloc method is used to select the first 1000 records from the dataframe.

iloc in Python stands for "integer location" and is a method for selecting data by integer indexing. It is frequently used in conjunction with Pandas DataFrames. The basic goal of iloc is to allow you to choose rows and columns from a DataFrame or Series based on their integer location rather than their labels. The frequency distribution of the 'channeltype' values in the selected subset is calculated by distribution. Then it is converted in to percentages also for users to view the counts as well as percentage values. This output is displayed with three Columns – Channel Type, Count and Percentage.

result_table returns the created DataFrame as the output of the function. When you call this function with a DataFrame, it will return a summary table showing the distribution of 'channeltype' values, their counts, and percentages within the first 1000 records of the input data.

dis displays the values of the top 1000 rows of the dataframe.

#### Loading top 1000 records into a separate CSV file, and to a database table
By using top_1000 and df.iloc, we selected rows from position 0 (inclusive) to 1000 (exclusive), which means selecting the first 1000 rows of the total 4000 rows of the DataFrame.

Then we Save the dataframe to a CSV file.

This code is used to take the DataFrame top_1000 and save it to a CSV file named "top_1000_channels.csv" in the current working directory. This CSV file can then be used for further analysis, sharing with others, or as input for other programs. In the above code When set to False it tells Pandas not to write row names (index) to the CSV file. If you omit this parameter or set it to True (which is the default), the row names will be included as the first column in the CSV file.

The shape of the result, as in the number of rows and columns is displayed later.

#### Connection with MySQL server
We created a connection URL that specifies the database type, username, password, host and the name of the database. We used the create_engine function to create a database engine, which will establish a connection to the specified MySQL database. The engine will allow you to interact with the database.

•	'mysql+pymysql' specifies the database dialect (MySQL) and the Python MySQL database driver (PyMySQL).
•	'group10' is the username
•	'assig***' represents the password
•	'localho***' is the database host (can be an IP address or a domain name
•	'assig***' is the name of the database you want to connect with
•	Then we establish a connection to the database by calling the database con=engine

Following these steps we are successfully able to load the CSV file in a database created on the MySQL server. 

## Deployment
There was no real-time deployment of this project. This project was a test to run a code for school. 
## Contributing

Contributions are always welcome! 

The following members contributed to this project:
ramidkc
jillshah
niteshtalukdar

See `contributing.md` for ways to get started.

Please adhere to this project's `code of conduct`.


## Authors

- [UzmaGithub](https://www.github.com/UzmaGithub)

Professor Omar Altrad
## License

License to use by Durham College


## Acknowledgements

Prof. Omar Altrad

Rami D KC

Jill Shah

Nitesh Talukdar

