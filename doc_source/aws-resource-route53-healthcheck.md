# AWS::Route53::HealthCheck<a name="aws-resource-route53-healthcheck"></a>

Use the `AWS::Route53::HealthCheck` resource to check the health of your resources before Amazon Route 53 responds to a DNS query\. For more information, see [How Health Checks Work in Simple Amazon Route 53 Configurations](http://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-simple-configs.html) in the *Amazon Route 53 Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-route53-healthcheck-syntax)
+ [Properties](#w3ab2c21c10e1014b9)
+ [Return Value](#w3ab2c21c10e1014c11)
+ [Example](#w3ab2c21c10e1014c13)

## Syntax<a name="aws-resource-route53-healthcheck-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-healthcheck-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::HealthCheck",
  "Properties" : {
    "[HealthCheckConfig](#cfn-route53-healthcheck-healthcheckconfig)" : HealthCheckConfig,
    "[HealthCheckTags](#cfn-route53-healthcheck-healthchecktags)" : [ HealthCheckTags, ... ]
  }
}
```

### YAML<a name="aws-resource-route53-healthcheck-syntax.yaml"></a>

```
Type: "AWS::Route53::HealthCheck"
Properties: 
  [HealthCheckConfig](#cfn-route53-healthcheck-healthcheckconfig):
    HealthCheckConfig
  [HealthCheckTags](#cfn-route53-healthcheck-healthchecktags):
    - HealthCheckTags
```

## Properties<a name="w3ab2c21c10e1014b9"></a>

`HealthCheckConfig`  <a name="cfn-route53-healthcheck-healthcheckconfig"></a>
An Amazon Route 53 health check\.  
*Required*: Yes  
*Type*: [Route 53 HealthCheck HealthCheckConfig](aws-properties-route53-healthcheck-healthcheckconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckTags`  <a name="cfn-route53-healthcheck-healthchecktags"></a>
An arbitrary set of tags \(key–value pairs\) for this health check\.  
*Required*: No  
*Type*: A list of [Amazon Route 53 HealthCheck HealthCheckTags](aws-properties-route53-healthcheck-healthchecktags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Value<a name="w3ab2c21c10e1014c11"></a>

### Ref<a name="w3ab2c21c10e1014c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the health check ID, such as `e0a123b4-4dba-4650-935e-example`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Example<a name="w3ab2c21c10e1014c13"></a>

The following example creates an Amazon Route 53 health check that sends request to the specified endpoint\.

### JSON<a name="aws-resource-route53-healthcheck-example.json"></a>

```
"myHealthCheck": {
  "Type": "AWS::Route53::HealthCheck",
  "Properties": {
    "HealthCheckConfig": {
      "IPAddress": "000.000.000.000",
      "Port": "80",
      "Type": "HTTP",
      "ResourcePath": "/example/index.html",
      "FullyQualifiedDomainName": "example.com",
      "RequestInterval": "30",
      "FailureThreshold": "3"
    },
    "HealthCheckTags" : [{
      "Key": "SampleKey1",
      "Value": "SampleValue1"
    },
    {
      "Key": "SampleKey2",
      "Value": "SampleValue2"
    }]
  }
}
```

### YAML<a name="aws-resource-route53-healthcheck-example.yaml"></a>

```
myHealthCheck: 
  Type: "AWS::Route53::HealthCheck"
  Properties: 
    HealthCheckConfig: 
      IPAddress: "000.000.000.000"
      Port: "80"
      Type: "HTTP"
      ResourcePath: "/example/index.html"
      FullyQualifiedDomainName: "example.com"
      RequestInterval: "30"
      FailureThreshold: "3"
    HealthCheckTags: 
      - 
        Key: "SampleKey1"
        Value: "SampleValue1"
      - 
        Key: "SampleKey2"
        Value: "SampleValue2"
```