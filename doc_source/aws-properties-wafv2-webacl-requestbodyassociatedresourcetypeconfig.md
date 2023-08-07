# AWS::WAFv2::WebACL RequestBodyAssociatedResourceTypeConfig<a name="aws-properties-wafv2-webacl-requestbodyassociatedresourcetypeconfig"></a>

Customizes the maximum size of the request body that your protected CloudFront distributions forward to AWS WAF for inspection\. The default size is 16 KB \(16,384 bytes\)\. 

**Note**  
You are charged additional fees when your protected resources forward body sizes that are larger than the default\. For more information, see [AWS WAF Pricing](http://aws.amazon.com/waf/pricing/)\.

This is used in the `AssociationConfig` of the web ACL\. 

## Syntax<a name="aws-properties-wafv2-webacl-requestbodyassociatedresourcetypeconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-requestbodyassociatedresourcetypeconfig-syntax.json"></a>

```
{
  "[DefaultSizeInspectionLimit](#cfn-wafv2-webacl-requestbodyassociatedresourcetypeconfig-defaultsizeinspectionlimit)" : String
}
```

### YAML<a name="aws-properties-wafv2-webacl-requestbodyassociatedresourcetypeconfig-syntax.yaml"></a>

```
  [DefaultSizeInspectionLimit](#cfn-wafv2-webacl-requestbodyassociatedresourcetypeconfig-defaultsizeinspectionlimit): String
```

## Properties<a name="aws-properties-wafv2-webacl-requestbodyassociatedresourcetypeconfig-properties"></a>

`DefaultSizeInspectionLimit`  <a name="cfn-wafv2-webacl-requestbodyassociatedresourcetypeconfig-defaultsizeinspectionlimit"></a>
Specifies the maximum size of the web request body component that an associated CloudFront distribution should send to AWS WAF for inspection\. This applies to statements in the web ACL that inspect the body or JSON body\.   
Default: `16 KB (16,384 bytes)`   
*Required*: Yes  
*Type*: String  
*Allowed values*: `KB_16 | KB_32 | KB_48 | KB_64`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)