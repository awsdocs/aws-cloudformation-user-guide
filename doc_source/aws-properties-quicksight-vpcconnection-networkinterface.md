# AWS::QuickSight::VPCConnection NetworkInterface<a name="aws-properties-quicksight-vpcconnection-networkinterface"></a>

The structure that contains information about a network interface\.

## Syntax<a name="aws-properties-quicksight-vpcconnection-networkinterface-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-quicksight-vpcconnection-networkinterface-syntax.json"></a>

```
{
  "[AvailabilityZone](#cfn-quicksight-vpcconnection-networkinterface-availabilityzone)" : String,
  "[ErrorMessage](#cfn-quicksight-vpcconnection-networkinterface-errormessage)" : String,
  "[NetworkInterfaceId](#cfn-quicksight-vpcconnection-networkinterface-networkinterfaceid)" : String,
  "[Status](#cfn-quicksight-vpcconnection-networkinterface-status)" : String,
  "[SubnetId](#cfn-quicksight-vpcconnection-networkinterface-subnetid)" : String
}
```

### YAML<a name="aws-properties-quicksight-vpcconnection-networkinterface-syntax.yaml"></a>

```
  [AvailabilityZone](#cfn-quicksight-vpcconnection-networkinterface-availabilityzone): String
  [ErrorMessage](#cfn-quicksight-vpcconnection-networkinterface-errormessage): String
  [NetworkInterfaceId](#cfn-quicksight-vpcconnection-networkinterface-networkinterfaceid): String
  [Status](#cfn-quicksight-vpcconnection-networkinterface-status): String
  [SubnetId](#cfn-quicksight-vpcconnection-networkinterface-subnetid): String
```

## Properties<a name="aws-properties-quicksight-vpcconnection-networkinterface-properties"></a>

`AvailabilityZone`  <a name="cfn-quicksight-vpcconnection-networkinterface-availabilityzone"></a>
The availability zone that the network interface resides in\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ErrorMessage`  <a name="cfn-quicksight-vpcconnection-networkinterface-errormessage"></a>
An error message\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-quicksight-vpcconnection-networkinterface-networkinterfaceid"></a>
The network interface ID\.  
*Required*: No  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^eni-[0-9a-z]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-quicksight-vpcconnection-networkinterface-status"></a>
The status of the network interface\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ATTACHMENT_FAILED_ROLLBACK_FAILED | AVAILABLE | CREATING | CREATION_FAILED | DELETED | DELETING | DELETION_FAILED | DELETION_SCHEDULED | UPDATE_FAILED | UPDATING`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-quicksight-vpcconnection-networkinterface-subnetid"></a>
The subnet ID associated with the network interface\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^subnet-[0-9a-z]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)