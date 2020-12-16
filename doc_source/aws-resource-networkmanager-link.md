# AWS::NetworkManager::Link<a name="aws-resource-networkmanager-link"></a>

Specifies a link for a site\.

## Syntax<a name="aws-resource-networkmanager-link-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-link-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::Link",
  "Properties" : {
      "[Bandwidth](#cfn-networkmanager-link-bandwidth)" : Bandwidth,
      "[Description](#cfn-networkmanager-link-description)" : String,
      "[GlobalNetworkId](#cfn-networkmanager-link-globalnetworkid)" : String,
      "[Provider](#cfn-networkmanager-link-provider)" : String,
      "[SiteId](#cfn-networkmanager-link-siteid)" : String,
      "[Tags](#cfn-networkmanager-link-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Type](#cfn-networkmanager-link-type)" : String
    }
}
```

### YAML<a name="aws-resource-networkmanager-link-syntax.yaml"></a>

```
Type: AWS::NetworkManager::Link
Properties: 
  [Bandwidth](#cfn-networkmanager-link-bandwidth): 
    Bandwidth
  [Description](#cfn-networkmanager-link-description): String
  [GlobalNetworkId](#cfn-networkmanager-link-globalnetworkid): String
  [Provider](#cfn-networkmanager-link-provider): String
  [SiteId](#cfn-networkmanager-link-siteid): String
  [Tags](#cfn-networkmanager-link-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Type](#cfn-networkmanager-link-type): String
```

## Properties<a name="aws-resource-networkmanager-link-properties"></a>

`Bandwidth`  <a name="cfn-networkmanager-link-bandwidth"></a>
The bandwidth for the link\.  
*Required*: Yes  
*Type*: [Bandwidth](aws-properties-networkmanager-link-bandwidth.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-networkmanager-link-description"></a>
A description of the link\.  
Length Constraints: Maximum length of 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalNetworkId`  <a name="cfn-networkmanager-link-globalnetworkid"></a>
The ID of the global network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Provider`  <a name="cfn-networkmanager-link-provider"></a>
The provider of the link\.  
Constraints: Cannot include the following characters: \| \\ ^  
Length Constraints: Maximum length of 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SiteId`  <a name="cfn-networkmanager-link-siteid"></a>
The ID of the site\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-networkmanager-link-tags"></a>
The tags for the link\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-networkmanager-link-type"></a>
The type of the link\.  
Constraints: Cannot include the following characters: \| \\ ^  
Length Constraints: Maximum length of 128 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-networkmanager-link-return-values"></a>

### Ref<a name="aws-resource-networkmanager-link-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IDs of the global network and link\. For example: `global-network-01231231231231231|link-11112222aaaabbbb1`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-link-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-link-return-values-fn--getatt-fn--getatt"></a>

`LinkArn`  <a name="LinkArn-fn::getatt"></a>
The ARN of the link\. For example, `arn:aws:networkmanager::123456789012:link/global-network-01231231231231231/link-11112222aaaabbbb1`\.

`LinkId`  <a name="LinkId-fn::getatt"></a>
The ID of the link\. For example, `link-11112222aaaabbbb1`\.

## Examples<a name="aws-resource-networkmanager-link--examples"></a>



### Link<a name="aws-resource-networkmanager-link--examples--Link"></a>

The following example creates a link in a global network\.

#### JSON<a name="aws-resource-networkmanager-link--examples--Link--json"></a>

```
{
    "Type": "AWS::NetworkManager::Link",
    "Properties": {
        "Description": "Broadband link",
        "GlobalNetworkId": {
            "Ref": "GlobalNetwork"
        },
        "SiteId": {
            "Fn::GetAtt": [
                "Site",
                "SiteId"
            ]
        },
        "Bandwidth": {
            "DownloadSpeed": 20,
            "UploadSpeed": 20
        },
        "Provider": "AnyCompany",
        "Type": "Broadband",
        "Tags": [
            {
                "Key": "Name",
                "Value": "broadband-link-1"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-networkmanager-link--examples--Link--yaml"></a>

```
Type: AWS::NetworkManager::Link
Properties:
  Description: "Broadband link"
  GlobalNetworkId: !Ref GlobalNetwork
  SiteId: !GetAtt Site.SiteId
  Bandwidth:
    DownloadSpeed: 20
    UploadSpeed: 20
  Provider: "AnyCompany"
  Type: "Broadband"
  Tags:
    - Key: Name
      Value: broadband-link-1
```