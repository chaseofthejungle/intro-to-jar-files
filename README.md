# Intro to JAR Files
**Definition:** JAR files are compressed Java archives (hence the extension '.jar'). These are bundles of Java-related files, assembled as Java archives. JAR files are convenient for unpacking and distributing Java web applets. 

Advantages of .jar files include the following:
<br /><br />
| Advantage | Explanation |  
| --- | --- |   
| **Accessible File Information** | Information about archived files, such as versioning and vendor details, can be stored conveniently. |  
| **Applet Portability** | .jar files are handled by the Java API, enabling compatibility in many software and hardware setups. |
| **Data Compression** | Java-related files can be compressed to simplify storage and enable convenient unpacking for usage. |  
| **Extension Packaging** | Turns apps into extensions and adds functonality to core Java. |
| **Faster Downloads** | Only one HTTP transaction (one connection) is necessary for Java applet class files (and related resources) to be sent to a web browser. |
| **Package Sealing** | By assuring that all classes in a package are included within a .jar file, version consistency can be sustained. |
| **Secure Digital Signatures** | These provide .jar files with trustworthiness. A .jar file can be signed with a private key, and a public key can be placed within the .jar for signature verification. |  

<br /><br />
**How to use .jar files:**  The Java Development Kit ('JDK') contains a Java Archive Tool for accomplishing .jar file tasks. To use this tool, you would use the `jar` command.

<br /><br />
Some common uses of the jar command ('jar tool'):
<br /><br />
| Usage | Explanation |
| --- | --- |
| **jar cf example-jar example-input-file** | Creates a .jar. *(Multiple input files can be specified.)* |
| **jar tf example-jar** | Displays contents of a .jar. |
| **jar xf example-jar specified-file** | Extracts specified files from a .jar. *(Multiple files can be specified.)* |
| **jar xf example-jar** | Extracts all contents of a .jar. |
| **jar uf example-jar example-input-file** | Updates JAR file contents *(Multiple input files can be specified. Alternatively, can update the manifest directly.)* |
| **java -jar app.jar** | Runs a .jar applet, using the manifest header of the Main-Class. |

<br /><br />
And, similarly, for the jarsigner command...  

| Usage | Explanation |
| --- | --- |
| **jarsigner -verify jar-file**| Verifies the signature of a .jar file. |

<br /><br />
How a .jar file should be ran depends on whether it: a) contains an applet for execution inside of a web browser, b) contains an app for command line execution, *or* c) contains code for usage as an extension.
  
<br /><br />
[Manifest files](/manifests.md) contain essential data about the files packaged within JARs. This 'metadata' includes dependencies with other JAR files, versioning and security information (such as electronic signing), and other important values related to identification and the various advantages associated with .jar files.
  
Upon creation of a JAR, a default manifest file is generated with a pathname of `META-INF/MANIFEST.MF`. Only one manifest file is permitted per JAR.

<br /><br />
Examples of APIs that integrate JAR files include:  
<br /><br />
| API | Explanation |
| --- | --- |
| **java.net.JarURLConnection** *(class)* | Provides URL connections to read JAR files (or entries within JAR files). |
| **java.net.URLClassLoader** *(class)* | Loads resources from URL search paths associated with JAR files/directories. |
| **java.util.jar** *(package)* | Contains classes for reading and writing JAR files. |

<br /><br />
**A note on WAR files:**  
  
[WAR (.war)](/wars.md) files are web app archives. A .war is a special kind of JAR that can distribute XML files, tag libraries, static webpages, Java classes, Java Servlets, and JavaServer pages. These resources, when integrated and implemented together, are considered a web application.

TODO #1: Create and link to text files (all 6 commands from the jar command table and the 1 from the jarsigner command table) outlining options for various command usages.  
TODO #2: Add details to manifests.md, including how to set app entry point and package version metadata, add classes to the classpath, and package seal and enhance security.  
