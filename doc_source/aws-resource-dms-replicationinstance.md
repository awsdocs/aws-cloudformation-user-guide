# AWS::DMS::ReplicationInstance<a name="aws-resource-dms-replicationinstance"></a>

The `AWS::DMS::ReplicationInstance` resource creates an AWS DMS replication instance\. 

## Syntax<a name="aws-resource-dms-replicationinstance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dms-replicationinstance-syntax.json"></a>

```
{
  "Type" : "AWS::DMS::ReplicationInstance",
  "Properties" : {
      "[AllocatedStorage](#cfn-dms-replicationinstance-allocatedstorage)" : Integer,
      "[AllowMajorVersionUpgrade](#cfn-dms-replicationinstance-allowmajorversionupgrade)" : Boolean,
      "[AutoMinorVersionUpgrade](#cfn-dms-replicationinstance-autominorversionupgrade)" : Boolean,
      "[AvailabilityZone](#cfn-dms-replicationinstance-availabilityzone)" : String,
      "[EngineVersion](#cfn-dms-replicationinstance-engineversion)" : String,
      "[KmsKeyId](#cfn-dms-replicationinstance-kmskeyid)" : String,
      "[MultiAZ](#cfn-dms-replicationinstance-multiaz)" : Boolean,
      "[PreferredMaintenanceWindow](#cfn-dms-replicationinstance-preferredmaintenancewindow)" : String,
      "[PubliclyAccessible](#cfn-dms-replicationinstance-publiclyaccessible)" : Boolean,
      "[ReplicationInstanceClass](#cfn-dms-replicationinstance-replicationinstanceclass)" : String,
      "[ReplicationInstanceIdentifier](#cfn-dms-replicationinstance-replicationinstanceidentifier)" : String,
      "[ReplicationSubnetGroupIdentifier](#cfn-dms-replicationinstance-replicationsubnetgroupidentifier)" : String,
      "[Tags](#cfn-dms-replicationinstance-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcSecurityGroupIds](#cfn-dms-replicationinstance-vpcsecuritygroupids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-dms-replicationinstance-syntax.yaml"></a>

```
Type: AWS::DMS::ReplicationInstance
Properties: 
  [AllocatedStorage](#cfn-dms-replicationinstance-allocatedstorage): Integer
  [AllowMajorVersionUpgrade](#cfn-dms-replicationinstance-allowmajorversionupgrade): Boolean
  [AutoMinorVersionUpgrade](#cfn-dms-replicationinstance-autominorversionupgrade): Boolean
  [AvailabilityZone](#cfn-dms-replicationinstance-availabilityzone): String
  [EngineVersion](#cfn-dms-replicationinstance-engineversion): String
  [KmsKeyId](#cfn-dms-replicationinstance-kmskeyid): String
  [MultiAZ](#cfn-dms-replicationinstance-multiaz): Boolean
  [PreferredMaintenanceWindow](#cfn-dms-replicationinstance-preferredmaintenancewindow): String
  [PubliclyAccessible](#cfn-dms-replicationinstance-publiclyaccessible): Boolean
  [ReplicationInstanceClass](#cfn-dms-replicationinstance-replicationinstanceclass): String
  [ReplicationInstanceIdentifier](#cfn-dms-replicationinstance-replicationinstanceidentifier): String
  [ReplicationSubnetGroupIdentifier](#cfn-dms-replicationinstance-replicationsubnetgroupidentifier): String
  [Tags](#cfn-dms-replicationinstance-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcSecurityGroupIds](#cfn-dms-replicationinstance-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-resource-dms-replicationinstance-properties"></a>

`AllocatedStorage`  <a name="cfn-dms-replicationinstance-allocatedstorage"></a>
The amount of storage \(in gigabytes\) to be initially allocated for the replication instance\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AllowMajorVersionUpgrade`  <a name="cfn-dms-replicationinstance-allowmajorversionupgrade"></a>
Indicates that major version upgrades are allowed\. Changing this parameter does not result in an outage, and the change is asynchronously applied as soon as possible\.  
This parameter must be set to `true` when specifying a value for the `EngineVersion` parameter that is a different major version than the replication instance's current version\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoMinorVersionUpgrade`  <a name="cfn-dms-replicationinstance-autominorversionupgrade"></a>
A value that indicates whether minor engine upgrades are applied automatically to the replication instance during the maintenance window\. This parameter defaults to `true`\.  
Default: `true`   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZone`  <a name="cfn-dms-replicationinstance-availabilityzone"></a>
The Availability Zone that the replication instance will be created in\.  
The default value is a random, system\-chosen Availability Zone in the endpoint's AWS Region, for example: `us-east-1d`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EngineVersion`  <a name="cfn-dms-replicationinstance-engineversion"></a>
The engine version number of the replication instance\.  
If an engine version number is not specified when a replication instance is created, the default is the latest engine version available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-dms-replicationinstance-kmskeyid"></a>
An AWS KMS key identifier that is used to encrypt the data on the replication instance\.  
If you don't specify a value for the `KmsKeyId` parameter, then AWS DMS uses your default encryption key\.  
AWS KMS creates the default encryption key for your AWS account\. Your AWS account has a different default encryption key for each AWS Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`MultiAZ`  <a name="cfn-dms-replicationinstance-multiaz"></a>
 Specifies whether the replication instance is a Multi\-AZ deployment\. You can't set the `AvailabilityZone` parameter if the Multi\-AZ parameter is set to `true`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-dms-replicationinstance-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur, in Universal Coordinated Time \(UTC\)\.  
 Format: `ddd:hh24:mi-ddd:hh24:mi`   
Default: A 30\-minute window selected at random from an 8\-hour block of time per AWS Region, occurring on a random day of the week\.  
Valid Days: Mon, Tue, Wed, Thu, Fri, Sat, Sun  
Constraints: Minimum 30\-minute window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PubliclyAccessible`  <a name="cfn-dms-replicationinstance-publiclyaccessible"></a>
 Specifies the accessibility options for the replication instance\. A value of `true` represents an instance with a public IP address\. A value of `false` represents an instance with a private IP address\. The default value is `true`\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReplicationInstanceClass`  <a name="cfn-dms-replicationinstance-replicationinstanceclass"></a>
The compute and memory capacity of the replication instance as defined for the specified replication instance class\. For example to specify the instance class dms\.c4\.large, set this parameter to `"dms.c4.large"`\.  
For more information on the settings and capacities for the available replication instance classes, see [ Selecting the right AWS DMS replication instance for your migration](https://docs.aws.amazon.com/dms/latest/userguide/CHAP_ReplicationInstance.html#CHAP_ReplicationInstance.InDepth)\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationInstanceIdentifier`  <a name="cfn-dms-replicationinstance-replicationinstanceidentifier"></a>
The replication instance identifier\. This parameter is stored as a lowercase string\.  
Constraints:  
+ Must contain 1\-63 alphanumeric characters or hyphens\.
+ First character must be a letter\.
+ Can't end with a hyphen or contain two consecutive hyphens\.
Example: `myrepinstance`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationSubnetGroupIdentifier`  <a name="cfn-dms-replicationinstance-replicationsubnetgroupidentifier"></a>
A subnet group to associate with the replication instance\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-dms-replicationinstance-tags"></a>
One or more tags to be assigned to the replication instance\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcSecurityGroupIds`  <a name="cfn-dms-replicationinstance-vpcsecuritygroupids"></a>
 Specifies the VPC security group to be used with the replication instance\. The VPC security group must work with the VPC containing the replication instance\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dms-replicationinstance-return-values"></a>

### Ref<a name="aws-resource-dms-replicationinstance-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the replication instance ARN\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-dms-replicationinstance-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-dms-replicationinstance-return-values-fn--getatt-fn--getatt"></a>

`ReplicationInstancePrivateIpAddresses`  <a name="ReplicationInstancePrivateIpAddresses-fn::getatt"></a>
One or more private IP addresses for the replication instance\.

`ReplicationInstancePublicIpAddresses`  <a name="ReplicationInstancePublicIpAddresses-fn::getatt"></a>
One or more public IP addresses for the replication instance\.

## Examples<a name="aws-resource-dms-replicationinstance--examples"></a>



### <a name="aws-resource-dms-replicationinstance--examples--"></a>

#### JSON<a name="aws-resource-dms-replicationinstance--examples----json"></a>

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

#### YAML<a name="aws-resource-dms-replicationinstance--examples----yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources: 
  BasicReplicationInstance: 
    Properties: 
      ReplicationInstanceClass: dms.t2.small
    Type: "AWS::DMS::ReplicationInstance"
```

## See also<a name="aws-resource-dms-replicationinstance--seealso"></a>
+  [CreateReplicationInstance](https://docs.aws.amazon.com/dms/latest/APIReference/API_CreateReplicationInstance.html) in the *AWS Database Migration Service API Reference* 
+  [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) 

