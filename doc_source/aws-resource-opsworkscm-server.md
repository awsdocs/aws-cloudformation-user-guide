# AWS::OpsWorksCM::Server<a name="aws-resource-opsworkscm-server"></a>

The `AWS::OpsWorksCM::Server` resource creates an AWS OpsWorks for Chef Automate or AWS OpsWorks for Puppet Enterprise configuration management server\. For more information, see [Create a Chef Automate Server in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opscm-create-server-cfn.html) or [Create a Puppet Enterprise Master in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opspup-create-server-cfn.html) in the *AWS OpsWorks User Guide*, and [CreateServer](https://docs.aws.amazon.com/opsworks-cm/latest/APIReference/API_CreateServer.html) in the *AWS OpsWorks CM API Reference*\.

## Syntax<a name="aws-resource-opsworkscm-server-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opsworkscm-server-syntax.json"></a>

```
{
  "Type" : "AWS::OpsWorksCM::Server",
  "Properties" : {
      "[AssociatePublicIpAddress](#cfn-opsworkscm-server-associatepublicipaddress)" : Boolean,
      "[BackupId](#cfn-opsworkscm-server-backupid)" : String,
      "[BackupRetentionCount](#cfn-opsworkscm-server-backupretentioncount)" : Integer,
      "[DisableAutomatedBackup](#cfn-opsworkscm-server-disableautomatedbackup)" : Boolean,
      "[Engine](#cfn-opsworkscm-server-engine)" : String,
      "[EngineAttributes](#cfn-opsworkscm-server-engineattributes)" : [ [EngineAttribute](aws-properties-opsworkscm-server-engineattribute.md), ... ],
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
Type: AWS::OpsWorksCM::Server
Properties: 
  [AssociatePublicIpAddress](#cfn-opsworkscm-server-associatepublicipaddress): Boolean
  [BackupId](#cfn-opsworkscm-server-backupid): String
  [BackupRetentionCount](#cfn-opsworkscm-server-backupretentioncount): Integer
  [DisableAutomatedBackup](#cfn-opsworkscm-server-disableautomatedbackup): Boolean
  [Engine](#cfn-opsworkscm-server-engine): String
  [EngineAttributes](#cfn-opsworkscm-server-engineattributes): 
    - [EngineAttribute](aws-properties-opsworkscm-server-engineattribute.md)
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

`AssociatePublicIpAddress`  <a name="cfn-opsworkscm-server-associatepublicipaddress"></a>
 Associate a public IP address with a server that you are launching\. Valid values are `true` or `false`\. The default value is `true`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupId`  <a name="cfn-opsworkscm-server-backupid"></a>
 If you specify this field, AWS OpsWorks CM creates the server by using the backup represented by BackupId\.   
*Required*: No  
*Type*: String  
*Maximum*: `79`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BackupRetentionCount`  <a name="cfn-opsworkscm-server-backupretentioncount"></a>
 The number of automated backups that you want to keep\. Whenever a new backup is created, AWS OpsWorks CM deletes the oldest backups if this number is exceeded\. The default value is `1`\.   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisableAutomatedBackup`  <a name="cfn-opsworkscm-server-disableautomatedbackup"></a>
 Enable or disable scheduled backups\. Valid values are `true` or `false`\. The default value is `true`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Engine`  <a name="cfn-opsworkscm-server-engine"></a>
 The configuration management engine to use\. Valid values include `ChefAutomate` and `Puppet`\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineAttributes`  <a name="cfn-opsworkscm-server-engineattributes"></a>
Optional engine attributes on a specified server\.   

**Attributes accepted in a Chef createServer request:**
+  `CHEF_AUTOMATE_PIVOTAL_KEY`: A base64\-encoded RSA public key\. The corresponding private key is required to access the Chef API\. When no CHEF\_AUTOMATE\_PIVOTAL\_KEY is set, a private key is generated and returned in the response\. 
+  `CHEF_AUTOMATE_ADMIN_PASSWORD`: The password for the administrative user in the Chef Automate web\-based dashboard\. The password length is a minimum of eight characters, and a maximum of 32\. The password can contain letters, numbers, and special characters \(\!/@\#$%^&\+=\_\)\. The password must contain at least one lower case letter, one upper case letter, one number, and one special character\. When no CHEF\_AUTOMATE\_ADMIN\_PASSWORD is set, one is generated and returned in the response\.

**Attributes accepted in a Puppet createServer request:**
+  `PUPPET_ADMIN_PASSWORD`: To work with the Puppet Enterprise console, a password must use ASCII characters\.
+  `PUPPET_R10K_REMOTE`: The r10k remote is the URL of your control repository \(for example, ssh://git@your\.git\-repo\.com:user/control\-repo\.git\)\. Specifying an r10k remote opens TCP port 8170\.
+  `PUPPET_R10K_PRIVATE_KEY`: If you are using a private Git repository, add PUPPET\_R10K\_PRIVATE\_KEY to specify a PEM\-encoded private SSH key\.
*Required*: No  
*Type*: List of [EngineAttribute](aws-properties-opsworkscm-server-engineattribute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineModel`  <a name="cfn-opsworkscm-server-enginemodel"></a>
 The engine model of the server\. Valid values in this release include `Monolithic` for Puppet and `Single` for Chef\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EngineVersion`  <a name="cfn-opsworkscm-server-engineversion"></a>
 The major release version of the engine that you want to use\. For a Chef server, the valid value for EngineVersion is currently `12`\. For a Puppet server, the valid value is `2017`\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceProfileArn`  <a name="cfn-opsworkscm-server-instanceprofilearn"></a>
The ARN of the instance profile that your Amazon EC2 instances use\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `arn:aws:iam::[0-9]{12}:instance-profile/.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-opsworkscm-server-instancetype"></a>
 The Amazon EC2 instance type to use\. For example, `m5.large`\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KeyPair`  <a name="cfn-opsworkscm-server-keypair"></a>
 The Amazon EC2 key pair to set for the instance\. This parameter is optional; if desired, you may specify this parameter to connect to your instances by using SSH\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreferredBackupWindow`  <a name="cfn-opsworkscm-server-preferredbackupwindow"></a>
 The start time for a one\-hour period during which AWS OpsWorks CM backs up application\-level data on your server if automated backups are enabled\. Valid values must be specified in one of the following formats:   
+  `HH:MM` for daily backups
+  `DDD:HH:MM` for weekly backups
The specified time is in coordinated universal time \(UTC\)\. The default value is a random, daily start time\.  
 **Example:** `08:00`, which represents a daily start time of 08:00 UTC\.  
 **Example:** `Mon:08:00`, which represents a start time of every Monday at 08:00 UTC\. \(8:00 a\.m\.\)  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-opsworkscm-server-preferredmaintenancewindow"></a>
 The start time for a one\-hour period each week during which AWS OpsWorks CM performs maintenance on the instance\. Valid values must be specified in the following format: `DDD:HH:MM`\. The specified time is in coordinated universal time \(UTC\)\. The default value is a random one\-hour period on Tuesday, Wednesday, or Friday\. See `TimeWindowDefinition` for more information\.   
 **Example:** `Mon:08:00`, which represents a start time of every Monday at 08:00 UTC\. \(8:00 a\.m\.\)   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-opsworkscm-server-securitygroupids"></a>
 A list of security group IDs to attach to the Amazon EC2 instance\. If you add this parameter, the specified security groups must be within the VPC that is specified by `SubnetIds`\.   
 If you do not specify this parameter, AWS OpsWorks CM creates one new security group that uses TCP ports 22 and 443, open to 0\.0\.0\.0/0 \(everyone\)\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServerName`  <a name="cfn-opsworkscm-server-servername"></a>
 The name of the server\. The server name must be unique within your AWS account, within each region\. Server names must start with a letter; then letters, numbers, or hyphens \(\-\) are allowed, up to a maximum of 40 characters\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `40`  
*Pattern*: `[a-zA-Z][a-zA-Z0-9\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceRoleArn`  <a name="cfn-opsworkscm-server-servicerolearn"></a>
 The service role that the AWS OpsWorks CM service backend uses to work with your account\. Although the AWS OpsWorks management console typically creates the service role for you, if you are using the AWS CLI or API commands, run the service\-role\-creation\.yaml AWS CloudFormation template, located at https://s3\.amazonaws\.com/opsworks\-cm\-us\-east\-1\-prod\-default\-assets/misc/opsworks\-cm\-roles\.yaml\. This template creates a CloudFormation stack that includes the service role and instance profile that you need\.   
*Required*: Yes  
*Type*: String  
*Pattern*: `arn:aws:iam::[0-9]{12}:role/.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetIds`  <a name="cfn-opsworkscm-server-subnetids"></a>
 The IDs of subnets in which to launch the server EC2 instance\.   
 Amazon EC2\-Classic customers: This field is required\. All servers must run within a VPC\. The VPC must have "Auto Assign Public IP" enabled\.   
 EC2\-VPC customers: This field is optional\. If you do not specify subnet IDs, your EC2 instances are created in a default subnet that is selected by Amazon EC2\. If you specify subnet IDs, the VPC must have "Auto Assign Public IP" enabled\.   
For more information about supported Amazon EC2 platforms, see [Supported Platforms](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-supported-platforms.html)\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-opsworkscm-server-return-values"></a>

### Ref<a name="aws-resource-opsworkscm-server-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the server's ARN, such as `arn:aws:OpsWorksCM:us-east-1:123456789012:server/server-a1bzhi`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-opsworkscm-server-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-opsworkscm-server-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the server, such as `arn:aws:OpsWorksCM:us-east-1:123456789012:server/server-a1bzhi`\.

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
A DNS name that can be used to access the engine\. Example: `myserver-asdfghjkl.us-east-1.opsworks.io`\.

## Examples<a name="aws-resource-opsworkscm-server--examples"></a>

### Create an AWS OpsWorks for Chef Automate server<a name="aws-resource-opsworkscm-server--examples--Create_an_AWS_OpsWorks_for_Chef_Automate_server"></a>

The following example creates an AWS OpsWorks for Chef Automate server\.

#### JSON<a name="aws-resource-opsworkscm-server--examples--Create_an_AWS_OpsWorks_for_Chef_Automate_server--json"></a>

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
                "Engine": "ChefAutomate",
                "EngineVersion": "2",
                "EngineAttributes": [
                    {
                        "Name": "CHEF_AUTOMATE_PIVOTAL_KEY",
                        "Value": {
                            "Ref": "PivotalKey"
                        }
                    },
                    {
                        "Name": "CHEF_AUTOMATE_ADMIN_PASSWORD",
                        "Value": {
                            "Ref": "Password"
                        }
                    }
                ],
                "EngineModel": "Single",
                "InstanceProfileArn": "INSTANCE-PROFILE-ARN",
                "InstanceType": "r5.xlarge",
                "PreferredBackupWindow": "08:00",
                "PreferredMaintenanceWindow": "Fri:08:00",
                "ServiceRoleArn": "SERVICE-ROLE-ARN"
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

#### YAML<a name="aws-resource-opsworkscm-server--examples--Create_an_AWS_OpsWorks_for_Chef_Automate_server--yaml"></a>

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
      Engine: 'ChefAutomate'
      EngineVersion: '2'
      EngineAttributes:
          - Name: "CHEF_AUTOMATE_PIVOTAL_KEY"
            Value:
                Ref: PivotalKey
          - Name: "CHEF_AUTOMATE_ADMIN_PASSWORD"
            Value:
                Ref: Password
      EngineModel: 'Single'
      InstanceProfileArn: "INSTANCE-PROFILE-ARN"
      InstanceType: 'r5.xlarge'
      PreferredBackupWindow: '08:00'
      PreferredMaintenanceWindow: 'Fri:08:00'
      ServiceRoleArn: "SERVICE-ROLE-ARN"
Outputs:
  endpoint:
    Description: OpsWorksCM Server Endpoint
    Value: !GetAtt [MyChefServer, Endpoint]
```

### Create an AWS OpsWorks for Puppet Enterprise server<a name="aws-resource-opsworkscm-server--examples--Create_an_AWS_OpsWorks_for_Puppet_Enterprise_server"></a>

The following example creates an AWS OpsWorks for Puppet Enterprise server\.

#### JSON<a name="aws-resource-opsworkscm-server--examples--Create_an_AWS_OpsWorks_for_Puppet_Enterprise_server--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "My OpsWorksCM Managed Server",
    "Parameters": {
        "AdminPassword": {
            "Type": "String"
        }
    },
    "Resources": {
        "TestServerDeleteMe": {
            "Type": "AWS::OpsWorksCM::Server",
            "Properties": {
                "AssociatePublicIpAddress": true,
                "BackupRetentionCount": "12",
                "DisableAutomatedBackup": false,
                "Engine": "Puppet",
                "EngineVersion": "2017",
                "EngineAttributes": [
                    {
                        "Name": "PUPPET_ADMIN_PASSWORD",
                        "Value": {
                            "Ref": "AdminPassword"
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
    }
}
```

#### YAML<a name="aws-resource-opsworkscm-server--examples--Create_an_AWS_OpsWorks_for_Puppet_Enterprise_server--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: IAM Resources for the AWS OpsWorks Managed Server.
Parameters:
    AdminPassword:
        Type: String
Resources:
  MyPuppetServer:
    Type: AWS::OpsWorksCM::Server
    Properties:
      BackupRetentionCount: '12'
      DisableAutomatedBackup: False
      Engine: 'Puppet'
      EngineVersion: '2017'
      EngineAttributes:
        - Name: "PUPPET_ADMIN_PASSWORD"
          Value:
              Ref: AdminPassword
      EngineModel: 'Monolithic'
      InstanceProfileArn: "INSTANCE-PROFILE-ARN"
      InstanceType: 'm4.large'
      PreferredBackupWindow: '08:00'
      PreferredMaintenanceWindow: 'Fri:08:00'
      ServiceRoleArn: "SERVICE-ROLE-ARN"
Outputs:
    endpoint:
      Description: OpsWorksCM Server Endpoint
      Value: !GetAtt [MyPuppetServer, Endpoint]
```

## See Also<a name="aws-resource-opsworkscm-server--seealso"></a>
+  [Create a Chef Automate Server in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opscm-create-server-cfn.html) in the *AWS OpsWorks User Guide* 
+  [Create a Puppet Enterprise Master in AWS CloudFormation](https://docs.aws.amazon.com/opsworks/latest/userguide/opspup-create-server-cfn.html) in the *AWS OpsWorks User Guide* 
+  [ `CreateServer` ](https://docs.aws.amazon.com/opsworks-cm/latest/APIReference/API_CreateServer.html) in the *AWS OpsWorks CM API Reference* 