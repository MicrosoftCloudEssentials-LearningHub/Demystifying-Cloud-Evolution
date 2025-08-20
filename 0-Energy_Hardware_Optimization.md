## Additional Important Technologies

<details>
  <summary><b>Networking & Storage Innovations</b></summary>

  ### Key Developments
  - **TCP/IP (1983)**
    - **Developers**: Vint Cerf and Bob Kahn
    - **Technical innovation**: Layered network protocols with end-to-end connectivity
    - **Impact**: Unified diverse networks into a single internetwork

  - **Ethernet Evolution**
    - **1980**: 10 Mbps shared media
    - **1995**: 100 Mbps Fast Ethernet
    - **1998**: 1 Gbps
    - **2002**: 10 Gbps
    - **2010+**: 40/100/400 Gbps

  - **Storage Area Networks (SANs)**
    - **Fibre Channel (1997)**: High-speed network technology specifically for storage
    - **iSCSI (2003)**: Storage protocol over TCP/IP networks
    - **Technical impact**: Separated storage from servers, enabled consolidation

  - **Software-Defined Networking (2011+)**
    - **OpenFlow**: Protocol separating control and data planes
    - **Technical architecture**: Centralized controllers, programmable forwarding
    - **Impact**: Enabled network automation, microsegmentation, policy-based control

  - **SR-IOV/RDMA**
    - **SR-IOV (Single Root I/O Virtualization)**: Hardware-assisted network virtualization
    - **RDMA (Remote Direct Memory Access)**: Network transfers without CPU involvement
    - **Energy efficiency**: Reduced CPU cycles per packet/transfer
    - **Performance**: Lower latency, higher throughput per watt
</details>

<details>
  <summary><b>Programming Models & Languages Evolution</b></summary>

  ### Key Developments
  - **Assembly Language (1950s)**
    - **Technical nature**: Human-readable mnemonics for machine code
    - **Impact**: First abstraction from raw binary programming

  - **High-level Languages**
    - **FORTRAN (1957)**: Scientific computing focus
    - **COBOL (1959)**: Business applications
    - **C (1972)**: Systems programming
    - **Impact**: Improved programmer productivity, code portability

  - **Object-Oriented Programming**
    - **Smalltalk (1972)**: First pure OOP language
    - **C++ (1985)**: Added OOP to C
    - **Java (1995)**: Platform independence with JVM
    - **Technical impact**: Encapsulation, inheritance, polymorphism

  - **Web Programming**
    - **JavaScript (1995)**: Client-side web programming
    - **PHP (1994), Ruby on Rails (2004)**: Server-side frameworks
    - **Node.js (2009)**: JavaScript on server-side
    - **Impact**: Enabled rich web applications

  - **Cloud-Native Programming Models**
    - **Reactive programming**: Handling asynchronous data streams
    - **Functional programming**: Immutable data, higher-order functions
    - **Infrastructure as Code**: Terraform, ARM templates, CloudFormation
    - **Technical impact**: Better aligned with distributed, elastic systems
</details>

<details>
  <summary><b>Database & Data Storage Evolution</b></summary>

  ### Key Developments
  - **Hierarchical Databases (1960s)**
    - **Example**: IBM's IMS
    - **Technical structure**: Tree-based data model
    - **Limitations**: Complex relationships required redundant data

  - **Relational Databases (1970s)**
    - **Edgar F. Codd**: Defined relational model at IBM
    - **SQL**: Standardized query language
    - **Technical innovations**: ACID transactions, normalized data
    - **Products**: Oracle, DB2, MySQL, SQL Server

  - **NoSQL Movement (2000s)**
    - **Types**: Document (MongoDB), Key-Value (Redis), Column (Cassandra), Graph (Neo4j)
    - **Technical drivers**: Scale-out architecture, schema flexibility
    - **CAP theorem**: Trade-offs between consistency, availability, partition tolerance
    - **Impact**: Enabled web-scale data storage

  - **NewSQL & Distributed SQL (2010s)**
    - **Examples**: Google Spanner, CockroachDB, Azure Cosmos DB
    - **Technical approach**: Distributed SQL systems with ACID guarantees
    - **Innovation**: Global distribution with consistency controls
    - **Impact**: Combined SQL familiarity with cloud-native scaling
</details>

