
# VM Rightsizing Details Dashboard for vRealize Operations 8.0 and 8.1
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
![Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Dashboard.png)

## Installation
1. Import the super metric at `Administration` / `Configuration` / `Super Metrics` / `Import Super Metric`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Import_Super_Metric.png)
2. Click `Browse...` then select the file named [SuperMetrics.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Supermetrics.json)
3. Edit the Policy at `Administration` / `Policies` / `Policy Library`.  The policy should be `vSphere Solution's Default Policy (DATE)` unless a new policy was explicitly created.  
![Policy Library](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Policy_Library.png)
4. Enable the Super Metrics for the specified object types.  Do not enable the super metric for `All Object Types`.  The list of super metrics and object types are listed in the [Super Metrics section](#Super-Metrics).  
![Policy Metrics](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Policy_Metrics.png)
5. Import the view at `Dashboards` / `Views` / `Import...`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Import_View.png)
6. Click `Browse...` then select the file named [Views.zip](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/raw/master/Views.zip)
7. The included views are listed in the [Views section](#Views)
8. Import the dashboard at `Dashboards` / `Actions` / `Manage Dashboards` / `Import Dashboards`  
![Import Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Import_Dashboard.png)
9. Click `Browse...` then select the file named [Dashboard.zip](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/raw/master/Dashboard.zip)
10. The dashboard should now be available in in the dashboard list  
![Dashboard List](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Dashboard_List.png)
11. The included dashboards are listed in the [Dashboards section](#Dashboards)

## Dashboards
| Dashboard Name | Dashboard Path |
|--|--|
| VM Rightsizing Details | Shared Dashboards (GBrandon)/Capacity |

## Views
| View Name | Name on Dashboard | View Type |
|--|--|--|
| Rightsizing - Conservative | Rightsizing - Conservative | Image |
| Rightsizing - Aggressive | Rightsizing - Aggressive | Image |
| Oversized Virtual Machine Details | 2A. Select an Oversized VM | List |
| Undersized Virtual Machine Details | 2B. Select an Undersized VM | List |
| Recommended Size - CPU | 3. Compare CPU Recommended Size to Historical Utilization | Trend |
| Recommended Size - Memory | 4. Compare Memory Recommended Size to Historical Utilization | Trend |
| CPU Queue Trend with Total Capacity | 5. Compare CPU Queue to Total Capacity | Trend |
| CPU Context Switch Rate per Second with Total Capacity | 6. Compare Context Switch Rate to Total Capacity | Trend |
| Guest Memory Paging | 7. Check for Guest Memory Paging | Trend |
| Rightsizing 90th Percentile (24 Hour) | 90th Percentile (24 Hours) | List |
| Rightsizing 90th Percentile (7 Days) | 90th Percentile (7 Days) | List |
| Rightsizing 90th Percentile (30 Days) | 90th Percentile (30 Days) | List |

## Super Metrics
| Object Type | Super Metric Name |
|--|--|
| Rightsize - Potential Cost Increase | Virtual Machine |
| Rightsize - Memory to Remove from Oversized VMs | Virtual Machine |
| Rightsize - vCPUs to Remove from Oversized VMs | Virtual Machine |
| Rightsize - Potential CPU Usage Reclaimable (GHz) | Virtual Machine |
| Rightsize - Potential CPU Usage Increase (GHz) | Virtual Machine |
| Rightsize - Potential Memory Consumed Reclaimable (GB) | Virtual Machine |
| Rightsize - Potential Memory Consumed Increase (GB) | Virtual Machine |
| Rightsize - Potential Cost Savings | Virtual Machine |
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
| Rightsize - vCPUs to Add to Undersized VMs | Cluster Compute Resource |
| Rightsize - vCPUs to Add to Undersized VMs | Custom Datacenter |
| Rightsize - vCPUs to Add to Undersized VMs | Datacenter |
| Rightsize - vCPUs to Add to Undersized VMs | vSphere World |
| Rightsize - vCPUs to Remove from Oversized VMs | Cluster Compute Resource |
| Rightsize - vCPUs to Remove from Oversized VMs | Custom Datacenter |
| Rightsize - vCPUs to Remove from Oversized VMs | Datacenter |
| Rightsize - vCPUs to Remove from Oversized VMs | vSphere World |
| Rightsize - Potential Cost Savings Total | Cluster Compute Resource |
| Rightsize - Potential Cost Savings Total | Custom Datacenter |
| Rightsize - Potential Cost Savings Total | Datacenter |
| Rightsize - Potential Cost Savings Total | vSphere World |
| Rightsize - Potential Cost Increase Total | Cluster Compute Resource |
| Rightsize - Potential Cost Increase Total | Custom Datacenter |
| Rightsize - Potential Cost Increase Total | Datacenter |
| Rightsize - Potential Cost Increase Total | vSphere World |

## Support

This dashboard requires vRealize Operation 8.0 or 8.1 Advanced or Enterprise edition.

Please open an [issue](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/issues) for feedback.

## Changelog
2020-01-14
* Initial release

2020-01-14
* Update readme

2020-04-29
* Added summary rollup metrics for cluster, datacenter, custom datacenter, and vSphere World
* Added CPU Queue view
* Added Context Switch Rate view
* Added Guest Memory Paging view
* Added 90th Percentile views
