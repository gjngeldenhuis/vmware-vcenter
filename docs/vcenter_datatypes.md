## vCenter resource types

### vc_affinity
Manage vCenter Cluster affinity rules
#### Parameters
* `name`: Name of the cluster rule
* `vm`: Array of virtual machines
* `rule_type`: Type of rule: affinity or anti_affinity
* `path`: The path to the Cluster, must be the absolute path
#### Autorequire
* vc_folder
* vc_datacenter


### vc_cluster
Manages vCenter Clusters
#### Parameters
* `name`: The path to the Cluster
* `transport`: A resource reference to a transport type declared elsewhere. Eg: `Transport['vcenter']`
* `ensure`: present/absent. Defaults to `present`
#### Autorequire
* vc_folder
* vc_datacenter


### vc_cluster_drs
Manages vCenter cluster's settings for DRS (Distributed Resource Scheduler). See [VMware Docs ](http://pubs.vmware.com/vsphere-50/topic/com.vmware.wssdk.apiref.doc_50/vim.cluster.ConfigSpecEx.html) for detailed information on properties and methods."
#### Parameters
* `path`: The namevar variable. The path to the cluster.
* `enabled`: Is DRS enabled? true or false
* `enable_vm_behavior_overrides`: Is VM-specific override of cluster-wide DRS behavior enabled? true or false
* `default_vm_behavior`: Cluster-wide default for DRS management of VMs: fullyAutomated, partiallyAutomated, or manual
* `vmotion_rate`: Aggressiveness of DRS actions or recommendations for vMotion: 1 (aggressive) through 5 (conservative)
#### Autorequire
* vc_cluster


### vc_cluster_evc
Manages vCenter cluster's settings for EVC (Enhanced Vmotion Compatibility).
#### Parameters
* `path`: The namevar variable. The path to the cluster.
* `evc_mode_key`: A string corresponding to the desired EVC Mode; or 'disabled' to disable EVC
#### Autorequire
* vc_cluster


### vc_cluster_ha
Manages vCenter cluster's settings for HA (High Availability)
#### Parameters
* `path`: The path to the cluster.
* `admission_control_enabled`:
* `admission_control_policy_type`:
* `cpu_failover_resources_percent`:
* `memory_failover_resources_percent`:
* `failover_hosts`:
* `failover_level`:
* `isolation_response`:
* `restart_priority`:
* `failure_interval`:
* `max_failures`:
* `max_failure_window`:
* `min_up_time`:
* `vm_monitoring`:
* `das_config_enabled`:
* `host_monitoring`:
* `das_config_vm_monitoring`:
* `transport`:

### vc_datacenter
Manages vCenter Datacenters.
#### Parameters
* `path`: The path to the Datacenter.
* `transport`:
#### Autorequire
* vc_folder

### vc_dvportgroup
Manages vCenter Distributed Virtual Portgroup
#### Parameters
* `dvportgroup_name`:
* `ensure`:

* `auto_expand`:
* `description`:
* `num_ports`:
* `port_name_format`:
* `type`:

* `policy_block_override_allowed`:
* `policy_ipfix_override_allowed`:
* `policy_live_port_moving_allowed`:
* `policy_network_resource_pool_override_allowed`:
* `policy_port_config_reset_at_disconnect`:
* `policy_security_policy_override_allowed`:
* `policy_shaping_override_allowed`:
* `policy_uplink_teaming_override_allowed`:
* `policy_vendor_config_override_allowed`:
* `policy_vlan_override_allowed`:

