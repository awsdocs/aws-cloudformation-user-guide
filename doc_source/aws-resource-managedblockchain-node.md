# AWS::ManagedBlockchain::Node<a name="aws-resource-managedblockchain-node"></a>

Creates a node on the specified blockchain network\.

Applies to Hyperledger Fabric and Ethereum\.

Ethereum on Managed Blockchain is in preview release and is subject to change\.

## Syntax<a name="aws-resource-managedblockchain-node-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-managedblockchain-node-syntax.json"></a>

```
{
  "Type" : "AWS::ManagedBlockchain::Node",
  "Properties" : {
      "[MemberId](#cfn-managedblockchain-node-memberid)" : String,
      "[NetworkId](#cfn-managedblockchain-node-networkid)" : String,
      "[NodeConfiguration](#cfn-managedblockchain-node-nodeconfiguration)" : NodeConfiguration
    }
}
```

### YAML<a name="aws-resource-managedblockchain-node-syntax.yaml"></a>

```
Type: AWS::ManagedBlockchain::Node
Properties: 
  [MemberId](#cfn-managedblockchain-node-memberid): String
  [NetworkId](#cfn-managedblockchain-node-networkid): String
  [NodeConfiguration](#cfn-managedblockchain-node-nodeconfiguration): 
    NodeConfiguration
```

## Properties<a name="aws-resource-managedblockchain-node-properties"></a>

`MemberId`  <a name="cfn-managedblockchain-node-memberid"></a>
The unique identifier of the member to which the node belongs\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkId`  <a name="cfn-managedblockchain-node-networkid"></a>
The unique identifier of the network that the node is in\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NodeConfiguration`  <a name="cfn-managedblockchain-node-nodeconfiguration"></a>
Configuration properties of a peer node\.  
*Required*: Yes  
*Type*: [NodeConfiguration](aws-properties-managedblockchain-node-nodeconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-managedblockchain-node-return-values"></a>

### Ref<a name="aws-resource-managedblockchain-node-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the node ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-managedblockchain-node-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-managedblockchain-node-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the node\.

`MemberId`  <a name="MemberId-fn::getatt"></a>
The unique identifier of the member in which the node is created\.

`NetworkId`  <a name="NetworkId-fn::getatt"></a>
The unique identifier of the network that the node is in\.

`NodeId`  <a name="NodeId-fn::getatt"></a>
The unique identifier of the node\.

## Examples<a name="aws-resource-managedblockchain-node--examples"></a>



### Create a Peer Node in a Member<a name="aws-resource-managedblockchain-node--examples--Create_a_Peer_Node_in_a_Member"></a>



#### YAML<a name="aws-resource-managedblockchain-node--examples--Create_a_Peer_Node_in_a_Member--yaml"></a>

```
Description: "Basic Node template"
Parameters:
  NetworkId:
    Type: String
  MemberId:
    Type: String
  InstanceType:
    Type: String
  AvailabilityZone:
    Type: String

Resources:
  InitialNode:
    Type: "AWS::ManagedBlockchain::Node"
    Properties:
      NetworkId: !Ref NetworkId
      MemberId: !Ref MemberId
      NodeConfiguration:
        InstanceType: !Ref InstanceType
        AvailabilityZone: !Ref AvailabilityZone
```

#### JSON<a name="aws-resource-managedblockchain-node--examples--Create_a_Peer_Node_in_a_Member--json"></a>

```
{
  "Description": "Basic Node template",
  "Parameters": {
    "NetworkId": {
      "Type": "String"
    },
    "MemberId": {
      "Type": "String"
    },
    "InstanceType": {
      "Type": "String"
    },
    "AvailabilityZone": {
      "Type": "String"
    }
  },
  "Resources": {
    "InitialNode": {
      "Type": "AWS::ManagedBlockchain::Node",
      "Properties": {
        "NetworkId": "NetworkId",
        "MemberId": "MemberId",
        "NodeConfiguration": {
          "InstanceType": "InstanceType",
          "AvailabilityZone": "AvailabilityZone"
        }
      }
    }
  }
}
```