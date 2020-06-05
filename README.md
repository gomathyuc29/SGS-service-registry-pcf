# ascend-service-registry-pcf
ascend-service-registry-pcf

The two projects ConsumerService and ProducerService were registered with a service registry in PCF.Interprocess communication was established between the two applications through service registry.

Please note:
1)Both the services should have the starter dependency for hosting them as Eureka clients under Pivotal.Search for Pivotal in the dependency search tab in Spring Initializr and chose Service Registry.
2)By default,security will be configured when this dependency is added. So to disable the same, write a configuration class where we permit all the requests to the application without authorization.
3)@LoadBalanced annotation is mandatory as was running to a weird error.https://stackoverflow.com/questions/38310904/java-net-unknownhostexception-during-eureka-service-discovery.
4)manifest.yml will have details of PCF configuration whereas Jenkins.file has commands to automate the build and deploy process.
