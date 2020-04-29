
# Cluster Capacity Dashboard for vRealize Operations 8.0 and 8.1
---------

Use this [vRealize Operations](https://www.vmware.com/products/vrealize-operations.html) dashboard to expore cluster capacity ranked by Time Remaining, Capacity Remaining, VMs Remaining, and Most Constrained Resource.  Select a cluster to see Total Capacity, Usable Capacity, Usage, and Demand for CPU, Memory and Disk Space in the selected cluster.

## Dashboard
![Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Dashboard.png)

## Installation
1. Import the super metric at `Administration` / `Configuration` / `Super Metrics` / `Import Super Metric`  
![Import Super Metric](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_Super_Metric.png)
2. Click `Browse...` then select the file named [Supermetrics.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Supermetrics.json)
3. Edit the Policy at `Administration` / `Policies` / `Policy Library`.  The policy should be `vSphere Solution's Default Policy (DATE)` unless a new policy was explicitly created.  
![Policy Library](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Policy_Library.png)
4. Enable the Super Metrics for the specified object types.  Do not enable the super metric for `All Object Types`.  The list of super metrics and object types are listed in the [Super Metrics section](#Super-Metrics).  
![Policy Metrics](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Policy_Metrics.png)
5. Import the custom groups at `Environment` / `Custom Groups` / `Gear Icon` / `Import Custom Group(s)`  
![Import Custom Groups](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_CustomGroup.png)
6. Click `Browse...` then select the file named [CustomGroups.json](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/CustomGroups.json)
7. The included custom groups are listed in the [Custom Groups section](#Custom-Groups).  
8. Import the view at `Dashboards` / `Views` / `Import...`  
![Import View](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_View.png)
9. Click `Browse...` then select the file named [Views.zip](https://github.com/notoriousbdg/vrops-dashboard-cluster_capacity/raw/master/Views.zip)
10. The included views are listed in the [Views section](#Views)
11. Import the dashboard at `Dashboards` / `Actions` / `Manage Dashboards` / `Import Dashboards`  
![Import Dashboard](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Import_Dashboard.png)
12. Click `Browse...` then select the file named [Dashboard.zip](https://github.com/notoriousbdg/vrops-dashboard-cluster_capacity/raw/master/Dashboard.zip)
13. The dashboard should now be available in in the dashboard list  
![Dashboard List](https://raw.githubusercontent.com/notoriousbdg/vrops-dashboard-cluster_capacity/master/Dashboard_List.png)
14. The included dashboards are listed in the [Dashboards section](#Dashboards)

## Dashboards
| Dashboard Name | Dashboard Path |
|--|--|
| Cluster Capacity | Shared Dashboards (GBrandon)/Capacity |

## Views
| View Name | Name on Dashboard | View Type |
|--|--|--|
| Time Remaining (Conservative) | Time Remaining (Conservative) | Image |
| Time Remaining (Aggressive) | Time Remaining (Aggressive) | Image |
| Capacity Remaining (Conservative) | Capacity Remaining (Conservative) | Image |
| Capacity Remaining (Aggressive) | Capacity Remaining (Aggressive) | Image |
| Capacity Terms | Capacity Terms | Image |
| Capacity Remaining with Most Constrained | Select a Cluster | List |
| Dedicated Failover Hosts | Dedicated Failover Hosts for Admission Control | List |
| HA CPU Slot Size | CPU Slot Size for Admission Control | Distribution |
| HA Memory Slot Size | Memory Slot Size for Admission Control | Distribution |
| Capacity CPU (Demand) Trend | CPU Capacity (Demand Model) | Trend |
| Capacity Memory (Demand) Trend | Memory Capacity (Demand Model) | Trend |
| Capacity Disk Space (Demand) Trend | Disk Space Capacity (Demand Model) | Trend |
| Capacity CPU (Allocation) Trend | CPU Capacity (Allocation Model) | Trend |
| Capacity Memory (Allocation) Trend | Memory Capacity (Allocation Model) | Trend |
| Capacity Disk Space (Allocation) Trend | Disk Space Capacity (Allocation Model) | Trend |

## Custom Groups
| Custom Group Name | Group Type |
|--|--|
| Most Constrained by CPU (Demand) | Environment |
| Most Constrained by Memory (Demand) | Environment |
| Most Constrained by Disk Space (Demand) | Environment |
| Most Constrained by CPU (Allocation) | Environment |
| Most Constrained by Memory (Allocation) | Environment |
| Most Constrained by Disk Space (Allocation) | Environment |
| Admission Control Policy - Disabled | Environment |
| Admission Control Policy - Cluster Resource Percentage | Environment |
| Admission Control Policy - Dedicated Failover Hosts | Environment |
| Admission Control Policy - Slot Policy (Powered-on VMs) | Environment |

## Super Metrics
| Object Type | Super Metric Name |
|--|--|
| Cluster Compute Resource | Most Constrained by CPU Demand |
| Cluster Compute Resource | Most Constrained by Memory Demand |
| Cluster Compute Resource | Most Constrained by Disk Space Demand |
| Cluster Compute Resource | Most Constrained by CPU Allocation |
| Cluster Compute Resource | Most Constrained by Memory Allocation |
| Cluster Compute Resource | Most Constrained by Disk Space Allocation |

## Support

This dashboard requires vRealize Operation 8.0 or 8.1 Advanced or Enterprise edition.

Please open an [issue](https://github.com/notoriousbdg/vrops-dashboard-cluster_capacity/issues) for feedback.

## Changelog
2020-03-20
* Initial release

2020-04-28
* Added readme to dashboard with diagrams
* Added Admission Control details
* Added Capacity Buffer settings
* Added Time Remaining widget
* Added Allocation Model section

2020-04-29
* Added missing Time Remaining views
