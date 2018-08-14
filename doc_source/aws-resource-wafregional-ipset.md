# AWS::WAFRegional::IPSet<a name="aws-resource-wafregional-ipset"></a>

The `AWS::WAFRegional::IPSet` resource creates an AWS WAF Regional `IPSet` that specifies which web requests to permit or block based on the IP addresses from which the requests originate\. For more information, see [CreateIPSet](http://docs.aws.amazon.com/waf/latest/APIReference/API_regional_CreateIPSet.html) in the *AWS WAF Regional API Reference*\.

**Topics**
+ [Syntax](#aws-resource-wafregional-ipset-syntax)
+ [Properties](#w3ab2c21c10e1217b9)
+ [Return Values](#w3ab2c21c10e1217c11)
+ [Examples](#w3ab2c21c10e1217c13)

## Syntax<a name="aws-resource-wafregional-ipset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-wafregional-ipset-syntax.json"></a>

```
{
  "Type" : "AWS::WAFRegional::IPSet",
  "Properties" : {
    "[IPSetDescriptors](#cfn-wafregional-ipset-ipsetdescriptors)" : [ IPSet descriptor, ... ],
    "[Name](#cfn-wafregional-ipset-name)" : String
  }
}
```

### YAML<a name="aws-resource-wafregional-ipset-syntax.yaml"></a>

```
Type: "AWS::WAFRegional::IPSet"
Properties: 
  [IPSetDescriptors](#cfn-wafregional-ipset-ipsetdescriptors):
    - IPSet descriptor
  [Name](#cfn-wafregional-ipset-name): String
```

## Properties<a name="w3ab2c21c10e1217b9"></a>

`IPSetDescriptors`  <a name="cfn-wafregional-ipset-ipsetdescriptors"></a>
The IP address type and IP address range \(in CIDR notation\) from which web requests originate\. If you associate the `IPSet` with a [web ACL](aws-resource-wafregional-webacl.md) that is associated with a Amazon CloudFront \(CloudFront\) distribution, this descriptor is the value of one of the following fields in the CloudFront access logs:    
`c-ip`  
If the viewer did not use an HTTP proxy or a load balancer to send the request  
`x-forwarded-for`  
If the viewer did use an HTTP proxy or a load balancer to send the request
*Required*: No  
*Type*: List of [AWS WAF Regional IPSet IPSetDescriptors](aws-properties-wafregional-ipset-ipsetdescriptors.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-wafregional-ipset-name"></a>
A friendly name or description of the `IPSet`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="w3ab2c21c10e1217c11"></a>

### Ref<a name="w3ab2c21c10e1217c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource physical ID, such as `1234a1a-a1b1-12a1-abcd-a123b123456`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="w3ab2c21c10e1217c13"></a>

### Define IP Addresses<a name="w3ab2c21c10e1217c13b2"></a>

The following example defines a set of IP addresses for a web access control list \(ACL\) rule\.

#### JSON<a name="aws-resource-wafregional-ipset-example1.json"></a>

```
"MyIPSetBlacklist": {
  "Type": "AWS::WAFRegional::IPSet",
  "Properties": {
    "Name": "IPSet for blacklisted IP addresses",
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

#### YAML<a name="aws-resource-wafregional-ipset-example1.yaml"></a>

```
MyIPSetBlacklist: 
  Type: "AWS::WAFRegional::IPSet"
  Properties: 
    Name: "IPSet for blacklisted IP addresses"
    IPSetDescriptors: 
      - 
        Type: "IPV4"
        Value: "192.0.2.44/32"
      - 
        Type: "IPV4"
        Value: "192.0.7.0/24"
```

### Associate an IPSet with a Web ACL Rule<a name="w3ab2c21c10e1217c13b4"></a>

The following example associates the `MyIPSetBlacklist` IP Set with a web ACL rule\.

#### JSON<a name="aws-resource-wafregional-ipset-example2.json"></a>

```
"MyIPSetRule" : {
  "Type": "AWS::WAFRegional::Rule",
  "Properties": {
    "Name": "MyIPSetRule",
    "MetricName" : "MyIPSetRule",
    "Predicates": [
      {
        "DataId" : {  "Ref" : "MyIPSetBlacklist" },
        "Negated" : false,
        "Type" : "IPMatch"
      }
    ]
  }      
}
```

#### YAML<a name="aws-resource-wafregional-ipset-example2.yaml"></a>

```
MyIPSetRule: 
  Type: "AWS::WAFRegional::Rule"
  Properties: 
    Name: "MyIPSetRule"
    MetricName: "MyIPSetRule"
    Predicates: 
      - 
        DataId: 
          Ref: "MyIPSetBlacklist"
        Negated: false
        Type: "IPMatch"
```

### Create a Web ACL<a name="w3ab2c21c10e1217c13b6"></a>

The following example associates the `MyIPSetRule` rule with a web ACL\. The web ACL allows requests that originate from all IP addresses except for addresses that are defined in the `MyIPSetRule`\.

#### JSON<a name="aws-resource-wafregional-ipset-example3.json"></a>

```
"MyWebACL": {
  "Type": "AWS::WAFRegional::WebACL",
  "Properties": {
    "Name": "WebACL to block blacklisted IP addresses",
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

#### YAML<a name="aws-resource-wafregional-ipset-example3.yaml"></a>

```
MyWebACL: 
  Type: "AWS::WAFRegional::WebACL"
  Properties: 
    Name: "WebACL to block blacklisted IP addresses"
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