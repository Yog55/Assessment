# Assessment
Assessment

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


#Task 1

Once JMeter has been started, open Task1.jmx.
Then select Run > Start
On the left pane, select View Results Tree and expand Question1, Question2, Question3 and Question4 in order to see the results of each API call.
