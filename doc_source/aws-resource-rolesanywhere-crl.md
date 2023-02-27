# AWS::RolesAnywhere::CRL<a name="aws-resource-rolesanywhere-crl"></a>

The state of the certificate revocation list \(CRL\) after a read or write operation\.

## Syntax<a name="aws-resource-rolesanywhere-crl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-rolesanywhere-crl-syntax.json"></a>

```
{
  "Type" : "AWS::RolesAnywhere::CRL",
  "Properties" : {
      "[CrlData](#cfn-rolesanywhere-crl-crldata)" : String,
      "[Enabled](#cfn-rolesanywhere-crl-enabled)" : Boolean,
      "[Name](#cfn-rolesanywhere-crl-name)" : String,
      "[Tags](#cfn-rolesanywhere-crl-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TrustAnchorArn](#cfn-rolesanywhere-crl-trustanchorarn)" : String
    }
}
```

### YAML<a name="aws-resource-rolesanywhere-crl-syntax.yaml"></a>

```
Type: AWS::RolesAnywhere::CRL
Properties: 
  [CrlData](#cfn-rolesanywhere-crl-crldata): String
  [Enabled](#cfn-rolesanywhere-crl-enabled): Boolean
  [Name](#cfn-rolesanywhere-crl-name): String
  [Tags](#cfn-rolesanywhere-crl-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TrustAnchorArn](#cfn-rolesanywhere-crl-trustanchorarn): String
```

## Properties<a name="aws-resource-rolesanywhere-crl-properties"></a>

`CrlData`  <a name="cfn-rolesanywhere-crl-crldata"></a>
The revocation record for a certificate, following the x509 v3 standard\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-rolesanywhere-crl-enabled"></a>
Indicates whether the certificate revocation list \(CRL\) is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-rolesanywhere-crl-name"></a>
The name of the certificate revocation list \(CRL\)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rolesanywhere-crl-tags"></a>
A list of tags to attach to the CRL\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustAnchorArn`  <a name="cfn-rolesanywhere-crl-trustanchorarn"></a>
The ARN of the TrustAnchor the certificate revocation list \(CRL\) will provide revocation for\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rolesanywhere-crl-return-values"></a>

### Ref<a name="aws-resource-rolesanywhere-crl-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns `CrlId`\.

### Fn::GetAtt<a name="aws-resource-rolesanywhere-crl-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-rolesanywhere-crl-return-values-fn--getatt-fn--getatt"></a>

`CrlId`  <a name="CrlId-fn::getatt"></a>
The unique primary identifier of the Crl 