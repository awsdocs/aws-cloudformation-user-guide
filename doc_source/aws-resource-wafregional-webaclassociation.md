# AWS::WAFRegional::WebACLAssociation<a name="aws-resource-wafregional-webaclassociation"></a>

**Note**  
This is ** AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF **, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

The AWS::WAFRegional::WebACLAssociation resource associates an AWS WAF Regional web access control group \(ACL\) with a resource\.

## Syntax<a name="aws-resource-wafregional-webaclassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-webaclassociation-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::WebACLAssociation",
  "Properties" : {
      "[ResourceArn](#cfn-wafregional-webaclassociation-resourcearn)" : String,
      "[WebACLId](#cfn-wafregional-webaclassociation-webaclid)" : String
    }
}
```

### YAML<a name="aws-resource-wafregional-webaclassociation-syntax.yaml"></a>

```
Type: AWS::WAFRegional::WebACLAssociation
Properties: 
  [ResourceArn](#cfn-wafregional-webaclassociation-resourcearn): String
  [WebACLId](#cfn-wafregional-webaclassociation-webaclid): String
```

## Properties<a name="aws-resource-wafregional-webaclassociation-properties"></a>

`ResourceArn`  <a name="cfn-wafregional-webaclassociation-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the resource to protect with the web ACL\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WebACLId`  <a name="cfn-wafregional-webaclassociation-webaclid"></a>
A unique identifier \(ID\) for the web ACL\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-wafregional-webaclassociation--examples"></a>



### Associate an Application Load Balancer resource with a web ACL<a name="aws-resource-wafregional-webaclassociation--examples--Associate_an_Application_Load_Balancer_resource_with_a_web_ACL"></a>

The following example associates an Application Load Balancer resource with a web ACL\.

#### JSON<a name="aws-resource-wafregional-webaclassociation--examples--Associate_an_Application_Load_Balancer_resource_with_a_web_ACL--json"></a>

```
"MyWebACLAssociation": {
  "Type": "AWS::WAFRegional::WebACLAssociation",
  "Properties": {
    "ResourceArn": { "Ref": "MyLoadBalancer" },
    "WebACLId": { "Ref": "MyWebACL" }
  }
}
```

#### YAML<a name="aws-resource-wafregional-webaclassociation--examples--Associate_an_Application_Load_Balancer_resource_with_a_web_ACL--yaml"></a>

```
MyWebACLAssociation:
  Type: "AWS::WAFRegional::WebACLAssociation"
  Properties:
    ResourceArn:
      Ref: MyLoadBalancer
    WebACLId:
      Ref: MyWebACL
```