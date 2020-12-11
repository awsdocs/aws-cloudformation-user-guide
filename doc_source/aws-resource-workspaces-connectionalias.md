# AWS::WorkSpaces::ConnectionAlias<a name="aws-resource-workspaces-connectionalias"></a>

The `AWS::WorkSpaces::ConnectionAlias` resource specifies a connection alias\. Connection aliases are used for cross\-Region redirection\. For more information, see [ Cross\-Region Redirection for Amazon WorkSpaces](https://docs.aws.amazon.com/workspaces/latest/adminguide/cross-region-redirection.html)\.

## Syntax<a name="aws-resource-workspaces-connectionalias-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-workspaces-connectionalias-syntax.json"></a>

```
{
  "Type" : "AWS::WorkSpaces::ConnectionAlias",
  "Properties" : {
      "[ConnectionString](#cfn-workspaces-connectionalias-connectionstring)" : String,
      "[Tags](#cfn-workspaces-connectionalias-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-workspaces-connectionalias-syntax.yaml"></a>

```
Type: AWS::WorkSpaces::ConnectionAlias
Properties: 
  [ConnectionString](#cfn-workspaces-connectionalias-connectionstring): 
    String
  [Tags](#cfn-workspaces-connectionalias-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-workspaces-connectionalias-properties"></a>

`ConnectionString`  <a name="cfn-workspaces-connectionalias-connectionstring"></a>
The connection string specified for the connection alias\. The connection string must be in the form of a fully qualified domain name \(FQDN\), such as `www.example.com`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[.0-9a-zA-Z\-]{1,255}$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-workspaces-connectionalias-tags"></a>
The tags to associate with the connection alias\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-workspaces-connectionalias-return-values"></a>

### Ref<a name="aws-resource-workspaces-connectionalias-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-workspaces-connectionalias-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-workspaces-connectionalias-return-values-fn--getatt-fn--getatt"></a>

`AliasId`  <a name="AliasId-fn::getatt"></a>
The identifier of the connection alias, returned as a string\.

`Associations`  <a name="Associations-fn::getatt"></a>
The association status of the connection alias, returned as an array of `ConnectionAliasAssociation` objects\.

`ConnectionAliasState`  <a name="ConnectionAliasState-fn::getatt"></a>
The current state of the connection alias, returned as a string\.

## See also<a name="aws-resource-workspaces-connectionalias--seealso"></a>
+ [ConnectionAlias](https://docs.aws.amazon.com/workspaces/latest/api/API_ConnectionAlias.html) in the *Amazon WorkSpaces API Reference*
+ [Cross\-Region Redirection for Amazon WorkSpaces](https://docs.aws.amazon.com/workspaces/latest/adminguide/cross-region-redirection.html) in the *Amazon WorkSpaces Administration Guide*

