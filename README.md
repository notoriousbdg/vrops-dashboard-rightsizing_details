
# Rightsizing Details Dashboard for vRealize Operations 8.0
---------

Use this [vRealize Operations](https://www.vmware.com/products/vrealize-operations.html) dashboard to expore rightsizing recommendations.  This dashboard will help answer these questions.

* How does vROps determine the recommended size for a VM?
* Which VMs are oversized?
* Which VMs are undersized?
* How do I justify the recommendation to the VM owner?
* What is the potential change to capacity if the VMs are rightsized?
* What is the potential change to VM cost if the VMs are rightsized?

## Dashboard
![Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Dashboard.png)

## Installation
1. Import the super metric at `Administration` / `Configuration` / `Super Metrics` / `Import Super Metric`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Import_Super_Metric.png)
2. Click `Browse...` then select the file named [SuperMetrics.json](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/raw/master/SuperMetrics.json)
3. Edit the Policy at `Administration` / `Policies` / `Policy Library`.  The policy should be `vSphere Solution's Default Policy (DATE)` unless a new policy was explicitly created.  
![Policy Library](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Policy_Library.png)
4. Enable `Super Metric|VMs Remaining (Average VM Size)` Super Metric on Virtual Machine objects only.
![Policy Metrics](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Policy_Metrics.png)
5. Import the view at `Dashboards` / `Views` / `Import...`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Import_View.png)
6. Click `Browse...` then select the file named [Views.zip](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/raw/master/Views.zip)
7. Import the dashboard at `Dashboards` / `Actions` / `Manage Dashboards` / `Import Dashboards`  
![Import Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Import_Dashboard.png)
8. Click `Browse...` then select the file named [Dashboard.zip](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/raw/master/Dashboard.zip)
9. The dashboard should now be available in in the dashboard list  
![Dashboard List](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-rightsizing_details/master/Dashboard_List.png)

## Support

This dashboard requires vRealize Operation 8.0 Advanced or Enterprise edition.

Please open an [issue](https://github.com/notoriousbdg/vrops-dashboard-rightsizing_details/issues) for feedback.
