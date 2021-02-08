# AWS::NetworkManager::GlobalNetwork<a name="aws-resource-networkmanager-globalnetwork"></a>

Creates a new, empty global network\.

## Syntax<a name="aws-resource-networkmanager-globalnetwork-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-globalnetwork-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::GlobalNetwork",
  "Properties" : {
      "[Description](#cfn-networkmanager-globalnetwork-description)" : String,
      "[Tags](#cfn-networkmanager-globalnetwork-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-networkmanager-globalnetwork-syntax.yaml"></a>

```
Type: AWS::NetworkManager::GlobalNetwork
Properties: 
  [Description](#cfn-networkmanager-globalnetwork-description): String
  [Tags](#cfn-networkmanager-globalnetwork-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-networkmanager-globalnetwork-properties"></a>

`Description`  <a name="cfn-networkmanager-globalnetwork-description"></a>
A description of the global network\.  
Length Constraints: Maximum length of 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkmanager-globalnetwork-tags"></a>
The tags for the global network\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-networkmanager-globalnetwork-return-values"></a>

### Ref<a name="aws-resource-networkmanager-globalnetwork-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the global network\. For example: `global-network-01231231231231231`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-globalnetwork-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-globalnetwork-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the global network\. For example, `arn:aws:networkmanager::123456789012:global-network/global-network-01231231231231231`\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the global network\. For example, `global-network-01231231231231231`\.

## Examples<a name="aws-resource-networkmanager-globalnetwork--examples"></a>



### Global Network<a name="aws-resource-networkmanager-globalnetwork--examples--Global_Network"></a>

The following example creates a global network\.

#### JSON<a name="aws-resource-networkmanager-globalnetwork--examples--Global_Network--json"></a>

```
{
    "Type": "AWS::NetworkManager::GlobalNetwork",
    "Properties": {
        "Description": "Global network for USA sites",
        "Tags": [
            {
                "Key": "Name",
                "Value": "global-network-usa"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-networkmanager-globalnetwork--examples--Global_Network--yaml"></a>

```
Type: 'AWS::NetworkManager::GlobalNetwork'
Properties:
  Description: Global network for USA sites
  Tags:
    - Key: Name
      Value: global-network-usa
```