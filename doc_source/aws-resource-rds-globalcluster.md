# AWS::RDS::GlobalCluster<a name="aws-resource-rds-globalcluster"></a>

The `AWS::RDS::GlobalCluster` resource creates or updates an Amazon Aurora global database spread across multiple AWS Regions\.

The global database contains a single primary cluster with read\-write capability, and a read\-only secondary cluster that receives data from the primary cluster through high\-speed replication performed by the Aurora storage subsystem\.

You can create a global database that is initially empty, and then add a primary cluster and a secondary cluster to it\.

For information about Aurora global databases, see [ Working with Amazon Aurora Global Databases](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/aurora-global-database.html) in the *Amazon Aurora User Guide*\.

## Syntax<a name="aws-resource-rds-globalcluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-globalcluster-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::GlobalCluster",
  "Properties" : {
      "[DeletionProtection](#cfn-rds-globalcluster-deletionprotection)" : Boolean,
      "[Engine](#cfn-rds-globalcluster-engine)" : String,
      "[EngineVersion](#cfn-rds-globalcluster-engineversion)" : String,
      "[GlobalClusterIdentifier](#cfn-rds-globalcluster-globalclusteridentifier)" : String,
      "[SourceDBClusterIdentifier](#cfn-rds-globalcluster-sourcedbclusteridentifier)" : String,
      "[StorageEncrypted](#cfn-rds-globalcluster-storageencrypted)" : Boolean
    }
}
```

### YAML<a name="aws-resource-rds-globalcluster-syntax.yaml"></a>

```
Type: AWS::RDS::GlobalCluster
Properties: 
  [DeletionProtection](#cfn-rds-globalcluster-deletionprotection): Boolean
  [Engine](#cfn-rds-globalcluster-engine): String
  [EngineVersion](#cfn-rds-globalcluster-engineversion): String
  [GlobalClusterIdentifier](#cfn-rds-globalcluster-globalclusteridentifier): String
  [SourceDBClusterIdentifier](#cfn-rds-globalcluster-sourcedbclusteridentifier): String
  [StorageEncrypted](#cfn-rds-globalcluster-storageencrypted): Boolean
```

## Properties<a name="aws-resource-rds-globalcluster-properties"></a>

`DeletionProtection`  <a name="cfn-rds-globalcluster-deletionprotection"></a>
 The deletion protection setting for the new global database\. The global database can't be deleted when deletion protection is enabled\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-rds-globalcluster-engine"></a>
The name of the database engine to be used for this DB cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-rds-globalcluster-engineversion"></a>
The engine version of the Aurora global database\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`GlobalClusterIdentifier`  <a name="cfn-rds-globalcluster-globalclusteridentifier"></a>
The cluster identifier of the new global database cluster\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceDBClusterIdentifier`  <a name="cfn-rds-globalcluster-sourcedbclusteridentifier"></a>
The DB cluster identifier or Amazon Resource Name \(ARN\) to use as the primary cluster of the global database\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StorageEncrypted`  <a name="cfn-rds-globalcluster-storageencrypted"></a>
The storage encryption setting for the global database cluster\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-rds-globalcluster-return-values"></a>

### Ref<a name="aws-resource-rds-globalcluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the global database cluster\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-rds-globalcluster--examples"></a>

### Creating a Global Database cluster for Aurora MySQL<a name="aws-resource-rds-globalcluster--examples--Creating_a_Global_Database_cluster_for_Aurora_MySQL"></a>

The following example creates a global database cluster with an Aurora MySQL DB cluster and DB instance\.

#### JSON<a name="aws-resource-rds-globalcluster--examples--Creating_a_Global_Database_cluster_for_Aurora_MySQL--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "GlobalClusterIdentifier": {
          "Type": "String",
          "Description": "Identifier used for global database cluster",
          "AllowedPattern": "^[a-zA-Z]{1}(?:-?[a-zA-Z0-9]){0,62}$"
        },
        "username": {
            "NoEcho": "true",
            "Description": "Username for MySQL database access",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "16",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
        },
        "password": {
            "NoEcho": "true",
            "Description": "Password for MySQL database access",
            "Type": "String",
            "MinLength": "8",
            "MaxLength": "41",
            "AllowedPattern": "[a-zA-Z0-9]*",
            "ConstraintDescription": "must contain only alphanumeric characters."
        }
    },
    "Resources": {
        "GlobalCluster": {
            "Type": "AWS::RDS::GlobalCluster",
            "Properties": {
                "GlobalClusterIdentifier": {
                    "Ref": "GlobalClusterIdentifier"
                },
                "SourceDBClusterIdentifier": {
                    "Ref": "RDSCluster"
                }
            }
        },
        "RDSCluster": {
            "Type": "AWS::RDS::DBCluster",
            "Properties": {
                "MasterUsername": {
                    "Ref": "username"
                },
                "MasterUserPassword": {
                    "Ref": "password"
                },
                "DBClusterParameterGroupName": "default.aurora-mysql5.7",
                "Engine": "aurora-mysql",
                "EngineVersion": "5.7.mysql_aurora.2.08.0"
            }
        },
        "RDSDBInstance": {
            "Type": "AWS::RDS::DBInstance",
            "Properties": {
                "Engine": "aurora-mysql",
                "DBClusterIdentifier": {
                    "Ref": "RDSCluster"
                },
                "DBParameterGroupName": "default.aurora-mysql5.7",
                "PubliclyAccessible": "true",
                "DBInstanceClass": "db.r5.xlarge"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-globalcluster--examples--Creating_a_Global_Database_cluster_for_Aurora_MySQL--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  GlobalClusterIdentifier:
    Type: String
    Description: Identifier used for global database cluster
    AllowedPattern: '^[a-zA-Z]{1}(?:-?[a-zA-Z0-9]){0,62}$'
  username:
    NoEcho: 'true'
    Description: Username for MySQL database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  password:
    NoEcho: 'true'
    Description: Password for MySQL database access
    Type: String
    MinLength: '8'
    MaxLength: '41'
    AllowedPattern: '[a-zA-Z0-9]*'
    ConstraintDescription: must contain only alphanumeric characters.
Resources:
  GlobalCluster:
    Type: 'AWS::RDS::GlobalCluster'
    Properties:
      GlobalClusterIdentifier: !Ref GlobalClusterIdentifier
      SourceDBClusterIdentifier: !Ref RDSCluster
  RDSCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      MasterUsername: !Ref username
      MasterUserPassword: !Ref password
      DBClusterParameterGroupName: default.aurora-mysql5.7
      Engine: aurora-mysql
      EngineVersion: 5.7.mysql_aurora.2.08.0
  RDSDBInstance:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      Engine: aurora-mysql
      DBClusterIdentifier: !Ref RDSCluster
      DBParameterGroupName: default.aurora-mysql5.7
      PubliclyAccessible: 'true'
      DBInstanceClass: db.r5.xlarge
```

### Creating a Global Database cluster for Aurora PostgreSQL<a name="aws-resource-rds-globalcluster--examples--Creating_a_Global_Database_cluster_for_Aurora_PostgreSQL"></a>

The following example creates a global database cluster with an Aurora PostgreSQL DB cluster and DB instance\.

#### JSON<a name="aws-resource-rds-globalcluster--examples--Creating_a_Global_Database_cluster_for_Aurora_PostgreSQL--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "GlobalClusterIdentifier": {
          "Type": "String",
          "Description": "Identifier used for global database cluster",
          "AllowedPattern": "^[a-zA-Z]{1}(?:-?[a-zA-Z0-9]){0,62}$"
        },
        "username": {
            "NoEcho": "true",
            "Description": "Username for PostgreSQL database access",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "16",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
        },
        "password": {
            "NoEcho": "true",
            "Description": "Password for PostgreSQL database access",
            "Type": "String",
            "MinLength": "8",
            "MaxLength": "41",
            "AllowedPattern": "[a-zA-Z0-9]*",
            "ConstraintDescription": "must contain only alphanumeric characters."
        }
    },
    "Resources": {
        "GlobalCluster": {
            "Type": "AWS::RDS::GlobalCluster",
            "Properties": {
                "GlobalClusterIdentifier": {
                    "Ref": "GlobalClusterIdentifier"
                },
                "SourceDBClusterIdentifier": {
                    "Ref": "RDSCluster"
                }
            }
        },
        "RDSCluster": {
            "Type": "AWS::RDS::DBCluster",
            "Properties": {
                "MasterUsername": {
                    "Ref": "username"
                },
                "MasterUserPassword": {
                    "Ref": "password"
                },
                "DBClusterParameterGroupName": "default.aurora-postgresql11",
                "Engine": "aurora-postgresql",
                "EngineVersion": "11.7"
            }
        },
        "RDSDBInstance": {
            "Type": "AWS::RDS::DBInstance",
            "Properties": {
                "Engine": "aurora-postgresql",
                "DBClusterIdentifier": {
                    "Ref": "RDSCluster"
                },
                "DBParameterGroupName": "default.aurora-postgresql11",
                "PubliclyAccessible": "true",
                "DBInstanceClass": "db.r5.xlarge"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-globalcluster--examples--Creating_a_Global_Database_cluster_for_Aurora_PostgreSQL--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  GlobalClusterIdentifier:
    Type: String
    Description: Identifier used for global database cluster
    AllowedPattern: '^[a-zA-Z]{1}(?:-?[a-zA-Z0-9]){0,62}$'
  username:
    NoEcho: 'true'
    Description: Username for PostgreSQL database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  password:
    NoEcho: 'true'
    Description: Password for PostgreSQL database access
    Type: String
    MinLength: '8'
    MaxLength: '41'
    AllowedPattern: '[a-zA-Z0-9]*'
    ConstraintDescription: must contain only alphanumeric characters.
Resources:
  GlobalCluster:
    Type: 'AWS::RDS::GlobalCluster'
    Properties:
      GlobalClusterIdentifier: !Ref GlobalClusterIdentifier
      SourceDBClusterIdentifier: !Ref RDSCluster
  RDSCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      MasterUsername: !Ref username
      MasterUserPassword: !Ref password
      DBClusterParameterGroupName: default.aurora-postgresql11
      Engine: aurora-postgresql
      EngineVersion: '11.7'
  RDSDBInstance:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      Engine: aurora-postgresql
      DBClusterIdentifier: !Ref RDSCluster
      DBParameterGroupName: default.aurora-postgresql11
      PubliclyAccessible: 'true'
      DBInstanceClass: db.r5.xlarge
```

### Adding an AWS Region to an Aurora database cluster<a name="aws-resource-rds-globalcluster--examples--Adding_an_AWS_Region_to_an_Aurora_database_cluster"></a>

The following example creates a new Aurora DB cluster, attaches it to a global database cluster as a read\-only secondary cluster, and then adds a DB instance to the new DB cluster\.

Specify the `GlobalClusterIdentifier` of a global database cluster with the primary DB cluster in a separate AWS Region\.

#### JSON<a name="aws-resource-rds-globalcluster--examples--Adding_an_AWS_Region_to_an_Aurora_database_cluster--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "GlobalClusterIdentifier": {
          "Type": "String",
          "Description": "Identifier used for global database cluster",
          "AllowedPattern": "^[a-zA-Z]{1}(?:-?[a-zA-Z0-9]){0,62}$"
        }
    },
    "Resources": {
        "RDSCluster": {
            "Type": "AWS::RDS::DBCluster",
            "Properties": {
                "GlobalClusterIdentifier": {
                    "Ref": "GlobalClusterIdentifier"
                },
                "DBClusterParameterGroupName": "default.aurora-mysql5.7",
                "Engine": "aurora-mysql",
                "EngineVersion": "5.7.mysql_aurora.2.08.0"
            }
        },
        "RDSDBInstance": {
            "Type": "AWS::RDS::DBInstance",
            "Properties": {
                "Engine": "aurora-mysql",
                "DBClusterIdentifier": {
                    "Ref": "RDSCluster"
                },
                "DBParameterGroupName": "default.aurora-mysql5.7",
                "PubliclyAccessible": "true",
                "DBInstanceClass": "db.r5.xlarge"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-globalcluster--examples--Adding_an_AWS_Region_to_an_Aurora_database_cluster--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  GlobalClusterIdentifier:
    Type: String
    Description: Identifier used for global database cluster
    AllowedPattern: '^[a-zA-Z]{1}(?:-?[a-zA-Z0-9]){0,62}$'
Resources:
  RDSCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      GlobalClusterIdentifier: !Ref GlobalClusterIdentifier
      DBClusterParameterGroupName: default.aurora-mysql5.7
      Engine: aurora-mysql
      EngineVersion: 5.7.mysql_aurora.2.08.0
  RDSDBInstance:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      Engine: aurora-mysql
      DBClusterIdentifier: !Ref RDSCluster
      DBParameterGroupName: default.aurora-mysql5.7
      PubliclyAccessible: 'true'
      DBInstanceClass: db.r5.xlarge
```

### Adding a DB cluster to a Global Database cluster<a name="aws-resource-rds-globalcluster--examples--Adding_a_DB_cluster_to_a_Global_Database_cluster"></a>

The following example adds a DB cluster to a global database cluster\.

The example includes the template that was used to create the DB cluster\. After the DB cluster created by the first template exists, the second template in the example adds the DB cluster to a global database cluster\.

#### JSON<a name="aws-resource-rds-globalcluster--examples--Adding_a_DB_cluster_to_a_Global_Database_cluster--json"></a>

```
The following template was used to create DB cluster that you want to add to the global database cluster.
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "username": {
            "NoEcho": "true",
            "Description": "Username for MySQL database access",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "16",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
         },
         "password": {
             "NoEcho": "true",
             "Description": "Password MySQL database access",
             "Type": "String",
             "MinLength": "8",
             "MaxLength": "41",
             "AllowedPattern": "[a-zA-Z0-9]*",
             "ConstraintDescription": "must contain only alphanumeric characters."
         }
    },
    "Resources": {
        "RDSCluster": {
            "Type": "AWS::RDS::DBCluster",
            "Properties": {
                "MasterUsername": {
                    "Ref": "username"
                },
                "MasterUserPassword": {
                    "Ref": "password"
                },
                "DBClusterParameterGroupName": "default.aurora-mysql5.7",
                "Engine": "aurora-mysql",
                "EngineVersion": "5.7.mysql_aurora.2.08.0"
            }
        },
        "RDSDBInstance": {
            "Type": "AWS::RDS::DBInstance",
                "Properties": {
                    "Engine": "aurora-mysql",
                    "DBClusterIdentifier": {
                        "Ref": "RDSCluster"
                },
                "DBParameterGroupName": "default.aurora-mysql5.7",
                "PubliclyAccessible": "true",
                "DBInstanceClass": "db.r5.xlarge"
            }
        }
    }
}
                
The following template adds the DB cluster created by the previous template to a global database cluster.
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "GlobalClusterIdentifier": {
            "Description": "Global cluster identifier",
            "Type": "String"
        },
        "username": {
            "NoEcho": "true",
            "Description": "Username for MySQL database access",
            "Type": "String",
            "MinLength": "1",
            "MaxLength": "16",
            "AllowedPattern": "[a-zA-Z][a-zA-Z0-9]*",
            "ConstraintDescription": "must begin with a letter and contain only alphanumeric characters."
        },
        "password": {
            "NoEcho": "true",
            "Description": "Password MySQL database access",
            "Type": "String",
            "MinLength": "8",
            "MaxLength": "41",
            "AllowedPattern": "[a-zA-Z0-9]*",
            "ConstraintDescription": "must contain only alphanumeric characters."
        }
    },
    "Resources": {
        "GlobalCluster": {
            "Type": "AWS::RDS::GlobalCluster",
            "Properties": {
                "GlobalClusterIdentifier": {
                    "Ref": "GlobalClusterIdentifier"
                },
                "SourceDBClusterIdentifier": {
                    "Ref": "RDSCluster"
                }
            }
        },
        "RDSCluster": {
            "Type": "AWS::RDS::DBCluster",
            "Properties": {
                "MasterUsername": {
                    "Ref": "username"
                },
                "MasterUserPassword": {
                    "Ref": "password"
                },
                "DBClusterParameterGroupName": "default.aurora-mysql5.7",
                "Engine": "aurora-mysql",
                "EngineVersion": "5.7.mysql_aurora.2.08.0"
            }
        },
        "RDSDBInstance": {
            "Type": "AWS::RDS::DBInstance",
            "Properties": {
                "Engine": "aurora-mysql",
                "DBClusterIdentifier": {
                    "Ref": "RDSCluster"
                },
                "DBParameterGroupName": "default.aurora-mysql5.7",
                "PubliclyAccessible": "true",
                "DBInstanceClass": "db.r5.xlarge"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-globalcluster--examples--Adding_a_DB_cluster_to_a_Global_Database_cluster--yaml"></a>

```
The following template created the DB cluster that you want to add to the global database cluster.
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  username:
    NoEcho: 'true'
    Description: Username for MySQL database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  password:
    NoEcho: 'true'
    Description: Password MySQL database access
    Type: String
    MinLength: '8'
    MaxLength: '41'
    AllowedPattern: '[a-zA-Z0-9]*'
    ConstraintDescription: must contain only alphanumeric characters.
Resources:
  RDSCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      MasterUsername: !Ref username
      MasterUserPassword: !Ref password
      DBClusterParameterGroupName: default.aurora-mysql5.7
      Engine: aurora-mysql
      EngineVersion: 5.7.mysql_aurora.2.08.0
  RDSDBInstance:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      Engine: aurora-mysql
      DBClusterIdentifier: !Ref RDSCluster
      DBParameterGroupName: default.aurora-mysql5.7
      PubliclyAccessible: 'true'
      DBInstanceClass: db.r5.xlarge
                
The following template adds the DB cluster created by the previous template to a global database cluster.
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  GlobalClusterIdentifier:
    Description: Global cluster identifier
    Type: String
  username:
    NoEcho: 'true'
    Description: Username for MySQL database access
    Type: String
    MinLength: '1'
    MaxLength: '16'
    AllowedPattern: '[a-zA-Z][a-zA-Z0-9]*'
    ConstraintDescription: must begin with a letter and contain only alphanumeric characters.
  password:
    NoEcho: 'true'
    Description: Password MySQL database access
    Type: String
    MinLength: '8'
    MaxLength: '41'
    AllowedPattern: '[a-zA-Z0-9]*'
    ConstraintDescription: must contain only alphanumeric characters.
Resources:
  GlobalCluster:
    Type: 'AWS::RDS::GlobalCluster'
    Properties:
      GlobalClusterIdentifier: !Ref GlobalClusterIdentifier
      SourceDBClusterIdentifier: !Ref RDSCluster
  RDSCluster:
    Type: 'AWS::RDS::DBCluster'
    Properties:
      MasterUsername: !Ref username
      MasterUserPassword: !Ref password
      DBClusterParameterGroupName: default.aurora-mysql5.7
      Engine: aurora-mysql
      EngineVersion: 5.7.mysql_aurora.2.08.0
  RDSDBInstance:
    Type: 'AWS::RDS::DBInstance'
    Properties:
      Engine: aurora-mysql
      DBClusterIdentifier: !Ref RDSCluster
      DBParameterGroupName: default.aurora-mysql5.7
      PubliclyAccessible: 'true'
      DBInstanceClass: db.r5.xlarge
```