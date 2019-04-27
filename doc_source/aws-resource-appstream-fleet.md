# AWS::AppStream::Fleet<a name="aws-resource-appstream-fleet"></a>

The `AWS::AppStream::Fleet` resource creates a fleet for Amazon AppStream 2\.0\. A fleet consists of streaming instances that run a specified image\.

## Syntax<a name="aws-resource-appstream-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::Fleet",
  "Properties" : {
      "[ComputeCapacity](#cfn-appstream-fleet-computecapacity)" : [ComputeCapacity](aws-properties-appstream-fleet-computecapacity.md),
      "[Description](#cfn-appstream-fleet-description)" : String,
      "[DisconnectTimeoutInSeconds](#cfn-appstream-fleet-disconnecttimeoutinseconds)" : Integer,
      "[DisplayName](#cfn-appstream-fleet-displayname)" : String,
      "[DomainJoinInfo](#cfn-appstream-fleet-domainjoininfo)" : [DomainJoinInfo](aws-properties-appstream-fleet-domainjoininfo.md),
      "[EnableDefaultInternetAccess](#cfn-appstream-fleet-enabledefaultinternetaccess)" : Boolean,
      "[FleetType](#cfn-appstream-fleet-fleettype)" : String,
      "[ImageArn](#cfn-appstream-fleet-imagearn)" : String,
      "[ImageName](#cfn-appstream-fleet-imagename)" : String,
      "[InstanceType](#cfn-appstream-fleet-instancetype)" : String,
      "[MaxUserDurationInSeconds](#cfn-appstream-fleet-maxuserdurationinseconds)" : Integer,
      "[Name](#cfn-appstream-fleet-name)" : String,
      "[Tags](#cfn-appstream-fleet-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcConfig](#cfn-appstream-fleet-vpcconfig)" : [VpcConfig](aws-properties-appstream-fleet-vpcconfig.md)
    }
}
```

### YAML<a name="aws-resource-appstream-fleet-syntax.yaml"></a>

```
Type: AWS::AppStream::Fleet
Properties : 
﻿  [ComputeCapacity](#cfn-appstream-fleet-computecapacity) : [ComputeCapacity](aws-properties-appstream-fleet-computecapacity.md)
﻿  [Description](#cfn-appstream-fleet-description) : String
﻿  [DisconnectTimeoutInSeconds](#cfn-appstream-fleet-disconnecttimeoutinseconds) : Integer
﻿  [DisplayName](#cfn-appstream-fleet-displayname) : String
﻿  [DomainJoinInfo](#cfn-appstream-fleet-domainjoininfo) : [DomainJoinInfo](aws-properties-appstream-fleet-domainjoininfo.md)
﻿  [EnableDefaultInternetAccess](#cfn-appstream-fleet-enabledefaultinternetaccess) : Boolean
﻿  [FleetType](#cfn-appstream-fleet-fleettype) : String
﻿  [ImageArn](#cfn-appstream-fleet-imagearn) : String
﻿  [ImageName](#cfn-appstream-fleet-imagename) : String
﻿  [InstanceType](#cfn-appstream-fleet-instancetype) : String
﻿  [MaxUserDurationInSeconds](#cfn-appstream-fleet-maxuserdurationinseconds) : Integer
﻿  [Name](#cfn-appstream-fleet-name) : String
﻿  [Tags](#cfn-appstream-fleet-tags) : 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
﻿  [VpcConfig](#cfn-appstream-fleet-vpcconfig) : [VpcConfig](aws-properties-appstream-fleet-vpcconfig.md)
```

## Properties<a name="aws-resource-appstream-fleet-properties"></a>

`ComputeCapacity`  <a name="cfn-appstream-fleet-computecapacity"></a>
The desired capacity for the fleet\.  
*Required*: Yes  
*Type*: [ComputeCapacity](aws-properties-appstream-fleet-computecapacity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-appstream-fleet-description"></a>
The description to display\.  
*Required*: No  
*Type*: String  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisconnectTimeoutInSeconds`  <a name="cfn-appstream-fleet-disconnecttimeoutinseconds"></a>
The time after disconnection when a session is considered to have ended, in seconds\. If a user who was disconnected reconnects within this time interval, the user is connected to their previous session\. Specify a value between 60 and 360000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DisplayName`  <a name="cfn-appstream-fleet-displayname"></a>
The fleet name to display\.  
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainJoinInfo`  <a name="cfn-appstream-fleet-domainjoininfo"></a>
The name of the directory and organizational unit \(OU\) to use to join the fleet to a Microsoft Active Directory domain\.   
*Required*: No  
*Type*: [DomainJoinInfo](aws-properties-appstream-fleet-domainjoininfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableDefaultInternetAccess`  <a name="cfn-appstream-fleet-enabledefaultinternetaccess"></a>
Enables or disables default internet access for the fleet\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FleetType`  <a name="cfn-appstream-fleet-fleettype"></a>
The fleet type\.    
ALWAYS\_ON  
Provides users with instant\-on access to their apps\. You are charged for all running instances in your fleet, even if no users are streaming apps\.  
ON\_DEMAND  
Provide users with access to applications after they connect, which takes one to two minutes\. You are charged for instance streaming when users are connected and a small hourly fee for instances that are not streaming apps\.
*Required*: No  
*Type*: String  
*Allowed Values*: `ALWAYS_ON | ON_DEMAND`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ImageArn`  <a name="cfn-appstream-fleet-imagearn"></a>
The ARN of the public, private, or shared image to use\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws:[A-Za-z0-9][A-Za-z0-9_/.-]{0,62}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9][A-Za-z0-9:_/+=,@.-]{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageName`  <a name="cfn-appstream-fleet-imagename"></a>
The name of the image used to create the fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-appstream-fleet-instancetype"></a>
The instance type to use when launching fleet instances\. The following instance types are available:  
+ stream\.standard\.medium
+ stream\.standard\.large
+ stream\.compute\.large
+ stream\.compute\.xlarge
+ stream\.compute\.2xlarge
+ stream\.compute\.4xlarge
+ stream\.compute\.8xlarge
+ stream\.memory\.large
+ stream\.memory\.xlarge
+ stream\.memory\.2xlarge
+ stream\.memory\.4xlarge
+ stream\.memory\.8xlarge
+ stream\.graphics\-design\.large
+ stream\.graphics\-design\.xlarge
+ stream\.graphics\-design\.2xlarge
+ stream\.graphics\-design\.4xlarge
+ stream\.graphics\-desktop\.2xlarge
+ stream\.graphics\-pro\.4xlarge
+ stream\.graphics\-pro\.8xlarge
+ stream\.graphics\-pro\.16xlarge
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxUserDurationInSeconds`  <a name="cfn-appstream-fleet-maxuserdurationinseconds"></a>
The maximum time that a streaming session can run, in seconds\. Specify a value between 600 and 360000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appstream-fleet-name"></a>
A unique name for the fleet\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9_.-]{0,100}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-appstream-fleet-tags"></a>
An array of key\-value pairs\. For more information, see [Using Cost Allocation Tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS Billing and Cost Management User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfig`  <a name="cfn-appstream-fleet-vpcconfig"></a>
The VPC configuration for the fleet\.  
*Required*: No  
*Type*: [VpcConfig](aws-properties-appstream-fleet-vpcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See Also<a name="aws-resource-appstream-fleet--seealso"></a>
+  [CreateFleet](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateFleet.html) in the *Amazon AppStream 2\.0 API Reference* 