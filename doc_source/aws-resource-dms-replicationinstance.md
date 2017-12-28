# AWS::DMS::ReplicationInstance<a name="aws-resource-dms-replicationinstance"></a>

The `AWS::DMS::ReplicationInstance` resource creates an AWS DMS replication instance\.


+ [Syntax](#aws-resource-dms-replicationinstance-syntax)
+ [Properties](#aws-resource-dms-replicationinstance-prop)
+ [Return Value](#w3ab2c21c10d323c11)
+ [Example](#aws-resource-dms-replicationinstance-example)
+ [See Also](#w3ab2c21c10d323c15)

## Syntax<a name="aws-resource-dms-replicationinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationinstance-syntax.json"></a>

```
{
  "Type": "AWS::DMS::ReplicationInstance",
  "Properties": {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-allocatedstorage)": Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-autominorversionupgrade)": Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-availabilityzone)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-engineversion)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-kmskeyid)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-multiaz)": Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-preferredmaintenancewindow)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-publiclyaccessible)": Boolean,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-replicationinstanceclass)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-replicationinstanceidentifier)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-replicationsubnetgroupidentifier)": String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-tags)": [ Resource Tag, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-vpcsecuritygroupids)": [ String, ... ]
  }
}
```

### YAML<a name="aws-resource-dms-replicationinstance-syntax.yaml"></a>

```
Type: "AWS::DMS::ReplicationInstance"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-allocatedstorage): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-autominorversionupgrade): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-availabilityzone): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-engineversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-kmskeyid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-multiaz): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-preferredmaintenancewindow): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-publiclyaccessible): Boolean
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-replicationinstanceclass): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-replicationinstanceidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-replicationsubnetgroupidentifier): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-tags): 
    - Resource Tag
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-dms-replicationinstance-vpcsecuritygroupids):
    - String
```

## Properties<a name="aws-resource-dms-replicationinstance-prop"></a>

`AllocatedStorage`  
The amount of storage \(in gigabytes\) to be initially allocated for the replication instance\.  
*Required: *No  
*Type*: Integer  
*Update requires*: No interruption

`AutoMinorVersionUpgrade`  
Indicates that minor engine upgrades will be applied automatically to the replication instance during the maintenance window\.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`AvailabilityZone`  
The EC2 Availability Zone that the replication instance will be created in\. The default value is a random, system\-chosen Availability Zone in the endpoint's region\.  
*Example*: `us-east-1d`  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`EngineVersion`  
The engine version number of the replication instance\.  
*Required: *No  
*Type*: String  
*Update requires*: Some interruptions

`KmsKeyId`  
The KMS key identifier that will be used to encrypt the content on the replication instance\. If you do not specify a value for the `KmsKeyId` parameter, then AWS DMS will use your default encryption key\. AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS region\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`MultiAZ`  
Specifies if the replication instance is a Multi\-AZ deployment\. You cannot set the `AvailabilityZone` parameter if the `MultiAZ` parameter is set to `true` \.  
*Required: *No  
*Type*: Boolean  
*Update requires*: No interruption

`PreferredMaintenanceWindow`  
The weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.   
*Format*: `ddd:hh24:mi-ddd:hh24:mi`  
*Default*: A 30\-minute window selected at random from an 8\-hour block of time per region, occurring on a random day of the week\.   
*Valid Values*: `Mon`, `Tue`, `Wed`, `Thu`, `Fri`, `Sat`, `Sun`  
*Constraints*: Minimum 30\-minute window  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`PubliclyAccessible`  
Specifies the accessibility options for the replication instance\. A value of `true` represents an instance with a public IP address\. A value of `false` represents an instance with a private IP address\. The default value is `true` \.  
*Required: *No  
*Type*: Boolean  
*Update requires*: Replacement

`ReplicationInstanceClass`  
The compute and memory capacity of the replication instance as specified by the replication instance class\.  
*Valid Values*: `dms.t2.micro`, `dms.t2.small`, `dms.t2.medium` , `dms.t2.large`, `dms.c4.large`, `dms.c4.xlarge`, `dms.c4.2xlarge`, `dms.c4.4xlarge`  
*Required: *Yes  
*Type*: String  
*Update requires*: Some interruptions

`ReplicationInstanceIdentifier`  
A name for the replication instance\. If you specify a name, AWS CloudFormation converts it to lower case\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the replication instance identifier\. For more information, see [Name Type](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
*Constraints*:  

+ Must contain from 1 to 63 alphanumeric characters or hyphens\.

+ First character must be a letter\.

+ Cannot end with a hyphen or contain two consecutive hyphens\.
*Example*: `myrepinstance`  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`ReplicationSubnetGroupIdentifier`  
A subnet group to associate with the replication instance\.  
*Required: *No  
*Type*: String  
*Update requires*: Replacement

`Tags`  
The tags that you want to attach to the DMS endpoint\.  
*Required: *No  
*Type*: List of resource tags in key\-value format  
*Update requires*: Replacement

VpcSecurityGroupIds  
Specifies the VPC security group to be used with the replication instance\. The VPC security group must work with the VPC containing the replication instance\.  
*Required: *No  
*Type*: List of String values  
*Update requires*: No interruption

## Return Value<a name="w3ab2c21c10d323c11"></a>

### Ref<a name="w3ab2c21c10d323c11b2"></a>

When you pass the logical ID of an `AWS::DMS::ReplicationInstance` resource to the intrinsic `Ref` function, the function returns the replication instance ARN\.

For more information about using the `Ref` function, see Ref\.

## Example<a name="aws-resource-dms-replicationinstance-example"></a>

### JSON<a name="aws-resource-dms-replicationinstance-example.json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "BasicReplicationInstance": {
      "Type": "AWS::DMS::ReplicationInstance",
      "Properties": {
        "ReplicationInstanceClass": "dms.t2.small"
      }
    }
  }
}
```

### YAML<a name="aws-resource-dms-replicationinstance-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  BasicReplicationInstance:
    Type: 'AWS::DMS::ReplicationInstance'
    Properties:
      ReplicationInstanceClass: dms.t2.small
```

## See Also<a name="w3ab2c21c10d323c15"></a>

+ [CreateReplicationInstance](http://docs.aws.amazon.com/dms/latest/APIReference/API_CreateReplicationInstance.html) in the *AWS Database Migration Service API Reference*\.

+ [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)