# Mingle
A python interface and schedule engine

## Concept
What if we had a healthcare interface engine that took the Apple mentality. That is, not to be capable of anything but to excel in what we do and what is needed.

Defining what is needed is hard to do on a global scale so perhaps the framework should be extensible. 

Lets try to establish some ideals:
* Open source so that companies and see and contribute to the base product
* Robust language that users can easily learn but is performant and natively server side
* Only web interface that can be local to an install or manage multiple installs
* Streamline connectors to allow extensibility but package functionality into common types
* File based configurations and common functions for customization and transparency
* Things like port managment and reporting built in
* Connector/Code environment promotion with source control tools such as storage/merge/compare
* Deliniation between inbound and outbound connectors
* Global view with filtering as needed
* One SIMPLE way to do anything, more methods doesnt make things easier
* Easily take a production scenario and test with customizations
* Not excelling in one area more than another (hl7 vs x12)
* Not aim to allow non-developers ability to maintain the system
* Small, portable, an os
* Archiving configurable and built in but extensible
* Reporting out the wazoo
* Schedule based processing (ala cron/windows scheduler - ex ftp, db, script, web service client, directory scanning)
* Realtime processing (tcp/ip, directory watching, web service server)
* No global modifications so that multiple vcersions have absolutely no issue residing on the same server
* Client gui should be web based and compatible with any server version
* Tools, tools, tools, oh, and reports - Things like script execution times, and the ability to play in a playground are crucial to fast and reliable development


## How could this be accomplished
I think this could be accomplished rather easily and incrementally with building a completely text file configuration and services that act upon those configurations. You could build the first and crucial aspects on an engine and have a crude method for configuring. Next you embed apache and build an api layer for configuring, monitoring, and process managment. Lastly you build a front end that is optionally deployed and serverd through the same embeded apache. This front end can be configured to look locally or at any server instance. These instances and thier api would therefore require port configureation so that each instance is groovy. 

## Getting Real
Before any real work could be completed we would need to compile a list of examples on how things are accomplished in python. This would then be compiled into a 0.1 version to test


Embedable Apache:
http://felix.apache.org/documentation/subprojects/apache-felix-framework/apache-felix-framework-launching-and-embedding.html

Python To C++:
http://stackoverflow.com/questions/672857/is-python-slower-than-java-c

Python Socket:
http://stackoverflow.com/questions/18971777/python-socket-server-client-programming
