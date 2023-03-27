# AWS::ManagedBlockchain::Accessor<a name="aws-resource-managedblockchain-accessor"></a>

Creates a new accessor for use with Managed Blockchain Ethereum nodes\. An accessor contains information required for token based access to your Ethereum nodes\.

## Syntax<a name="aws-resource-managedblockchain-accessor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-managedblockchain-accessor-syntax.json"></a>

```
{
  "Type" : "AWS::ManagedBlockchain::Accessor",
  "Properties" : {
      "[AccessorType](#cfn-managedblockchain-accessor-accessortype)" : String,
      "[Tags](#cfn-managedblockchain-accessor-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-managedblockchain-accessor-syntax.yaml"></a>

```
Type: AWS::ManagedBlockchain::Accessor
Properties: 
  [AccessorType](#cfn-managedblockchain-accessor-accessortype): String
  [Tags](#cfn-managedblockchain-accessor-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-managedblockchain-accessor-properties"></a>

`AccessorType`  <a name="cfn-managedblockchain-accessor-accessortype"></a>
The type of the accessor\.  
Currently, accessor type is restricted to `BILLING_TOKEN`\.
*Required*: Yes  
*Type*: String  
*Allowed values*: `BILLING_TOKEN`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-managedblockchain-accessor-tags"></a>
The tags assigned to the Accessor\.  
For more information about tags, see [Tagging Resources](https://docs.aws.amazon.com/managed-blockchain/latest/ethereum-dev/tagging-resources.html) in the *Amazon Managed Blockchain Ethereum Developer Guide*, or [Tagging Resources](https://docs.aws.amazon.com/managed-blockchain/latest/hyperledger-fabric-dev/tagging-resources.html) in the *Amazon Managed Blockchain Hyperledger Fabric Developer Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-managedblockchain-accessor-return-values"></a>

### Ref<a name="aws-resource-managedblockchain-accessor-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Accessor ID\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-managedblockchain-accessor-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-managedblockchain-accessor-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the accessor\. For more information about ARNs and their format, see [Amazon Resource Names \(ARNs\)](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the * AWS General Reference*\.

`BillingToken`  <a name="BillingToken-fn::getatt"></a>
The billing token is a property of the accessor\. Use this token to make Ethereum API calls to your Ethereum node\. The billing token is used to track your accessor object for billing Ethereum API requests made to your Ethereum nodes\.

`CreationDate`  <a name="CreationDate-fn::getatt"></a>
The creation date and time of the accessor\.

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier of the accessor\.

`Status`  <a name="Status-fn::getatt"></a>
The current status of the accessor\.