<details>
  <summary><b>Security & Governance Evolution</b></summary>

  ### Key Developments
  - **Encryption Evolution**
    - **DES (1977)**: Early symmetric encryption standard
    - **RSA (1977)**: Public-key cryptography
    - **SSL/TLS**: Secured web communications
    - **Technical impact**: Enabled secure communication over public networks

  - **Identity & Access Management**
    - **LDAP (1993)**: Directory services protocol
    - **SAML (2002), OAuth (2010), OpenID Connect (2014)**: Federation standards
    - **Technical evolution**: From local accounts to federated identity

  - **Cloud Security Models**
    - **Shared responsibility model**: Dividing security duties between provider and customer
    - **Zero Trust**: "Never trust, always verify" approach
    - **Technical implementations**: Microsegmentation, JIT/JEA access, continuous verification
    - **Impact**: Adapted security for perimeter-less environments

  - **Regulatory Evolution**
    - **SOX (2002)**: Financial controls and reporting
    - **PCI DSS (2004)**: Payment card security
    - **GDPR (2016)**: Data protection and privacy
    - **Impact**: Formalized compliance requirements for systems
</details>

<details>
  <summary><b>DevOps & Operational Evolution</b></summary>

  ### Key Developments
  - **Agile Movement (2001)**
    - **Key innovation**: Iterative development with frequent feedback
    - **Technical practices**: Continuous integration, test automation
    - **Impact**: Shorter development cycles, improved adaptability

  - **DevOps (2009+)**
    - **Key principles**: Culture, automation, measurement, sharing
    - **Technical practices**: CI/CD pipelines, infrastructure as code
    - **Tools**: Jenkins, Git, Ansible, Terraform
    - **Impact**: Broke down silos between development and operations

  - **SRE (Site Reliability Engineering)**
    - **Origin**: Google approach to operations at scale
    - **Technical practices**: Error budgets, toil reduction, automation
    - **Key metrics**: SLIs, SLOs, SLAs
    - **Impact**: Applied software engineering to operational problems

  - **GitOps (2017+)**
    - **Technical approach**: Git repositories as source of truth for infrastructure
    - **Key components**: Declarative configurations, automated reconciliation
    - **Tools**: Flux, ArgoCD, Crossplane
    - **Impact**: Auditable, repeatable infrastructure management
</details>

## Azure Cloud Architecture

<details>
  <summary><b>Azure Service Delivery Layers</b></summary>

  ### Physical Infrastructure
  - **Regions & Availability Zones**
    - **Design**: Physically separate datacenters with independent power, cooling, networking
    - **Fault domains**: Isolation boundaries for hardware failures
    - **Technical implementation**: Dedicated dark fiber connections between zones

  - **Network Infrastructure**
    - **Global backbone**: Microsoft's private fiber network
    - **Software-Defined Networking**: Programmable network fabric
    - **ExpressRoute**: Dedicated private connections to Azure

  ### Core Platform
  - **Azure Resource Manager (ARM)**
    - **Technical role**: Control plane for all Azure resources
    - **Key concepts**: Resource providers, resource groups, RBAC
    - **Declarative model**: JSON/Bicep templates define desired state

  - **Virtualization Stack**
    - **Hypervisor**: Hyper-V based virtualization
    - **Storage virtualization**: Blob, disk, file abstractions
    - **Network virtualization**: Virtual networks, NSGs, UDRs

  ### Service Orchestration
  - **Compute Services**
    - **VMs**: IaaS offering with full control
    - **App Service**: PaaS with managed runtime environments
    - **Azure Kubernetes Service**: Managed Kubernetes control plane
    - **Azure Functions**: Event-driven serverless compute

  - **Storage & Databases**
    - **Storage accounts**: Blob, file, queue, table
    - **SQL databases**: Azure SQL DB, PostgreSQL, MySQL
    - **NoSQL options**: Cosmos DB (multi-model)
    - **Caching**: Redis Cache

  ### Integration & Connectivity
  - **Messaging Services**
    - **Service Bus**: Enterprise messaging
    - **Event Grid**: Event routing
    - **Event Hubs**: Big data streaming
    - **Storage Queues**: Simple queuing

  - **API Management**
    - **Gateway**: Request routing, transformation
    - **Developer portal**: Documentation, subscription management
    - **Policies**: Security, caching, transformation

  ### Security & Governance
  - **Azure Entra ID (formerly Azure AD)**
    - **Identity services**: Authentication, SSO, conditional access
    - **B2B/B2C**: External identity collaboration

  - **Azure Policy & Blueprints**
    - **Policy definitions**: Governance rules
    - **Initiatives**: Policy groups
    - **Blueprints**: Environment templates with policies
