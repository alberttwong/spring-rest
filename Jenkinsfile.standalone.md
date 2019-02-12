1. Create your app by `oc new-app --name=spring-rest java:8~https://github.com/alberttwong/spring-rest.git`
2. Uncheck auto deploy when you have new images or config changes within your project's deployment configuration
3. Modify your Jekinsfile.standalone as needed (ie. change the app names)
4. Modify your the Jenkinsfile.standalone.yaml deployment configuration (ie. change the git url of the app and name)
5. Create the Jenkins Pipeline config in OCP by `oc create -f https://raw.githubusercontent.com/alberttwong/spring-rest/master/Jenkinsfile.standalone.yaml`
6. Optional: Configure your project's githook to push an event to OCP to run the Jenkins Pipeline.
