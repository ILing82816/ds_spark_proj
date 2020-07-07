# Big Data Spark System: Project Overview (with Chunchu Liu and Yuke Liu)   

## part 1: Setting up Spark and Test
After download Spark package and install scala, we run Spark Shell with YARN:
`cd spark`    
`bin/spark-shell --master yarn --deploy-mode client`
We use part1.scala to test. Our output is down below:  
![image](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part1.png)<br />
We also run Spark example program with YARN:
`bin/spark submit class org.apache.spark.examples.SparkPi
--master yarn\
--deploy mode client\
--driver memory 512m\
--executor memory 512m\
--executor cores 1\
--queue default\
examples/jars/spark-examples*.jar\
10`  
Our output:  
![](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part1master.png)<br />

## part 2: Developing Spark programs
We use part2.scala to printout the total listening counts of each artist.  
Our output:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part2.png)<br />

## part 3C: Developing Spark programs
We use part3c.scala to group the access logs by the timestamp in month.
* First, we read the file as a dataframe as shown below:   
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3c1.png)<br />  
* Then, we filtered the data with year and month:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3c2.png)<br />  

Our output is show below:  
![image](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3c3.png)<br />  

## part 3D: Developing Spark programs
We use part3d.scala to do the simple linear regression on the grouped result using Spark MLlib and save the model to a output file.  
Our datafram:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3d1.png)<br />
The coefficients of model:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3d2.png)<br />
The intercept of model:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3d3.png)<br />
Using Root Mean Squared Error to evaluate model:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3d4.png)<br />
Using R square to evaluate model:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3d5.png)<br />
The model we save:  
![image.png](https://github.com/yukel27/Cloud-Computing/blob/master/Mini%20Project%202/images/part3d6.png)<br />
