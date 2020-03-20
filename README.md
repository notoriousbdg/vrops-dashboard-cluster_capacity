
# Cluster Capacity Dashboard for vRealize Operations 8.0
---------

Use this [vRealize Operations](https://www.vmware.com/products/vrealize-operations.html) dashboard to expore cluster capacity ranked by Time Remaining, Capacity Remaining, VMs Remaining, and Most Constrained Resource.  Select a cluster to see Total Capacity, Usable Capacity, Usage, and Demand for CPU, Memory and Disk Space in the selected cluster.

## Dashboard
![Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Dashboard.png)

## Installation
1. Import the super metric at `Administration` / `Configuration` / `Super Metrics` / `Import Super Metric`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_Super_Metric.png)
2. Click `Browse...` then select the file named [Supermetrics.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Supermetrics.json)
3. Edit the Policy at `Administration` / `Policies` / `Policy Library`.  The policy should be `vSphere Solution's Default Policy (DATE)` unless a new policy was explicitly created.  
![Policy Library](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Policy_Library.png)
4. Enable Super Metrics that start with `Super Metric|Most Constrained` for Cluster Compute Resource objects only.
![Policy Metrics](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Policy_Metrics.png)
5. Import the custom groups at `Environment` / `Custom Groups` / `Gear Icon` / `Import Custom Group(s)`  
![Import Custom Groups](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_CustomGroup.png)
6. Click `Browse...` then select the file named [CustomGroups.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/CustomGroups.json)
7. Import the view at `Dashboards` / `Views` / `Import...`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_View.png)
8. Click `Browse...` then select the file named [Views.zip](https://github.com/notoriousbdg/vrops-dashboard-cluster_capacity/raw/master/Views.zip)
9. Import the dashboard at `Dashboards` / `Actions` / `Manage Dashboards` / `Import Dashboards`  
![Import Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_Dashboard.png)
10. Click `Browse...` then select the file named [Dashboard.zip](https://github.com/notoriousbdg/vrops-dashboard-cluster_capacity/raw/master/Dashboard.zip)
11. The dashboard should now be available in in the dashboard list  
![Dashboard List](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Dashboard_List.png)

## Support

This dashboard requires vRealize Operation 8.0 Advanced or Enterprise edition.

Please open an [issue](https://github.com/notoriousbdg/vrops-dashboard-cluster_capacity/issues) for feedback.