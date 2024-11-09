# intro-to-jar-files
**Definition:** JAR files are compressed Java archive (hence the extension '.jar') files, used to bundle more than one Java-related file together for unpacking and distribution.  

Advantages of .jar files include the following:  

| Advantage | Explanation |  
| --- | --- |   
| Accessible File Information | Information about archived files, such as versioning and vendor details, can be stored conveniently. |  
| Applet Portability | .jar files are handled by the Java API, enabling compatibility in many software and hardware setups. |
| Data Compression | Java-related files can be compressed to simplify storage and enable convenient unpacking for usage. |  
| Extension Packaging | Turns apps into extensions and adds functonality to core Java. |
| Faster Downloads | Only one HTTP transaction (one connection) is necessary for Java applet class files (and related resources) to be sent to a web browser. |
| Pacakage Sealing | By assuring that all classes in a package are included within a .jar file, version consistency can be sustained. |
| Secure Digital Signatures | .jar files can be trusted with permissions based on utilizing these as a security mechanism. | 

Common jar command uses:

| Command | Explanation |
| --- | --- |
| jar cf example-jar example-input-file | Creates a .jar. (Multiple input files can be specified.) |
| jar tf example-jar | Displays contents of a .jar. |
| jar xf example-jar specified-file | Extracts specified files from a .jar. (Multiple files can be specified.) |
| jar xf example-jar | Extracts all contents of a .jar. |
| java -jar app.jar | Runs a .jar applet, using the manifest header of the Main-Class. |

Examples of APIs that integrate JAR files include:  

| API | Explanation |
| --- | --- |
| java.net.JarURLConnection *(class)* | Provides URL connections to read JAR files (or entries within JAR files). |
| java.net.URLClassLoader *(class)* | Loads resources from URL search paths associated with JAR files/directories. |
| java.util.jar *(package)* | Contains classes for reading and writing JAR files. |

TODO #1: Outline the basics of .jar files.  
TODO #2: Explain how manifest files work.  
TODO #3: Provide an overview of .jar file signatures.  
