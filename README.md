# Big-data
Generating Movie Recommendations from 1 million user ratings data, using Hadoop map-reduce and Spark on AWS cloud clusters.

In hadoop map reduce folder the program will be run on EMR cluster which is present in Amazon Web Services. In order to run the map reduce program type the following command in your python cmd console. 

  python MovieSimilaritiesLarge.py -r emr --num-ec2-instances=5 --items=ml-1m/movies.dat ml-1m/ratings.dat > recommendations.txt
  
The program will be executed and the output will be saved in the recommendations.txt file. 
If any problem occurs with your amazon EMR cluster while running trouble shoot the cluster by using the following command:
  python -m mrjob.tools.emr.fetch_logs --find-failure j-1NXMMBNEQHAFT (substitute with your job id)
  
In order to refine the results you can increase the threshold values to that the output will be more refined. And also if you want to refine and view your results on one particular movie then run the second python code in the map reduce folder taking the recommendations.txt file as the input. for example I have refined my search results on star wars movies. 
