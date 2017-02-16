node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'
   
   git url: 'https://github.com/GeneChuang1/jenkins_pipeline_java_maven.git'

   // Get the maven tool.
   // ** NOTE: This 'M3' maven tool must be configured
   // **       in the global configuration.           
   def mvnHome = tool 'M3'

   // Mark the code build 'stage'....
   stage 'Build'
   // Run the maven build
   //Original Code:
   bat "${mvnHome}/bin/mvn -Dmaven.test.failure.ignore clean package"
   //sh "${mvnHome}/bin/mvn -Dmaven.test.failure.ignore clean package"
   //step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.xml'])

	//Start of Gene's Test Code:
	//try {
	//	sh "${mvnHome}/bin/mvn -Dmaven.test.failure.ignore clean package"
	//} catch (err){
	//	step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/TEST-*.*.xml'])
	//	throw err
	//}
	//End of Gene's Test Code
	
}