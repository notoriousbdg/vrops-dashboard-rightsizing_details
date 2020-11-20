
# VM Rightsizing Details Dashboard for vRealize Operations 8.2, and Cloud
---------

Use this [vRealize Operations](https://www.vmware.com/products/vrealize-operations.html) dashboard to expore rightsizing recommendations.  This dashboard will help answer these questions.  

* How does vROps determine the recommended size for a VM?
* Which VMs are oversized?
* Which VMs are undersized?
* How do I justify the recommendation to the VM owner?
* What is the potential change to capacity if the VMs are rightsized?
* What is the potential change to VM cost if the VMs are rightsized?

More detailed description of Rightsizing with vRealize Operations is available [here](http://blogs.vmware.com/management/2020/01/rightsizing-vms-with-vrealize-operations.html).

## Dashboard
![Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/images/Dashboard.png)

## Installation
1. Import the super metrics at `Administration` / `Configuration` / `Super Metrics` / `Import Super Metric`  
![Import Super Metric](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/images/Supermetric_Import.png)
2. Click `Browse...` then select the file named [Supermetrics.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Supermetrics.json)
3. For each Super Metric listed in the [Super Metrics section](#Super-Metrics), click on the vertical kebab and select edit.  
![Policy Metrics](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/images/Supermetric_Edit.png)
4. Enable the Super Metric for each Policy shown in the `Enable in a Policy` stage of the wizard.
![Policy Library](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/images/Supermetric_Policy.png)
5. Repeat the previous 2 steps for the remaining Super Metrics listed in the [Super Metrics section](#Super-Metrics).
6. Import the view at `Dashboards` / `Views` / `Import...`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/images/View_Import.png)
7. Click `Browse...` then select the file named [Views.zip](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/raw/master/Views.zip)
8. The included views are listed in the [Views section](#Views)
9. Import the dashboard at `Dashboards` / `Actions` / `Manage Dashboards` / `Import Dashboards`  
![Import Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/images/Dashboard_Import.png)
10. Click `Browse...` then select the file named [Dashboard.zip](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/raw/master/Dashboard.zip)
11. The dashboard should now be available in in the dashboard list  
![Dashboard List](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/images/Dashboard_List.png)
12. The included dashboards are listed in the [Dashboards section](#Dashboards)

## Dashboards
| Dashboard Name | Dashboard Path |
|--|--|
| VM Rightsizing Details | Shared Dashboards (GBrandon)/Capacity |

## Views
| View Name | Name on Dashboard | View Type |
|--|--|--|
| Rightsizing &#124; Conservative Diagram | Rightsizing - Conservative | Image |
| Rightsizing &#124; Aggressive Diagram | Rightsizing - Aggressive | Image |
| Rightsizing &#124; Undersized Virtual Machine Details | Select an Undersized VM to View Recommendations | List |
| Rightsizing &#124; Oversized Virtual Machine Details | Select an Oversized VM to View Recommendations | List |
| Rightsizing &#124; VM Oversized and Undersized Status | Search for a VM to View Recommendations | List |
| Rightsizing &#124; Guest Memory Not Collecting Warning | Additional Information | Text |
| Rightsizing &#124; Recommended Size - CPU | Compare CPU Recommended Size to Historical Utilization | Trend |
| Rightsizing &#124; Recommended Size - Memory | Compare Memory Recommended Size to Historical Utilization | Trend |
| Rightsizing &#124; Recommended Size - Disk Space | Compare Disk Space Recommended Size to Historical Utilization | Trend |
| Rightsizing &#124; CPU Demand (95th Percentile) | CPU Demand MHz (95th Percentile) | List |
| Rightsizing &#124; CPU Workload (95th Percentile) | CPU Workload % (95th Percentile) | List |
| Rightsizing &#124; Memory Utilization (95th Percentile) | Memory Utilization GB (95th Percentile) | List |
| Rightsizing &#124; Memory Workload (95th Percentile) | Memory Workload % (95th Percentile) | List |
| Rightsizing &#124; Guest Virtual Disks | Virtual Disks | List |
| Rightsizing &#124; Guest Virtual Disks | Guest Filesystems | List |
| Rightsizing &#124; CPU Queue Trend with Total Capacity | Compare CPU Queue to Total Capacity | Trend |
| Rightsizing &#124; CPU Context Switch Rate per Second with Total Capacity | Compare Context Switch Rate to Total Capacity | Trend |
| Rightsizing &#124; Guest Memory Paging | Check for Guest Memory Paging | Trend |

## Super Metrics
| Object Type | Super Metric Name |
|--|--|
| CPU Queue Total Capacity | Virtual Machine |
| Context Swap Rate Total Capacity | Virtual Machine |
| Rightsize - Memory to Add to Undersized VMs | Cluster Compute Resource |
| Rightsize - Memory to Add to Undersized VMs | Custom Datacenter |
| Rightsize - Memory to Add to Undersized VMs | Datacenter |
| Rightsize - Memory to Add to Undersized VMs | vSphere World |
| Rightsize - Memory to Remove from Oversized VMs | Cluster Compute Resource |
| Rightsize - Memory to Remove from Oversized VMs | Custom Datacenter |
| Rightsize - Memory to Remove from Oversized VMs | Datacenter |
| Rightsize - Memory to Remove from Oversized VMs | vSphere World |
| Rightsize - Potential Cost Increase | Virtual Machine |
| Rightsize - Potential Cost Increase Total | Cluster Compute Resource |
| Rightsize - Potential Cost Increase Total | Custom Datacenter |
| Rightsize - Potential Cost Increase Total | Datacenter |
| Rightsize - Potential Cost Increase Total | vSphere World |
| Rightsize - Potential Cost Savings | Virtual Machine |
| Rightsize - Potential Cost Savings Total | Cluster Compute Resource |
| Rightsize - Potential Cost Savings Total | Custom Datacenter |
| Rightsize - Potential Cost Savings Total | Datacenter |
| Rightsize - Potential Cost Savings Total | vSphere World |
| Rightsize - Potential CPU Usage Increase (GHz) | Virtual Machine |
| Rightsize - Potential CPU Usage Reclaimable (GHz) | Virtual Machine |
| Rightsize - Potential Memory Consumed Increase (GB) | Virtual Machine |
| Rightsize - Potential Memory Consumed Reclaimable (GB) | Virtual Machine |
| Rightsize - vCPUs to Add to Undersized VMs | Cluster Compute Resource |
| Rightsize - vCPUs to Add to Undersized VMs | Custom Datacenter |
| Rightsize - vCPUs to Add to Undersized VMs | Datacenter |
| Rightsize - vCPUs to Add to Undersized VMs | vSphere World |
| Rightsize - vCPUs to Remove from Oversized VMs | Cluster Compute Resource |
| Rightsize - vCPUs to Remove from Oversized VMs | Custom Datacenter |
| Rightsize - vCPUs to Remove from Oversized VMs | Datacenter |
| Rightsize - vCPUs to Remove from Oversized VMs | vSphere World |

## Support

This dashboard requires vRealize Operation 8.2 Advanced or Enterprise edition or vRealize Operations Cloud.

A version compatible with vRealize Operations 8.0 and 8.1 is available [here](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/tree/vrops-8.1).

Please open an [issue](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/issues) for feedback.

## Changelog
2020-01-14
* Initial release

2020-01-15
* Update readme

2020-04-29
* Fixed URLs in readme
* Added summary rollup metrics for cluster, datacenter, custom datacenter, and vSphere World
* Added CPU Queue view
* Added Context Switch Rate view
* Added Guest Memory Paging view
* Added 90th Percentile views
* Added VM Properties widgets

2020-05-13
* Update readme
* Removed Rightsize - Memory to Remove from Oversized VMs and Rightsize - vCPUs to Remove from Oversized VMs super metrics for Virtual Machine objects

2020-11-20
* Improved text formatting for both light and dark modes
* Added warning for VMs with guest memory metrics not collecting
* Added VM age
* Added disk space recommendations, list of virtual disks, and list of guest file systems
* Improved percentile format covering CPU demand, CPU workload, memory utilizaiton, and memory workload
* A version compatible with vRealize Operations 8.0 and 8.1 was moved [here](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/tree/vrops-8.1).