Minimal launchpad update test
---

To verify that in-place launchpad updates work ( or not ):

* build the project using `mvn clean package`
* run the launchpad using `java -jar target/launchpad-update-test-0.0.1-SNAPSHOT.jar` and wait for the installation to complete
* stop the launchpad process
* uncomment the org.freemarker:freemarker bundle from list.xml
* build the project using `mvn clean package`
* run the launchpad using `java -jar target/launchpad-update-test-0.0.1-SNAPSHOT.jar` and wait for the installation to complete

The test is successful is the freemarker bundle is present in the newly-launched launchpad.
