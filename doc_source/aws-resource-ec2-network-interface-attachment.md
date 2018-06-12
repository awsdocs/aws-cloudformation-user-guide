# AWS::EC2::NetworkInterfaceAttachment<a name="aws-resource-ec2-network-interface-attachment"></a>

Attaches an elastic network interface \(ENI\) to an Amazon EC2 instance\. You can use this resource type to attach additional network interfaces to an instances without interruption\.

**Topics**
+ [Syntax](#aws-resource-ec2-networkinterfaceattachment-syntax)
+ [Properties](#w3ab2c21c10d443b9)
+ [Return Values](#w3ab2c21c10d443c11)
+ [Example](#w3ab2c21c10d443c13)

## Syntax<a name="aws-resource-ec2-networkinterfaceattachment-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinterfaceattachment-syntax.json"></a>

```
{
   "Type" : "AWS::EC2::NetworkInterfaceAttachment",
   "Properties" : {
      "[DeleteOnTermination](#cfn-ec2-network-interface-attachment-deleteonterm)": Boolean,
      "[DeviceIndex](#cfn-ec2-network-interface-attachment-deviceindex)": String,
      "[InstanceId](#cfn-ec2-network-interface-attachment-instanceid)": String,
      "[NetworkInterfaceId](#cfn-ec2-network-interface-attachment-networkinterfaceid)": String
   }
}
```

### YAML<a name="aws-resource-ec2-networkinterfaceattachment-syntax.yaml"></a>

```
Type: "AWS::EC2::NetworkInterfaceAttachment"
Properties: 
  [DeleteOnTermination](#cfn-ec2-network-interface-attachment-deleteonterm): Boolean
  [DeviceIndex](#cfn-ec2-network-interface-attachment-deviceindex): String
  [InstanceId](#cfn-ec2-network-interface-attachment-instanceid): String
  [NetworkInterfaceId](#cfn-ec2-network-interface-attachment-networkinterfaceid): String
```

## Properties<a name="w3ab2c21c10d443b9"></a>

`DeleteOnTermination`  <a name="cfn-ec2-network-interface-attachment-deleteonterm"></a>
Whether to delete the network interface when the instance terminates\. By default, this value is set to `True`\.  
*Required*: No  
*Type*: Boolean\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DeviceIndex`  <a name="cfn-ec2-network-interface-attachment-deviceindex"></a>
The network interface's position in the attachment order\. For example, the first attached network interface has a `DeviceIndex` of `0`\.  
*Required*: Yes\.  
*Type*: String\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceId`  <a name="cfn-ec2-network-interface-attachment-instanceid"></a>
The ID of the instance to which you will attach the ENI\.  
*Required*: Yes\.  
*Type*: String\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`NetworkInterfaceId`  <a name="cfn-ec2-network-interface-attachment-networkinterfaceid"></a>
The ID of the ENI that you want to attach\.  
*Required*: Yes\.  
*Type*: String\.  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d443c11"></a>

### Ref<a name="w3ab2c21c10d443c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10d443c13"></a>

Attaching `MyNetworkInterface` to `MyInstance`

### JSON<a name="aws-resource-ec2-networkinterfaceattachment-example-1.json"></a>

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

### YAML<a name="aws-resource-ec2-networkinterfaceattachment-example-1.yaml"></a>

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