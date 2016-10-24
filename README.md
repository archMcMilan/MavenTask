#Task1:  
  - Create project with exec plugin.  
  - Main class should work with parameters.  
  - Write command examples for maven to run project.  
  - Create build profile that will turn on exec plugin.  
  - Use property to specify main class.
  
#Guide1:  

Exec plugin here is set to <b>'install'</b> phase.  
To run exec plugin with default settings from .pom file, choose <b>execution</b> profile:  
>mvn clean install -P execution  
  
To change main class and arguments:    
>mvn clean install -P execution -Dexec.main=ua.tasks.ap.AppRunner2 -Dexec.args="'hello' 'world'"


#Task2:  
  - Create project with 2 types of test - ITest and simple test.  
  - Configure maven to run build without ITests.  
  - Create profile to run build with ITests, only ITests.  
  - Use maven properties to configure ITest name convention.
  
#Guide2:  

To run all test - use profile <b>testingAll</b> or just default profile
>mvn clean test -P testingAll
>mvn clean test
  
To run only <b>ITest</b> use <b>testingITest</b> profile
>mvn clean test -P testingITest
  
To run all except <b>ITest</b> use <b>testingWithoutITest</b> profile
>mvn clean test -P testingWithoutITest
