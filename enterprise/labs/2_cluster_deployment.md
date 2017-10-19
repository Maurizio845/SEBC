```

{
	"timestamp": "2017-10-18T12:02:09.114Z",
	"clusters": [{
		"name": "Maurizio845",
		"version": "CDH5",
		"services": [{
			"name": "zookeeper",
			"type": "ZOOKEEPER",
			"config": {
				"roleTypeConfigs": [{
					"roleType": "SERVER",
					"items": [{
						"name": "zookeeper_server_java_heapsize",
						"value": "851443712"
					}]
				}],
				"items": []
			},
			"roles": [{
				"name": "zookeeper-SERVER-0c5f413bf1f1bd3469685fe733595204",
				"type": "SERVER",
				"hostRef": {
					"hostId": "i-0d21923d1c466f447"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "4lrtdlfaa17448eignuyuoa8l"
					}, {
						"name": "serverId",
						"value": "2"
					}]
				}
			}, {
				"name": "zookeeper-SERVER-eb4cebab6d3bdb6893e5f3174b2a1920",
				"type": "SERVER",
				"hostRef": {
					"hostId": "i-0bc61918d34d60c52"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "1j6dsbpwcvg3rhpayxs7suw5b"
					}, {
						"name": "serverId",
						"value": "1"
					}]
				}
			}, {
				"name": "zookeeper-SERVER-f8c4b8c87f39e0728b68ea1ed9c3199c",
				"type": "SERVER",
				"hostRef": {
					"hostId": "i-04ed825ee0ab25be6"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "zqzz2cv0el6k8wdw9xtt4yjq"
					}, {
						"name": "serverId",
						"value": "3"
					}]
				}
			}],
			"displayName": "ZooKeeper"
		}, {
			"name": "yarn",
			"type": "YARN",
			"config": {
				"roleTypeConfigs": [{
					"roleType": "GATEWAY",
					"items": [{
						"name": "mapred_reduce_tasks",
						"value": "4"
					}, {
						"name": "mapred_submit_replication",
						"value": "1"
					}]
				}, {
					"roleType": "NODEMANAGER",
					"items": [{
						"name": "rm_cpu_shares",
						"value": "1800"
					}, {
						"name": "rm_io_weight",
						"value": "900"
					}, {
						"name": "yarn_nodemanager_heartbeat_interval_ms",
						"value": "100"
					}, {
						"name": "yarn_nodemanager_local_dirs",
						"value": "/yarn/nm"
					}, {
						"name": "yarn_nodemanager_log_dirs",
						"value": "/yarn/container-logs"
					}, {
						"name": "yarn_nodemanager_resource_cpu_vcores",
						"value": "3"
					}, {
						"name": "yarn_nodemanager_resource_memory_mb",
						"value": "2048"
					}]
				}, {
					"roleType": "RESOURCEMANAGER",
					"items": [{
						"name": "yarn_scheduler_maximum_allocation_mb",
						"value": "4096"
					}, {
						"name": "yarn_scheduler_maximum_allocation_vcores",
						"value": "3"
					}, {
						"name": "yarn_scheduler_minimum_allocation_mb",
						"value": "512"
					}]
				}],
				"items": [{
					"name": "hdfs_service",
					"value": "hdfs"
				}, {
					"name": "rm_dirty",
					"value": "true"
				}, {
					"name": "rm_last_allocation_percentage",
					"value": "90"
				}, {
					"name": "yarn_service_cgroups",
					"value": "false"
				}, {
					"name": "yarn_service_lce_always",
					"value": "false"
				}, {
					"name": "zk_authorization_secret_key",
					"value": "VmieCqjItnqRC2LjZ36cCi5qK4pNqg"
				}, {
					"name": "zookeeper_service",
					"value": "zookeeper"
				}]
			},
			"roles": [{
				"name": "yarn-GATEWAY-7de3dcb304dd5ab7155b7a4eb6d975b5",
				"type": "GATEWAY",
				"hostRef": {
					"hostId": "i-0f263fc29c46f8ae7"
				},
				"config": {
					"items": []
				}
			}, {
				"name": "yarn-JOBHISTORY-eb4cebab6d3bdb6893e5f3174b2a1920",
				"type": "JOBHISTORY",
				"hostRef": {
					"hostId": "i-0bc61918d34d60c52"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "bi4s81ctezhiia5nvxvkg5cd7"
					}]
				}
			}, {
				"name": "yarn-NODEMANAGER-0c5f413bf1f1bd3469685fe733595204",
				"type": "NODEMANAGER",
				"hostRef": {
					"hostId": "i-0d21923d1c466f447"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "69pvlxicpgwxl9mrluetnq4g0"
					}]
				}
			}, {
				"name": "yarn-NODEMANAGER-eb4cebab6d3bdb6893e5f3174b2a1920",
				"type": "NODEMANAGER",
				"hostRef": {
					"hostId": "i-0bc61918d34d60c52"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "4qmhcx9z1tq17rpsdnvlw2d1c"
					}]
				}
			}, {
				"name": "yarn-NODEMANAGER-f8c4b8c87f39e0728b68ea1ed9c3199c",
				"type": "NODEMANAGER",
				"hostRef": {
					"hostId": "i-04ed825ee0ab25be6"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "aedpxycnsm6im7wo16akbstqv"
					}]
				}
			}, {
				"name": "yarn-RESOURCEMANAGER-f8c4b8c87f39e0728b68ea1ed9c3199c",
				"type": "RESOURCEMANAGER",
				"hostRef": {
					"hostId": "i-04ed825ee0ab25be6"
				},
				"config": {
					"items": [{
						"name": "rm_id",
						"value": "31"
					}, {
						"name": "role_jceks_password",
						"value": "841onkexpjc1s36qe1957aidm"
					}]
				}
			}],
			"displayName": "YARN (MR2 Included)"
		}, {
			"name": "hdfs",
			"type": "HDFS",
			"config": {
				"roleTypeConfigs": [{
					"roleType": "DATANODE",
					"items": [{
						"name": "datanode_java_heapsize",
						"value": "1073741824"
					}, {
						"name": "dfs_data_dir_list",
						"value": "/dfs/dn"
					}, {
						"name": "dfs_datanode_du_reserved",
						"value": "5270942105"
					}, {
						"name": "dfs_datanode_max_locked_memory",
						"value": "4294967296"
					}, {
						"name": "rm_cpu_shares",
						"value": "200"
					}, {
						"name": "rm_io_weight",
						"value": "100"
					}]
				}, {
					"roleType": "GATEWAY",
					"items": [{
						"name": "dfs_client_use_trash",
						"value": "true"
					}]
				}, {
					"roleType": "JOURNALNODE",
					"items": [{
						"name": "dfs_journalnode_edits_dir",
						"value": "/dfs/jn"
					}]
				}, {
					"roleType": "NAMENODE",
					"items": [{
						"name": "dfs_name_dir_list",
						"value": "/dfs/nn"
					}, {
						"name": "dfs_namenode_servicerpc_address",
						"value": "8022"
					}, {
						"name": "namenode_java_heapsize",
						"value": "1781530624"
					}]
				}, {
					"roleType": "SECONDARYNAMENODE",
					"items": [{
						"name": "fs_checkpoint_dir_list",
						"value": "/dfs/snn"
					}, {
						"name": "secondary_namenode_java_heapsize",
						"value": "1781530624"
					}]
				}],
				"items": [{
					"name": "dfs_ha_fencing_cloudera_manager_secret_key",
					"value": "NfXYbWqZ992Bz0pR3THbZowEZHdPGZ"
				}, {
					"name": "dfs_ha_fencing_methods",
					"value": "shell(true)"
				}, {
					"name": "fc_authorization_secret_key",
					"value": "4bg6oErTxwPaSdz7L2hBEfNyz3bBhC"
				}, {
					"name": "http_auth_signature_secret",
					"value": "E6fXmITDY60px9lMXMRoTaJCcZv34Q"
				}, {
					"name": "rm_dirty",
					"value": "false"
				}, {
					"name": "rm_last_allocation_percentage",
					"value": "10"
				}, {
					"name": "zookeeper_service",
					"value": "zookeeper"
				}]
			},
			"roles": [{
				"name": "hdfs-DATANODE-0c5f413bf1f1bd3469685fe733595204",
				"type": "DATANODE",
				"hostRef": {
					"hostId": "i-0d21923d1c466f447"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "2bl512e3csbgdkmmlxomdfjoz"
					}]
				}
			}, {
				"name": "hdfs-DATANODE-eb4cebab6d3bdb6893e5f3174b2a1920",
				"type": "DATANODE",
				"hostRef": {
					"hostId": "i-0bc61918d34d60c52"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "cdon0uc5pb91rvaoz54yd68aw"
					}]
				}
			}, {
				"name": "hdfs-DATANODE-f8c4b8c87f39e0728b68ea1ed9c3199c",
				"type": "DATANODE",
				"hostRef": {
					"hostId": "i-04ed825ee0ab25be6"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "1p4ptrstjwb3hmt5iyj1stmqs"
					}]
				}
			}, {
				"name": "hdfs-FAILOVERCONTROLLER-eb4cebab6d3bdb6893e5f3174b2a1920",
				"type": "FAILOVERCONTROLLER",
				"hostRef": {
					"hostId": "i-0bc61918d34d60c52"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "aweza5wow2axl8q07ihzyg65c"
					}]
				}
			}, {
				"name": "hdfs-FAILOVERCONTROLLER-f8c4b8c87f39e0728b68ea1ed9c3199c",
				"type": "FAILOVERCONTROLLER",
				"hostRef": {
					"hostId": "i-04ed825ee0ab25be6"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "al0hy83uojpceq3jtwp688h59"
					}]
				}
			}, {
				"name": "hdfs-GATEWAY-7de3dcb304dd5ab7155b7a4eb6d975b5",
				"type": "GATEWAY",
				"hostRef": {
					"hostId": "i-0f263fc29c46f8ae7"
				},
				"config": {
					"items": []
				}
			}, {
				"name": "hdfs-JOURNALNODE-8397292c02b410400737bd1ac37a2948",
				"type": "JOURNALNODE",
				"hostRef": {
					"hostId": "i-0247564d43c6800b0"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "5b9n5wsf1qiotd9nvqn15gg11"
					}]
				}
			}, {
				"name": "hdfs-JOURNALNODE-eb4cebab6d3bdb6893e5f3174b2a1920",
				"type": "JOURNALNODE",
				"hostRef": {
					"hostId": "i-0bc61918d34d60c52"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "4f6amqgwy5ogvjqrosbpcza1e"
					}]
				}
			}, {
				"name": "hdfs-JOURNALNODE-f8c4b8c87f39e0728b68ea1ed9c3199c",
				"type": "JOURNALNODE",
				"hostRef": {
					"hostId": "i-04ed825ee0ab25be6"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "40x2pcmis52h8ak9p4tjytku"
					}]
				}
			}, {
				"name": "hdfs-NAMENODE-eb4cebab6d3bdb6893e5f3174b2a1920",
				"type": "NAMENODE",
				"hostRef": {
					"hostId": "i-0bc61918d34d60c52"
				},
				"config": {
					"items": [{
						"name": "autofailover_enabled",
						"value": "true"
					}, {
						"name": "dfs_federation_namenode_nameservice",
						"value": "nameservice1"
					}, {
						"name": "dfs_namenode_quorum_journal_name",
						"value": "nameservice1"
					}, {
						"name": "namenode_id",
						"value": "40"
					}, {
						"name": "role_jceks_password",
						"value": "aep2regg3cdqbq03mwu6zkqno"
					}]
				}
			}, {
				"name": "hdfs-NAMENODE-f8c4b8c87f39e0728b68ea1ed9c3199c",
				"type": "NAMENODE",
				"hostRef": {
					"hostId": "i-04ed825ee0ab25be6"
				},
				"config": {
					"items": [{
						"name": "autofailover_enabled",
						"value": "true"
					}, {
						"name": "dfs_federation_namenode_nameservice",
						"value": "nameservice1"
					}, {
						"name": "dfs_namenode_quorum_journal_name",
						"value": "nameservice1"
					}, {
						"name": "namenode_id",
						"value": "33"
					}, {
						"name": "role_jceks_password",
						"value": "19fo9v5ldt78fdldavy252muk"
					}]
				}
			}, {
				"name": "hdfs-NFSGATEWAY-7de3dcb304dd5ab7155b7a4eb6d975b5",
				"type": "NFSGATEWAY",
				"hostRef": {
					"hostId": "i-0f263fc29c46f8ae7"
				},
				"config": {
					"items": [{
						"name": "role_jceks_password",
						"value": "77zg0hsn5weghxn7qxobrluqb"
					}]
				}
			}],
			"displayName": "HDFS"
		}]
	}],
	"hosts": [{
		"hostId": "i-0d21923d1c466f447",
		"ipAddress": "172.31.18.0",
		"hostname": "ip-172-31-18-0.eu-central-1.compute.internal",
		"rackId": "/default",
		"config": {
			"items": []
		}
	}, {
		"hostId": "i-0bc61918d34d60c52",
		"ipAddress": "172.31.22.85",
		"hostname": "ip-172-31-22-85.eu-central-1.compute.internal",
		"rackId": "/default",
		"config": {
			"items": []
		}
	}, {
		"hostId": "i-0f263fc29c46f8ae7",
		"ipAddress": "172.31.25.67",
		"hostname": "ip-172-31-25-67.eu-central-1.compute.internal",
		"rackId": "/default",
		"config": {
			"items": []
		}
	}, {
		"hostId": "i-04ed825ee0ab25be6",
		"ipAddress": "172.31.26.116",
		"hostname": "ip-172-31-26-116.eu-central-1.compute.internal",
		"rackId": "/default",
		"config": {
			"items": []
		}
	}, {
		"hostId": "i-0247564d43c6800b0",
		"ipAddress": "172.31.29.107",
		"hostname": "ip-172-31-29-107.eu-central-1.compute.internal",
		"rackId": "/default",
		"config": {
			"items": []
		}
	}],
	"users": [{
		"name": "Maurizio845",
		"roles": ["ROLE_ADMIN"],
		"pwHash": "6b0ec9dbf53b1838bdf9bd413e52eb30019d5cb2753dd61fa5e67774e2b6b7bf",
		"pwSalt": -2790361905037284388,
		"pwLogin": true
	}, {
		"name": "__cloudera_internal_user__mgmt-EVENTSERVER-0c5f413bf1f1bd3469685fe733595204",
		"roles": ["ROLE_USER"],
		"pwHash": "22c16a6015109595e367350db21c90a6f2c97a566d8187494bf9ae76b130e5dc",
		"pwSalt": -2307417368266220194,
		"pwLogin": true
	}, {
		"name": "__cloudera_internal_user__mgmt-HOSTMONITOR-0c5f413bf1f1bd3469685fe733595204",
		"roles": ["ROLE_USER"],
		"pwHash": "7c718fba1458c101176acd05fd28228e2e39b51d9a318c38a1366698ab8c756c",
		"pwSalt": -954362658986704271,
		"pwLogin": true
	}, {
		"name": "__cloudera_internal_user__mgmt-REPORTSMANAGER-0c5f413bf1f1bd3469685fe733595204",
		"roles": ["ROLE_USER"],
		"pwHash": "d4604fbe957e7f36692afa5b5bc4f95fb8b7614a40949afa42547168c660fb14",
		"pwSalt": -940517503849045497,
		"pwLogin": true
	}, {
		"name": "__cloudera_internal_user__mgmt-SERVICEMONITOR-0c5f413bf1f1bd3469685fe733595204",
		"roles": ["ROLE_USER"],
		"pwHash": "3ff737c2fec546fe181c2b09314198f5e3a190e6033a1ae219f94c644cf451f9",
		"pwSalt": 7987070509490411077,
		"pwLogin": true
	}, {
		"name": "admin",
		"roles": ["ROLE_LIMITED"],
		"pwHash": "0fc7093056f10a9514c9f8219599907e1c559f7f9335acc75e72686e02a3da57",
		"pwSalt": 2662467643084213306,
		"pwLogin": true
	}, {
		"name": "minotaur ",
		"roles": ["ROLE_CONFIGURATOR"],
		"pwHash": "5283812e129fd14366fe35ddb69915243ba632b0aece4f0a6de03a310d44ded5",
		"pwSalt": -6472878657528556918,
		"pwLogin": true
	}, {
		"name": "minotaur01",
		"roles": ["ROLE_CONFIGURATOR"],
		"pwHash": "d8901d6d7c8a8e3291996b096c49aa0b9d122e9712b6a9f813a122b2136f2053",
		"pwSalt": 6558550456130766379,
		"pwLogin": true
	}],
	"versionInfo": {
		"version": "5.8.3",
		"buildUser": "jenkins",
		"buildTimestamp": "20161019-1014",
		"gitHash": "518f0d6d44abc87bc392646e4369a20c8192b7cf",
		"snapshot": false
	},
	"managementService": {
		"name": "mgmt",
		"type": "MGMT",
		"config": {
			"roleTypeConfigs": [{
				"roleType": "EVENTSERVER",
				"items": [{
					"name": "event_server_heapsize",
					"value": "851443712"
				}]
			}, {
				"roleType": "HOSTMONITOR",
				"items": [{
					"name": "firehose_heapsize",
					"value": "851443712"
				}, {
					"name": "firehose_non_java_memory_bytes",
					"value": "1107296256"
				}]
			}, {
				"roleType": "REPORTSMANAGER",
				"items": [{
					"name": "headlamp_database_host",
					"value": "ip-172-31-26-116.eu-central-1.compute.internal"
				}, {
					"name": "headlamp_database_name",
					"value": "rman"
				}, {
					"name": "headlamp_database_password",
					"value": "rman"
				}, {
					"name": "headlamp_database_user",
					"value": "rman"
				}, {
					"name": "headlamp_heapsize",
					"value": "851443712"
				}]
			}, {
				"roleType": "SERVICEMONITOR",
				"items": [{
					"name": "firehose_heapsize",
					"value": "851443712"
				}, {
					"name": "firehose_non_java_memory_bytes",
					"value": "1107296256"
				}]
			}],
			"items": []
		},
		"roles": [{
			"name": "mgmt-ALERTPUBLISHER-0c5f413bf1f1bd3469685fe733595204",
			"type": "ALERTPUBLISHER",
			"hostRef": {
				"hostId": "i-0d21923d1c466f447"
			},
			"config": {
				"items": [{
					"name": "role_jceks_password",
					"value": "a0yp5fzk5sp4jgcxgt3ugsuxt"
				}]
			}
		}, {
			"name": "mgmt-EVENTSERVER-0c5f413bf1f1bd3469685fe733595204",
			"type": "EVENTSERVER",
			"hostRef": {
				"hostId": "i-0d21923d1c466f447"
			},
			"config": {
				"items": [{
					"name": "role_jceks_password",
					"value": "ata6nsnlbst8621y92wiwowjc"
				}]
			}
		}, {
			"name": "mgmt-HOSTMONITOR-0c5f413bf1f1bd3469685fe733595204",
			"type": "HOSTMONITOR",
			"hostRef": {
				"hostId": "i-0d21923d1c466f447"
			},
			"config": {
				"items": [{
					"name": "role_jceks_password",
					"value": "1rpr423am0bvb5cwasy69gs9p"
				}]
			}
		}, {
			"name": "mgmt-REPORTSMANAGER-0c5f413bf1f1bd3469685fe733595204",
			"type": "REPORTSMANAGER",
			"hostRef": {
				"hostId": "i-0d21923d1c466f447"
			},
			"config": {
				"items": [{
					"name": "role_jceks_password",
					"value": "63rjv39v9p48ppkqolmtqoat2"
				}]
			}
		}, {
			"name": "mgmt-SERVICEMONITOR-0c5f413bf1f1bd3469685fe733595204",
			"type": "SERVICEMONITOR",
			"hostRef": {
				"hostId": "i-0d21923d1c466f447"
			},
			"config": {
				"items": [{
					"name": "role_jceks_password",
					"value": "6bk5lt0zbqh9q10eci78w0iwb"
				}]
			}
		}],
		"displayName": "Cloudera Management Service"
	},
	"managerSettings": {
		"items": [{
			"name": "CLUSTER_STATS_START",
			"value": "10/26/2012 19:10"
		}, {
			"name": "PUBLIC_CLOUD_STATUS",
			"value": "ON_PUBLIC_CLOUD"
		}, {
			"name": "REMOTE_PARCEL_REPO_URLS",
			"value": "https://archive.cloudera.com/cdh5/parcels/5.8.3/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
		}]
	}
}

```