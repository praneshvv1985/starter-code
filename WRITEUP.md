# Resource Justification

## Virtual Machine (VM)

### Cost
A Virtual Machine can be more expensive for this CMS application because the server must stay running continuously and requires payment for compute, storage, and networking resources. There can also be extra cost for maintenance and administration, since the developer is responsible for managing the operating system, updates, and security patches.

### Scalability
A VM can scale, but scaling usually requires more manual work. If traffic increases, additional VMs, load balancers, and configuration steps may be needed. This makes scaling slower and less convenient compared to a managed platform service.

### Availability
Availability on a VM depends on how the infrastructure is configured. To achieve higher availability, multiple VMs and additional failover or load balancing setup may be required. This increases complexity and requires more effort from the developer or administrator.

### Workflow
The workflow for a VM is more infrastructure-focused. The developer must create and manage the virtual machine, install dependencies, configure the runtime environment, secure the server, and maintain updates. This gives more control, but it also increases setup time and operational overhead.

## Azure App Service

### Cost
Azure App Service is generally more cost-effective for this type of web application because it is a managed service. It reduces the need to manage infrastructure directly, which saves both time and administrative effort. For a CMS app, App Service provides a good balance between price and convenience.

### Scalability
App Service provides built-in scaling options, making it easier to handle more traffic without major manual configuration. The application can be scaled up or out through Azure settings, which makes growth simpler and faster compared to managing multiple virtual machines.

### Availability
App Service offers strong availability because Microsoft manages the underlying infrastructure. It includes platform-managed reliability features, reducing the burden on the developer. This makes it a better choice for maintaining stable uptime for a web application like this CMS.

### Workflow
The workflow in App Service is simpler and more efficient for deployment. Code can be deployed directly from source control or deployment tools, and the platform manages the runtime, patches, and much of the infrastructure. This allows the developer to focus mainly on building and updating the application instead of managing servers.

## Chosen Solution

I chose **Azure App Service** for deploying this CMS application. It is better suited for a Python web application that needs quick deployment, easy management, and reliable hosting. App Service reduces infrastructure work while still providing scalability and availability, making it more practical than a Virtual Machine for this project.

App Service is also a better fit because this CMS application does not require deep operating system control or custom server-level configuration. Since the main goal is to deploy and manage a web app efficiently, App Service provides the best balance of simplicity, performance, and maintainability.

## What Changes Could Affect This Decision

My decision could change if the application required more control over the operating system, network configuration, or installed software. For example, if the CMS needed custom background services, special system packages, or advanced networking rules, then a Virtual Machine would become more suitable.

The decision might also change if the application had very specific security, compliance, or infrastructure requirements that App Service could not fully support. In that case, I would need a VM so I could control the full server environment, customize configurations, and manage the infrastructure in a more detailed way.