</details>

## Practical Implementation Examples

<details>
  <summary><b>Energy-Efficient Cloud Design Patterns</b></summary>

  ### Architectural Approaches
  - **Scale-to-zero pattern**
    - **Technique**: Automatically scale down to zero instances when not in use
    - **Implementation**: Azure Functions consumption plan, AKS with KEDA
    - **Impact**: Eliminates idle resource consumption

  - **Compute-storage proximity**
    - **Technique**: Place computation close to data
    - **Implementation**: Azure Blob near compute, Redis caching
    - **Impact**: Reduces network traffic, lowers latency

  - **Right-sizing resources**
    - **Technique**: Match resource allocation to actual needs
    - **Implementation**: VM rightsizing, autoscaling, burstable instances
    - **Impact**: Eliminates waste from overprovisioning

  ### Code Examples
  ```powershell
  # Azure PowerShell example for scheduling VM shutdown during off-hours
  $automationAccountName = "energy-optimization"
  $resourceGroupName = "production-rg"
  
  # Create automation account
  New-AzAutomationAccount -Name $automationAccountName `
                          -ResourceGroupName $resourceGroupName `
                          -Location "EastUS"
  
  # Import runbook
  $runbookUri = "https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/quickstarts/microsoft.automation/automation-schedule-source-control-jobs/scripts/Stop-AzureVMs.ps1"
  Import-AzAutomationRunbook -AutomationAccountName $automationAccountName `
                           -ResourceGroupName $resourceGroupName `
                           -Name "StopVMsOffHours" `
                           -Type PowerShell `
                           -Uri $runbookUri
  
  # Create schedule (stop VMs at 7PM weekdays)
  $schedule = New-AzAutomationSchedule -AutomationAccountName $automationAccountName `
                                     -ResourceGroupName $resourceGroupName `
                                     -Name "WeekdayEvening" `
                                     -StartTime "19:00" `
                                     -DaysOfWeek Monday,Tuesday,Wednesday,Thursday,Friday `
                                     -WeekInterval 1
  
  # Link runbook to schedule
  Register-AzAutomationScheduledRunbook -AutomationAccountName $automationAccountName `
                                       -ResourceGroupName $resourceGroupName `
                                       -RunbookName "StopVMsOffHours" `
                                       -ScheduleName "WeekdayEvening"
  ```

  ### Monitoring for Energy Efficiency
  ```yaml
  # Example Azure Monitor query to identify underutilized VMs
  Perf
  | where ObjectName == "Processor" and CounterName == "% Processor Time"
  | summarize AvgCPU = avg(CounterValue) by Computer
  | where AvgCPU < 10
  | join (
      Perf
      | where ObjectName == "Memory" and CounterName == "% Committed Bytes In Use"
      | summarize AvgMem = avg(CounterValue) by Computer
  ) on Computer
  | where AvgMem < 40
  | project Computer, AvgCPU, AvgMem, 
           Recommendation = "Consider downsizing this VM to reduce cost and energy"
  ```
</details>

