# AWS::WAFv2::IPSet<a name="aws-resource-wafv2-ipset"></a>

**Note**  
This is the latest version of **AWS WAF**, named AWS WAFV2, released in November, 2019\. For information, including how to migrate your AWS WAF resources from the prior release, see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. 

Use an [AWS::WAFv2::IPSet](#aws-resource-wafv2-ipset) to identify web requests that originate from specific IP addresses or ranges of IP addresses\. For example, if you're receiving a lot of requests from a ranges of IP addresses, you can configure AWS WAF to block them using an IP set that lists those IP addresses\. 

You use an IP set by providing its Amazon Resource Name \(ARN\) to the rule statement `IPSetReferenceStatement`, when you add a rule to a rule group or web ACL\. 

## Syntax<a name="aws-resource-wafv2-ipset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafv2-ipset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFv2::IPSet",
  "Properties" : {
      "[Addresses](#cfn-wafv2-ipset-addresses)" : [ String, ... ],
      "[Description](#cfn-wafv2-ipset-description)" : String,
      "[IPAddressVersion](#cfn-wafv2-ipset-ipaddressversion)" : String,
      "[Name](#cfn-wafv2-ipset-name)" : String,
      "[Scope](#cfn-wafv2-ipset-scope)" : String,
      "[Tags](#cfn-wafv2-ipset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-wafv2-ipset-syntax.yaml"></a>

```
Type: AWS::WAFv2::IPSet
Properties: 
  [Addresses](#cfn-wafv2-ipset-addresses): 
    - String
  [Description](#cfn-wafv2-ipset-description): String
  [IPAddressVersion](#cfn-wafv2-ipset-ipaddressversion): String
  [Name](#cfn-wafv2-ipset-name): String
  [Scope](#cfn-wafv2-ipset-scope): String
  [Tags](#cfn-wafv2-ipset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-wafv2-ipset-properties"></a>

`Addresses`  <a name="cfn-wafv2-ipset-addresses"></a>
Contains an array of strings that specify one or more IP addresses or blocks of IP addresses in Classless Inter\-Domain Routing \(CIDR\) notation\. AWS WAF supports all address ranges for IP versions IPv4 and IPv6\.   
Examples:   
+ To configure AWS WAF to allow, block, or count requests that originated from the IP address 192\.0\.2\.44, specify `192.0.2.44/32`\.
+ To configure AWS WAF to allow, block, or count requests that originated from IP addresses from 192\.0\.2\.0 to 192\.0\.2\.255, specify `192.0.2.0/24`\.
+ To configure AWS WAF to allow, block, or count requests that originated from the IP address 1111:0000:0000:0000:0000:0000:0000:0111, specify `1111:0000:0000:0000:0000:0000:0000:0111/128`\.
+ To configure AWS WAF to allow, block, or count requests that originated from IP addresses 1111:0000:0000:0000:0000:0000:0000:0000 to 1111:0000:0000:0000:ffff:ffff:ffff:ffff, specify `1111:0000:0000:0000:0000:0000:0000:0000/64`\.
For more information about CIDR notation, see the Wikipedia entry [Classless Inter\-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-wafv2-ipset-description"></a>
A friendly description of the IP set\. You cannot change the description of an IP set after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `^[\w+=:#@/\-,\.][\w+=:#@/\-,\.\s]+[\w+=:#@/\-,\.]$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPAddressVersion`  <a name="cfn-wafv2-ipset-ipaddressversion"></a>
Specify IPV4 or IPV6\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `IPV4 | IPV6`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-wafv2-ipset-name"></a>
A friendly name of the IP set\. You cannot change the name of an `IPSet` after you create it\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `^[\w\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scope`  <a name="cfn-wafv2-ipset-scope"></a>
Specifies whether this is for an AWS CloudFront distribution or for a regional application\. A regional application can be an Application Load Balancer \(ALB\), an Amazon API Gateway REST API, or an AWS AppSync GraphQL API\. Valid Values are `CLOUDFRONT` and `REGIONAL`\.   
For `CLOUDFRONT`, you must create your WAFv2 resources in the US East \(N\. Virginia\) Region, `us-east-1`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-wafv2-ipset-tags"></a>
Key:value pairs associated with an AWS resource\. The key:value pair can be anything you define\. Typically, the tag key represents a category \(such as "environment"\) and the tag value represents a specific value within that category \(such as "test," "development," or "production"\)\. You can add up to 50 tags to each AWS resource\.  
To modify tags on existing resources, use the AWS WAF console or the APIs\. With AWS CloudFormation, you can only add tags to AWS WAF resources during resource creation\. 
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-wafv2-ipset-return-values"></a>

### Ref<a name="aws-resource-wafv2-ipset-return-values-ref"></a>

The `Ref` for the resource, containing the resource name, physical ID, and scope, formatted as follows: `name|id|scope`\.

For example: `my-webacl-name|1234a1a-a1b1-12a1-abcd-a123b123456|REGIONAL`

### Fn::GetAtt<a name="aws-resource-wafv2-ipset-return-values-fn--getatt"></a>

#### <a name="aws-resource-wafv2-ipset-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the IP set\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the IP set\.

## Examples<a name="aws-resource-wafv2-ipset--examples"></a>



### Create an IP set<a name="aws-resource-wafv2-ipset--examples--Create_an_IP_set"></a>

The following shows an example IP set specification\. 

#### JSON<a name="aws-resource-wafv2-ipset--examples--Create_an_IP_set--json"></a>

```
"Description": "Sample IPSet",
  "Resources": {
    "SampleIPSet": {
      "Type": "AWS::WAFv2::IPSet",
      "Properties": {
        "Description": "SampleIPSet",
        "Name": "SampleIPSSet",
        "Scope": "REGIONAL",
        "IPAddressVersion": "IPV4",
        "Addresses": [
          "1.2.1.1/32"
        ]
      }
    }
  }
```

#### YAML<a name="aws-resource-wafv2-ipset--examples--Create_an_IP_set--yaml"></a>

```
Description: Sample IPSet
  Resources:
    SampleIPSet:
      Type: 'AWS::WAFv2::IPSet'
      Properties:
        Description: SampleIPSet
        Name: SampleIPSet
        Scope: REGIONAL
        IPAddressVersion: IPV4
        Addresses:
          - 1.2.1.1/32
```