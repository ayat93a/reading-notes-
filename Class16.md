# Serverless
Serverless is a cloud computing execution model that 

- Automatically provisions the computing resources required to run application code on demand, or in response to a specific event;
- Automatically scales those resources up or down in response to increased or decreased demand;
- Automatically scales resources to zero when the application stops running. 
- Serverless offloads all management responsibility for backend cloud infrastructure and operations tasks - provisioning, scheduling, scaling, patching and more - to the cloud provider. This gives developers more time to develop and optimize their front-end application code and business logic.\
 And with serverless, customers never pay for idle capacity.\
 They pay only for the resources required to run their applications, and only when those applications are running.

# Serverless pros and cons
## Pros
Serverless offers a number of individual technical and business benefits:
- As previously said, serverless allows development teams to concentrate on producing code rather than maintaining infrastructure. It provides developers a lot more time to experiment and improve the functionality and business logic of their front-end applications.
- As previously stated, serverless clients just pay for execution. The meter begins when the request is sent and ends when the request is completed. Compare this to the infrastructure as a service (IaaS) compute model, in which clients pay for virtual machines (VMs) and other resources needed to run applications from the time they are provisioned until they are expressly decommissioned.
- Serverless is a polyglot environment that allows developers to code in whatever language or framework they're familiar with, such as Java, Python, or Node.js.
- Because developers don't have to explain infrastructure needed to integrate, test, distribute, and deploy code builds into production, Serverless streamlines deployment and, in a broader sense, DevOps processes.
Serverless computing can be quicker and more cost-effective than conventional kinds of computing for certain workloads, such as those that demand parallel processing.
- Serverless application development solutions offer near-total insight into system and user timings, as well as the ability to systematically aggregate such data.

## Cons
With so much to like about serverless computing, organizations are using it for a wide variety of applications . However, there are certain applications for which serverless is not favorable, or which present technical and business trade-offs to consider:
- Serverless delivers considerable cost reductions for spiky workloads due to its ability to scale up and down on demand in response to workload. However, it may not provide the same cost reductions for workloads that are predictable, stable, or long-running; in these circumstances, a traditional server infrastructure may be more straightforward and cost-effective.
- Starts with a cold: Because serverless architectures avoid long-running processes in favor of scaling up and down to zero, they must occasionally restart from the beginning to service a new request. This starting delay isn't obvious or harmful to consumers in some apps. However, for other applications, such as financial trading applications, the latency is intolerable.
- Monitoring and debugging are difficult in any distributed system, but moving to a serverless design (or microservices architecture, or a hybrid of the two) simply adds to the difficulty. For example, using existing tools or methods, teams may find it difficult or impossible to monitor or debug serverless operations.
- Serverless architectures are built to take advantage of a managed cloud environment and, in terms of architectural models, go the furthest in decoupling a workload from something more portable, such as a virtual machine (VM) or Docker container. Much of the value of cloud may be discovered for certain firms by tightly integrating with the native managed services of a single cloud platform; for others, cloud can lead to significant lock-in.