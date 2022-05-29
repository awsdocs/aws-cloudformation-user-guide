# AWS::WAF::IPSet<a name="aws-resource-waf-ipset"></a>

**Note**  
This is ** AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF **, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

Contains one or more IP addresses or blocks of IP addresses specified in Classless Inter\-Domain Routing \(CIDR\) notation\. AWS WAF supports IPv4 address ranges: /8 and any range between /16 through /32\. AWS WAF supports IPv6 address ranges: /24, /32, /48, /56, /64, and /128\.

To specify an individual IP address, you specify the four\-part IP address followed by a `/32`, for example, 192\.0\.2\.0/32\. To block a range of IP addresses, you can specify /8 or any range between /16 through /32 \(for IPv4\) or /24, /32, /48, /56, /64, or /128 \(for IPv6\)\. For more information about CIDR notation, see the Wikipedia entry [Classless Inter\-Domain Routing](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)\. 

## Syntax<a name="aws-resource-waf-ipset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-waf-ipset-syntax.json"></a>

```
{
  "Type" : "AWS::WAF::IPSet",
  "Properties" : {
      "[IPSetDescriptors](#cfn-waf-ipset-ipsetdescriptors)" : [ IPSetDescriptor, ... ],
      "[Name](#cfn-waf-ipset-name)" : String
    }
}
```

### YAML<a name="aws-resource-waf-ipset-syntax.yaml"></a>

```
Type: AWS::WAF::IPSet
Properties: 
  [IPSetDescriptors](#cfn-waf-ipset-ipsetdescriptors): 
    - IPSetDescriptor
  [Name](#cfn-waf-ipset-name): String
```

## Properties<a name="aws-resource-waf-ipset-properties"></a>

`IPSetDescriptors`  <a name="cfn-waf-ipset-ipsetdescriptors"></a>
The IP address type \(`IPV4` or `IPV6`\) and the IP address range \(in CIDR notation\) that web requests originate from\. If the `WebACL` is associated with an Amazon CloudFront distribution and the viewer did not use an HTTP proxy or a load balancer to send the request, this is the value of the c\-ip field in the CloudFront access logs\.  
*Required*: No  
*Type*: List of [IPSetDescriptor](aws-properties-waf-ipset-ipsetdescriptors.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-waf-ipset-name"></a>
The name of the `IPSet`\. You can't change the name of an `IPSet` after you create it\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-waf-ipset-return-values"></a>

### Ref<a name="aws-resource-waf-ipset-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource physical ID, such as 1234a1a\-a1b1\-12a1\-abcd\-a123b123456\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-waf-ipset--examples"></a>



### Define IP Addresses<a name="aws-resource-waf-ipset--examples--Define_IP_Addresses"></a>

The following example defines a set of IP addresses for a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-waf-ipset--examples--Define_IP_Addresses--json"></a>

```
"MyIPSetDenylist": {
  "Type": "AWS::WAF::IPSet",
  "Properties": {
    "Name": "IPSet for deny listed IP addresses",
    "IPSetDescriptors": [
      {
        "Type" : "IPV4",
        "Value" : "192.0.2.44/32"
      },
      {
        "Type" : "IPV4",
        "Value" : "192.0.7.0/24"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-waf-ipset--examples--Define_IP_Addresses--yaml"></a>

```
MyIPSetDenylist: 
  Type: "AWS::WAF::IPSet"
  Properties: 
    Name: "IPSet for deny listed IP addresses"
    IPSetDescriptors: 
      - 
        Type: "IPV4"
        Value: "192.0.2.44/32"
      - 
        Type: "IPV4"
        Value: "192.0.7.0/24"
```

### Associate an IPSet with a Web ACL Rule<a name="aws-resource-waf-ipset--examples--Associate_an_IPSet_with_a_Web_ACL_Rule"></a>

The following example associates the `MyIPSetDenylist` IP Set with a web ACL rule\.

#### JSON<a name="aws-resource-waf-ipset--examples--Associate_an_IPSet_with_a_Web_ACL_Rule--json"></a>

```
"MyIPSetRule" : {
  "Type": "AWS::WAF::Rule",
  "Properties": {
    "Name": "MyIPSetRule",
    "MetricName" : "MyIPSetRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "MyIPSetDenylist" },
        "Negated" : false,
        "Type" : "IPMatch"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-waf-ipset--examples--Associate_an_IPSet_with_a_Web_ACL_Rule--yaml"></a>

```
MyIPSetRule: 
  Type: "AWS::WAF::Rule"
  Properties: 
    Name: "MyIPSetRule"
    MetricName: "MyIPSetRule"
    Predicates: 
      - 
        DataId: 
          Ref: "MyIPSetDenylist"
        Negated: false
        Type: "IPMatch"
```

### Create a Web ACL<a name="aws-resource-waf-ipset--examples--Create_a_Web_ACL"></a>

The following example associates the `MyIPSetRule` rule with a web ACL\. The web ACL allows requests that originate from all IP addresses except for addresses that are defined in the `MyIPSetRule`\.

#### JSON<a name="aws-resource-waf-ipset--examples--Create_a_Web_ACL--json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAF::WebACL",
  "Properties": {
    "Name": "WebACL to block IP addresses",
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
        "RuleId" : { "Ref" : "MyIPSetRule" }
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-waf-ipset--examples--Create_a_Web_ACL--yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAF::WebACL"
  Properties: 
    Name: "WebACL to block IP addresses"
    DefaultAction: 
      Type: "ALLOW"
    MetricName: "MyWebACL"
    Rules: 
      - 
        Action: 
          Type: "BLOCK"
        Priority: 1
        RuleId: 
          Ref: "MyIPSetRule"
```