<details>
  <summary><b>Kubernetes Orchestration Patterns</b></summary>

  ### Key Orchestration Concepts
  - **Declarative configuration**
    - **Technique**: Define desired state, let controllers reconcile
    - **Implementation**: Kubernetes manifests, Helm charts, Kustomize
    - **Benefits**: Consistency, repeatability, auditability

  - **Pod resource management**
    - **Technique**: Define requests and limits appropriately
    - **Implementation**: CPU/memory settings in pod specs
    - **Impact**: Better scheduling decisions, higher cluster utilization

  - **Autoscaling strategies**
    - **HPA (Horizontal Pod Autoscaler)**: Scale replicas based on metrics
    - **VPA (Vertical Pod Autoscaler)**: Adjust resource requests
    - **Cluster Autoscaler**: Add/remove nodes as needed
    - **KEDA**: Event-driven autoscaling

  ### Implementation Examples
  ```yaml
  # Example Kubernetes deployment with autoscaling and resource settings
  apiVersion: apps/v1
  kind: Deployment
  metadata:
    name: efficient-app
  spec:
    replicas: 2
    selector:
      matchLabels:
        app: efficient-app
    template:
      metadata:
        labels:
          app: efficient-app
      spec:
        containers:
        - name: app
          image: myregistry.azurecr.io/efficient-app:v1
          resources:
            requests:
              cpu: 100m
              memory: 128Mi
            limits:
              cpu: 500m
              memory: 256Mi
          readinessProbe:
            httpGet:
              path: /healthz
              port: 8080
            initialDelaySeconds: 5
            periodSeconds: 10
  ---
  apiVersion: autoscaling/v2
  kind: HorizontalPodAutoscaler
  metadata:
    name: efficient-app-hpa
  spec:
    scaleTargetRef:
      apiVersion: apps/v1
      kind: Deployment
      name: efficient-app
    minReplicas: 2
    maxReplicas: 10
    metrics:
    - type: Resource
      resource:
        name: cpu
        target:
          type: Utilization
          averageUtilization: 60
    - type: Resource
      resource:
        name: memory
        target:
          type: Utilization
          averageUtilization: 70
  ```

  ### Practical Tips for Efficient Orchestration
  - Schedule pod anti-affinity to spread workloads across nodes
  - Use pod topology spread constraints for multi-zone resilience
  - Implement node taints/tolerations to direct specialized workloads to appropriate hardware
  - Set up pod disruption budgets to maintain availability during updates
  - Use node selectors for workloads with specific hardware requirements (GPUs, SSD storage)
</details>

<details>
  <summary><b>Azure Cloud-Native Implementation</b></summary>

  ### Azure Kubernetes Service (AKS)
  - **Architecture best practices**
    - Use managed identity for cluster authentication
    - Implement network policies for pod-to-pod communication
    - Enable Azure CNI for advanced networking features
    - Consider AKS virtual nodes for burst scenarios

  - **AKS deployment example**
    ```bash
    # Create a resource group
    az group create --name myAKSGroup --location eastus
    
    # Create AKS cluster with energy-efficient features
    az aks create \
      --resource-group myAKSGroup \
      --name myAKSCluster \
      --node-count 3 \
      --enable-cluster-autoscaler \
      --min-count 1 \
      --max-count 5 \
      --enable-managed-identity \
      --network-plugin azure \
      --network-policy calico \
      --node-vm-size Standard_D4s_v3
    
    # Enable AKS node auto-shutdown to save energy in dev/test environments
    az vm auto-shutdown -g MC_myAKSGroup_myAKSCluster_eastus \
      --name aks-nodepool1-12345678-0 \
      --time 1900
    ```

  ### Serverless Computing with Azure Functions
  - **Event-driven, auto-scaling architecture**
    - Only runs when triggered (consumption plan)
    - Scales based on event queue length
    - Reduces energy usage compared to always-on services

  - **Function implementation example**
    ```csharp
    // Azure Function that processes messages efficiently
    public static class EnergyEfficientFunction
    {
        [FunctionName("ProcessQueueMessage")]
        public static async Task Run(
            [ServiceBusTrigger("myqueue", Connection = "ServiceBusConnection")] string myQueueItem,
            [CosmosDB(
                databaseName: "mydb",
                containerName: "mycoll",
                Connection = "CosmosDBConnection")]
                DocumentClient client,
            ILogger log)
        {
            log.LogInformation($"Processing message: {myQueueItem}");
            
            // Process in batches where possible to reduce connection overhead
            var documents = JsonConvert.DeserializeObject<List<Document>>(myQueueItem);
            
            // Use bulk operations for efficiency
            var tasks = documents.Select(doc => client.UpsertDocumentAsync(
                UriFactory.CreateDocumentCollectionUri("mydb", "mycoll"),
                doc));
                
            await Task.WhenAll(tasks);
        }
    }
    ```

  ### Azure App Service with Efficient Scaling
  - **Scaling configuration**
    ```json
    {
      "name": "autoscalesetting",
      "properties": {
        "profiles": [
          {
            "name": "Auto scale profile",
            "capacity": {
              "minimum": "1",
              "maximum": "10",
              "default": "1"
            },
            "rules": [
              {
                "metricTrigger": {
                  "metricName": "CpuPercentage",
                  "metricResourceUri": "/subscriptions/{subscription-id}/resourceGroups/{resource-group}/providers/Microsoft.Web/serverFarms/{app-service-plan}",
                  "timeGrain": "PT1M",
                  "statistic": "Average",
                  "timeWindow": "PT10M",
                  "timeAggregation": "Average",
                  "operator": "GreaterThan",
                  "threshold": 70
                },
                "scaleAction": {
                  "direction": "Increase",
                  "type": "ChangeCount",
                  "value": "1",
                  "cooldown": "PT5M"
                }
              },
              {
                "metricTrigger": {
                  "metricName": "CpuPercentage",
                  "metricResourceUri": "/subscriptions/{subscription-id}/resourceGroups/{resource-group}/providers/Microsoft.Web/serverFarms/{app-service-plan}",
                  "timeGrain": "PT1M",
                  "statistic": "Average",
                  "timeWindow": "PT10M",
                  "timeAggregation": "Average",
                  "operator": "LessThan",
                  "threshold": 30
                },
                "scaleAction": {
                  "direction": "Decrease",
                  "type": "ChangeCount",
                  "value": "1",
                  "cooldown": "PT5M"
                }
              }
            ]
          }
        ]
      }
    }
    ```
