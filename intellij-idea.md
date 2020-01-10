(c) 2018-04-06 Christoph Knabe

# IntelliJ IDEA (IDE)

IntelliJ IDEA is a Java centered IDE, which supports  many tools and languages. It includes support for build tools like Maven, Gradle, and SBT, as well as versioning tools as **git**. The **Community Edition** is free, but supports mostly only pure programming. Also the **Scala** Plugin is free. In contrary the **Ultimate Edition** is free only for universities, but includes support for many frameworks.

## Installation (with special Respect to Scala)

* Look at the IntelliJ IDEA download page https://www.jetbrains.com/idea/download and click on **Download** under **Community**, unless you need the ultimate variant. This will download a file named `ideaIC-2018.1.tar.gz`(on Linux) or newer.
* Check the SHA-256 checksum as indicated on the following page.
* Unpack the file to your prefered location. On Linux I usually take `/opt`. A directory `/opt/idea-IC-181.4203.550` or newer will be created.
* In my experience the newest IDEA version does not always support the newest version of the Scala Plugin. You should check the version compatibility table at the plugin page http://plugins.jetbrains.com/plugin/1347-scala 
  Here we can see, that the newest Scala Plugin version 2018.1 is compatible with the IDEA build versions 181-182, so it is OK.
* **Install JetBrains Plugins**: 
  a) Markdown Plugin: Goto File > Settings... > Plugins > Install JetBrains plugin... Scroll to *Markdown support* and click on *Install*.
  b) Scala Plugin: Goto File > Settings... > Plugins > Install JetBrains plugin... Scroll to *Scala* and click on *Install*.
  c) Click on *Restart IntelliJ IDEA*.
* On Linux create a Freedesktop.org starter entry: Copy the file [idea2018.1.desktop](idea2018.1.desktop) into directory `~/.local/share/applications` and edit it by a programming editor or by a Desktop Starter Editor. In this file you have to replace all references to IDEA versions by the current ones.
  Now you can start IntelliJ IDEA from the start Menu. 

