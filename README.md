## SETUP
1. Provide database connetion properties in the application.properties, application-dev.properties, and application-qa.properties files. <br>
   Depending on **VM Options** you set, the database connection details will be processed either DEV or QA.
2. Add VM Options
` -Dspring.profiles.active=dev `
