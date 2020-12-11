# AWS::AppStream::Fleet<a name="aws-resource-appstream-fleet"></a>

The `AWS::AppStream::Fleet` resource creates a fleet for Amazon AppStream 2\.0\. A fleet consists of streaming instances that run a specified image\.

## Syntax<a name="aws-resource-appstream-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::Fleet",
  "Properties" : {
      "[ComputeCapacity](#cfn-appstream-fleet-computecapacity)" : ComputeCapacity,
      "[Description](#cfn-appstream-fleet-description)" : String,
      "[DisconnectTimeoutInSeconds](#cfn-appstream-fleet-disconnecttimeoutinseconds)" : Integer,
      "[DisplayName](#cfn-appstream-fleet-displayname)" : String,
      "[DomainJoinInfo](#cfn-appstream-fleet-domainjoininfo)" : DomainJoinInfo,
      "[EnableDefaultInternetAccess](#cfn-appstream-fleet-enabledefaultinternetaccess)" : Boolean,
      "[FleetType](#cfn-appstream-fleet-fleettype)" : String,
      "[IamRoleArn](#cfn-appstream-fleet-iamrolearn)" : String,
      "[IdleDisconnectTimeoutInSeconds](#cfn-appstream-fleet-idledisconnecttimeoutinseconds)" : Integer,
      "[ImageArn](#cfn-appstream-fleet-imagearn)" : String,
      "[ImageName](#cfn-appstream-fleet-imagename)" : String,
      "[InstanceType](#cfn-appstream-fleet-instancetype)" : String,
      "[MaxUserDurationInSeconds](#cfn-appstream-fleet-maxuserdurationinseconds)" : Integer,
      "[Name](#cfn-appstream-fleet-name)" : String,
      "[StreamView](#cfn-appstream-fleet-streamview)" : String,
      "[Tags](#cfn-appstream-fleet-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpcConfig](#cfn-appstream-fleet-vpcconfig)" : VpcConfig
    }
}
```

### YAML<a name="aws-resource-appstream-fleet-syntax.yaml"></a>

```
Type: AWS::AppStream::Fleet
Properties: 
  [ComputeCapacity](#cfn-appstream-fleet-computecapacity): 
    ComputeCapacity
  [Description](#cfn-appstream-fleet-description): String
  [DisconnectTimeoutInSeconds](#cfn-appstream-fleet-disconnecttimeoutinseconds): Integer
  [DisplayName](#cfn-appstream-fleet-displayname): String
  [DomainJoinInfo](#cfn-appstream-fleet-domainjoininfo): 
    DomainJoinInfo
  [EnableDefaultInternetAccess](#cfn-appstream-fleet-enabledefaultinternetaccess): Boolean
  [FleetType](#cfn-appstream-fleet-fleettype): String
  [IamRoleArn](#cfn-appstream-fleet-iamrolearn): String
  [IdleDisconnectTimeoutInSeconds](#cfn-appstream-fleet-idledisconnecttimeoutinseconds): Integer
  [ImageArn](#cfn-appstream-fleet-imagearn): String
  [ImageName](#cfn-appstream-fleet-imagename): String
  [InstanceType](#cfn-appstream-fleet-instancetype): String
  [MaxUserDurationInSeconds](#cfn-appstream-fleet-maxuserdurationinseconds): Integer
  [Name](#cfn-appstream-fleet-name): String
  [StreamView](#cfn-appstream-fleet-streamview): String
  [Tags](#cfn-appstream-fleet-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpcConfig](#cfn-appstream-fleet-vpcconfig): 
    VpcConfig
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
The amount of time that a streaming session remains active after users disconnect\. If users try to reconnect to the streaming session after a disconnection or network interruption within this time interval, they are connected to their previous session\. Otherwise, they are connected to a new session with a new streaming instance\.   
Specify a value between 60 and 360000\.  
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
*Allowed values*: `ALWAYS_ON | ON_DEMAND`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`IamRoleArn`  <a name="cfn-appstream-fleet-iamrolearn"></a>
The ARN of the IAM role that is applied to the fleet\. To assume a role, the fleet instance calls the AWS Security Token Service \(STS\) `AssumeRole` API operation and passes the ARN of the role to use\. The operation creates a new session with temporary credentials\. AppStream 2\.0 retrieves the temporary credentials and creates the **appstream\_machine\_role** credential profile on the instance\.  
For more information, see [Using an IAM Role to Grant Permissions to Applications and Scripts Running on AppStream 2\.0 Streaming Instances](https://docs.aws.amazon.com/appstream2/latest/developerguide/using-iam-roles-to-grant-permissions-to-applications-scripts-streaming-instances.html) in the *Amazon AppStream 2\.0 Administration Guide*\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws(?:\-cn|\-iso\-b|\-iso|\-us\-gov)?:[A-Za-z0-9][A-Za-z0-9_/.-]{0,62}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9][A-Za-z0-9:_/+=,@.\\-]{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdleDisconnectTimeoutInSeconds`  <a name="cfn-appstream-fleet-idledisconnecttimeoutinseconds"></a>
The amount of time that users can be idle \(inactive\) before they are disconnected from their streaming session and the `DisconnectTimeoutInSeconds` time interval begins\. Users are notified before they are disconnected due to inactivity\. If they try to reconnect to the streaming session before the time interval specified in `DisconnectTimeoutInSeconds` elapses, they are connected to their previous session\. Users are considered idle when they stop providing keyboard or mouse input during their streaming session\. File uploads and downloads, audio in, audio out, and pixels changing do not qualify as user activity\. If users continue to be idle after the time interval in `IdleDisconnectTimeoutInSeconds` elapses, they are disconnected\.  
To prevent users from being disconnected due to inactivity, specify a value of 0\. Otherwise, specify a value between 60 and 3600\.  
If you enable this feature, we recommend that you specify a value that corresponds exactly to a whole number of minutes \(for example, 60, 120, and 180\)\. If you don't do this, the value is rounded to the nearest minute\. For example, if you specify a value of 70, users are disconnected after 1 minute of inactivity\. If you specify a value that is at the midpoint between two different minutes, the value is rounded up\. For example, if you specify a value of 90, users are disconnected after 2 minutes of inactivity\. 
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageArn`  <a name="cfn-appstream-fleet-imagearn"></a>
The ARN of the public, private, or shared image to use\.  
*Required*: No  
*Type*: String  
*Pattern*: `^arn:aws(?:\-cn|\-iso\-b|\-iso|\-us\-gov)?:[A-Za-z0-9][A-Za-z0-9_/.-]{0,62}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9_/.-]{0,63}:[A-Za-z0-9][A-Za-z0-9:_/+=,@.\\-]{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageName`  <a name="cfn-appstream-fleet-imagename"></a>
The name of the image used to create the fleet\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceType`  <a name="cfn-appstream-fleet-instancetype"></a>
The instance type to use when launching fleet instances\. The following instance types are available:  
+ stream\.standard\.small
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
+ stream\.memory\.z1d\.large
+ stream\.memory\.z1d\.xlarge
+ stream\.memory\.z1d\.2xlarge
+ stream\.memory\.z1d\.3xlarge
+ stream\.memory\.z1d\.6xlarge
+ stream\.memory\.z1d\.12xlarge
+ stream\.graphics\-design\.large
+ stream\.graphics\-design\.xlarge
+ stream\.graphics\-design\.2xlarge
+ stream\.graphics\-design\.4xlarge
+ stream\.graphics\-desktop\.2xlarge
+ stream\.graphics\.g4dn\.xlarge
+ stream\.graphics\.g4dn\.2xlarge
+ stream\.graphics\.g4dn\.4xlarge
+ stream\.graphics\.g4dn\.8xlarge
+ stream\.graphics\.g4dn\.12xlarge
+ stream\.graphics\.g4dn\.16xlarge
+ stream\.graphics\-pro\.4xlarge
+ stream\.graphics\-pro\.8xlarge
+ stream\.graphics\-pro\.16xlarge
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaxUserDurationInSeconds`  <a name="cfn-appstream-fleet-maxuserdurationinseconds"></a>
The maximum amount of time that a streaming session can remain active, in seconds\. If users are still connected to a streaming instance five minutes before this limit is reached, they are prompted to save any open documents before being disconnected\. After this time elapses, the instance is terminated and replaced by a new instance\.  
Specify a value between 600 and 360000\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appstream-fleet-name"></a>
A unique name for the fleet\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9_.-]{0,100}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StreamView`  <a name="cfn-appstream-fleet-streamview"></a>
The AppStream 2\.0 view that is displayed to your users when they stream from the fleet\. When `APP` is specified, only the windows of applications opened by users display\. When `DESKTOP` is specified, the standard desktop that is provided by the operating system displays\.  
The default value is `APP`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `APP | DESKTOP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

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

## See also<a name="aws-resource-appstream-fleet--seealso"></a>
+  [CreateFleet](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateFleet.html) in the *Amazon AppStream 2\.0 API Reference* 

