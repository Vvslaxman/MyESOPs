# MyESOPs

- cloned master-esops branch from repo
- first open ESOP.Solution and clean and build the solution file that builds 47 files inside it and generate build files in ESOP.RuntimePool
- copy all the folders and files present in ESOP.RuntimePool and paste them inside the Bin folder of MyESOPWebAPI and ESOPWEB
- ensure all the files have been pasted inside bin folders respectively
- now perform cleaning and building of MyESOPWebAPI solution,ensure there are no errors.
- if getting any error then try checking whether or not that missing file is present in bin folder or not, if not then go to ESOP.RuntimePool and paste it in bin folder or else try building the ESOP.Solution againa and replace the generated build files.
- restore databses ESOPManager, MailerDB, EDNUX_QA and update the connection strings using MD5 encryption in web.config file.
- now try cleaning and building solution, if o errors then publish the solution into a new folder.
- open ESOPWEB and copy all build files generated into bin folder.
- update the Application path in both web.config files, change the connections strings coorectly.
- check on any dependency and version conflicts being arised during cleaning and building of website
- if any errors try updated customErrors line in web.config file from "Off"->"On" and "Off"->"RemoteOnly" for better detailed error understanding.
- if no errors then publish the website with Do not merge and create separate assembly for each in the file in precompile options during publishing.
- if there are any errors while publishing publish the website using msbuild as:
  ```bash
  msbuild "C:\ED18Repo\ESOPWEB\website.publishproj" /p:DeployOnBuild=true /p:Configuration=Release  /p:PrecompileBeforePublish=true /p:OutputPath="C:\esopout" /p:PublishDir="C:\web"  /verbosity:diagnostic
  ```
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### MyESOPS
- downgradde node to 14.8 and npm to 6.14
- install angualr cli 13 verison and run the appliction using npm start
- build the same
  
