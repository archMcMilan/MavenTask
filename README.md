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
