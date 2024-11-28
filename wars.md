# Intro to WAR Files

**Definition:** WAR (.war) files are web app archives. A .war is a special kind of [JAR file](README.md) that can distribute XML files, tag libraries, static webpages,
Java classes, Java Servlets, and JavaServer pages. These resources, when integrated and implemented together, are considered a web application.

**Advantages of WARs:**

* Versions of deployed apps can be simply identified.
* .war files can be digitally signed just like .jar files, making identification of the origin of source code easy.
* Web apps can be tested and deployed (even in multiple environments) quickly and efficiently.
* .war files are supported by all Java EE containers.
* [Model-View-Controller](https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller) software design can be easily adhered to.

**A Disadvantage of WARs:**

* Source code modifications require WARa to be repackaged and redeployed.
* .war structure/infrastructure may be overextensive, depending on app requirements.

**On the importance of web.xml files:**

* A file called 'web.xml' is located within an /WEB-INF directory of each .war file (with some exceptions).
  + If an app only serves JSPs, a web.xml file is not required.
  + Otherwise, the structure of the .war's web app is defined within this file.
    - A web.xml file informs a servlet container as to which particular servlet a URL request is meant be routed.
      + This is important because the servlet container is responsible for providing deployed services.
    - A web.xml file defines context variables and environmental dependencies, to be referenced within servlets.
