# AwsSchool
Welcome to Headstorm AWS School! This series focuses on learning the core elements of AWS, and building the 
necessary skills and intuition for both cloud platforms in general and AWS specific services.

## Learning AWS
AWS has tons of services, and it can be overwhelming when starting. Knowing where to look and what to look for
is one of the best things you can do to give yourself the best chance of success. AWS provides documentation about 
each of their services, including user guides, whitepapers, and blogs. These three resources will provide almost 
all the information that's available on a given service. If there are missing or poorly explained sections of AWS' 
documentation, you can actually open a pull request on [their public docs repo](https://github.com/awsdocs), check the
[AWS forums](https://forums.aws.amazon.com/index.jspa?categoryID=1), or check out stack overflow. However,
note that AWS services are changing and evloving constantly, and info on stack overflow may be dated or incorrect.

Once you are comfortable with the foundational services, it's highly recommended to read through the
[Well-Architected Framework](https://aws.amazon.com/architecture/well-architected/), and the whitepapers for 
each of the 5 pillars. These whitepapers give great insight into the design decisions at AWS, and the intended usages
of its services and key concerns like elasticity, availability, and durability.  

## Foundational Services
AWS is a huge platform, with dozens of services and products. Many of the products are specialized and designed 
to solve a niche problem, while other services are more general purpose. A key aspect of AWS' design is that every product at AWS is built on other AWS 
services. These services that are at the core of AWS are called *Foundational Services*.

The foundational services are:
* Amazon Elastic Compute Cloud (EC2) - "How can I get a machine to run software"
* Amazon Virtual Private Cloud (VPC) - "How can I get my compute resources on a network with traffic routed correctly"
* Amazon Simple Storage Service (S3) - "How can I persist data and access it from the internet"
* Amazon Elastic Block Store (EBS) - "How can I attach filesystems and volumes to compute resources"

Each of these foundational services will be covered in depth in their own sections. For now, we will stick to
a brief overview of what these services are and what they do.

#### EC2
EC2 is the service that supplies compute resources. AWS handles this with the concept of *instances*, which are 
essentially VMs that are managed by AWS. A single EC2 instance provides a virtual machine with a set amount of resources    
(CPU, RAM, Network bandwidth). We will skip over disk space for now, as disk and volumes are a large subject on their own 
within AWS. The core idea here is that anything within AWS that uses compute, i.e. any software that runs, is running 
on EC2.

#### VPC
Virtual Private Clouds are the networking services within AWS. A single VPC is roughly analagous to a data center.
Compute resources must deployed _within_ a VPC - they can't just exist in a void. The VPC service is a collection of 
networking tools and products that ultimately define network topology, and host things like firewalls and load balances for your resources.
  
#### S3
The Simple Storage Service (S3) is an object store. This services provides data persistence that can be accessed 
over the internet. On the surface it may look and feel like an SFTP server or filesystem, but it really is just a 
general purpose storage system that stores objects and metadata about those objects. An object can be anything - 
config files, images, jars, blobs, etc.

#### EBS  
Elastic Block Storage is block storage that can be attached to EC2 instances. This is different from S3, as EBS volumes
can function as filesystems and boot volumes for compute resources. EBS volumes are their own entities, and can
attached to multiple compute resources, detached, and reattached somewhere else. Their lifecycle is completely
independent of any compute resources they may be used with.


### Next Steps
More content will be added periodically.