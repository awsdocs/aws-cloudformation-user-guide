# AWS::OpsWorksCM::Server<a name="aws-resource-opsworkscm-server"></a>

The `AWS::OpsWorksCM::Server` resource creates an AWS OpsWorks for Chef Automate or AWS OpsWorks for Puppet Enterprise configuration management server\. For more information, see [Create a Chef Automate Server in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opscm-create-server-cfn.html) or [Create a Puppet Enterprise Master in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opspup-create-server-cfn.html) in the *AWS OpsWorks User Guide*, and [CreateServer](https://docs.aws.amazon.com/opsworks-cm/latest/APIReference/API_CreateServer.html) in the *AWS OpsWorks CM API Reference*\.

## Syntax<a name="aws-resource-opsworkscm-server-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworkscm-server-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorksCM::Server",
  "Properties" : {
    "[BackupId](#cfn-opsworkscm-server-backupid)" : String,
    "[BackupRetentionCount](#cfn-opsworkscm-server-backupretentioncount)" : Integer,
    "[DisableAutomatedBackup](#cfn-opsworkscm-server-disableautomatedbackup)" : Boolean,
    "[Engine](#cfn-opsworkscm-server-engine)" : String,
    "[EngineAttributes](#cfn-opsworkscm-server-engineattributes)" : [ [*EngineAttribute*](aws-properties-opsworkscm-server-engineattribute.md), ... ],
    "[EngineModel](#cfn-opsworkscm-server-enginemodel)" : String,
    "[EngineVersion](#cfn-opsworkscm-server-engineversion)" : String,
    "[InstanceProfileArn](#cfn-opsworkscm-server-instanceprofilearn)" : String,
    "[InstanceType](#cfn-opsworkscm-server-instancetype)" : String,
    "[KeyPair](#cfn-opsworkscm-server-keypair)" : String,
    "[PreferredBackupWindow](#cfn-opsworkscm-server-preferredbackupwindow)" : String,
    "[PreferredMaintenanceWindow](#cfn-opsworkscm-server-preferredmaintenancewindow)" : String,
    "[SecurityGroupIds](#cfn-opsworkscm-server-securitygroupids)" : [ String, ... ],
    "[ServerName](#cfn-opsworkscm-server-servername)" : String,
    "[ServiceRoleArn](#cfn-opsworkscm-server-servicerolearn)" : String,
    "[SubnetIds](#cfn-opsworkscm-server-subnetids)" : [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-opsworkscm-server-syntax.yaml"></a>

```
Type: "AWS::OpsWorksCM::Server"
Properties:
  [BackupId](#cfn-opsworkscm-server-backupid): String
  [BackupRetentionCount](#cfn-opsworkscm-server-backupretentioncount): Integer
  [DisableAutomatedBackup](#cfn-opsworkscm-server-disableautomatedbackup): Boolean
  [Engine](#cfn-opsworkscm-server-engine): String
  [EngineAttributes](#cfn-opsworkscm-server-engineattributes): 
    - [*EngineAttribute*](aws-properties-opsworkscm-server-engineattribute.md)
  [EngineModel](#cfn-opsworkscm-server-enginemodel): String
  [EngineVersion](#cfn-opsworkscm-server-engineversion): String
  [InstanceProfileArn](#cfn-opsworkscm-server-instanceprofilearn): String
  [InstanceType](#cfn-opsworkscm-server-instancetype): String
  [KeyPair](#cfn-opsworkscm-server-keypair): String
  [PreferredBackupWindow](#cfn-opsworkscm-server-preferredbackupwindow): String
  [PreferredMaintenanceWindow](#cfn-opsworkscm-server-preferredmaintenancewindow): String
  [SecurityGroupIds](#cfn-opsworkscm-server-securitygroupids): 
    - String
  [ServerName](#cfn-opsworkscm-server-servername): String
  [ServiceRoleArn](#cfn-opsworkscm-server-servicerolearn): String
  [SubnetIds](#cfn-opsworkscm-server-subnetids): 
    - String
```

## Properties<a name="aws-resource-opsworkscm-server-properties"></a>

`BackupId`  <a name="cfn-opsworkscm-server-backupid"></a>
If you specify this field, AWS OpsWorks CM creates the server by using the backup represented by `BackupId`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`BackupRetentionCount`  <a name="cfn-opsworkscm-server-backupretentioncount"></a>
The number of automated backups that you want to keep\. Whenever a new backup is created, AWS OpsWorks CM deletes the oldest backups if this number is exceeded\. The default value is 1\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`DisableAutomatedBackup`  <a name="cfn-opsworkscm-server-disableautomatedbackup"></a>
Enable or disable scheduled backups\. Valid values are `true` or `false`\. The default value is `false`\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Engine`  <a name="cfn-opsworkscm-server-engine"></a>
The configuration management engine to use\. Valid values are `Chef` or `Puppet`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`EngineAttributes`  <a name="cfn-opsworkscm-server-engineattributes"></a>
In a `createServer()` request, `EngineAttributes` contains the administrator credentials to access the configuration management server\. These credentials are not stored by AWS OpsWorks CM\.  

**Attributes accepted in a `createServer` request for Chef Automate:**
+ `CHEF_PIVOTAL_KEY`: A base64\-encoded RSA public key\. When no CHEF\_PIVOTAL\_KEY is set, a private key is generated by AWS OpsWorks for Chef Automate and returned in the response\. The corresponding private key is required to access the Chef API\.

**Attributes accepted in a `createServer` request for Puppet Enterprise:**
+ `PUPPET_ADMIN_PASSWORD`: An administrator password that you can use to sign in to the Puppet Enterprise console after the server is online\. The password must use between 8 and 32 ASCII characters\.
+ `PUPPET_R10K_REMOTE`: The r10k remote is the URL of your control repository \(for example, ssh://git@your\.git\-repo\.com:user/control\-repo\.git\)\. Specifying an r10k remote opens TCP port 8170\.
+ `PUPPET_R10K_PRIVATE_KEY`: If you are using a private Git repository, add PUPPET\_R10K\_PRIVATE\_KEY to specify a PEM\-encoded private SSH key\.
 *Required*: No  
 *Type*: List of [EngineAttribute](aws-properties-opsworkscm-server-engineattribute.md) property types  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`EngineModel`  <a name="cfn-opsworkscm-server-enginemodel"></a>
The engine model of the server\. Valid values include `Monolithic` for Puppet and `Single` for Chef\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`EngineVersion`  <a name="cfn-opsworkscm-server-engineversion"></a>
The engine version of the server\. For a Chef server, the valid value for `EngineVersion` is `12`\. For a Puppet server, the valid value is `2017`\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InstanceProfileArn`  <a name="cfn-opsworkscm-server-instanceprofilearn"></a>
The instance profile ARN of the server\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`InstanceType`  <a name="cfn-opsworkscm-server-instancetype"></a>
The instance type for the server, as specified in the AWS CloudFormation stack\. This might not be the same instance type that is shown for the server in the Amazon EC2 console\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`KeyPair`  <a name="cfn-opsworkscm-server-keypair"></a>
The key pair associated with the server\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`PreferredBackupWindow`  <a name="cfn-opsworkscm-server-preferredbackupwindow"></a>
The preferred backup period specified for the server\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`PreferredMaintenanceWindow`  <a name="cfn-opsworkscm-server-preferredmaintenancewindow"></a>
The preferred maintenance period specified for the server\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SecurityGroupIds`  <a name="cfn-opsworkscm-server-securitygroupids"></a>
The security group IDs for the server, as specified in the AWS CloudFormation stack\. These might not be the same security groups that are shown for the server in the Amazon EC2 console\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ServerName`  <a name="cfn-opsworkscm-server-servername"></a>
The name of the server\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ServiceRoleArn`  <a name="cfn-opsworkscm-server-servicerolearn"></a>
The service role ARN used to create the server\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`SubnetIds`  <a name="cfn-opsworkscm-server-subnetids"></a>
The subnet IDs specified in a `createServer()` request\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-opsworkscm-server-returnvalues"></a>

### Ref<a name="aws-resource-opsworkscm-server-ref"></a>

When you pass the logical ID of an `AWS::OpsWorksCM::Server` resource to the intrinsic `Ref` function, the function returns the server's ARN, such as `arn:aws:OpsWorksCM:us-east-1:123456789012:server/server-a1bzhi`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-opsworkscm-server-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Endpoint`  
A DNS name that can be used to access the engine\. Example: `myserver-asdfghjkl.us-east-1.opsworks.io`\.

`Arn`  
The Amazon Resource Name \(ARN\) of the server, such as `arn:aws:OpsWorksCM:us-east-1:123456789012:server/server-a1bzhi`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-opsworkscm-server-examples"></a>

### Create an AWS OpsWorks for Chef Automate server<a name="aws-resource-opsworkscm-server-example1"></a>

The following example creates an AWS OpsWorks for Chef Automate server\.

#### JSON<a name="aws-resource-opsworkscm-server-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Parameters": {
        "PivotalKey": {
            "Type": "String"
        },
        "Password": {
            "Type": "String"
        }
    },
    "Resources": {
        "MyChefServer": {
            "Type": "AWS::OpsWorksCM::Server",
            "Properties": {
                "BackupRetentionCount": "12",
                "DisableAutomatedBackup": false,
                "Engine": "Chef",
                "EngineVersion": "12",
                "EngineAttributes": [
                    {
                        "Name": "CHEF_PIVOTAL_KEY",
                        "Value": {
                            "Ref": "PivotalKey"
                        }
                    },
                    {
                        "Name": "CHEF_DELIVERY_ADMIN_PASSWORD",
                        "Value": {
                            "Ref": "Password"
                        }
                    }
                ],
                "EngineModel": "Single",
                "InstanceProfileArn": "arn:aws:iam::123456789012:instance-profile/MyInstanceProfile",
                "InstanceType": "m4.xlarge",
                "PreferredBackupWindow": "08:00",
                "PreferredMaintenanceWindow": "Fri:08:00",
                "ServiceRoleArn": "arn:aws:iam::123456789012:role/MyServiceRole"
            }
        }
    },
    "Outputs": {
        "endpoint": {
            "Description": "OpsWorksCM Server Endpoint",
            "Value": {
                "Fn::GetAtt": [
                    "MyChefServer",
                    "Endpoint"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-opsworkscm-server-example1.yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Parameters:
    PivotalKey:
        Type: String
    Password:
        Type: String
Resources:
  MyChefServer:
    Type: AWS::OpsWorksCM::Server
    Properties:
      BackupRetentionCount: '12'
      DisableAutomatedBackup: False
      Engine: 'Chef'
      EngineVersion: '12'
      EngineAttributes:
          - Name: "CHEF_PIVOTAL_KEY"
            Value:
                Ref: PivotalKey
          - Name: "CHEF_DELIVERY_ADMIN_PASSWORD"
            Value:
                Ref: Password
      EngineModel: 'Single'
      InstanceProfileArn: "arn:aws:iam::123456789012:instance-profile/MyInstanceProfile"
      InstanceType: 'm4.xlarge'
      PreferredBackupWindow: '08:00'
      PreferredMaintenanceWindow: 'Fri:08:00'
      ServiceRoleArn: "arn:aws:iam::123456789012:role/MyServiceRole"
Outputs:
  endpoint:
    Description: OpsWorksCM Server Endpoint
    Value: !GetAtt [MyChefServer, Endpoint]
```

## See Also<a name="aws-resource-opsworkscm-server-seealso"></a>
+ [Create a Chef Automate Server in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opscm-create-server-cfn.html) in the *AWS OpsWorks User Guide* 
+ [Create a Puppet Enterprise Master in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opspup-create-server-cfn.html) in the *AWS OpsWorks User Guide* 
+ [https://docs.aws.amazon.com/opsworks-cm/latest/APIReference/API_CreateServer.html](https://docs.aws.amazon.com/opsworks-cm/latest/APIReference/API_CreateServer.html) in the *AWS OpsWorks CM API Reference*