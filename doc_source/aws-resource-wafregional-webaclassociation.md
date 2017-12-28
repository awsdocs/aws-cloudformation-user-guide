# AWS::WAFRegional::WebACLAssociation<a name="aws-resource-wafregional-webaclassociation"></a>

The `AWS::WAFRegional::WebACLAssociation` resource associates an AWS WAF Regional web access control group \(ACL\) with a resource\. For more information, see [AssociateWebACL](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_AssociateWebACL.html) in the *AWS WAF Regional API Reference*\.


+ [Syntax](#aws-resource-wafregional-webaclassociation-syntax)
+ [Properties](#w3ab2c21c10e1091b9)
+ [Example](#w3ab2c21c10e1091c11)

## Syntax<a name="aws-resource-wafregional-webaclassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-webaclassociation-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::WebACLAssociation",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-wafregional-webaclassociation-resourcearn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-wafregional-webaclassociation-webaclid)" : String
  }
}
```

### YAML<a name="aws-resource-wafregional-webaclassociation-syntax.yaml"></a>

```
Type: "AWS::WAFRegional::WebACLAssociation"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-wafregional-webaclassociation-resourcearn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-wafregional-webaclassociation-webaclid): String
```

## Properties<a name="w3ab2c21c10e1091b9"></a>

**Note**  
For more information about constraints and values for each property, see [AssociateWebACL](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_AssociateWebACL.html) in the *AWS WAF Regional API Reference*\.

`ResourceArn`  
The Amazon Resource Name \(ARN\) of the resource to protect with the web ACL\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`WebACLId`  
A unique identifier \(ID\) for the web ACL\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

## Example<a name="w3ab2c21c10e1091c11"></a>

### <a name="w3ab2c21c10e1091c11b2"></a>

The following example associates an Application load balancer resource with a web ACL\.

#### JSON<a name="aws-resource-wafregional-webaclassociation-example1.json"></a>

```
"MyWebACLAssociation": {
  "Type": "AWS::WAFRegional::WebACLAssociation",
  "Properties": {
    "ResourceArn": { "Ref": "MyLoadBalancer" },
    "WebACLId": { "Ref": "MyWebACL" }
  }
}
```

#### YAML<a name="aws-resource-wafregional-webaclassociation-example1.yaml"></a>

```
MyWebACLAssociation:
  Type: "AWS::WAFRegional::WebACLAssociation"
  Properties:
    ResourceArn:
      Ref: MyLoadBalancer
    WebACLId:
      Ref: MyWebACL
```