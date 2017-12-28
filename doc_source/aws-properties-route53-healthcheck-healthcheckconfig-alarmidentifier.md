# Amazon Route 53 AlarmIdentifier<a name="aws-properties-route53-healthcheck-healthcheckconfig-alarmidentifier"></a>

The `AlarmIdentifier` subproperty describes the name and Region that are associated with an [Route 53 HealthCheckConfig](aws-properties-route53-healthcheck-healthcheckconfig.md) property\.

## Syntax<a name="w3ab2c21c14e1447b5"></a>

### JSON<a name="aws-properties-route53-healthcheck-healthcheckconfig-alarmidentifier-syntax.json"></a>

```
{
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-healthcheckconfig-alarmidentifier-name)" : String,
  "[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-healthcheckconfig-alarmidentifier-region)" : String
}
```

### YAML<a name="aws-properties-route53-healthcheck-healthcheckconfig-alarmidentifier-syntax.yaml"></a>

```
[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-healthcheckconfig-alarmidentifier-name): String
[[ERROR] BAD/MISSING LINK TEXT](#cfn-route53-healthcheckconfig-alarmidentifier-region): String
```

## Properties<a name="w3ab2c21c14e1447b7"></a>

`Name`  
The name of the Amazon CloudWatch alarm that you want Route 53 health checkers to use to determine whether this health check is healthy\.  
*Required: *Yes  
*Type*: String

`Region`  
A complex type that identifies the CloudWatch alarm that you want Route 53 health checkers to use to determine whether this health check is healthy\. For example, `us-west-2`\.  
*Required: *Yes  
*Type*: String