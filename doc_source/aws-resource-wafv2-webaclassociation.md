# AWS::WAFv2::WebACLAssociation<a name="aws-resource-wafv2-webaclassociation"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use a web ACL association to define an association between a Web ACL and a regional application resource, to protect the resource\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, or an AWS AppSync GraphQL API\. 

For AWS CloudFront, don't use this resource\. Instead, use your CloudFront distribution configuration\. To associate a Web ACL with a distribution, provide the Amazon Resource Name \(ARN\) of the [AWS::WAFv2::WebACL](aws-resource-wafv2-webacl.md) to your CloudFront distribution configuration\. To disassociate a web ACL, provide an empty ARN\. For information, see [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)\. 

## Syntax<a name="aws-resource-wafv2-webaclassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-webaclassociation-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::WebACLAssociation",
  "Properties" : {
      "[ResourceArn](#cfn-wafv2-webaclassociation-resourcearn)" : String,
      "[WebACLArn](#cfn-wafv2-webaclassociation-webaclarn)" : String
    }
}
```

### YAML<a name="aws-resource-wafv2-webaclassociation-syntax.yaml"></a>

```
Type: AWS::WAFv2::WebACLAssociation
Properties: 
  [ResourceArn](#cfn-wafv2-webaclassociation-resourcearn): String
  [WebACLArn](#cfn-wafv2-webaclassociation-webaclarn): String
```

## Properties<a name="aws-resource-wafv2-webaclassociation-properties"></a>

`ResourceArn`  <a name="cfn-wafv2-webaclassociation-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the resource to associate with the web ACL\.   
The ARN must be in one of the following formats:  
+ For an Application Load Balancer: `arn:aws:elasticloadbalancing:region:account-id:loadbalancer/app/load-balancer-name/load-balancer-id ` 
+ For an Amazon API Gateway REST API: `arn:aws:apigateway:region::/restapis/api-id/stages/stage-name ` 
+ For an AppSync GraphQL API: `arn:aws:appsync:region:account-id:apis/ GraphQLApiId`
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WebACLArn`  <a name="cfn-wafv2-webaclassociation-webaclarn"></a>
The Amazon Resource Name \(ARN\) of the Web ACL that you want to associate with the resource\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-wafv2-webaclassociation-return-values"></a>

### Ref<a name="aws-resource-wafv2-webaclassociation-return-values-ref"></a>

The `Ref` for the resource, containing the resource name, physical ID, and scope, formatted as follows: `name|id|scope`\.

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`

## Examples<a name="aws-resource-wafv2-webaclassociation--examples"></a>



### Create a web ACL association<a name="aws-resource-wafv2-webaclassociation--examples--Create_a_web_ACL_association"></a>

The following shows an example web ACL association specification\. 

#### YAML<a name="aws-resource-wafv2-webaclassociation--examples--Create_a_web_ACL_association--yaml"></a>

```
Resources:
  SampleWebACLAssociation:
    Type: 'AWS::WAFv2::WebACLAssociation'
    Properties:
      WebACLArn: ExampleARNForWebACL
      ResourceArn: ExampleARNForRegionalResource
```

#### JSON<a name="aws-resource-wafv2-webaclassociation--examples--Create_a_web_ACL_association--json"></a>

```
"Resources": {
        "SampleWebACLAssociation": {
            "Type": "AWS::WAFv2::WebACLAssociation",
            "Properties": {
                "WebACLArn": "WebACLArn",
                "ResourceArn": "APIGatewayOrALBArn"
            }
        }
    }
```