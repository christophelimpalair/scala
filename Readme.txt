Make sure you have at least Scala 2.10.3

https://blogs.oracle.com/arungupta/entry/scala_and_maven_getting_started

mvn archetype:generate \
      -DarchetypeGroupId=org.scala-tools.archetypes \
      -DarchetypeArtifactId=scala-archetype-simple  \
      -DremoteRepositories=http://scala-tools.org/repo-releases \
      -DgroupId=org.glassfish.samples \
      -DartifactId=scala-helloworld \
      -Dversion=1.0-SNAPSHOT

Add this to pom.xml file:
<configuration>
  <launchers>
    <launcher>
      <id>sample</id>
      <mainClass>org.glassfish.samples.App</mainClass>
      <args>
        <arg>${basedir}</arg>
      </args>
    </launcher>
  </launchers>
</configuration>

Also add this to your pom.xml

http://blog.cloudera.com/blog/2014/04/how-to-run-a-simple-apache-spark-app-in-cdh-5/

Make sure you edit <groupId>org.scalatest</groupId> to have the following:
<artifactId>scalatest_2.10</artifactId>
<version>2.2.3</version>

$ mvn package

/usr/local/spark (your spark directory)/bin

$ ./spark-submit --class App --master local ~/Documents/projects/scala-helloworld/target/App.scala-1.0-SNAPSHOT.jar