* `default_port_config_blocked_inherited`:
* `default_port_config_blocked_value`:
* `default_port_config_in_shaping_policy_average_bandwidth_inherited`:
* `default_port_config_in_shaping_policy_average_bandwidth_value`:
* `default_port_config_in_shaping_policy_burst_size_inherited`:
* `default_port_config_in_shaping_policy_burst_size_value`:
* `default_port_config_in_shaping_policy_enabled_inherited`:
* `default_port_config_in_shaping_policy_enabled_value`:
* `default_port_config_in_shaping_policy_inherited`:
* `default_port_config_in_shaping_policy_peak_bandwidth_inherited`:
* `default_port_config_in_shaping_policy_peak_bandwidth_value`:
* `default_port_config_ipfix_enabled_inherited`:
* `default_port_config_ipfix_enabled_value`:
* `default_port_config_lacp_policy_enable_inherited`:
* `default_port_config_lacp_policy_enable_value`:
* `default_port_config_lacp_policy_inherited`:
* `default_port_config_lacp_policy_mode_inherited`:
* `default_port_config_lacp_policy_mode_value`:
* `default_port_config_network_resource_pool_key_inherited`:
* `default_port_config_network_resource_pool_key_value`:
* `default_port_config_out_shaping_policy_average_bandwidth_inherited`:
* `default_port_config_out_shaping_policy_average_bandwidth_value`:
* `default_port_config_out_shaping_policy_burst_size_inherited`:
* `default_port_config_out_shaping_policy_burst_size_value`:
* `default_port_config_out_shaping_policy_enabled_inherited`:
* `default_port_config_out_shaping_policy_enabled_value`:
* `default_port_config_out_shaping_policy_inherited`:
* `default_port_config_out_shaping_policy_peak_bandwidth_inherited`:
* `default_port_config_out_shaping_policy_peak_bandwidth_value`:
* `default_port_config_security_policy_allow_promiscuous_inherited`:
* `default_port_config_security_policy_allow_promiscuous_value`:
* `default_port_config_security_policy_forged_transmits_inherited`:
* `default_port_config_security_policy_forged_transmits_value`:
* `default_port_config_security_policy_inherited`:
* `default_port_config_security_policy_mac_changes_inherited`:
* `default_port_config_security_policy_mac_changes_value`:
* `default_port_config_tx_uplink_inherited`:
* `default_port_config_tx_uplink_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_beacon_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_beacon_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_duplex_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_duplex_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_error_percent_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_error_percent_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_speed_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_speed_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_full_duplex_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_full_duplex_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_percentage_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_percentage_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_speed_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_speed_value`:
* `default_port_config_uplink_teaming_policy_inherited`:
* `default_port_config_uplink_teaming_policy_notify_switches_inherited`:
* `default_port_config_uplink_teaming_policy_notify_switches_value`:
* `default_port_config_uplink_teaming_policy_policy_inherited`:
* `default_port_config_uplink_teaming_policy_policy_value`:
* `default_port_config_uplink_teaming_policy_reverse_policy_inherited`:
* `default_port_config_uplink_teaming_policy_reverse_policy_value`:
* `default_port_config_uplink_teaming_policy_rolling_order_inherited`:
* `default_port_config_uplink_teaming_policy_rolling_order_value`:
* `default_port_config_uplink_teaming_policy_uplink_port_order_active_uplink_port`:
* `default_port_config_uplink_teaming_policy_uplink_port_order_inherited`:
* `default_port_config_uplink_teaming_policy_uplink_port_order_standby_uplink_port`:

