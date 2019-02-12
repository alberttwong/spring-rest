1. Create your app by `oc new-app --name=spring-rest java:8~https://github.com/alberttwong/spring-rest.git` or filling out the form in the service catalog.
2. Uncheck auto deploy when you have new images or config changes within your project's deployment configuration
3. Modify your Jekinsfile.standalone as needed (ie. change the app names) and commit into git.
4. Modify your the Jenkinsfile.standalone.yaml deployment configuration (ie. change the git url of the app and name) and commit into git.
5. Create the Jenkins Pipeline config in OCP by `oc create -f https://raw.githubusercontent.com/alberttwong/spring-rest/master/Jenkinsfile.standalone.yaml` or executing the YAML within the service catalog.
6. Run a Jenkins pipeline by `oc start-build spring-rest-build` (the name you used in Jenkinsfile.standalone.yaml) or clicking via the UI.
6. Optional: Configure your project's githook to push an event to OCP to run the Jenkins Pipeline.
