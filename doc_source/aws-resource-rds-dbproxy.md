# AWS::RDS::DBProxy<a name="aws-resource-rds-dbproxy"></a>

The `AWS::RDS::DBProxy` resource creates or updates a DB proxy\.

For information about RDS Proxy for Amazon RDS, see [ Managing Connections with Amazon RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html) in the *Amazon RDS User Guide*\.

For information about RDS Proxy for Amazon Aurora, see [ Managing Connections with Amazon RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-proxy.html) in the *Amazon Aurora User Guide*\.

**Note**  
Limitations apply to RDS Proxy, including DB engine version limitations and AWS Region limitations\.  
For information about limitations that apply to RDS Proxy for Amazon RDS, see [ Limitations for RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/rds-proxy.html#rds-proxy.limitations) in the *Amazon RDS User Guide*\.  
For information about that apply to RDS Proxy for Amazon Aurora, see [ Limitations for RDS Proxy](https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/rds-proxy.html#rds-proxy.limitations) in the *Amazon Aurora User Guide*\.

## Syntax<a name="aws-resource-rds-dbproxy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rds-dbproxy-syntax.json"></a>

```
{
  "Type" : "AWS::RDS::DBProxy",
  "Properties" : {
      "[Auth](#cfn-rds-dbproxy-auth)" : [ AuthFormat, ... ],
      "[DBProxyName](#cfn-rds-dbproxy-dbproxyname)" : String,
      "[DebugLogging](#cfn-rds-dbproxy-debuglogging)" : Boolean,
      "[EngineFamily](#cfn-rds-dbproxy-enginefamily)" : String,
      "[IdleClientTimeout](#cfn-rds-dbproxy-idleclienttimeout)" : Integer,
      "[RequireTLS](#cfn-rds-dbproxy-requiretls)" : Boolean,
      "[RoleArn](#cfn-rds-dbproxy-rolearn)" : String,
      "[Tags](#cfn-rds-dbproxy-tags)" : [ TagFormat, ... ],
      "[VpcSecurityGroupIds](#cfn-rds-dbproxy-vpcsecuritygroupids)" : [ String, ... ],
      "[VpcSubnetIds](#cfn-rds-dbproxy-vpcsubnetids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-rds-dbproxy-syntax.yaml"></a>

```
Type: AWS::RDS::DBProxy
Properties: 
  [Auth](#cfn-rds-dbproxy-auth): 
    - AuthFormat
  [DBProxyName](#cfn-rds-dbproxy-dbproxyname): String
  [DebugLogging](#cfn-rds-dbproxy-debuglogging): Boolean
  [EngineFamily](#cfn-rds-dbproxy-enginefamily): String
  [IdleClientTimeout](#cfn-rds-dbproxy-idleclienttimeout): Integer
  [RequireTLS](#cfn-rds-dbproxy-requiretls): Boolean
  [RoleArn](#cfn-rds-dbproxy-rolearn): String
  [Tags](#cfn-rds-dbproxy-tags): 
    - TagFormat
  [VpcSecurityGroupIds](#cfn-rds-dbproxy-vpcsecuritygroupids): 
    - String
  [VpcSubnetIds](#cfn-rds-dbproxy-vpcsubnetids): 
    - String
```

## Properties<a name="aws-resource-rds-dbproxy-properties"></a>

`Auth`  <a name="cfn-rds-dbproxy-auth"></a>
The authorization mechanism that the proxy uses\.  
*Required*: Yes  
*Type*: List of [AuthFormat](aws-properties-rds-dbproxy-authformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DBProxyName`  <a name="cfn-rds-dbproxy-dbproxyname"></a>
The identifier for the proxy\. This name must be unique for all proxies owned by your AWS account in the specified AWS Region\. An identifier must begin with a letter and must contain only ASCII letters, digits, and hyphens; it can't end with a hyphen or contain two consecutive hyphens\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DebugLogging`  <a name="cfn-rds-dbproxy-debuglogging"></a>
Whether the proxy includes detailed information about SQL statements in its logs\. This information helps you to debug issues involving SQL behavior or the performance and scalability of the proxy connections\. The debug information includes the text of SQL statements that you submit through the proxy\. Thus, only enable this setting when needed for debugging, and only when you have security measures in place to safeguard any sensitive information that appears in the logs\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineFamily`  <a name="cfn-rds-dbproxy-enginefamily"></a>
The kinds of databases that the proxy can connect to\. This value determines which database network protocol the proxy recognizes when it interprets network traffic to and from the database\. The engine family applies to MySQL and PostgreSQL for both RDS and Aurora\.  
*Valid values*: `MYSQL` \| `POSTGRESQL`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IdleClientTimeout`  <a name="cfn-rds-dbproxy-idleclienttimeout"></a>
The number of seconds that a connection to the proxy can be inactive before the proxy disconnects it\. You can set this value higher or lower than the connection timeout limit for the associated database\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RequireTLS`  <a name="cfn-rds-dbproxy-requiretls"></a>
A Boolean parameter that specifies whether Transport Layer Security \(TLS\) encryption is required for connections to the proxy\. By enabling this setting, you can enforce encrypted TLS connections to the proxy\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-rds-dbproxy-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that the proxy uses to access secrets in AWS Secrets Manager\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rds-dbproxy-tags"></a>
An optional set of key\-value pairs to associate arbitrary data of your choosing with the proxy\.  
*Required*: No  
*Type*: List of [TagFormat](aws-properties-rds-dbproxy-tagformat.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-rds-dbproxy-vpcsecuritygroupids"></a>
One or more VPC security group IDs to associate with the new proxy\.  
If you plan to update the resource, don't specify VPC security groups in a shared VPC\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSubnetIds`  <a name="cfn-rds-dbproxy-vpcsubnetids"></a>
One or more VPC subnet IDs to associate with the new proxy\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-rds-dbproxy-return-values"></a>

### Ref<a name="aws-resource-rds-dbproxy-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the DB proxy\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-rds-dbproxy-return-values-fn--getatt"></a>

#### <a name="aws-resource-rds-dbproxy-return-values-fn--getatt-fn--getatt"></a>

`DBProxyArn`  <a name="DBProxyArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) representing the target group\.

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
The writer endpoint for the RDS DB instance or Aurora DB cluster\.

## Examples<a name="aws-resource-rds-dbproxy--examples"></a>

### Creating a DB Proxy and registering a DB instance<a name="aws-resource-rds-dbproxy--examples--Creating_a_DB_Proxy_and_registering_a_DB_instance"></a>

The following example creates a DB proxy and registers a DB instance\.

#### JSON<a name="aws-resource-rds-dbproxy--examples--Creating_a_DB_Proxy_and_registering_a_DB_instance--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "ProxyName": {
            "Type": "String",
            "Default": "exampleProxy"
        },
        "InstanceName": {
            "Type": "String",
            "Default": "database-1"
        },
        "BootstrapSecretReaderRoleArn": {
            "Type": "String",
            "Default": "arn:aws:iam::123456789012:role/RDSSecretReaderRoleForDBProxy"
        },
        "BootstrapProxySecretArn": {
            "Type": "String",
            "Default": "arn:aws:secretsmanager:us-west-2:123456789012:secret:MySecretForDBProxy"
        },
        "SubnetIds": {
            "Type": "String",
            "Default": "subnet-01b761b31fb498f20,subnet-012b9a958ef0f9949,subnet-05e8e263052025378"
        }
    },
    "Resources": {
        "TestDBProxy": {
            "Type": "AWS::RDS::DBProxy",
            "Properties": {
                "DebugLogging": true,
                "DBProxyName": {
                    "Ref": "ProxyName"
                },
                "EngineFamily": "MYSQL",
                "IdleClientTimeout": 120,
                "RequireTLS": true,
                "RoleArn": {
                    "Ref": "BootstrapSecretReaderRoleArn"
                },
                "Auth": [
                    {
                        "AuthScheme": "SECRETS",
                        "SecretArn": {
                            "Ref": "BootstrapProxySecretArn"
                        },
                        "IAMAuth": "DISABLED"
                    }
                ],
                "VpcSubnetIds": {
                    "Fn::Split": [
                        ",",
                        {
                            "Ref": "SubnetIds"
                        }
                    ]
                }
            }
        },
        "ProxyTargetGroup": {
            "Type": "AWS::RDS::DBProxyTargetGroup",
            "Properties": {
                "DBProxyName": {
                    "Ref": "TestDBProxy"
                },
                "DBInstanceIdentifiers": [
                    {
                        "Ref": "InstanceName"
                    }
                ],
                "TargetGroupName": "default",
                "ConnectionPoolConfigurationInfo": {
                    "MaxConnectionsPercent": 12,
                    "MaxIdleConnectionsPercent": 11,
                    "ConnectionBorrowTimeout": 120
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-rds-dbproxy--examples--Creating_a_DB_Proxy_and_registering_a_DB_instance--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Parameters:
  ProxyName:
    Type: String
    Default: exampleProxy
  InstanceName:
    Type: String
    Default: database-1
  BootstrapSecretReaderRoleArn:
    Type: String
    Default: arn:aws:iam::123456789012:role/RDSSecretReaderRoleForDBProxy
  BootstrapProxySecretArn:
    Type: String
    Default: arn:aws:secretsmanager:us-west-2:123456789012:secret:MySecretForDBProxy
  SubnetIds:
    Type: String
    Default: subnet-01b761b31fb498f20,subnet-012b9a958ef0f9949,subnet-05e8e263052025378
Resources:
  TestDBProxy:
    Type: AWS::RDS::DBProxy
    Properties:
      DebugLogging: true
      DBProxyName: !Ref ProxyName
      EngineFamily: MYSQL
      IdleClientTimeout: 120
      RequireTLS: true
      RoleArn:
        !Ref BootstrapSecretReaderRoleArn
      Auth:
        - {AuthScheme: SECRETS, SecretArn: !Ref BootstrapProxySecretArn, IAMAuth: DISABLED}
      VpcSubnetIds:
        Fn::Split: [",", !Ref SubnetIds]
  ProxyTargetGroup:
    Type: AWS::RDS::DBProxyTargetGroup
    Properties:
      DBProxyName: !Ref TestDBProxy
      DBInstanceIdentifiers: [!Ref InstanceName]
      TargetGroupName: default
      ConnectionPoolConfigurationInfo:
          MaxConnectionsPercent: 12
          MaxIdleConnectionsPercent: 11
          ConnectionBorrowTimeout: 120
```