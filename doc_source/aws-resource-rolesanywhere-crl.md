# AWS::RolesAnywhere::CRL<a name="aws-resource-rolesanywhere-crl"></a>

 Creates a Crl\. 

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
 x509 v3 Certificate Revocation List to revoke auth for corresponding certificates presented in CreateSession operations  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enabled`  <a name="cfn-rolesanywhere-crl-enabled"></a>
 The enabled status of the resource\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-rolesanywhere-crl-name"></a>
 The customer specified name of the resource\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-rolesanywhere-crl-tags"></a>
 A list of Tags\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrustAnchorArn`  <a name="cfn-rolesanywhere-crl-trustanchorarn"></a>
The ARN of the TrustAnchor the certificate revocation list \(CRL\) will provide revocation for\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1011`  
*Pattern*: `^arn:aws(-[^:]+)?:rolesanywhere(:.*){2}(:trust-anchor.*)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-rolesanywhere-crl-return-values"></a>

### Ref<a name="aws-resource-rolesanywhere-crl-return-values-ref"></a>

 The name of the CRL\. 

### Fn::GetAtt<a name="aws-resource-rolesanywhere-crl-return-values-fn--getatt"></a>

 

#### <a name="aws-resource-rolesanywhere-crl-return-values-fn--getatt-fn--getatt"></a>

`CrlId`  <a name="CrlId-fn::getatt"></a>
The unique primary identifier of the Crl 