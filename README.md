In this challenge, is all  about knowledge of SparkSQL to determine key metrics about home sales data. Then the  Spark is used here to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

**Instructions**

1.Import the necessary PySpark SQL functions for this assignment.
2.Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.
3.Create a temporary table called home_sales.
4.Answer the following questions using SparkSQL:
5.What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
6.What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
7.What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
8.What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
9.Cache your temporary table home_sales.
10.Check if your temporary table is cached.
11.Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
12.Partition by the "date_built" field on the formatted parquet home sales data.
13.Create a temporary table for the parquet data.
14.Run the query that filters the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.
15.Uncache the home_sales temporary table.
16.Verify that the home_sales temporary table is uncached using PySpark.


**Set up Instructions**

**Local System Users**:-
#the version used in the local system
!pip3 install pyspark
!pip3 install findspark

# Start a SparkSession
import findspark
findspark.init()

spark_version = 'spark-3.4.0' #the correct version of spark when doing it in your loacal system
os.environ['SPARK_VERSION']=spark_version

os.environ["JAVA_HOME"] ="/Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home"
os.environ["SPARK_HOME"] = "/opt/anaconda3/lib/python3.12/site-packages/pyspark"


**Google colab users**:-

#the version used in the google colab
!pip install pyspark
!pip install findspark

# Start a SparkSession
import findspark
findspark.init()

spark_version = 'spark-3.5.3'
os.environ['SPARK_VERSION']=spark_version

os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-11-openjdk-amd64"
os.environ["SPARK_HOME"] = f"/content/{spark_version}-bin-hadoop3"

