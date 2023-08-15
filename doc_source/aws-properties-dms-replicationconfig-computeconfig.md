# AWS::DMS::ReplicationConfig ComputeConfig<a name="aws-properties-dms-replicationconfig-computeconfig"></a>

Configuration parameters for provisioning an AWS DMS Serverless replication\.

## Syntax<a name="aws-properties-dms-replicationconfig-computeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dms-replicationconfig-computeconfig-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-dms-replicationconfig-computeconfig-availabilityzone)" : String,
  "[DnsNameServers](#cfn-dms-replicationconfig-computeconfig-dnsnameservers)" : String,
  "[KmsKeyId](#cfn-dms-replicationconfig-computeconfig-kmskeyid)" : String,
  "[MaxCapacityUnits](#cfn-dms-replicationconfig-computeconfig-maxcapacityunits)" : Integer,
  "[MinCapacityUnits](#cfn-dms-replicationconfig-computeconfig-mincapacityunits)" : Integer,
  "[MultiAZ](#cfn-dms-replicationconfig-computeconfig-multiaz)" : Boolean,
  "[PreferredMaintenanceWindow](#cfn-dms-replicationconfig-computeconfig-preferredmaintenancewindow)" : String,
  "[ReplicationSubnetGroupId](#cfn-dms-replicationconfig-computeconfig-replicationsubnetgroupid)" : String,
  "[VpcSecurityGroupIds](#cfn-dms-replicationconfig-computeconfig-vpcsecuritygroupids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-dms-replicationconfig-computeconfig-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-dms-replicationconfig-computeconfig-availabilityzone): String
  [DnsNameServers](#cfn-dms-replicationconfig-computeconfig-dnsnameservers): String
  [KmsKeyId](#cfn-dms-replicationconfig-computeconfig-kmskeyid): String
  [MaxCapacityUnits](#cfn-dms-replicationconfig-computeconfig-maxcapacityunits): Integer
  [MinCapacityUnits](#cfn-dms-replicationconfig-computeconfig-mincapacityunits): Integer
  [MultiAZ](#cfn-dms-replicationconfig-computeconfig-multiaz): Boolean
  [PreferredMaintenanceWindow](#cfn-dms-replicationconfig-computeconfig-preferredmaintenancewindow): String
  [ReplicationSubnetGroupId](#cfn-dms-replicationconfig-computeconfig-replicationsubnetgroupid): String
  [VpcSecurityGroupIds](#cfn-dms-replicationconfig-computeconfig-vpcsecuritygroupids): 
    - String
```

## Properties<a name="aws-properties-dms-replicationconfig-computeconfig-properties"></a>

`AvailabilityZone`  <a name="cfn-dms-replicationconfig-computeconfig-availabilityzone"></a>
The Availability Zone where the AWS DMS Serverless replication using this configuration will run\. The default value is a random, system\-chosen Availability Zone in the configuration's AWS Region, for example, `"us-west-2"`\. You can't set this parameter if the `MultiAZ` parameter is set to `true`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DnsNameServers`  <a name="cfn-dms-replicationconfig-computeconfig-dnsnameservers"></a>
A list of custom DNS name servers supported for the AWS DMS Serverless replication to access your source or target database\. This list overrides the default name servers supported by the AWS DMS Serverless replication\. You can specify a comma\-separated list of internet addresses for up to four DNS name servers\. For example: `"1.1.1.1,2.2.2.2,3.3.3.3,4.4.4.4"`   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-dms-replicationconfig-computeconfig-kmskeyid"></a>
An AWS Key Management Service \(AWS KMS\) key Amazon Resource Name \(ARN\) that is used to encrypt the data during AWS DMS Serverless replication\.  
If you don't specify a value for the `KmsKeyId` parameter, AWS DMS uses your default encryption key\.  
 AWS KMS creates the default encryption key for your Amazon Web Services account\. Your AWS account has a different default encryption key for each AWS Region\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxCapacityUnits`  <a name="cfn-dms-replicationconfig-computeconfig-maxcapacityunits"></a>
Specifies the maximum value of the AWS DMS capacity units \(DCUs\) for which a given AWS DMS Serverless replication can be provisioned\. A single DCU is 2GB of RAM, with 1 DCU as the minimum value allowed\. The list of valid DCU values includes 1, 2, 4, 8, 16, 32, 64, 128, 192, 256, and 384\. So, the maximum value that you can specify for AWS DMS Serverless is 384\. The `MaxCapacityUnits` parameter is the only DCU parameter you are required to specify\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MinCapacityUnits`  <a name="cfn-dms-replicationconfig-computeconfig-mincapacityunits"></a>
Specifies the minimum value of the AWS DMS capacity units \(DCUs\) for which a given AWS DMS Serverless replication can be provisioned\. A single DCU is 2GB of RAM, with 1 DCU as the minimum value allowed\. The list of valid DCU values includes 1, 2, 4, 8, 16, 32, 64, 128, 192, 256, and 384\. So, the minimum DCU value that you can specify for AWS DMS Serverless is 1\. You don't have to specify a value for the `MinCapacityUnits` parameter\. If you don't set this value, AWS DMS scans the current activity of available source tables to identify an optimum setting for this parameter\. If there is no current source activity or AWS DMS can't otherwise identify a more appropriate value, it sets this parameter to the minimum DCU value allowed, 1\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiAZ`  <a name="cfn-dms-replicationconfig-computeconfig-multiaz"></a>
Specifies whether the AWS DMS Serverless replication is a Multi\-AZ deployment\. You can't set the `AvailabilityZone` parameter if the `MultiAZ` parameter is set to `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredMaintenanceWindow`  <a name="cfn-dms-replicationconfig-computeconfig-preferredmaintenancewindow"></a>
The weekly time range during which system maintenance can occur for the AWS DMS Serverless replication, in Universal Coordinated Time \(UTC\)\. The format is `ddd:hh24:mi-ddd:hh24:mi`\.  
The default is a 30\-minute window selected at random from an 8\-hour block of time per AWS Region\. This maintenance occurs on a random day of the week\. Valid values for days of the week include `Mon`, `Tue`, `Wed`, `Thu`, `Fri`, `Sat`, and `Sun`\.  
Constraints include a minimum 30\-minute window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReplicationSubnetGroupId`  <a name="cfn-dms-replicationconfig-computeconfig-replicationsubnetgroupid"></a>
Specifies a subnet group identifier to associate with the AWS DMS Serverless replication\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcSecurityGroupIds`  <a name="cfn-dms-replicationconfig-computeconfig-vpcsecuritygroupids"></a>
Specifies the virtual private cloud \(VPC\) security group to use with the AWS DMS Serverless replication\. The VPC security group must work with the VPC containing the replication\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)