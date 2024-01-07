# DevOps

## Cloud Computing Basics

#### Vertiacal vs Horizontal Scaling

#### Vertical Scaling

Upgrading the machine (better hardware).

Hardwarecost rises exponentional to the added resources.

Low max throughput.

#### Horizontal Scaling

Adding new machines to increase througput.

Hardwarecost rises linear to the added resources.

Cheap common hardware can be used.

High max throughput.

### Advantages of the cloud

Add/Remove resources on demand.

No idling. Only pay for what you use.

Auto-Scaling groups.

### Public Cloud

The infrastructure can be used by the gerneral public and is owned and managed by an organization.

Advantages:
- no need to bother with hardware installation and maintenance.
- ready to use resources and high scalability

Disadvantages:
- Vendor lock-in
- Data ownership
- security not in own hands

### Private Cloud

The infrastracture is reserved for exclusive use by a single organization. It is owned and managed either by the organization themselfs or by a third party.

Advantages:
- Data is owned
- less vendor lock-in

Disadvantages:
- Higher upfront investment
- Complex deployment

### Community Cloud

The infrastructure is reserved for exclusive user of a specific community.

Advantages:
- Less vendor lock-in while also reducing investment costs

Disadvantages:
- Agreements between different organizations in a community can be difficult to negotiate.

### Hybrid Cloud

Any combination of public, private and community clouds.

Advantages:
- Advantages of different approaches can level out certain disadvantages

Disadvatages:
- added complexity

### Cloud Computing Service Models

#### SaaS - Software as a Service

The end user only interacts with the application.
Everything from hardware to app software is managed by the cloud provider.

(e.g.: Gmail, Dropbox, Google Docs)

#### FaaS - Function as a Service

Physical servers are not visible to the user. The user deploys the code on the cloud using a specific runtime.
When the code is run capacity and bandwithd are scaled automatically by the cloud provider.
The user pays on a per user basis not for servers with a specific capacity.

(e.g.: AWS Lambda)

#### PaaS - Platform as a Service

The cloud provider provides a platform which enables its users to run applications and manage data.
Everything from the hardware to the middleware is managed by the cloud provider.
The user is only responsible for the data and application.

#### IaaS - Infrastructure as a Service

The cloud provider is only responsible for the hardware.
Everything else including the operating system is part of the users responsibility.

#### Other service models

- CaaS : Container as a Service
- SaaS : Storage as a Service
- DaaS : Data as a Service
- Gaas : Cloud gaming