</details>

<details>
  <summary><b>Advanced Governance & Policy Implementation</b></summary>

  ### Azure Policy Implementation
  - **Energy efficiency policies**
    - Enforce VM SKUs with higher perf-per-watt
    - Require auto-shutdown on dev/test resources
    - Mandate storage tiering for infrequently accessed data

  ```json
  {
    "properties": {
      "displayName": "Require auto-shutdown for non-production VMs",
      "policyType": "Custom",
      "mode": "All",
      "description": "This policy ensures non-production VMs have auto-shutdown configured",
      "parameters": {},
      "policyRule": {
        "if": {
          "allOf": [
            {
              "field": "type",
              "equals": "Microsoft.Compute/virtualMachines"
            },
            {
              "field": "tags['environment']",
              "in": ["dev", "test", "qa"]
            }
          ]
        },
        "then": {
          "effect": "deployIfNotExists",
          "details": {
            "type": "Microsoft.DevTestLab/schedules",
            "deploymentScope": "resourceGroup",
            "existenceScope": "resourceGroup",
            "existenceCondition": {
              "field": "name",
              "like": "shutdown-computevm-*"
            },
            "roleDefinitionIds": [
              "/providers/Microsoft.Authorization/roleDefinitions/b24988ac-6180-42a0-ab88-20f7382dd24c"
            ],
            "deployment": {
              "properties": {
                "mode": "incremental",
                "template": {
                  "$schema": "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#",
                  "contentVersion": "1.0.0.0",
                  "parameters": {
                    "vmName": { "type": "string" }
                  },
                  "resources": [
                    {
                      "type": "Microsoft.DevTestLab/schedules",
                      "name": "[concat('shutdown-computevm-', parameters('vmName'))]",
                      "apiVersion": "2018-09-15",
                      "location": "[resourceGroup().location]",
                      "properties": {
                        "status": "Enabled",
                        "taskType": "ComputeVmShutdownTask",
                        "dailyRecurrence": {
                          "time": "1900"
                        },
                        "timeZoneId": "UTC",
                        "targetResourceId": "[resourceId('Microsoft.Compute/virtualMachines', parameters('vmName'))]"
                      }
                    }
                  ]
                },
                "parameters": {
                  "vmName": {
                    "value": "[field('name')]"
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  ```

  ### Comprehensive Governance Framework
  - **Management Groups structure**
    - Top-level policies for org-wide standards
    - Environment-specific policies (prod, dev, test)
    - Workload-specific optimizations

  - **Resource tagging strategy**
    - Ownership and cost allocation
    - Environment classification
    - Energy efficiency targets
    - Shutdown/startup schedule eligibility

  - **Implementation example with Azure CLI**
    ```bash
    # Create a policy initiative for energy efficiency
    az policy set-definition create \
      --name 'energy-efficient-compute' \
      --display-name 'Energy Efficient Computing Standards' \
      --description 'Set of policies to ensure energy efficient resource usage' \
      --definitions '[
        {"policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/custom-vm-shutdown"},
        {"policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/custom-storage-lifecycle"},
        {"policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/custom-compute-rightsize"}
      ]'
    
    # Assign to management group
    az policy assignment create \
      --name 'enforce-energy-efficiency' \
      --scope '/providers/Microsoft.Management/managementGroups/development' \
      --policy-set-definition 'energy-efficient-compute'
    ```
