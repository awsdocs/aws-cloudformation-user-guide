# AWS::Events::Endpoint Primary<a name="aws-properties-events-endpoint-primary"></a>

The primary Region of the endpoint\.

## Syntax<a name="aws-properties-events-endpoint-primary-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-events-endpoint-primary-syntax.json"></a>

```
{
  "[HealthCheck](#cfn-events-endpoint-primary-healthcheck)" : String
}
```

### YAML<a name="aws-properties-events-endpoint-primary-syntax.yaml"></a>

```
  [HealthCheck](#cfn-events-endpoint-primary-healthcheck): String
```

## Properties<a name="aws-properties-events-endpoint-primary-properties"></a>

`HealthCheck`  <a name="cfn-events-endpoint-primary-healthcheck"></a>
The ARN of the health check used by the endpoint to determine whether failover is triggered\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1600`  
*Pattern*: `^arn:aws([a-z]|\-)*:route53:::healthcheck/[\-a-z0-9]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)