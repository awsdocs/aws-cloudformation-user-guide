# AWS::ManagedBlockchain::Node<a name="aws-resource-managedblockchain-node"></a>

Creates a node on the specified blockchain network\.

Applies to Hyperledger Fabric and Ethereum\.

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
The unique identifier of the member to which the node belongs\. Applies only to Hyperledger Fabric\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkId`  <a name="cfn-managedblockchain-node-networkid"></a>
The unique identifier of the network for the node\.  
Ethereum public networks have the following `NetworkId`s:  
+  `n-ethereum-mainnet` 
+  `n-ethereum-goerli` 
+  `n-ethereum-rinkeby` 
+  `n-ethereum-ropsten` 
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
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
The unique identifier of the member in which the node is created\. Applies only to Hyperledger Fabric\.

`NetworkId`  <a name="NetworkId-fn::getatt"></a>
The unique identifier of the network that the node is in\.

`NodeId`  <a name="NodeId-fn::getatt"></a>
The unique identifier of the node\.

## Examples<a name="aws-resource-managedblockchain-node--examples"></a>



### Create a node on an Ethereum network<a name="aws-resource-managedblockchain-node--examples--Create_a_node_on_an_Ethereum_network"></a>



#### YAML<a name="aws-resource-managedblockchain-node--examples--Create_a_node_on_an_Ethereum_network--yaml"></a>

```
Description: "Basic Ethereum node template"
Parameters:
  NetworkId:
    Type: String
  InstanceType:
    Type: String
  AvailabilityZone: 
    Type: String
Resources:
  Node:
    Type: "AWS::ManagedBlockchain::Node"
    Properties:
      NetworkId: !Ref NetworkId
      NodeConfiguration:
        InstanceType: !Ref InstanceType
        AvailabilityZone: !Ref AvailabilityZone
```

#### JSON<a name="aws-resource-managedblockchain-node--examples--Create_a_node_on_an_Ethereum_network--json"></a>

```
{
    "Description": "Basic Ethereum node template",
    "Parameters": {
        "NetworkId": {
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
        "Node": {
            "Type": "AWS::ManagedBlockchain::Node",
            "Properties": {
                "NetworkId": "NetworkId",
                "NodeConfiguration": {
                    "InstanceType": "InstanceType",
                    "AvailabilityZone": "AvailabilityZone"
                }
            }
        }
    }
}
```

### Create a node in a Hyperledger Fabric network member<a name="aws-resource-managedblockchain-node--examples--Create_a_node_in_a_Hyperledger_Fabric_network_member"></a>



#### YAML<a name="aws-resource-managedblockchain-node--examples--Create_a_node_in_a_Hyperledger_Fabric_network_member--yaml"></a>

```
Description: "Basic Hyperledger Fabric node template"
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

#### JSON<a name="aws-resource-managedblockchain-node--examples--Create_a_node_in_a_Hyperledger_Fabric_network_member--json"></a>

```
{
  "Description": "Basic Hyperledger Fabric node template",
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