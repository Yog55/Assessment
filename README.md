# Assessment
Tools Used for the Assessment: JMeter 4.0

# Setup
#1 - Ensure Java is installed on the test machine. The version used on the development machine was - java version "1.8.0_161".

#2 - Download the Task1 and Task2 Folders and place them in a folder called Assessment

#3 - Download Jmeter 4 from the following URL: https://archive.apache.org/dist/jmeter/binaries/apache-jmeter-4.0.zip

#4 - Unzip the above JMeter into the Assessment folder

#5 - Download the chromedriver.exe and place it into the bin directory of JMeter ... apache-jmeter-4.0 > bin >

#6 - Download the jmeter-plugins-manager-1.3.jar file and put the file into the lib/ext directory of JMeter ... apache-jmeter-4.0 > lib > ext >

#7 Start JMeter ... apache-jmeter-4.0 > bin > jmeter.bat

#8 Click "Options" and then "Plugins Manager", select the Available Plugins tab. Select "Selenium/WebDriver Support" and then select the button on the bottom right titled "Apply Changes and Restart JMeter".

#9 The folder structure and naming conventions of the files in the Assessment folder should look like follows:

Assessment > Task1 > Task1.jmx
Assessment > Task2 > Task2.jmx
Assessment > Task2 > User.csv
Assessment > apache-jmeter-4.0 > lib > ext > jmeter-plugins-manager-1.3.jar
Assessment > apache-jmeter-4.0 > bin > chromedriver.exe
Assessment > apache-jmeter-4.0 > bin > jmeter.bat


# Task 1

Once JMeter has been started, open Task1.jmx.
Then select Run > Start
On the left pane, select View Results Tree and expand Question1, Question2, Question3 and Question4 in order to see the results of each API call.

![task1_0](https://user-images.githubusercontent.com/16992657/50120021-f5776480-025c-11e9-99b0-24e9fd9147da.JPG)

For the task to use code, in order to verify “retriever” breed is within the list.
Code was written within a beanshell assertion in order to verify that the response contained the "retriever" breed.

![task1_1](https://user-images.githubusercontent.com/16992657/50120022-f5776480-025c-11e9-8314-d9999dc5b786.JPG)

The output of the API request to produce a list of sub-breeds for "retriever".

![task1_2](https://user-images.githubusercontent.com/16992657/50120023-f5776480-025c-11e9-9a5e-efdcba5b9abb.JPG)

The output of the API request to produce a random image / link for the sub-breed “golden”

![task1_3](https://user-images.githubusercontent.com/16992657/50120019-f4dece00-025c-11e9-807e-d5ad0420c8c6.JPG)




# Task 2

Once JMeter has been started, open Task2.jmx.
Then select Run > Start
On the left pane, select View Results Tree and expand the items, the items marked in green indicates that the step has passed.
If an item is in red, it indicates that the step has failed.

![task2_0](https://user-images.githubusercontent.com/16992657/50118634-ff976400-0258-11e9-89af-7c590bd47a0a.JPG)

The test is automated using JMeter with the webdriver plugin. The first navigation step can be viewed by selecting Navigate from the left pane and the code can be viewed on the main pane.

![task2_1](https://user-images.githubusercontent.com/16992657/50118753-6452be80-0259-11e9-9ae3-5461cf2117e6.JPG)

This component also had a regular expression extractor that extracts all first names from the table.

![task2_2](https://user-images.githubusercontent.com/16992657/50118754-64eb5500-0259-11e9-9f8c-eab0ef98ef54.JPG)

It then validates if you are on the table by comparing all the first names in the table to your name.
Your name can be set by select the Test Plan and setting the value for the parameter called "sMyName".
The value of "sMyName" is then compared to all the values in the table. If the value does not appear in the table then the "Validate that you are on the User List Table" will appear red in the playback and if the value is found, it will be green.

![task2_3](https://user-images.githubusercontent.com/16992657/50118757-6583eb80-0259-11e9-98ee-d06d76519ead.JPG)

The code to add users to the table is stored in the Add Users component, in order to view the code, please select the component in the left pane.

![task2_3](https://user-images.githubusercontent.com/16992657/50118757-6583eb80-0259-11e9-98ee-d06d76519ead.JPG)

Values that are added to the table are fed in from a CSV file. The username is created dynamically in the code in order to ensure that it is unique, a prefix for the username is set in the variable in the test plan "pUsernamePrefix".

![task2_5](https://user-images.githubusercontent.com/16992657/50118760-661c8200-0259-11e9-90d8-cdeb2a9cca49.JPG)

![task2_4](https://user-images.githubusercontent.com/16992657/50118759-6583eb80-0259-11e9-977e-d6509d633535.JPG)

There is also a response assertion on Add Users in order to ensure that the users that were created appear in the table.







