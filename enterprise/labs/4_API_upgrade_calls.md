```
[root@ip-172-31-6-242 centos]# curl -u admin:admin 'http://13.59.169.94:7180/api/version'
v16
[root@ip-172-31-6-242 centos]# curl -u admin:admin 'http://13.59.169.94:7180/api/v16/cm/version'
{
  "version" : "5.11.2",
  "buildUser" : "jenkins",
  "buildTimestamp" : "20170811-0014",
  "gitHash" : "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
  "snapshot" : false
}
[root@ip-172-31-6-242 centos]# curl -u admin:admin 'http://13.59.169.94:7180/api/v16/users'
{
  "items" : [ {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ]
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ]
  }, {
    "name" : "wjguerrero",
    "roles" : [ "ROLE_ADMIN" ]
  } ]
}
[root@ip-172-31-6-242 centos]# curl -u admin:admin 'http://13.59.169.94:7180/api/v16/cm/config'
{
  "items" : [ {
    "name" : "CLUSTER_STATS_START",
    "value" : "10/27/2012 18:40",
    "sensitive" : false
  }, {
    "name" : "KDC_HOST",
    "value" : "ip-172-31-6-242.us-east-2.compute.internal",
    "sensitive" : false
  }, {
    "name" : "KRB_ENC_TYPES",
    "value" : "arcfour-hmac",
    "sensitive" : false
  }, {
    "name" : "KRB_MANAGE_KRB5_CONF",
    "value" : "true",
    "sensitive" : false
  }, {
    "name" : "MAX_RENEW_LIFE",
    "value" : "604800",
    "sensitive" : false
  }, {
    "name" : "REMOTE_PARCEL_REPO_URLS",
    "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/",
    "sensitive" : false
  }, {
    "name" : "SECURITY_REALM",
    "value" : "WGSEBC.COM",
    "sensitive" : false
  } ]
}
[root@ip-172-31-6-242 centos]# curl -u admin:admin 'http://13.59.169.94:7180/api/v16/cm/scmDbInfo'
{
  "scmDbType" : "MYSQL",
  "embeddedDbUsed" : false
}
[root@ip-172-31-6-242 centos]# curl -u admin:admin 'http://13.59.169.94:7180/api/v16/cm/deployment'
{
  "timestamp" : "2017-10-05T19:09:46.840Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "wjguerrero",
    "version" : "CDH5",
    "fullVersion" : "5.9.3",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-6-242.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_password",
          "sensitive" : true
        }, {
          "name" : "hive_proxy_user_groups_list",
          "value" : "hive,hue",
          "sensitive" : false
        }, {
          "name" : "hive_service_config_safety_valve",
          "value" : "<property>\n  <name>hive.server2.authentication</name>\n  <value>KERBEROS</value>\n</property>\n<property>\n  <name>hive.server2.authentication.kerberos.principal</name>\n  <value>hive/_HOST@WGSEBC.COM</value>\n</property>\n<property>\n <name>hive.stats.ndv.error</name>\n <value>5.0</value>\n</property>",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "sentry_service",
          "value" : "sentry",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-fed7fa33e7e1d934998e53c26de5d786",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-05c6d2c62e9a9615d"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1izfeof7p11ycbyqxsw6kujsy",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3galtaxbfpean3ygih4so0x1v",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6cwsycnf9o88uuy54twcp25sv",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      }, {
        "name" : "hive-WEBHCAT-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "WEBHCAT",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_webhcat_secret_key",
            "value" : "mk5Vr0MRATR0aSiAajykIxZTKP4BDx",
            "sensitive" : true
          }, {
            "name" : "role_jceks_password",
            "value" : "dc3atxixik65j6jaxgfn68g2n",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-WEBHCAT-BASE"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "858993459",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "2377069363",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "400",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "83sxk8ox50r8o2f24rfms94k6",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "1",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "70tsga4o5p9opg6md44cb6ysh",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "3",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4tgm04s31wo3yr3fp7j9kay2y",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "2",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ {
            "name" : "dataDir",
            "value" : "/disco1/zookeeper",
            "sensitive" : false
          }, {
            "name" : "dataLogDir",
            "value" : "/disco1/zookeeper",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-6-242.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "database_password",
          "value" : "secretpassword",
          "sensitive" : true
        }, {
          "name" : "database_type",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-HTTPFS-c894c47ad13e88fdb8c2d98256338ef5",
          "sensitive" : false
        }, {
          "name" : "oozie_service",
          "value" : "oozie",
          "sensitive" : false
        }, {
          "name" : "sentry_service",
          "value" : "sentry",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-fed7fa33e7e1d934998e53c26de5d786",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "i-05c6d2c62e9a9615d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ww979m0z1v0s1izreqvy5kfb",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "gpYBfIiBswuc16uqHV7WOw2HQq0aoH",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      }, {
        "name" : "hue-KT_RENEWER-fed7fa33e7e1d934998e53c26de5d786",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "i-05c6d2c62e9a9615d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dzq7ecp2w2yg98rdt2ifg7rjm",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-KT_RENEWER-BASE"
        }
      } ],
      "displayName" : "Hue",
      "roleConfigGroups" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-BASE",
        "displayName" : "Load Balancer Default Group",
        "roleType" : "HUE_LOAD_BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-HUE_SERVER-BASE",
        "displayName" : "Hue Server Default Group",
        "roleType" : "HUE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ {
            "name" : "hue_http_port",
            "value" : "1888",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-BASE",
        "displayName" : "Kerberos Ticket Renewer Default Group",
        "roleType" : "KT_RENEWER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "atbuipt3amy21j2k6wqogv7cb",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-6-242.us-east-2.compute.internal",
            "sensitive" : false
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie",
            "sensitive" : true
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql",
            "sensitive" : false
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "rm_dirty",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "IvKRU1aBIfeUP6vToMxHIBJS5cmLZQ",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4mwpuq5fgn75f6p2fckuz9eyo",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "39vko2gkoteiqndeufygmhrs6",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "80",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "mgoneduc0y8indtpa64cuvzq",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/disco1/yarn/nm,/disco2/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/disco1/yarn/container-logs,/disco2/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5334",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5334",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "8",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_client_use_datanode_hostname",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding",
          "sensitive" : false
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "N5YpICT7Lcy77eznYZLsr0n05oxZa2",
          "sensitive" : true
        }, {
          "name" : "dfs_namenode_acls_enabled",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "t4xVROEpu8seRSvIj4hN8Ut4xa8eFm",
          "sensitive" : true
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos",
          "sensitive" : false
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "bky90EKKG0Ii40q9WWq7y4R8hLOBi6",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2ln50trowt2ztyk4rhmm6305w",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ewf376vi57qv1zd2ny9bge3hr",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9e93qkivmuz14jejughtiztbw",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eqw8o4rz4sega8wg6juws66sw",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "94gpge7xmvv7ycexwc849y1cu",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-HTTPFS-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "HTTPFS",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5w175zadivz3wqk0hr1s4akkn",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-HTTPFS-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "87w05al5rq46xjmjp9oub3o2m",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "h67yunvcq7qd93yncjna75a9",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7mwoxnyg01tttuvg16eqh9vtq",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-836bffd2ca7e541e2fbf0fa44bc05645",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-0f0e2b60a8b4d8c75"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "89",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "9645zhyll22d9spbk3mu4yca4",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-c894c47ad13e88fdb8c2d98256338ef5",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "i-026c57eaf03f2ef56"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "83",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "dppv7bkr6lwa7arreqcbasjb1",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/disco1/dfs/dn,/disco2/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/disco1/jn_edits",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/disco1/dfs/nn,/disco2/dfs/nn",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022",
            "sensitive" : false
          }, {
            "name" : "dfs_safemode_min_datanodes",
            "value" : "0",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/disco1/dfs/snn",
            "sensitive" : false
          } ]
        }
      } ],
      "replicationSchedules" : [ {
        "id" : 3,
        "startTime" : "2017-10-03T14:31:00.000Z",
        "interval" : 0,
        "intervalUnit" : "MINUTE",
        "paused" : false,
        "nextRun" : null,
        "alertOnStart" : false,
        "alertOnSuccess" : false,
        "alertOnFail" : false,
        "alertOnAbort" : false,
        "hdfsArguments" : {
          "sourceService" : {
            "peerName" : "danielrozental",
            "clusterName" : "cluster",
            "serviceName" : "hdfs"
          },
          "sourcePath" : "/user/hdfs/danielrozental/teragen",
          "destinationPath" : "/user/hdfs/danielrozental/teragen/*",
          "mapreduceServiceName" : "yarn",
          "dryRun" : false,
          "abortOnError" : false,
          "removeMissingFiles" : false,
          "preserveReplicationCount" : true,
          "preserveBlockSize" : true,
          "preservePermissions" : true,
          "skipChecksumChecks" : false,
          "skipTrash" : false,
          "replicationStrategy" : "DYNAMIC",
          "preserveXAttrs" : false,
          "exclusionFilters" : [ ]
        },
        "active" : false
      } ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-6-242.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "sentry_server_database_password",
          "value" : "sentry_password",
          "sensitive" : true
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,wjguerrero",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "sentry-GATEWAY-fed7fa33e7e1d934998e53c26de5d786",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "i-05c6d2c62e9a9615d"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "sentry-GATEWAY-BASE"
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-fd95557aece3b915ca27b4e65de4b0c9",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "i-0a85591a702a0e11c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "306mdghc8f2udkazsgdj53oh2",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "sentry-SENTRY_SERVER-BASE"
        }
      } ],
      "displayName" : "Sentry",
      "roleConfigGroups" : [ {
        "name" : "sentry-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "sentry"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-BASE",
        "displayName" : "Sentry Server Default Group",
        "roleType" : "SENTRY_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "sentry"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.9.3-1.cdh5.9.3.p0.4",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.9.3-1.cdh5.9.3.p0.4",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ],
    "uuid" : "e9442332-374d-463e-9fe6-d12b7b9a3239"
  } ],
  "hosts" : [ {
    "hostId" : "i-0f0e2b60a8b4d8c75",
    "ipAddress" : "172.31.0.4",
    "hostname" : "ip-172-31-0-4.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-026c57eaf03f2ef56",
    "ipAddress" : "172.31.13.29",
    "hostname" : "ip-172-31-13-29.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-0a85591a702a0e11c",
    "ipAddress" : "172.31.5.64",
    "hostname" : "ip-172-31-5-64.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "i-05c6d2c62e9a9615d",
    "ipAddress" : "172.31.6.242",
    "hostname" : "ip-172-31-6-242.us-east-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-fed7fa33e7e1d934998e53c26de5d786",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "564a8390b3a8a6a425d27e10577ce6c0a50836811ad775e81f6416ceca82f7d0",
    "pwSalt" : 7342624510887913694,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-fed7fa33e7e1d934998e53c26de5d786",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "68321667ae58f4e6bbb72a4408a504871f88c9bb89adf41614bd3fac58f2de56",
    "pwSalt" : -911429293810496738,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-fed7fa33e7e1d934998e53c26de5d786",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "f99e84f587419ee16ac0d54449a5d15a5aecb22e5ec384055814abe2083c60a3",
    "pwSalt" : 3732741235937743221,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-fed7fa33e7e1d934998e53c26de5d786",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "310d89fcfb54c8472665330719c3464d241309147d47f79cb09f5f47b18761e8",
    "pwSalt" : -3559134860433559578,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-fed7fa33e7e1d934998e53c26de5d786",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6cba280d0a973bd58ec799cfe6a6b27296c908119f10f8c9aa363215818002dd",
    "pwSalt" : 7431231967426344340,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "b2d9fc8954915425851c205fb607ceddc9d7e9ac19f605d1271f29f309dece7b",
    "pwSalt" : -637932736642996507,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "6996105f683efb16ec41ae0903b7a0b0b3323f931800080081d7b2c9c22dcf2e",
    "pwSalt" : -6135932253030859525,
    "pwLogin" : true
  }, {
    "name" : "wjguerrero",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "fc08106f0a556b4c15b417bd5446644f687c4562357eaf3e02fa8812c68b584f",
    "pwSalt" : -6983747476629367581,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.11.2",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170811-0014",
    "gitHash" : "3c3ea33a12076fb83a8f11c4452c52fac685d01b",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-fed7fa33e7e1d934998e53c26de5d786",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "i-05c6d2c62e9a9615d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8di0oh13wledu3xdd8kk4evm4",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ACTIVITYMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-fed7fa33e7e1d934998e53c26de5d786",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "i-05c6d2c62e9a9615d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3c82ife8rqcwqz4urose96bne",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-fed7fa33e7e1d934998e53c26de5d786",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "i-05c6d2c62e9a9615d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bp3ffq3j8ebjkrn58tv095tcq",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-fed7fa33e7e1d934998e53c26de5d786",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "i-05c6d2c62e9a9615d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "asl4hkgulm3opd6rsbolww31p",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-fed7fa33e7e1d934998e53c26de5d786",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "i-05c6d2c62e9a9615d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4la9k4prhmbpeara4r15nmvcz",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-fed7fa33e7e1d934998e53c26de5d786",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "i-05c6d2c62e9a9615d"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "11cig375qotslgigkboe2rvzo",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-6-242.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "firehose_database_name",
          "value" : "amon",
          "sensitive" : false
        }, {
          "name" : "firehose_database_password",
          "value" : "amon_password",
          "sensitive" : true
        }, {
          "name" : "firehose_database_user",
          "value" : "amon",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-6-242.us-east-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_password",
          "sensitive" : true
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-TELEMETRYPUBLISHER-BASE",
      "displayName" : "Telemetry Publisher Default Group",
      "roleType" : "TELEMETRYPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false",
      "sensitive" : false
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/27/2012 18:40",
      "sensitive" : false
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAAA9AAEACldHU0VCQy5DT00ADGNsb3VkZXJhLXNjbQAAAAFZ1QjKAQAXABAgnGF02kkMrrQi8/paeuY0AAAAAQ==",
      "sensitive" : true
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@WGSEBC.COM",
      "sensitive" : false
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-6-242.us-east-2.compute.internal",
      "sensitive" : false
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac",
      "sensitive" : false
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true",
      "sensitive" : false
    }, {
      "name" : "MAX_RENEW_LIFE",
      "value" : "604800",
      "sensitive" : false
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD",
      "sensitive" : false
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,https://archive.cloudera.com/navigator-keytrustee5/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/",
      "sensitive" : false
    }, {
      "name" : "SECURITY_REALM",
      "value" : "WGSEBC.COM",
      "sensitive" : false
    } ]
  },
  "allHostsConfig" : {
    "items" : [ ]
  },
  "peers" : [ {
    "name" : "danielrozental",
    "type" : "REPLICATION",
    "url" : "http://ec2-18-221-181-66.us-east-2.compute.amazonaws.com:7180/",
    "username" : "__cloudera_internal_user__7f30c0b8-bf02-4b10-961b-ed7f86755089",
    "password" : "a9976ee8-dadb-47d5-9eb3-91136d4a9cd19fae8d90-ef61-4820-b37d-6953a7c227d6",
    "clouderaManagerCreatedUser" : true
  } ],
  "hostTemplates" : {
    "items" : [ ]
  }
```
