# AWS::EC2::NetworkInterfaceAttachment<a name="aws-resource-ec2-networkinterfaceattachment"></a>

Attaches an elastic network interface \(ENI\) to an Amazon EC2 instance\. You can use this resource type to attach additional network interfaces to an instance without interruption\.

## Syntax<a name="aws-resource-ec2-networkinterfaceattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinterfaceattachment-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInterfaceAttachment",
  "Properties" : {
      "[DeleteOnTermination](#cfn-ec2-networkinterfaceattachment-deleteontermination)" : Boolean,
      "[DeviceIndex](#cfn-ec2-networkinterfaceattachment-deviceindex)" : String,
      "[InstanceId](#cfn-ec2-networkinterfaceattachment-instanceid)" : String,
      "[NetworkInterfaceId](#cfn-ec2-networkinterfaceattachment-networkinterfaceid)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-networkinterfaceattachment-syntax.yaml"></a>

```
Type: AWS::EC2::NetworkInterfaceAttachment
Properties: 
  [DeleteOnTermination](#cfn-ec2-networkinterfaceattachment-deleteontermination): Boolean
  [DeviceIndex](#cfn-ec2-networkinterfaceattachment-deviceindex): String
  [InstanceId](#cfn-ec2-networkinterfaceattachment-instanceid): String
  [NetworkInterfaceId](#cfn-ec2-networkinterfaceattachment-networkinterfaceid): String
```

## Properties<a name="aws-resource-ec2-networkinterfaceattachment-properties"></a>

`DeleteOnTermination`  <a name="cfn-ec2-networkinterfaceattachment-deleteontermination"></a>
Whether to delete the network interface when the instance terminates\. By default, this value is set to `true`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeviceIndex`  <a name="cfn-ec2-networkinterfaceattachment-deviceindex"></a>
The network interface's position in the attachment order\. For example, the first attached network interface has a `DeviceIndex` of 0\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceId`  <a name="cfn-ec2-networkinterfaceattachment-instanceid"></a>
The ID of the instance to which you will attach the ENI\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInterfaceId`  <a name="cfn-ec2-networkinterfaceattachment-networkinterfaceid"></a>
The ID of the ENI that you want to attach\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-networkinterfaceattachment-return-values"></a>

### Ref<a name="aws-resource-ec2-networkinterfaceattachment-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the resource name\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-networkinterfaceattachment-return-values-fn--getatt"></a>

#### <a name="aws-resource-ec2-networkinterfaceattachment-return-values-fn--getatt-fn--getatt"></a>

`AttachmentId`  <a name="AttachmentId-fn::getatt"></a>
Property description not available\.

## Examples<a name="aws-resource-ec2-networkinterfaceattachment--examples"></a>



### Network interface attachment<a name="aws-resource-ec2-networkinterfaceattachment--examples--Network_interface_attachment"></a>

The following example attaches `MyNetworkInterface` to `MyInstance`\.

#### JSON<a name="aws-resource-ec2-networkinterfaceattachment--examples--Network_interface_attachment--json"></a>

```
"NetworkInterfaceAttachment" : {
   "Type" : "AWS::EC2::NetworkInterfaceAttachment",
      "Properties" : {
         "InstanceId" : {"Ref" : "MyInstance"},
         "NetworkInterfaceId" : {"Ref" : "MyNetworkInterface"},
         "DeviceIndex" : "1" 
      }
}
```

#### YAML<a name="aws-resource-ec2-networkinterfaceattachment--examples--Network_interface_attachment--yaml"></a>

```
NetworkInterfaceAttachment:
   Type: AWS::EC2::NetworkInterfaceAttachment
   Properties:
      InstanceId:
         Ref: MyInstance
      NetworkInterfaceId:
         Ref: MyNetworkInterface
      DeviceIndex: 1
```