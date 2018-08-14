# AWS::WAFRegional::WebACL<a name="aws-resource-wafregional-webacl"></a>

The `AWS::WAFRegional::WebACL` resource creates an AWS WAF Regional web access control group \(ACL\) containing the rules that identify the Amazon CloudFront \(CloudFront\) web requests that you want to allow, block, or count\. For more information, see [CreateWebACL](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_CreateWebACL.html) in the *AWS WAF Regional API Reference*\.

**Topics**
+ [Syntax](#aws-resource-wafregional-webacl-syntax)
+ [Properties](#w3ab2c21c10e1233b9)
+ [Return Values](#w3ab2c21c10e1233c11)
+ [Examples](#w3ab2c21c10e1233c13)

## Syntax<a name="aws-resource-wafregional-webacl-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-webacl-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::WebACL",
  "Properties" : {
    "[DefaultAction](#cfn-wafregional-webacl-defaultaction)" : Action,
    "[MetricName](#cfn-wafregional-webacl-metricname)" : String,
    "[Name](#cfn-wafregional-webacl-name)" : String,
    "[Rules](#cfn-wafregional-webacl-rules)" : [ Rule, ... ]
  }
}
```

### YAML<a name="aws-resource-wafregional-webacl-syntax.yaml"></a>

```
Type: "AWS::WAFRegional::WebACL"
Properties: 
  [DefaultAction](#cfn-wafregional-webacl-defaultaction):
    Action
  [MetricName](#cfn-wafregional-webacl-metricname): String
  [Name](#cfn-wafregional-webacl-name): String
  [Rules](#cfn-wafregional-webacl-rules):
    - Rule
```

## Properties<a name="w3ab2c21c10e1233b9"></a>

`DefaultAction`  <a name="cfn-wafregional-webacl-defaultaction"></a>
The action that you want AWS WAF to take when a request doesn't match the criteria in any of the rules that are associated with the web ACL\.  
*Required*: Yes  
*Type*: [AWS WAF Regional WebACL Action](aws-properties-wafregional-webacl-action.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MetricName`  <a name="cfn-wafregional-webacl-metricname"></a>
A friendly name or description for the Amazon CloudWatch metric of this web ACL\. For valid values, see the `MetricName` parameter of the [CreateWebACL](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_CreateWebACL.html) action in the *AWS WAF Regional API Reference*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-wafregional-webacl-name"></a>
A friendly name or description of the web ACL\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Rules`  <a name="cfn-wafregional-webacl-rules"></a>
The rules to associate with the web ACL and the settings for each rule\.  
*Required*: No  
*Type*: List of [AWS WAF Regional WebACL Rules](aws-properties-wafregional-webacl-rules.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10e1233c11"></a>

### Ref<a name="w3ab2c21c10e1233c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name, such as `1234a1a-a1b1-12a1-abcd-a123b123456`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10e1233c13"></a>

### Create a Web ACL<a name="w3ab2c21c10e1233c13b2"></a>

The following example defines a web ACL that allows, by default, any web request\. However, if the request matches any rule, AWS WAF blocks the request\. AWS WAF evaluates each rule in priority order, starting with the lowest value\.

#### JSON<a name="aws-resource-wafregional-webacl-example1.json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
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

#### YAML<a name="aws-resource-wafregional-webacl-example1.yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
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

### Associate a Web ACL with a CloudFront Distribution<a name="w3ab2c21c10e1233c13b4"></a>

The follow example associates the `MyWebACL` web ACL with a CloudFront distribution\. The web ACL restricts which requests can access content served by CloudFront\.

#### JSON<a name="aws-resource-wafregional-webacl-example2.json"></a>

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

#### YAML<a name="aws-resource-wafregional-webacl-example2.yaml"></a>

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