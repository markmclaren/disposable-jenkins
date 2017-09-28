# disposable-jenkins
A throwaway Jenkins server in a Maven build

_When all you have is Maven everything looks like a lifecycle phase or goal._

Admittedly this could so easily have been a Vagrantfile, Docker image or some Gradle cleverness but I wanted something quick and dirty to mess around with Jenkins.

So I chose a Maven WAR overlay of Jenkins.

I tend to run it using:

`mvn tomcat7:run-war`

The JENKINS_HOME location is ~/target/jenkins_home (so a Maven clean will get rid of it).

After the initial run I tend to edit _~/target/jenkins_home/config.xml_ to specify _&lt;useSecurity>false&lt;/useSecurity>_.

I've primed this one with the Job DSL, text-finder and repository-connector plugins because they are currently of interest to me, other than that - it is just a disposable Jenkins installation.
