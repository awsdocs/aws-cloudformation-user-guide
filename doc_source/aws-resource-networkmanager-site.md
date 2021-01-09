# AWS::NetworkManager::Site<a name="aws-resource-networkmanager-site"></a>

Specifies a site in a global network\.

## Syntax<a name="aws-resource-networkmanager-site-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-networkmanager-site-syntax.json"></a>

```
{
  "Type" : "AWS::NetworkManager::Site",
  "Properties" : {
      "[Description](#cfn-networkmanager-site-description)" : String,
      "[GlobalNetworkId](#cfn-networkmanager-site-globalnetworkid)" : String,
      "[Location](#cfn-networkmanager-site-location)" : Location,
      "[Tags](#cfn-networkmanager-site-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-networkmanager-site-syntax.yaml"></a>

```
Type: AWS::NetworkManager::Site
Properties: 
  [Description](#cfn-networkmanager-site-description): String
  [GlobalNetworkId](#cfn-networkmanager-site-globalnetworkid): String
  [Location](#cfn-networkmanager-site-location): 
    Location
  [Tags](#cfn-networkmanager-site-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-networkmanager-site-properties"></a>

`Description`  <a name="cfn-networkmanager-site-description"></a>
A description of your site\.  
Length Constraints: Maximum length of 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalNetworkId`  <a name="cfn-networkmanager-site-globalnetworkid"></a>
The ID of the global network\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Location`  <a name="cfn-networkmanager-site-location"></a>
The site location\. This information is used for visualization in the Network Manager console\. If you specify the address, the latitude and longitude are automatically calculated\.  
+  `Address`: The physical address of the site\.
+  `Latitude`: The latitude of the site\. 
+  `Longitude`: The longitude of the site\.
*Required*: No  
*Type*: [Location](aws-properties-networkmanager-site-location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-networkmanager-site-tags"></a>
The tags for the site\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-networkmanager-site-return-values"></a>

### Ref<a name="aws-resource-networkmanager-site-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the IDs of the global network and the site\. For example: `global-network-01231231231231231|site-444555aaabbb11223`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-networkmanager-site-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-networkmanager-site-return-values-fn--getatt-fn--getatt"></a>

`SiteArn`  <a name="SiteArn-fn::getatt"></a>
The ARN of the site\. For example, `arn:aws:networkmanager::123456789012:site/global-network-01231231231231231/site-444555aaabbb11223`\.

`SiteId`  <a name="SiteId-fn::getatt"></a>
The ID of the site\. For example, `site-444555aaabbb11223`\.

## Examples<a name="aws-resource-networkmanager-site--examples"></a>



### Site<a name="aws-resource-networkmanager-site--examples--Site"></a>

The following example creates a site in a global network\.

#### JSON<a name="aws-resource-networkmanager-site--examples--Site--json"></a>

```
{
    "Type": "AWS::NetworkManager::Site",
    "Properties": {
        "Description": "Chicago office",
        "GlobalNetworkId": {
            "Ref": "GlobalNetwork"
        },
        "Location": {
            "Address": "227 W Monroe St, Chicago, IL 60606",
            "Latitude": "41.880520",
            "Longitude": "-87.634720"
        },
        "Tags": [
            {
                "Key": "Network",
                "Value": "north-america"
            }
        ]
    }
}
```

#### YAML<a name="aws-resource-networkmanager-site--examples--Site--yaml"></a>

```
Type: AWS::NetworkManager::Site
Properties:
  Description: "Chicago office"
  GlobalNetworkId: !Ref GlobalNetwork
  Location:
    Address: "227 W Monroe St, Chicago, IL 60606"
    Latitude: "41.880520"
    Longitude: "-87.634720"
  Tags:
    - Key: Network
      Value: north-america
```