</details>

## Further Research and Resources

<details>
  <summary><b>List of References</b></summary>

- [Azure Architecture Center](https://learn.microsoft.com/azure/architecture/)
- [Azure Resource Manager & Bicep](https://learn.microsoft.com/azure/azure-resource-manager/)
- [Azure Well-Architected (cost, reliability, ops)](https://learn.microsoft.com/azure/well-architected/)
- [CNCF (Cloud Native Computing Foundation) Kubernetes Docs](https://kubernetes.io/docs/)
- [Linux Foundation (power management overview)](https://www.kernel.org/doc/html/latest/)
- [Intel 4004 history](https://www.intel.com/content/www/us/en/history/museum-story-of-intel-4004.html)
</details>

<details>
  <summary><b>Research Opportunities</b></summary>

  ### Emerging Technologies
  - **Quantum Computing**
    - Potential to solve specific problems exponentially faster
    - Different energy profile from classical computing
    - Major cloud providers developing quantum services

  - **Advanced Cooling Technologies**
    - Two-phase immersion cooling
    - Direct-to-chip liquid cooling
    - Waste heat recovery and reuse

  - **Software-Hardware Co-design**
    - Domain-specific architectures (NPUs, DPUs)
    - Workload-optimized systems
    - Heterogeneous computing

  ### Industry Trends
  - **Data Sovereignty & Regional Computing**
    - Regulatory impacts on cloud architecture
    - Data residency requirements
    - Energy implications of geographic distribution

  - **Sustainable Software Engineering**
    - Carbon-aware development practices
    - Energy efficiency as a software metric
    - Tools for measuring application carbon footprint

  - **Edge-Cloud Continuum**
    - Computation placement optimization
    - Data gravity considerations
    - Energy implications of edge processing vs. centralized cloud
</details>


Bridge to practice:
- Hardware selections now emphasize performance‑per‑watt, density, cooling, and accelerator fit (CPU vs GPU/FPGA).  
- Declarative orchestration (K8s) reconciles desired state → scale, resilience, higher utilization.  
- Azure’s control planes (ARM) translate user intent into scheduled resources across HW/SW layers.

## Learning Goals
- Explain how server components are selected for energy efficiency and cost (perf/W, PUE, cooling, accelerators).
- Show how automation/orchestration (Kubernetes) enables safe, elastic scale.
- Map HW↔SW layers that deliver Azure services (control vs data plane, availability constructs).
- Reproduce local demos to internalize concepts (no subscriptions needed).

## Demos (Local-First)

### Demo A: Energy-Efficient Compute on a Single Node
What you do:
- Characterize workloads (CPU vs memory) and observe perf-per-watt changes under different limits.

Windows PowerShell (pwsh):
```powershell
# Install tools (choose one package manager)
winget install -e --id Docker.DockerDesktop
winget install -e --id Kubernetes.kubectl
winget install -e --id Kind.Kind

# Optional: Windows performance report (snapshot)
powercfg /energy /output "$env:USERPROFILE\Desktop\energy-report.html" /duration 60
```

Experiment ideas:
- Run a CPU load container and vary CPU limits; measure elapsed time vs resource use.
- If you have Intel Power Gadget installed, log power while the load runs (Intel-only).  
- Discuss DVFS, C/P-states, bin‑packing, and effect on throughput vs energy.

```powershell
# Run a CPU stress container locally
docker run --rm -it --cpus 0.5 alpine sh -c "apk add --no-cache stress-ng && stress-ng --cpu 2 --timeout 45s"
docker run --rm -it --cpus 2.0 alpine sh -c "apk add --no-cache stress-ng && stress-ng --cpu 4 --timeout 45s"
```

Talking points:
- Utilization curves are nonlinear: “just enough” scaling often improves perf/W.
- Rack-level: efficient PSUs, airflow, liquid/advanced cooling, power capping (Redfish/IPMI).

### Demo B: Orchestration & Autoscaling with Kubernetes (kind)
Goal:
- Show declarative desired state, rolling updates, and CPU-based autoscaling.

Create a local cluster and deploy:
```powershell
kind create cluster --name evo
kubectl apply -f https://k8s.io/examples/application/deployment.yaml
# Expose & autoscale
kubectl expose deployment nginx-deployment --type=NodePort --port=80
kubectl autoscale deployment nginx-deployment --cpu-percent=50 --min=1 --max=5
# Generate load (use a busybox Job)
kubectl apply -f https://k8s.io/examples/application/hpa/php-apache.yaml
```

Observe:
```powershell
kubectl get hpa -w
kubectl get pods -w
kubectl describe hpa nginx-deployment
```

Discuss:
- Controllers reconcile desired → actual state.
- HPA/VPA/Cluster Autoscaler roles; bin‑packing raises utilization and can reduce energy per request.

### Demo C: HW↔SW Layering Flow (Bicep offline + K8s data/control paths)
Intent:
- Show how a user “intent” becomes resources, and how control/data planes differ.

Bicep offline (no sign‑in) – compile only:
```powershell
# Install Bicep CLI
winget install -e --id Microsoft.Bicep
# Example: compile a VM definition locally (template.bicep → template.json)
bicep build template.bicep
```

K8s data vs control path:
- Control: API Server → Scheduler → Controller Manager → kubelet → Containers.
- Data: client → Service/Ingress → Pod (app) → storage/network plugins.

Use readiness/liveness, PDBs, and a rolling update:
```powershell
# Example manifests below in Appendix; apply them to see rollout and disruption behavior
kubectl apply -f ./manifests/app-deployment.yaml
kubectl rollout status deployment/app
kubectl apply -f ./manifests/pdb.yaml
```

## Important Considerations for Production Environment
- Architecture & availability: Multi‑AZ/zone, fault & update domains, regional pairs.
- Capacity & quotas: plan headroom; use autoscale with safeguards.
- Security baseline: identity (Managed Identity), secrets (Key Vault), network isolation, private endpoints.
- Observability: metrics, logs, traces; SLOs/error budgets; cost telemetry.
- Governance: policy-as-code, tagging, RBAC; drift detection and CI/CD gates.
- Sustainability: measure PUE/carbon intensity; use right‑sizing and scheduling windows.

## Slide & Visual Placeholders
- Timeline: “1801 → 2020s” stripe with callouts (Jacquard, Turing, Web, Azure, K8s).
- Perf‑per‑watt vs utilization curve; PUE overview.
- Kubernetes reconciliation loop and autoscale timeline.
- Azure layered diagram: silicon → servers → racks → fabric → hypervisor/container → orchestrators → ARM → services.

## Appendix: Commands & Manifests

<details>
<summary><b>Manifests: simple app + HPA</b></summary>

```yaml
# manifests/app-deployment.yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: app
spec:
  replicas: 1
  selector:
    matchLabels:
      app: demo
  template:
    metadata:
      labels:
        app: demo
    spec:
      containers:
        - name: app
          image: nginx
          ports:
            - containerPort: 80
          resources:
            requests:
              cpu: "100m"
              memory: "128Mi"
            limits:
              cpu: "500m"
              memory: "256Mi"
          readinessProbe:
            httpGet:
              path: /
              port: 80
            initialDelaySeconds: 5
            periodSeconds: 5
---
apiVersion: v1
kind: Service
metadata:
  name: app
spec:
  type: NodePort
  selector:
    app: demo
  ports:
    - port: 80
      targetPort: 80
```

```yaml
# manifests/hpa.yaml
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: app
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: app
  minReplicas: 1
  maxReplicas: 5
  metrics:
    - type: Resource
      resource:
        name: cpu
        target:
          type: Utilization
          averageUtilization: 50
```

```yaml
# manifests/pdb.yaml
apiVersion: policy/v1
kind: PodDisruptionBudget
metadata:
  name: app-pdb
spec:
  minAvailable: 1
  selector:
    matchLabels:
      app: demo
```
</details>

---

> Reuse and adapt. For official implementation details or Azure deployments, consult Microsoft Learn and linked documentation above.
