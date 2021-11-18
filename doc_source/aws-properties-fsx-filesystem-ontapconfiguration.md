# AWS::FSx::FileSystem OntapConfiguration<a name="aws-properties-fsx-filesystem-ontapconfiguration"></a>

<a name="aws-properties-fsx-filesystem-ontapconfiguration-description"></a>The `OntapConfiguration` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::FSx::FileSystem](aws-resource-fsx-filesystem.md)\.

## Syntax<a name="aws-properties-fsx-filesystem-ontapconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-fsx-filesystem-ontapconfiguration-syntax.json"></a>

```
{
  "[AutomaticBackupRetentionDays](#cfn-fsx-filesystem-ontapconfiguration-automaticbackupretentiondays)" : Integer,
  "[DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-ontapconfiguration-dailyautomaticbackupstarttime)" : String,
  "[DeploymentType](#cfn-fsx-filesystem-ontapconfiguration-deploymenttype)" : String,
  "[DiskIopsConfiguration](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration)" : DiskIopsConfiguration,
  "[EndpointIpAddressRange](#cfn-fsx-filesystem-ontapconfiguration-endpointipaddressrange)" : String,
  "[FsxAdminPassword](#cfn-fsx-filesystem-ontapconfiguration-fsxadminpassword)" : String,
  "[PreferredSubnetId](#cfn-fsx-filesystem-ontapconfiguration-preferredsubnetid)" : String,
  "[RouteTableIds](#cfn-fsx-filesystem-ontapconfiguration-routetableids)" : [ String, ... ],
  "[ThroughputCapacity](#cfn-fsx-filesystem-ontapconfiguration-throughputcapacity)" : Integer,
  "[WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-ontapconfiguration-weeklymaintenancestarttime)" : String
}
```

### YAML<a name="aws-properties-fsx-filesystem-ontapconfiguration-syntax.yaml"></a>

```
  [AutomaticBackupRetentionDays](#cfn-fsx-filesystem-ontapconfiguration-automaticbackupretentiondays): Integer
  [DailyAutomaticBackupStartTime](#cfn-fsx-filesystem-ontapconfiguration-dailyautomaticbackupstarttime): String
  [DeploymentType](#cfn-fsx-filesystem-ontapconfiguration-deploymenttype): String
  [DiskIopsConfiguration](#cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration): 
    DiskIopsConfiguration
  [EndpointIpAddressRange](#cfn-fsx-filesystem-ontapconfiguration-endpointipaddressrange): String
  [FsxAdminPassword](#cfn-fsx-filesystem-ontapconfiguration-fsxadminpassword): String
  [PreferredSubnetId](#cfn-fsx-filesystem-ontapconfiguration-preferredsubnetid): String
  [RouteTableIds](#cfn-fsx-filesystem-ontapconfiguration-routetableids): 
    - String
  [ThroughputCapacity](#cfn-fsx-filesystem-ontapconfiguration-throughputcapacity): Integer
  [WeeklyMaintenanceStartTime](#cfn-fsx-filesystem-ontapconfiguration-weeklymaintenancestarttime): String
```

## Properties<a name="aws-properties-fsx-filesystem-ontapconfiguration-properties"></a>

`AutomaticBackupRetentionDays`  <a name="cfn-fsx-filesystem-ontapconfiguration-automaticbackupretentiondays"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DailyAutomaticBackupStartTime`  <a name="cfn-fsx-filesystem-ontapconfiguration-dailyautomaticbackupstarttime"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeploymentType`  <a name="cfn-fsx-filesystem-ontapconfiguration-deploymenttype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`DiskIopsConfiguration`  <a name="cfn-fsx-filesystem-ontapconfiguration-diskiopsconfiguration"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [DiskIopsConfiguration](aws-properties-fsx-filesystem-ontapconfiguration-diskiopsconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointIpAddressRange`  <a name="cfn-fsx-filesystem-ontapconfiguration-endpointipaddressrange"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`FsxAdminPassword`  <a name="cfn-fsx-filesystem-ontapconfiguration-fsxadminpassword"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreferredSubnetId`  <a name="cfn-fsx-filesystem-ontapconfiguration-preferredsubnetid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RouteTableIds`  <a name="cfn-fsx-filesystem-ontapconfiguration-routetableids"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ThroughputCapacity`  <a name="cfn-fsx-filesystem-ontapconfiguration-throughputcapacity"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WeeklyMaintenanceStartTime`  <a name="cfn-fsx-filesystem-ontapconfiguration-weeklymaintenancestarttime"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)