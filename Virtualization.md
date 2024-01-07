# DevOps

## Virtualization

### Virtualization Implementations

#### Full Virtualization

Everything is virtualized. (Con: increased latency)

#### Paravirtualization

OS is virtualization aware.

#### Hardware-assisted Virtualization

Hardware is virtualization aware.

### Hypervisor

#### Type 1 Hypervisors

"bare metal" hypervisors.
Runs directly on the hardware and guest OS run 1 level above the hypervisor.

#### Type 2 Hypervisors

Runs as an application on host OS.
Guest OS run above host OS and hypervisor.

## Data Center Storage

Storage needs to be redundant and always available.

### Redundant Array of Independant Disks (RAID)

Data loss prevention.

General summary: Data is stored on multiple disks. If one disk fails, data can be recovered from another disk.

### RAID 0 striping

Not fault tolerant.

Data is not duplicated. Its just stored on 2 seperate disks.

Only used for faster access.

### RAID 1 mirroring

fault tolerant.

Data is copied on multiple disks.

### RAID 5 parity

Data is striped on multiple (more than 2) disks.
It is not duplicated.
Alongside the data parity is stored.
Parity is used to recreate the data if dataloss occurs.

### Block vs File level storage

#### Block level storage

Data is written to and accessed from storage volumes.

DAS (Direct attached storage) : storage is attached to a server

#### File level storage

Data is written to disks and accessed from the file system.

NAS (Network attached storage) : connect to storage device through a network.
Appears to the client as a fileserver.

SAN (Storage area network) : clustered storage device which can be accessed through a network.
Appears to the client as a disk.

### Storage Provisioning

Thin Provisioning: allocates storage on demand

Thick Provisioning. pre-allocate a certain amount of storage