* `default_port_config_vlan_type_vmware_distributed_virtual_switch_pvlan_spec_inherited`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_pvlan_spec_pvlan_id`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_trunk_vlan_spec_inherited`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_trunk_vlan_spec_vlan_id`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_vlan_id_spec_inherited`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_vlan_id_spec_vlan_id `:


### vc_dvswitch
Manages vCenter Distributed Virtual Switch. The `vcenter::dvswitch` defined type encapsulates this resource.
#### Parameters
* `name`: {path to dvswitch}{:optional tag to make resource name unique}
* `path`: The path to the dvswitch
* `config_version`:
* `contact_info`:
* `contact_name`:
* `default_proxy_switch_max_num_ports`:
* `description`:
* `dvswitch_name`:
* `extension_key`:
* `host`:
* `link_discovery_protocol_config_operation`:
* `link_discovery_protocol_config_protocol`:
* `max_mtu`:
* `num_standalone_ports`:
* `policy_auto_pre_install_allowed`:
* `policy_auto_upgrade_allowed`:
* `policy_partial_upgrade_allowed`:
* `switch_ip_address`:
* `uplink_portgroup`:
* `uplink_port_name`:
* `vendor_specific_config`:
* `default_port_config_blocked_inherited`:
* `default_port_config_blocked_value`:

##### Shaping Policy
* `default_port_config_in_shaping_policy_inherited`:
* `default_port_config_in_shaping_policy_average_bandwidth_inherited`:
* `default_port_config_in_shaping_policy_average_bandwidth_value`:
* `default_port_config_in_shaping_policy_burst_size_inherited`:
* `default_port_config_in_shaping_policy_burst_size_value`:
* `default_port_config_in_shaping_policy_enabled_inherited`:
* `default_port_config_in_shaping_policy_enabled_value`:
* `default_port_config_in_shaping_policy_peak_bandwidth_inherited`:
* `default_port_config_in_shaping_policy_peak_bandwidth_value`:

##### IP Fix
* `default_port_config_ipfix_enabled_inherited`:
* `default_port_config_ipfix_enabled_value`:

##### LACP Policy
* `default_port_config_lacp_policy_inherited`:
* `default_port_config_lacp_policy_enable_inherited`:
* `default_port_config_lacp_policy_enable_value`:
* `default_port_config_lacp_policy_mode_inherited`:
* `default_port_config_lacp_policy_mode_value`:

##### Network resource pool
* `default_port_config_network_resource_pool_key_inherited`:
* `default_port_config_network_resource_pool_key_value`:

##### Port Config Out Shaping Policy
* `default_port_config_out_shaping_policy_average_bandwidth_inherited`:
* `default_port_config_out_shaping_policy_average_bandwidth_value`:
* `default_port_config_out_shaping_policy_burst_size_inherited`:
* `default_port_config_out_shaping_policy_burst_size_value`:
* `default_port_config_out_shaping_policy_enabled_inherited`:
* `default_port_config_out_shaping_policy_enabled_value`:
* `default_port_config_out_shaping_policy_inherited`:
* `default_port_config_out_shaping_policy_peak_bandwidth_inherited`:
* `default_port_config_out_shaping_policy_peak_bandwidth_value`:

##### Port Config Security Policy
* `default_port_config_security_policy_inherited`:
* `default_port_config_security_policy_allow_promiscuous_inherited`:
* `default_port_config_security_policy_allow_promiscuous_value`:
* `default_port_config_security_policy_forged_transmits_inherited`:
* `default_port_config_security_policy_forged_transmits_value`:
* `default_port_config_security_policy_mac_changes_inherited`:
* `default_port_config_security_policy_mac_changes_value`:

##### Port Config TX Uplink
* `default_port_config_tx_uplink_inherited`:
* `default_port_config_tx_uplink_value`:

#### Port Config Uplink Teaming Policy Failure Criteria
* `default_port_config_uplink_teaming_policy_failure_criteria_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_beacon_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_beacon_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_duplex_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_duplex_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_error_percent_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_error_percent_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_speed_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_check_speed_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_full_duplex_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_full_duplex_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_percentage_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_percentage_value`:
* `default_port_config_uplink_teaming_policy_failure_criteria_speed_inherited`:
* `default_port_config_uplink_teaming_policy_failure_criteria_speed_value`:

##### Port Config Uplink Teaming Policy
* `default_port_config_uplink_teaming_policy_inherited`:
* `default_port_config_uplink_teaming_policy_notify_switches_inherited`:
* `default_port_config_uplink_teaming_policy_notify_switches_value`:
* `default_port_config_uplink_teaming_policy_policy_inherited`:
* `default_port_config_uplink_teaming_policy_policy_value`:
* `default_port_config_uplink_teaming_policy_reverse_policy_inherited`:
* `default_port_config_uplink_teaming_policy_reverse_policy_value`:
* `default_port_config_uplink_teaming_policy_rolling_order_inherited`:
* `default_port_config_uplink_teaming_policy_rolling_order_value`:

##### Port Config Uplink Teaming Policy Uplink
* `default_port_config_uplink_teaming_policy_uplink_port_order_inherited`:
* `default_port_config_uplink_teaming_policy_uplink_port_order_active_uplink_port`:
* `default_port_config_uplink_teaming_policy_uplink_port_order_standby_uplink_port`:

##### Port Config Vlan Type VMware distributed virtual switch
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_pvlan_spec_inherited`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_pvlan_spec_pvlan_id`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_trunk_vlan_spec_inherited`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_trunk_vlan_spec_vlan_id`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_vlan_id_spec_inherited`:
* `default_port_config_vlan_type_vmware_distributed_virtual_switch_vlan_id_spec_vlan_id`:




