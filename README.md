# dockercon

![Alt text](https://github.com/darrinsolomon/dockercon/blob/master/demo.png?raw=true "dockercon_demo")

<B>Story Line</B>

Our fictional company has decided to leverage the benefits of Docker EE and MuleSoft Anypoint Platform to build out a new microservice architecture for their ecommerce order placement business process.  They want to build a microservice architecture leveraging the API-Led Connectivity (ALC) Approach, and they decide to build three domain objects- 1) ‘Orders’, a system that will contain the actual order 2) ‘Product’, a system that contains all products in inventory 3) ‘placeOrder’, an orchestration business process to orchestrate the restful calls and to place the Order on a message queue.  They will also create an Experience API for a mobile experience which will reuse all of the objects built to create the business processes as well as leverage reusable traits specific for this experience.  This organization believes in polyglot development processes, and decide to build some microservices in Mule and some in Docker Desktop.  Somewhere along their journey, the company acquires a much smaller company (retail petstore).  They don’t want to distract from their ALC initiative but they do want to bring the acquired company’s inventory data into the placeOrder process they are building.  They need to also make sure that the small company assets are discoverable, managed and secure.

<B>Scenarios – What to show</B>

1) First a contract will be defined for all of the objects.  We begin discovery of assets using the Anypoint Exchange, and discover Catalyst Accelerator for Retail.  We leverage that asset to customize the RAML’s for the System, Process, and Experience API’s.
2) We leverage the Mocking service to begin coding the Mobile Application
3) We leverage Docker Desktop to build out the implementation of the Docker services
4) We use Jenkins pipeline to deploy the proxy Mules API gateways for Orders and products, and the Mules for placeOrder and the experience API
5) We build a SOAP to REST mule for the retail petstore and check that into GitHub
6) We build a new flow to aggregate the petstore inventory with the original product object and check that into GitHub
7) We use Jenkins pipeline to deploy those updates
8) We use API Manager to layer security and other policy

<B>Platform capabilities to discuss in use case context</B>

Microservices are onboarded to Anypoint embracing polyglot development.  
API Contracts built with domain design with bounded contexts
Independently deployable and scalable leveraging object stores, MQ
Gateway patterns and security (zero trust) is layered across the ALC 
DevOps friendly using deployment pipelines, unit testing, etc
Full Observability across heterogeneous application network (monitoring telemetry) via API Visualizer
Monitoring of the Application Network through Anypoint Monitoring
Synthetic testing done through Anypoint Functional Monitoring
Autoscaling and other microservices patterns (bounded contexts, independent deployability)
