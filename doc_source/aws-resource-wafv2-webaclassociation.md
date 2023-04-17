# AWS::WAFv2::WebACLAssociation<a name="aws-resource-wafv2-webaclassociation"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use a web ACL association to define an association between a web ACL and a regional application resource, to protect the resource\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, an AWS AppSync GraphQL API, an Amazon Cognito user pool, or an AWS App Runner service\. 

For Amazon CloudFront, don't use this resource\. Instead, use your CloudFront distribution configuration\. To associate a web ACL with a distribution, provide the Amazon Resource Name \(ARN\) of the [AWS::WAFv2::WebACL](aws-resource-wafv2-webacl.md) to your CloudFront distribution configuration\. To disassociate a web ACL, provide an empty ARN\. For information, see [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)\. 

When you create a web ACL or make changes to a web ACL or web ACL components, like rules and rule groups, AWS WAF propagates the changes everywhere that the web ACL and its components are stored and used\. Your changes are applied within seconds, but there might be a brief period of inconsistency when the changes have arrived in some places and not in others\. So, for example, if you change a rule action setting, the action might be the old action in one area and the new action in another area\. Or if you add an IP address to an IP set used in a blocking rule, the new address might briefly be blocked in one area while still allowed in another\. This temporary inconsistency can occur when you first associate a web ACL with an AWS resource and when you change a web ACL that is already associated with a resource\. Generally, any inconsistencies of this type last only a few seconds\.

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
+ For an Application Load Balancer: `arn:partition:elasticloadbalancing:region:account-id:loadbalancer/app/load-balancer-name/load-balancer-id ` 
+ For an Amazon API Gateway REST API: `arn:partition:apigateway:region::/restapis/api-id/stages/stage-name ` 
+ For an AWS AppSync GraphQL API: `arn:partition:appsync:region:account-id:apis/GraphQLApiId ` 
+ For an Amazon Cognito user pool: `arn:partition:cognito-idp:region:account-id:userpool/user-pool-id ` 
+ For an AWS App Runner service: `arn:partition:apprunner:region:account-id:service/apprunner-service-name/apprunner-service-id ` 
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`WebACLArn`  <a name="cfn-wafv2-webaclassociation-webaclarn"></a>
The Amazon Resource Name \(ARN\) of the web ACL that you want to associate with the resource\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-wafv2-webaclassociation-return-values"></a>

### Ref<a name="aws-resource-wafv2-webaclassociation-return-values-ref"></a>

The `Ref` for the resource, containing the resource name, physical ID, and scope, formatted as follows: `name|id|scope`\.

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`\.

## Examples<a name="aws-resource-wafv2-webaclassociation--examples"></a>



### Create a web ACL association<a name="aws-resource-wafv2-webaclassociation--examples--Create_a_web_ACL_association"></a>

The following shows an example web ACL association specification\. 

#### YAML<a name="aws-resource-wafv2-webaclassociation--examples--Create_a_web_ACL_association--yaml"></a>

```
  SampleWebACLAssociation:
    Type: 'AWS::WAFv2::WebACLAssociation'
    Properties:
      WebACLArn: ExampleARNForWebACL
      ResourceArn: ExampleARNForRegionalResource
```

#### JSON<a name="aws-resource-wafv2-webaclassociation--examples--Create_a_web_ACL_association--json"></a>

```
  "SampleWebACLAssociation": {
    "Type": "AWS::WAFv2::WebACLAssociation",
    "Properties": {
      "WebACLArn": "WebACLArn",
      "ResourceArn": "APIGatewayOrALBArn"
    }
  }
```