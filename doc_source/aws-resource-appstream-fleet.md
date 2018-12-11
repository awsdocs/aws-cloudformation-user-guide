# AWS::AppStream::Fleet<a name="aws-resource-appstream-fleet"></a>

The `AWS::AppStream::Fleet` resource creates a fleet for Amazon AppStream 2\.0\. A fleet consists of streaming instances that run a specified image\. For more information, see [CreateFleet](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateFleet.html) in the *Amazon AppStream 2\.0 API Reference*\. 

## Syntax<a name="aws-resource-appstream-fleet-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-fleet-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::Fleet",
  "Properties" : {
    "[ComputeCapacity](#cfn-appstream-fleet-computecapacity)" : [*ComputeCapacity*](aws-properties-appstream-fleet-computecapacity.md),
    "[Description](#cfn-appstream-fleet-description)" : String,
    "[DisconnectTimeoutInSeconds](#cfn-appstream-fleet-disconnecttimeoutinseconds)" : Integer,
    "[DisplayName](#cfn-appstream-fleet-displayname)" : String,
              "[DomainJoinInfo](#cfn-appstream-fleet-domainjoininfo)" : [*DomainJoinInfo*](aws-properties-appstream-fleet-domainjoininfo.md),
    "[EnableDefaultInternetAccess](#cfn-appstream-fleet-enabledefaultinternetaccess)" : Boolean,
    "[FleetType](#cfn-appstream-fleet-fleettype)" : String,
    "[ImageArn](#cfn-appstream-fleet-imagearn)" : String,
    "[ImageName](#cfn-appstream-fleet-imagename)" : String,
    "[InstanceType](#cfn-appstream-fleet-instancetype)" : String,
    "[MaxUserDurationInSeconds](#cfn-appstream-fleet-maxuserdurationinseconds)" : Integer,
    "[Name](#cfn-appstream-fleet-name)" : String,
    "[VpcConfig](#cfn-appstream-fleet-vpcconfig)" : [*VpcConfig*](aws-properties-appstream-fleet-vpcconfig.md)
  }
}
```

### YAML<a name="aws-resource-appstream-fleet-syntax.yaml"></a>

```
Type: "AWS::AppStream::Fleet"
Properties:
  [ComputeCapacity](#cfn-appstream-fleet-computecapacity): [*ComputeCapacity*](aws-properties-appstream-fleet-computecapacity.md)
  [Description](#cfn-appstream-fleet-description): String
  [DisconnectTimeoutInSeconds](#cfn-appstream-fleet-disconnecttimeoutinseconds): Integer
  [DisplayName](#cfn-appstream-fleet-displayname): String
  [DomainJoinInfo](#cfn-appstream-fleet-domainjoininfo): [*DomainJoinInfo*](aws-properties-appstream-fleet-domainjoininfo.md)
  [EnableDefaultInternetAccess](#cfn-appstream-fleet-enabledefaultinternetaccess): Boolean
  [FleetType](#cfn-appstream-fleet-fleettype): String
  [ImageArn](#cfn-appstream-fleet-imagearn): String
  [ImageName](#cfn-appstream-fleet-imagename): String
  [InstanceType](#cfn-appstream-fleet-instancetype): String
  [MaxUserDurationInSeconds](#cfn-appstream-fleet-maxuserdurationinseconds): Integer
  [Name](#cfn-appstream-fleet-name): String
  [VpcConfig](#cfn-appstream-fleet-vpcconfig): [*VpcConfig*](aws-properties-appstream-fleet-vpcconfig.md)
```

## Properties<a name="aws-resource-appstream-fleet-properties"></a>

`ComputeCapacity`  <a name="cfn-appstream-fleet-computecapacity"></a>
The desired capacity for the fleet\.  
 *Required*: Yes  
 *Type*: [ComputeCapacity](aws-properties-appstream-fleet-computecapacity.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-appstream-fleet-description"></a>
The description to display\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DisconnectTimeoutInSeconds`  <a name="cfn-appstream-fleet-disconnecttimeoutinseconds"></a>
The time after disconnection when a session is considered to have ended, in seconds\. If a user who was disconnected reconnects within this time interval, the user is connected to their previous session\. Specify a value between 60 and 57600\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DisplayName`  <a name="cfn-appstream-fleet-displayname"></a>
The fleet name to display\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DomainJoinInfo`  <a name="cfn-appstream-fleet-domainjoininfo"></a>
The information needed to join a Microsoft Active Directory domain\.  
 *Required*: No  
 *Type*: [DomainJoinInfo](aws-properties-appstream-fleet-domainjoininfo.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`EnableDefaultInternetAccess`  <a name="cfn-appstream-fleet-enabledefaultinternetaccess"></a>
Enables or disables default internet access for the fleet\.  
 *Required*: No  
 *Type*: Boolean  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`FleetType`  <a name="cfn-appstream-fleet-fleettype"></a>
The fleet type\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`ImageArn`  <a name="cfn-appstream-fleet-imagearn"></a>
The ARN of the public, private, or shared image to use\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ImageName`  <a name="cfn-appstream-fleet-imagename"></a>
The name of the image used to create the fleet\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`InstanceType`  <a name="cfn-appstream-fleet-instancetype"></a>
The instance type to use when launching fleet instances\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`MaxUserDurationInSeconds`  <a name="cfn-appstream-fleet-maxuserdurationinseconds"></a>
The maximum time that a streaming session can run, in seconds\. Specify a value between 600 and 57600\.   
 *Required*: No  
 *Type*: Integer  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-appstream-fleet-name"></a>
A unique name for the fleet\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`VpcConfig`  <a name="cfn-appstream-fleet-vpcconfig"></a>
The VPC configuration for the fleet\.  
 *Required*: No  
 *Type*: [VpcConfig](aws-properties-appstream-fleet-vpcconfig.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-resource-appstream-fleet-seealso"></a>
+ [CreateFleet](https://docs.aws.amazon.com/appstream2/latest/APIReference/API_CreateFleet.html) in the *Amazon AppStream 2\.0 API Reference*