### vc_dvswitch_migrate
Manages Distributed Virtual Switch migration on an ESXi host by moving vmknics and vmnics from standard to distributed switch
#### Parameters
* `host`: Name of ESXi host, as known to vCenter
* `dvswitch`: Path of the destination distributed virtual switch
* `name`: {name of host}:{path of dvswitch}[:{optional tag}
* `vmk0`: For kernel port vmk0, name of the destination dvportgroup
* `vmk1`: For kernel port vmk1, name of the destination dvportgroup
* `vmk2`: For kernel port vmk2, name of the destination dvportgroup
* `vmk3`: For kernel port vmk3, name of the destination dvportgroup
* `vmnic0`: For uplink port vmnic0, name of the destination dvportgroup
* `vmnic1`: For uplink port vmnic1, name of the destination dvportgroup
* `vmnic2`: For uplink port vmnic2, name of the destination dvportgroup
* `vmnic3`: For uplink port vmnic3, name of the destination dvportgroup

### vc_dvswitch_nioc
Manages vCenter Distributed Virtual Switch Network Resource Management (NIOC)
#### Parameters
* `name`: {path to dvswitch}{:optional tag to make resource name unique}
* `path`: The path to the dvswitch.
* `network_resource_management_enabled`: Enable or disable NIOC (network resource management); true/false

#### Autorequire
* vc_dvswitch


### vc_dvswitch_pool
Manages vCenter Distributed Virtual Switch Network Resource Pool Management
#### Parameters
* `name`: {path to dvswitch}:{network resource pool key}"
* `dvswitch_path`: The path to the dvportgroup.
* `dvswitch_name`:
* `key`: pool identifier
* `description`: A string describing the network resource pool
* `limit`: Maximum allowed usage for network clients belonging to this resource pool per host. To set to Unlimited set this to -1
* `priority_tag`: QOS priority tag
* `shares`: network shares
* `level`: Share level ('custom', 'high', 'low', 'normal')

#### Autorequire
* vc_dvswitch


### vc_extension
Interface with vcenter extension manager
Note: Create is not yet implemented for vcenter extension manager.
#### Parameters
* `name`: Extension name


### vc_folder
Manage vCenter folders
#### Parameters
* `path`: Namevar. The path to the folder.
#### Autorequire
* vc_folder
* vc_datacenter

### vc_host
Manage vCenter hosts.
#### Parameters
`name`: ESX hostname or ip address.
`username`: ESX username.
`password`: ESX password.
`sslthumbprint`: ESX host ssl thumbprint.
`secure`: Add host require sslthumprint verification.
`path`: "The path to the host."
#### Autorequire
* vc_datacenter
* vc_folder
* vc_cluster
* anchor


### vc_host_group
Manages vCenter cluster's settings for Host Groups used for VM-Host rules. See VMware [docs](http://pubs.vmware.com/vsphere-55/index.jsp#com.vmware.wssdk.apiref.doc/vim.cluster.HostGroup.html) for more information.
#### Parameters
* `name`: Name of the host group
* `path`: The path to the Cluster.
* `hosts`: Array of hosts

#### Autorequire
* vc_folder
* vc_datacenter


### vc_ip_pool
Manage vCenter IpPools. See VMware [docs](http://pubs.vmware.com/vsphere-55/index.jsp#com.vmware.wssdk.apiref.doc/vim.vApp.IpPool.html) for more information.
#### Parameters
* `label`: Namevar. Pool name, the pool name must be unique within the datacenter.
* `datacenter`: The datacenter target for the IpPool
* `force_destroy`: If true, the pool will be destroyed even if it is in use.


### vc_storagepod
This resource allows for the creation of a Storage Cluster, as well as the addition of datastores to the Cluster.
#### Parameters
* `datacenter`: Datacenter in which the cluster will be used
* `datastores`: Array of Datastores to be added to Storage Pod


### vc_vm
Manage vCenter VMs. Warning, this type / provider is currently experimental
#### Parameters
* `ensure`:
* `name`: The vm name
* `cpucount`:
* `memory`:
* `guestid`:
* `datastore`:
* `graceful_shutdown`: Perform a graceful shutdown if possible.  This parameter has no effect unless :power_state is set to :poweredOff
* `power_state`: set the powerstate for the vm to either poweredOn/poweredOff, for poweredOff, if tools is running a shutdownGuest will be issued, otherwise powerOffVM_TASK
* `datacenter_name`:



### vc_vm_group
Manages vCenter cluster's settings for VM Groups used for VM-Host rules. See VMware [docs](http://pubs.vmware.com/vsphere-55/index.jsp#com.vmware.wssdk.apiref.doc/vim.cluster.VmGroup.html) for more information.
#### Parameters
* `name`: Name of the cluster rule
* `path`: The path to the Cluster
* `vms`: Array of virtual machines

#### Autorequire
* vc_folder
* vc_datacenter

### vc_vm_host_rule
Manages vCenter cluster's settings for VM-Host rules. See VMware [docs](http://pubs.vmware.com/vsphere-55/index.jsp?topic=%2Fcom.vmware.wssdk.apiref.doc%2Fvim.cluster.VmHostRuleInfo.html) for more information
#### Parameters
* `name`: Name of the rule
* `path`: The path to the Cluster


### vc_vpxsettings
Manage vCenter vpxsettings ( event.maxAge, mail.smtp.server, etc )
#### Parameters
* `name`:
* `vpx_settings`:
