# AWS::GlobalAccelerator::Listener<a name="aws-resource-globalaccelerator-listener"></a>

The `AWS::GlobalAccelerator::Listener` resource is a Global Accelerator resource type that contains information about how you create a listener to process inbound connections from clients to an accelerator\. Connections arrive to assigned static IP addresses on a port, port range, or list of port ranges that you specify\.

## Syntax<a name="aws-resource-globalaccelerator-listener-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-globalaccelerator-listener-syntax.json"></a>

```
{
  "Type" : "AWS::GlobalAccelerator::Listener",
  "Properties" : {
      "[AcceleratorArn](#cfn-globalaccelerator-listener-acceleratorarn)" : String,
      "[ClientAffinity](#cfn-globalaccelerator-listener-clientaffinity)" : String,
      "[PortRanges](#cfn-globalaccelerator-listener-portranges)" : [ PortRange, ... ],
      "[Protocol](#cfn-globalaccelerator-listener-protocol)" : String
    }
}
```

### YAML<a name="aws-resource-globalaccelerator-listener-syntax.yaml"></a>

```
Type: AWS::GlobalAccelerator::Listener
Properties: 
  [AcceleratorArn](#cfn-globalaccelerator-listener-acceleratorarn): String
  [ClientAffinity](#cfn-globalaccelerator-listener-clientaffinity): String
  [PortRanges](#cfn-globalaccelerator-listener-portranges): 
    - PortRange
  [Protocol](#cfn-globalaccelerator-listener-protocol): String
```

## Properties<a name="aws-resource-globalaccelerator-listener-properties"></a>

`AcceleratorArn`  <a name="cfn-globalaccelerator-listener-acceleratorarn"></a>
The Amazon Resource Name \(ARN\) of your accelerator\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientAffinity`  <a name="cfn-globalaccelerator-listener-clientaffinity"></a>
Client affinity lets you direct all requests from a user to the same endpoint, if you have stateful applications, regardless of the port and protocol of the client request\. Client affinity gives you control over whether to always route each client to the same specific endpoint\.  
AWS Global Accelerator uses a consistent\-flow hashing algorithm to choose the optimal endpoint for a connection\. If client affinity is `NONE`, Global Accelerator uses the "five\-tuple" \(5\-tuple\) properties—source IP address, source port, destination IP address, destination port, and protocol—to select the hash value, and then chooses the best endpoint\. However, with this setting, if someone uses different ports to connect to Global Accelerator, their connections might not be always routed to the same endpoint because the hash value changes\.   
If you want a given client to always be routed to the same endpoint, set client affinity to `SOURCE_IP` instead\. When you use the `SOURCE_IP` setting, Global Accelerator uses the "two\-tuple" \(2\-tuple\) properties— source \(client\) IP address and destination IP address—to select the hash value\.  
The default value is `NONE`\.  
*Required*: No  
*Type*: String  
*Allowed values*: `NONE | SOURCE_IP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortRanges`  <a name="cfn-globalaccelerator-listener-portranges"></a>
The list of port ranges for the connections from clients to the accelerator\.  
*Required*: Yes  
*Type*: List of [PortRange](aws-properties-globalaccelerator-listener-portrange.md)  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-globalaccelerator-listener-protocol"></a>
The protocol for the connections from clients to the accelerator\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `TCP | UDP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-globalaccelerator-listener-return-values"></a>

### Ref<a name="aws-resource-globalaccelerator-listener-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the listener, such as `arn:aws:globalaccelerator::012345678901:accelerator/1234abcd-abcd-1234-abcd-1234abcdefgh/listener/0123vxyz`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-globalaccelerator-listener-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-globalaccelerator-listener-return-values-fn--getatt-fn--getatt"></a>

`ListenerArn`  <a name="ListenerArn-fn::getatt"></a>
The ARN of the listener, such as `arn:aws:globalaccelerator::012345678901:accelerator/1234abcd-abcd-1234-abcd-1234abcdefgh/listener/0123vxyz`\.

## Examples<a name="aws-resource-globalaccelerator-listener--examples"></a>



### Add a listener<a name="aws-resource-globalaccelerator-listener--examples--Add_a_listener"></a>

These are examples to specify a listener\.

#### JSON<a name="aws-resource-globalaccelerator-listener--examples--Add_a_listener--json"></a>

```
"Resources": {
    "Listener": {
        "Type": "AWS::GlobalAccelerator::Listener",
        "Properties": {
            "AcceleratorArn": {
                "Ref": "Accelerator"
            },
            "Protocol": "TCP",
            "PortRanges": [
                {
                    "FromPort": 80,
                    "ToPort": 80
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-globalaccelerator-listener--examples--Add_a_listener--yaml"></a>

```
Listener:
  Type: AWS::GlobalAccelerator::Listener
  Properties:
    AcceleratorArn:
      Ref: Accelerator
    Protocol: TCP
    PortRanges:
    - FromPort: 80
      ToPort: 80
```