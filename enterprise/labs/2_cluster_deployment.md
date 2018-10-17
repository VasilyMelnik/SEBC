{
  "timestamp" : "2018-10-17T09:42:57.908Z",
  "clusters" : [ {
    "name" : "VasilyMelnik",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "1698693120"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "169869312"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "829423616"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "1877947187"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "316"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "instance-2.europe-north1-a.c.cloudera-218907.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "123456"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-1c18658e3ae374c37c5ed8dd464888dc",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-1c7ae2e3daed6497aa99fcced56d312d",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "3ce8d240-cc6b-40ec-88a1-2d2b09de878a"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-8224a9d3eb629a79144c9a3eeb827b54",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "538f7aae-58a5-40f3-84c6-355a27e48f4d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-96ccd50a21b987a8eb08865c1d02f0e8",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "df479fdd-b961-4c56-ae75-7b6ee513f616"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-1c18658e3ae374c37c5ed8dd464888dc",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9f2py2inpbgsuthgv3xwhky9s"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1xryvzicgnjslzdfcyik0mlwi"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "service_health_suppression_zookeeper_canary_health",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-1c7ae2e3daed6497aa99fcced56d312d",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "3ce8d240-cc6b-40ec-88a1-2d2b09de878a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3wsc5npnyjrs85xd2uftfksyr"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-8224a9d3eb629a79144c9a3eeb827b54",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "538f7aae-58a5-40f3-84c6-355a27e48f4d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7l7zujhk347k48f3w5cysx3qk"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-96ccd50a21b987a8eb08865c1d02f0e8",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "df479fdd-b961-4c56-ae75-7b6ee513f616"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "r5d2ceakc7zscu81fc1rlh3n"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "instance-2.europe-north1-a.c.cloudera-218907.internal"
        }, {
          "name" : "database_password",
          "value" : "123456"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-f03899e2cd6cea8e8e9a4f56f40e07d2"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dto38fjqt6p5pzz4amlxxevsz"
          } ]
        }
      }, {
        "name" : "hue-HUE_SERVER-1c18658e3ae374c37c5ed8dd464888dc",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "243d2ec8-c47a-458b-967c-6d34f5ad9550"
          }, {
            "name" : "role_jceks_password",
            "value" : "at5pzsvkax9l9bb0x9rnbb7dc"
          }, {
            "name" : "secret_key",
            "value" : "xbefn0UZJt0DfEwiDkjDBp5KtaGYgI"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "instance-2.europe-north1-a.c.cloudera-218907.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "123456"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-1c18658e3ae374c37c5ed8dd464888dc",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7l2l04jv8g9lkbk4noe1xjsiv"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "3"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "829423616"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "3147"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "resource_manager_java_heapsize",
            "value" : "829423616"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "3147"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_scheduler_minimum_allocation_mb",
            "value" : "128"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "true"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "9OELMsywfJQCbwJOnzJVIwP9UFgD0d"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "45s8y4w4koi68rogiu14bcdng"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1c7ae2e3daed6497aa99fcced56d312d",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "3ce8d240-cc6b-40ec-88a1-2d2b09de878a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_health_suppression_node_manager_unexpected_exits",
            "value" : "true"
          }, {
            "name" : "role_jceks_password",
            "value" : "2r3jkgzcxwl9r9mkz51ntfgrh"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-8224a9d3eb629a79144c9a3eeb827b54",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "538f7aae-58a5-40f3-84c6-355a27e48f4d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "e980j6dc4ddbzez91l3wplris"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-96ccd50a21b987a8eb08865c1d02f0e8",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "df479fdd-b961-4c56-ae75-7b6ee513f616"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "25y8urb6xdqdlgv1gutwi4jzb"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "55"
          }, {
            "name" : "role_jceks_password",
            "value" : "c4ccdox7ew20o5epjrvfeihg1"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "829423616"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "4293264998"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_hosts_decommission",
            "value" : "instance-2.europe-north1-a.c.cloudera-218907.internal"
          }, {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "829423616"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "829423616"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "RJegjFZZbm8L7JE1yPhfW3ta5Uop8V"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "ghHVFyEBJLUiKqJMNGTUoy0huq5BHa"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "JurFCv8xuep1w0rywWPWn74uDnXd1L"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "service_health_suppression_hdfs_blocks_with_corrupt_replicas",
          "value" : "true"
        }, {
          "name" : "service_health_suppression_hdfs_missing_blocks",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-1c18658e3ae374c37c5ed8dd464888dc",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "61rdgsdtjgudzxnyy1du1azn1"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-1c7ae2e3daed6497aa99fcced56d312d",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "3ce8d240-cc6b-40ec-88a1-2d2b09de878a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dd6jgh6in8070ugeckgz9k4u8"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-8224a9d3eb629a79144c9a3eeb827b54",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "538f7aae-58a5-40f3-84c6-355a27e48f4d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8mv0dcgvn9qaznzehzo6a7y6f"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-96ccd50a21b987a8eb08865c1d02f0e8",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "df479fdd-b961-4c56-ae75-7b6ee513f616"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c4ddk78pun2vlkh2v98r3xmd2"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-1c18658e3ae374c37c5ed8dd464888dc",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3a47khdqbj0hxgps6c9rvzfyf"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ezjv6g7my651u2vyfcdui3xva"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-1c7ae2e3daed6497aa99fcced56d312d",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "3ce8d240-cc6b-40ec-88a1-2d2b09de878a"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4g5ngptimbj3nzccfqnlldjjo"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-8224a9d3eb629a79144c9a3eeb827b54",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "538f7aae-58a5-40f3-84c6-355a27e48f4d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "629lpuufskg6gimico53foqd5"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-96ccd50a21b987a8eb08865c1d02f0e8",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "df479fdd-b961-4c56-ae75-7b6ee513f616"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5vkzlfgdn4z5xd0vdrguac9zn"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-1c18658e3ae374c37c5ed8dd464888dc",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "63"
          }, {
            "name" : "role_jceks_password",
            "value" : "1s6s3pjdz0whjpa445a7luj3e"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-f03899e2cd6cea8e8e9a4f56f40e07d2",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "57"
          }, {
            "name" : "role_jceks_password",
            "value" : "bfy105bao75hg67kcy0lrvked"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf",
    "ipAddress" : "10.166.0.3",
    "hostname" : "instance-2.europe-north1-a.c.cloudera-218907.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98",
    "ipAddress" : "10.166.0.4",
    "hostname" : "instance-3.europe-north1-a.c.cloudera-218907.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "538f7aae-58a5-40f3-84c6-355a27e48f4d",
    "ipAddress" : "10.166.0.5",
    "hostname" : "instance-4.europe-north1-a.c.cloudera-218907.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "df479fdd-b961-4c56-ae75-7b6ee513f616",
    "ipAddress" : "10.166.0.6",
    "hostname" : "instance-5.europe-north1-a.c.cloudera-218907.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "3ce8d240-cc6b-40ec-88a1-2d2b09de878a",
    "ipAddress" : "10.166.0.2",
    "hostname" : "instance-6.europe-north1-a.c.cloudera-218907.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "VasilyMelnik",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "74f2620207fb894e2e911747934ec3af0969d521a31a18f281f8263c6395e9a8",
    "pwSalt" : 5045114991944036444,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-1c18658e3ae374c37c5ed8dd464888dc",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "faeb26e6de5d1c2cf376ed7951a76404ccfd07214295e407c2dd52deb6f3b617",
    "pwSalt" : -5674417758380137086,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-f03899e2cd6cea8e8e9a4f56f40e07d2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b580ad94ddc55e346a1e30e836697208ca9e39d29d9a09b07a9931f28177ad33",
    "pwSalt" : -3159609385906703434,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-f03899e2cd6cea8e8e9a4f56f40e07d2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f2e952afe5ab22e2723c95d710bf6b47aa6ef7fdfc10a67f5d1e87bc3f51276a",
    "pwSalt" : -9042356096959963344,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-1c18658e3ae374c37c5ed8dd464888dc",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "3a3076733e09db91353d1719505e6832ce9ef24f4cb2ea1f06d2dddf3c282eec",
    "pwSalt" : 2958066202952560029,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-f03899e2cd6cea8e8e9a4f56f40e07d2",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "cf6ba99dc5983598befe867c8b0b23f3cbd486aa714854d9db64fcf962c4b58d",
    "pwSalt" : -1748067693867530765,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "06408e1196754a10e8f61294c09a6fb9ae671f0f529f16793078d35c4b2dc5ce",
    "pwSalt" : 7955501063888580792,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "cdaac31cf0516baafa356042bc084666e3606e7cca6f23c00c405293a7e606ca",
    "pwSalt" : -8479924341922972576,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.15.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20180731-0834",
    "gitHash" : "6e046fd999fd99e7e12299386ba69b23afa43c60",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "829423616"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "829423616"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1077936128"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "instance-2.europe-north1-a.c.cloudera-218907.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "123456"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "829423616"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1077936128"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-f03899e2cd6cea8e8e9a4f56f40e07d2",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7wcugq0n671ir17gdl37vb8ro"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-f03899e2cd6cea8e8e9a4f56f40e07d2",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3afqkzc8okgog6sxiapv3wkqs"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-f03899e2cd6cea8e8e9a4f56f40e07d2",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "akmq1anrw32r7u2wuhcqdf78y"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-1c18658e3ae374c37c5ed8dd464888dc",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "615e4d9e-eb74-4320-90a2-6afead8a03cf"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3r5b3rupe5ttsptqabbf95wg1"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-f03899e2cd6cea8e8e9a4f56f40e07d2",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "70ccd253-578d-4d61-ad88-1f83a6484f98"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "27ff3o4995heronnj2tbufwb9"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/21/2012 18:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "NOT_ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.13.3.2/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }
}