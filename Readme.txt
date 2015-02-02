I recommend IntelliJ IDEA for building and compiling Scala programs/jars. It is far easier.

In IntelliJ, install the Scala plugin, create a new Scala project, then add Framework support (maven) by right clicking the project.

Edit your POM file to match the one in this repository. (Thanks Joel Miller for the POM file)

All you have to do is edit the POM <groupID> and <artifactID> to match your project name/package name.

Enjoy!