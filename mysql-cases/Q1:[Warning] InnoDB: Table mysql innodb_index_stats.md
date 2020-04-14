# 现象
```
2020-01-03T03:31:42.835046Z 2 [Warning] InnoDB: Table mysql/innodb_index_stats has length mismatch in the column name table_name.  Please run mysql_upgrade
2020-01-03T03:31:42.835115Z 2 [Warning] InnoDB: Table mysql/innodb_index_stats has length mismatch in the column name table_name.  Please run mysql_upgrade
```

# 解决方式
[安装完mysql 5.7.27，数据库报错日志](https://ciasm.blog.csdn.net/article/details/102928671)
执行 mysql_upgrade -S *.sock

# 执行结果
```
root@mmm02:~# mysql_upgrade -S /db/3307/mysqld.sock
Checking if update is needed.
Checking server version.
Running queries to upgrade MySQL server.
Checking system database.
mysql.columns_priv                                 OK
mysql.db                                           OK
mysql.engine_cost                                  OK
mysql.event                                        OK
mysql.func                                         OK
mysql.general_log                                  OK
mysql.gtid_executed                                OK
mysql.help_category                                OK
mysql.help_keyword                                 OK
mysql.help_relation                                OK
mysql.help_topic                                   OK
mysql.innodb_index_stats                           OK
mysql.innodb_table_stats                           OK
mysql.ndb_binlog_index                             OK
mysql.plugin                                       OK
mysql.proc                                         OK
mysql.procs_priv                                   OK
mysql.proxies_priv                                 OK
mysql.server_cost                                  OK
mysql.servers                                      OK
mysql.slave_master_info                            OK
mysql.slave_relay_log_info                         OK
mysql.slave_worker_info                            OK
mysql.slow_log                                     OK
mysql.tables_priv                                  OK
mysql.time_zone                                    OK
mysql.time_zone_leap_second                        OK
mysql.time_zone_name                               OK
mysql.time_zone_transition                         OK
mysql.time_zone_transition_type                    OK
mysql.user                                         OK
Found outdated sys schema version 1.5.0.
Upgrading the sys schema.
Checking databases.
jumpserver.auth_group                              OK
jumpserver.auth_group_permissions                  OK
jumpserver.auth_permission                         OK
jumpserver.django_admin_log                        OK
jumpserver.django_content_type                     OK
jumpserver.django_session                          OK
jumpserver.jasset_asset                            OK
jumpserver.jasset_asset_group                      OK
jumpserver.jasset_assetalias                       OK
jumpserver.jasset_assetgroup                       OK
jumpserver.jasset_assetrecord                      OK
jumpserver.jasset_idc                              OK
jumpserver.jlog_alert                              OK
jumpserver.jlog_execlog                            OK
jumpserver.jlog_filelog                            OK
jumpserver.jlog_log                                OK
jumpserver.jlog_termlog                            OK
jumpserver.jlog_termlog_user                       OK
jumpserver.jlog_ttylog                             OK
jumpserver.jperm_permlog                           OK
jumpserver.jperm_permpush                          OK
jumpserver.jperm_permrole                          OK
jumpserver.jperm_permrole_sudo                     OK
jumpserver.jperm_permrule                          OK
jumpserver.jperm_permrule_asset                    OK
jumpserver.jperm_permrule_asset_group              OK
jumpserver.jperm_permrule_role                     OK
jumpserver.jperm_permrule_user                     OK
jumpserver.jperm_permrule_user_group               OK
jumpserver.jperm_permsudo                          OK
jumpserver.juser_admingroup                        OK
jumpserver.juser_document                          OK
jumpserver.juser_user                              OK
jumpserver.juser_user_group                        OK
jumpserver.juser_user_groups                       OK
jumpserver.juser_user_user_permissions             OK
jumpserver.juser_usergroup                         OK
jumpserver.setting                                 OK
module_check.modulename                            OK
module_check.redislist                             OK
module_check.redislistv2                           OK
nginx.dnspod_modify_record                         OK
nginx.modify_record                                OK
nginx.nginx_info                                   OK
nginx.nginx_status                                 OK
nginx.route53_domain_info                          OK
nginx_log_analyze.nginx_log_min_count              OK
opsadmin.auth_group                                OK
opsadmin.auth_group_permissions                    OK
opsadmin.auth_permission                           OK
opsadmin.auth_user                                 OK
opsadmin.auth_user_groups                          OK
opsadmin.auth_user_user_permissions                OK
opsadmin.deploydb_module                           OK
opsadmin.deploydb_note                             OK
opsadmin.deploydb_permission                       OK
opsadmin.deploydb_project                          OK
opsadmin.deploydb_task                             OK
opsadmin.django_admin_log                          OK
opsadmin.django_content_type                       OK
opsadmin.django_session                            OK
opsadmin.manual_sshuserlist                        OK
opsadmin.opsdb_devicetype                          OK
opsadmin.opsdb_directconnect                       OK
opsadmin.opsdb_host                                OK
opsadmin.opsdb_idc                                 OK
opsadmin.opsdb_rack                                OK
opsadmin.opsdb_recorderbandwidth                   OK
opsadmin.opsdb_recorderdevice                      OK
opsadmin.opsdb_recordermaintenance                 OK
opsadmin.opsdb_redisinfo                           OK
opsadmin.opstower_action                           OK
opsadmin.opstower_note                             OK
opsadmin.opstower_permission                       OK
opsadmin.opstower_project                          OK
opsadmin.opstower_task                             OK
ossinfo.ossinfo                                    OK
osticket.ost__search                               OK
osticket.ost_api_key                               OK
osticket.ost_attachment                            OK
osticket.ost_canned_response                       OK
osticket.ost_config                                OK
osticket.ost_content                               OK
osticket.ost_department                            OK
osticket.ost_draft                                 OK
osticket.ost_email                                 OK
osticket.ost_email_account                         OK
osticket.ost_email_template                        OK
osticket.ost_email_template_group                  OK
osticket.ost_faq                                   OK
osticket.ost_faq_category                          OK
osticket.ost_faq_topic                             OK
osticket.ost_file                                  OK
osticket.ost_file_chunk                            OK
osticket.ost_filter                                OK
osticket.ost_filter_action                         OK
osticket.ost_filter_rule                           OK
osticket.ost_form                                  OK
osticket.ost_form_entry                            OK
osticket.ost_form_entry_values                     OK
osticket.ost_form_field                            OK
osticket.ost_help_topic                            OK
osticket.ost_help_topic_form                       OK
osticket.ost_list                                  OK
osticket.ost_list_items                            OK
osticket.ost_lock                                  OK
osticket.ost_note                                  OK
osticket.ost_organization                          OK
osticket.ost_organization__cdata                   OK
osticket.ost_plugin                                OK
osticket.ost_queue                                 OK
osticket.ost_role                                  OK
osticket.ost_sequence                              OK
osticket.ost_session                               OK
osticket.ost_sla                                   OK
osticket.ost_staff                                 OK
osticket.ost_staff_dept_access                     OK
osticket.ost_syslog                                OK
osticket.ost_task                                  OK
osticket.ost_task__cdata                           OK
osticket.ost_team                                  OK
osticket.ost_team_member                           OK
osticket.ost_thread                                OK
osticket.ost_thread_collaborator                   OK
osticket.ost_thread_entry                          OK
osticket.ost_thread_entry_email                    OK
osticket.ost_thread_event                          OK
osticket.ost_ticket                                OK
osticket.ost_ticket__cdata                         OK
osticket.ost_ticket_priority                       OK
osticket.ost_ticket_status                         OK
osticket.ost_translation                           OK
osticket.ost_user                                  OK
osticket.ost_user__cdata                           OK
osticket.ost_user_account                          OK
osticket.ost_user_email                            OK
sys.sys_config                                     OK
titan.auth_group                                   OK
titan.auth_group_permissions                       OK
titan.auth_permission                              OK
titan.authtoken_token                              OK
titan.celery_taskmeta                              OK
titan.celery_tasksetmeta                           OK
titan.django_admin_log                             OK
titan.django_content_type                          OK
titan.django_migrations                            OK
titan.django_session                               OK
titan.djcelery_crontabschedule                     OK
titan.djcelery_intervalschedule                    OK
titan.djcelery_periodictask                        OK
titan.djcelery_periodictasks                       OK
titan.djcelery_taskstate                           OK
titan.djcelery_workerstate                         OK
titan.guardian_groupobjectpermission               OK
titan.guardian_userobjectpermission                OK
titan.k8s_deployment                               OK
titan.k8s_deploymentlog                            OK
titan.tapp_api                                     OK
titan.tapp_app                                     OK
titan.tasset_asset                                 OK
titan.tasset_assetcost                             OK
titan.tasset_assetgroup                            OK
titan.tasset_bandwidth                             OK
titan.tasset_bandwidthrecord                       OK
titan.tasset_broadcard                             OK
titan.tasset_devices                               OK
titan.tasset_enginerooms                           OK
titan.tasset_externalnetwork                       OK
titan.tasset_factories                             OK
titan.tasset_getinfo                               OK
titan.tasset_host                                  OK
titan.tasset_host_group                            OK
titan.tasset_idc                                   OK
titan.tasset_internalnetwork                       OK
titan.tasset_netassetopsrecord                     OK
titan.tasset_netcable                              OK
titan.tasset_opticalfiber                          OK
titan.tasset_opticalmodule                         OK
titan.tasset_powermodule                           OK
titan.tasset_rack                                  OK
titan.tasset_racks                                 OK
titan.tasset_saltstackhost                         OK
titan.tasset_tag                                   OK
titan.tasset_tag_assets                            OK
titan.tasset_types                                 OK
titan.tconfig_configfile                           OK
titan.tconfig_rollbackconfigfile                   OK
titan.tdocker_ackrecord                            OK
titan.tdocker_application                          OK
titan.tdocker_application_cfg                      OK
titan.tdocker_assistinstance                       OK
titan.tdocker_deletedtag                           OK
titan.tdocker_deploy                               OK
titan.tdocker_deploy_alert_user                    OK
titan.tdocker_dockeropslog                         OK
titan.tdocker_fluentd                              OK
titan.tdocker_image                                OK
titan.tdocker_image_docker_host                    OK
titan.tdocker_image_favorite                       OK
titan.tdocker_imagebuildhistory                    OK
titan.tdocker_imagepullhistory                     OK
titan.tdocker_imagetag                             OK
titan.tdocker_instanceconfig                       OK
titan.tdocker_moduleconfig                         OK
titan.tdocker_moduleconfiglog                      OK
titan.tdocker_moduleinsconfig                      OK
titan.tdocker_redis                                OK
titan.tdocker_redismq                              OK
titan.tdocker_redisresourcepool                    OK
titan.tdocker_router                               OK
titan.tdocker_taskprogress                         OK
titan.tdomain_domaininfo                           OK
titan.tdomain_ngclusterinfo                        OK
titan.tdomain_nghostinfo                           OK
titan.tdomain_sslinfo                              OK
titan.tevents_portwhitelist                        OK
titan.tevents_resapplication                       OK
titan.tevents_trouble                              OK
titan.titan_dockerevent                            OK
titan.titan_dockeropsrecord                        OK
titan.titan_servmgrrecord                          OK
titan.tscan_events                                 OK
titan.tserver_cron                                 OK
titan.tserver_initserverresult                     OK
titan.tserver_nginxdomain                          OK
titan.tserver_nginxupstream                        OK
titan.tserver_nginxurlapi                          OK
titan.tserver_octopus                              OK
titan.tserver_octopusconfig                        OK
titan.tserver_octopusresult                        OK
titan.tserver_rollbacknginxdomain                  OK
titan.tserver_rollbacknginxupstream                OK
titan.tuser_perm                                   OK
titan.tuser_role                                   OK
titan.tuser_role_perm                              OK
titan.tuser_user                                   OK
titan.tuser_user_group                             OK
titan.tuser_user_groups                            OK
titan.tuser_user_image_approve                     OK
titan.tuser_user_perm                              OK
titan.tuser_user_role                              OK
titan.tuser_user_user_permissions                  OK
titan.tuser_usergroup                              OK
titan.tuser_usergroup_perm                         OK
voip_config.postboy_config_all                     OK
voip_config.postboy_list                           OK
voip_config.postkid_config_all                     OK
voip_config.postkid_list                           OK
voip_config.postman_config_all                     OK
voip_config.postman_config_all_new                 OK
voip_config.postman_list                           OK
zabbix.acknowledges                                OK
zabbix.actions                                     OK
zabbix.alerts                                      OK
zabbix.application_discovery                       OK
zabbix.application_prototype                       OK
zabbix.application_template                        OK
zabbix.applications                                OK
zabbix.auditlog                                    OK
zabbix.auditlog_details                            OK
zabbix.autoreg_host                                OK
zabbix.conditions                                  OK
zabbix.config                                      OK
zabbix.corr_condition                              OK
zabbix.corr_condition_group                        OK
zabbix.corr_condition_tag                          OK
zabbix.corr_condition_tagpair                      OK
zabbix.corr_condition_tagvalue                     OK
zabbix.corr_operation                              OK
zabbix.correlation                                 OK
zabbix.dbversion                                   OK
zabbix.dchecks                                     OK
zabbix.dhosts                                      OK
zabbix.drules                                      OK
zabbix.dservices                                   OK
zabbix.escalations                                 OK
zabbix.event_recovery                              OK
zabbix.event_tag                                   OK
zabbix.events                                      OK
zabbix.expressions                                 OK
zabbix.functions                                   OK
zabbix.globalmacro                                 OK
zabbix.globalvars                                  OK
zabbix.graph_discovery                             OK
zabbix.graph_theme                                 OK
zabbix.graphs                                      OK
zabbix.graphs_items                                OK
zabbix.group_discovery                             OK
zabbix.group_prototype                             OK
zabbix.groups                                      OK
zabbix.history                                     OK
zabbix.history_log                                 OK
zabbix.history_str                                 OK
zabbix.history_text                                OK
zabbix.history_uint                                OK
zabbix.host_discovery                              OK
zabbix.host_inventory                              OK
zabbix.hostmacro                                   OK
zabbix.hosts                                       OK
zabbix.hosts_groups                                OK
zabbix.hosts_templates                             OK
zabbix.housekeeper                                 OK
zabbix.httpstep                                    OK
zabbix.httpstepitem                                OK
zabbix.httptest                                    OK
zabbix.httptestitem                                OK
zabbix.icon_map                                    OK
zabbix.icon_mapping                                OK
zabbix.ids                                         OK
zabbix.images                                      OK
zabbix.interface                                   OK
zabbix.interface_discovery                         OK
zabbix.item_application_prototype                  OK
zabbix.item_condition                              OK
zabbix.item_discovery                              OK
zabbix.items                                       OK
zabbix.items_applications                          OK
zabbix.maintenances                                OK
zabbix.maintenances_groups                         OK
zabbix.maintenances_hosts                          OK
zabbix.maintenances_windows                        OK
zabbix.mappings                                    OK
zabbix.media                                       OK
zabbix.media_type                                  OK
zabbix.opcommand                                   OK
zabbix.opcommand_grp                               OK
zabbix.opcommand_hst                               OK
zabbix.opconditions                                OK
zabbix.operations                                  OK
zabbix.opgroup                                     OK
zabbix.opinventory                                 OK
zabbix.opmessage                                   OK
zabbix.opmessage_grp                               OK
zabbix.opmessage_usr                               OK
zabbix.optemplate                                  OK
zabbix.problem                                     OK
zabbix.problem_tag                                 OK
zabbix.profiles                                    OK
zabbix.proxy_autoreg_host                          OK
zabbix.proxy_dhistory                              OK
zabbix.proxy_history                               OK
zabbix.regexps                                     OK
zabbix.rights                                      OK
zabbix.screen_user                                 OK
zabbix.screen_usrgrp                               OK
zabbix.screens                                     OK
zabbix.screens_items                               OK
zabbix.scripts                                     OK
zabbix.service_alarms                              OK
zabbix.services                                    OK
zabbix.services_links                              OK
zabbix.services_times                              OK
zabbix.sessions                                    OK
zabbix.slides                                      OK
zabbix.slideshow_user                              OK
zabbix.slideshow_usrgrp                            OK
zabbix.slideshows                                  OK
zabbix.sysmap_element_url                          OK
zabbix.sysmap_url                                  OK
zabbix.sysmap_user                                 OK
zabbix.sysmap_usrgrp                               OK
zabbix.sysmaps                                     OK
zabbix.sysmaps_elements                            OK
zabbix.sysmaps_link_triggers                       OK
zabbix.sysmaps_links                               OK
zabbix.task                                        OK
zabbix.task_close_problem                          OK
zabbix.timeperiods                                 OK
zabbix.trends                                      OK
zabbix.trends_uint                                 OK
zabbix.trigger_depends                             OK
zabbix.trigger_discovery                           OK
zabbix.trigger_tag                                 OK
zabbix.triggers                                    OK
zabbix.users                                       OK
zabbix.users_groups                                OK
zabbix.usrgrp                                      OK
zabbix.valuemaps                                   OK
zabbix_yewu.acknowledges                           OK
zabbix_yewu.actions                                OK
zabbix_yewu.alerts                                 OK
zabbix_yewu.application_discovery                  OK
zabbix_yewu.application_prototype                  OK
zabbix_yewu.application_template                   OK
zabbix_yewu.applications                           OK
zabbix_yewu.auditlog                               OK
zabbix_yewu.auditlog_details                       OK
zabbix_yewu.autoreg_host                           OK
zabbix_yewu.conditions                             OK
zabbix_yewu.config                                 OK
zabbix_yewu.corr_condition                         OK
zabbix_yewu.corr_condition_group                   OK
zabbix_yewu.corr_condition_tag                     OK
zabbix_yewu.corr_condition_tagpair                 OK
zabbix_yewu.corr_condition_tagvalue                OK
zabbix_yewu.corr_operation                         OK
zabbix_yewu.correlation                            OK
zabbix_yewu.dbversion                              OK
zabbix_yewu.dchecks                                OK
zabbix_yewu.dhosts                                 OK
zabbix_yewu.drules                                 OK
zabbix_yewu.dservices                              OK
zabbix_yewu.escalations                            OK
zabbix_yewu.event_recovery                         OK
zabbix_yewu.event_tag                              OK
zabbix_yewu.events                                 OK
zabbix_yewu.expressions                            OK
zabbix_yewu.functions                              OK
zabbix_yewu.globalmacro                            OK
zabbix_yewu.globalvars                             OK
zabbix_yewu.graph_discovery                        OK
zabbix_yewu.graph_theme                            OK
zabbix_yewu.graphs                                 OK
zabbix_yewu.graphs_items                           OK
zabbix_yewu.group_discovery                        OK
zabbix_yewu.group_prototype                        OK
zabbix_yewu.groups                                 OK
zabbix_yewu.history                                OK
zabbix_yewu.history_log                            OK
zabbix_yewu.history_str                            OK
zabbix_yewu.history_text                           OK
zabbix_yewu.history_uint                           OK
zabbix_yewu.host_discovery                         OK
zabbix_yewu.host_inventory                         OK
zabbix_yewu.hostmacro                              OK
zabbix_yewu.hosts                                  OK
zabbix_yewu.hosts_groups                           OK
zabbix_yewu.hosts_templates                        OK
zabbix_yewu.housekeeper                            OK
zabbix_yewu.httpstep                               OK
zabbix_yewu.httpstepitem                           OK
zabbix_yewu.httptest                               OK
zabbix_yewu.httptestitem                           OK
zabbix_yewu.icon_map                               OK
zabbix_yewu.icon_mapping                           OK
zabbix_yewu.ids                                    OK
zabbix_yewu.images                                 OK
zabbix_yewu.interface                              OK
zabbix_yewu.interface_discovery                    OK
zabbix_yewu.item_application_prototype             OK
zabbix_yewu.item_condition                         OK
zabbix_yewu.item_discovery                         OK
zabbix_yewu.items                                  OK
zabbix_yewu.items_applications                     OK
zabbix_yewu.maintenances                           OK
zabbix_yewu.maintenances_groups                    OK
zabbix_yewu.maintenances_hosts                     OK
zabbix_yewu.maintenances_windows                   OK
zabbix_yewu.mappings                               OK
zabbix_yewu.media                                  OK
zabbix_yewu.media_type                             OK
zabbix_yewu.opcommand                              OK
zabbix_yewu.opcommand_grp                          OK
zabbix_yewu.opcommand_hst                          OK
zabbix_yewu.opconditions                           OK
zabbix_yewu.operations                             OK
zabbix_yewu.opgroup                                OK
zabbix_yewu.opinventory                            OK
zabbix_yewu.opmessage                              OK
zabbix_yewu.opmessage_grp                          OK
zabbix_yewu.opmessage_usr                          OK
zabbix_yewu.optemplate                             OK
zabbix_yewu.problem                                OK
zabbix_yewu.problem_tag                            OK
zabbix_yewu.profiles                               OK
zabbix_yewu.proxy_autoreg_host                     OK
zabbix_yewu.proxy_dhistory                         OK
zabbix_yewu.proxy_history                          OK
zabbix_yewu.regexps                                OK
zabbix_yewu.rights                                 OK
zabbix_yewu.screen_user                            OK
zabbix_yewu.screen_usrgrp                          OK
zabbix_yewu.screens                                OK
zabbix_yewu.screens_items                          OK
zabbix_yewu.scripts                                OK
zabbix_yewu.service_alarms                         OK
zabbix_yewu.services                               OK
zabbix_yewu.services_links                         OK
zabbix_yewu.services_times                         OK
zabbix_yewu.sessions                               OK
zabbix_yewu.slides                                 OK
zabbix_yewu.slideshow_user                         OK
zabbix_yewu.slideshow_usrgrp                       OK
zabbix_yewu.slideshows                             OK
zabbix_yewu.sysmap_element_url                     OK
zabbix_yewu.sysmap_url                             OK
zabbix_yewu.sysmap_user                            OK
zabbix_yewu.sysmap_usrgrp                          OK
zabbix_yewu.sysmaps                                OK
zabbix_yewu.sysmaps_elements                       OK
zabbix_yewu.sysmaps_link_triggers                  OK
zabbix_yewu.sysmaps_links                          OK
zabbix_yewu.task                                   OK
zabbix_yewu.task_close_problem                     OK
zabbix_yewu.timeperiods                            OK
zabbix_yewu.trends                                 OK
zabbix_yewu.trends_uint                            OK
zabbix_yewu.trigger_depends                        OK
zabbix_yewu.trigger_discovery                      OK
zabbix_yewu.trigger_tag                            OK
zabbix_yewu.triggers                               OK
zabbix_yewu.users                                  OK
zabbix_yewu.users_groups                           OK
zabbix_yewu.usrgrp                                 OK
zabbix_yewu.valuemaps                              OK
Upgrade process completed successfully.
Checking if update is needed.
```

# 新老mysql版本
1. 老mysql
```
mysql> select version();
+------------+
| version()  |
+------------+
| 5.7.13-log |
+------------+
```

2. 新mysql

```
mysql> select version();
+-----------------------------+
| version()                   |
+-----------------------------+
| 5.7.27-0ubuntu0.16.04.1-log |
+-----------------------------+
```