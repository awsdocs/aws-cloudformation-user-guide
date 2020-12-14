# AWS::WAF::WebACL<a name="aws-resource-waf-webacl"></a>

Contains the `Rules` that identify the requests that you want to allow, block, or count\. In a `WebACL`, you also specify a default action \(`ALLOW` or `BLOCK`\), and the action for each `Rule` that you add to a `WebACL`, for example, block requests from specified IP addresses or block requests from specified referrers\. You also associate the `WebACL` with a CloudFront distribution to identify the requests that you want AWS WAF to filter\. If you add more than one `Rule` to a `WebACL`, a request needs to match only one of the specifications to be allowed, blocked, or counted\.

## Syntax<a name="aws-resource-waf-webacl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-waf-webacl-syntax.json"></a>

```
{
  "Type" : "AWS::WAF::WebACL",
  "Properties" : {
      "[DefaultAction](#cfn-waf-webacl-defaultaction)" : WafAction,
      "[MetricName](#cfn-waf-webacl-metricname)" : String,
      "[Name](#cfn-waf-webacl-name)" : String,
      "[Rules](#cfn-waf-webacl-rules)" : [ ActivatedRule, ... ]
    }
}
```

### YAML<a name="aws-resource-waf-webacl-syntax.yaml"></a>

```
Type: AWS::WAF::WebACL
Properties: 
  [DefaultAction](#cfn-waf-webacl-defaultaction): 
    WafAction
  [MetricName](#cfn-waf-webacl-metricname): String
  [Name](#cfn-waf-webacl-name): String
  [Rules](#cfn-waf-webacl-rules): 
    - ActivatedRule
```

## Properties<a name="aws-resource-waf-webacl-properties"></a>

`DefaultAction`  <a name="cfn-waf-webacl-defaultaction"></a>
The action to perform if none of the `Rules` contained in the `WebACL` match\. The action is specified by the `WafAction` object\.  
*Required*: Yes  
*Type*: [WafAction](aws-properties-waf-webacl-action.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MetricName`  <a name="cfn-waf-webacl-metricname"></a>
A friendly name or description for the metrics for this `WebACL`\. The name can contain only alphanumeric characters \(A\-Z, a\-z, 0\-9\), with maximum length 128 and minimum length one\. It can't contain whitespace or metric names reserved for AWS WAF, including "All" and "Default\_Action\." You can't change `MetricName` after you create the `WebACL`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-waf-webacl-name"></a>
A friendly name or description of the `WebACL`\. You can't change the name of a `WebACL` after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Rules`  <a name="cfn-waf-webacl-rules"></a>
An array that contains the action for each `Rule` in a `WebACL`, the priority of the `Rule`, and the ID of the `Rule`\.  
*Required*: No  
*Type*: List of [ActivatedRule](aws-properties-waf-webacl-rules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-waf-webacl-return-values"></a>

### Ref<a name="aws-resource-waf-webacl-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-waf-webacl--examples"></a>



### Create a Web ACL<a name="aws-resource-waf-webacl--examples--Create_a_Web_ACL"></a>

The following example defines a web ACL that allows, by default, any web request\. However, if the request matches any rule, AWS WAF blocks the request\. AWS WAF evaluates each rule in priority order, starting with the lowest value\.

#### JSON<a name="aws-resource-waf-webacl--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAF::WebACL",
  "Properties": {
    "Name": "WebACL to with three rules",
    "DefaultAction": {
      "Type": "ALLOW"
    },
    "MetricName" : "MyWebACL",
    "Rules": [
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 1,
        "RuleId" : { "Ref" : "MyRule" }
      },
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 2,
        "RuleId" : { "Ref" : "BadReferersRule" }
      },
      {
        "Action" : {
          "Type" : "BLOCK"
        },
        "Priority" : 3,
        "RuleId" : { "Ref" : "SqlInjRule" }
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-waf-webacl--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAF::WebACL"
  Properties: 
    Name: "WebACL to with three rules"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "MyWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "MyRule"
      - 
        Action: 
          Type: "BLOCK"
        Priority: 2
        RuleId: 
          Ref: "BadReferersRule"
      - 
        Action: 
          Type: "BLOCK"
        Priority: 3
        RuleId: 
          Ref: "SqlInjRule"
```

### Associate a Web ACL with a CloudFront Distribution<a name="aws-resource-waf-webacl--examples--Associate_a_Web_ACL_with_a_CloudFront_Distribution"></a>

The follow example associates the `MyWebACL` web ACL with a CloudFront distribution\. The web ACL restricts which requests can access content served by CloudFront\.

#### JSON<a name="aws-resource-waf-webacl--examples--Associate_a_Web_ACL_with_a_CloudFront_Distribution--json"></a>

```
"myDistribution": {
  "Type": "AWS::CloudFront::Distribution",
  "Properties": {
    "DistributionConfig": {    
      "WebACLId": { "Ref" : "MyWebACL" },
      "Origins": [
        {
          "DomainName": "test.example.com",
          "Id": "myCustomOrigin",
          "CustomOriginConfig": {
            "HTTPPort": "80",
            "HTTPSPort": "443",
            "OriginProtocolPolicy": "http-only"
          }
        }
      ],
      "Enabled": "true",
      "Comment": "TestDistribution",
      "DefaultRootObject": "index.html",
      "DefaultCacheBehavior": {
        "TargetOriginId": "myCustomOrigin",
        "SmoothStreaming" : "false",
        "ForwardedValues": {
          "QueryString": "false",
          "Cookies" : { "Forward" : "all" }
        },
        "ViewerProtocolPolicy": "allow-all"
      },
      "CustomErrorResponses" : [
        {
          "ErrorCode" : "404",
          "ResponsePagePath" : "/error-pages/404.html",
          "ResponseCode" : "200",
          "ErrorCachingMinTTL" : "30"
        }
      ],
      "PriceClass" : "PriceClass_200",
      "Restrictions" : {
        "GeoRestriction" : {
          "RestrictionType" : "whitelist",
          "Locations" : [ "AQ", "CV" ]
        }
      },
      "ViewerCertificate" : { "CloudFrontDefaultCertificate" : "true" }
    }
  }
}
```

#### YAML<a name="aws-resource-waf-webacl--examples--Associate_a_Web_ACL_with_a_CloudFront_Distribution--yaml"></a>

```
myDistribution: 
  Type: "AWS::CloudFront::Distribution"
  Properties: 
    DistributionConfig: 
      WebACLId: 
        Ref: "MyWebACL"
      Origins: 
        - 
          DomainName: "test.example.com"
          Id: "myCustomOrigin"
          CustomOriginConfig: 
            HTTPPort: "80"
            HTTPSPort: "443"
            OriginProtocolPolicy: "http-only"
      Enabled: "true"
      Comment: "TestDistribution"
      DefaultRootObject: "index.html"
      DefaultCacheBehavior: 
        TargetOriginId: "myCustomOrigin"
        SmoothStreaming: "false"
        ForwardedValues: 
          QueryString: "false"
          Cookies: 
            Forward: "all"
        ViewerProtocolPolicy: "allow-all"
      CustomErrorResponses: 
        - 
          ErrorCode: "404"
          ResponsePagePath: "/error-pages/404.html"
          ResponseCode: "200"
          ErrorCachingMinTTL: "30"
      PriceClass: "PriceClass_200"
      Restrictions: 
        GeoRestriction: 
          RestrictionType: "whitelist"
          Locations: 
            - "AQ"
            - "CV"
      ViewerCertificate: 
        CloudFrontDefaultCertificate: "true"
```