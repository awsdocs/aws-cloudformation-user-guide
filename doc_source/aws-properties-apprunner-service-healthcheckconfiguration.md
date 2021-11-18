# AWS::AppRunner::Service HealthCheckConfiguration<a name="aws-properties-apprunner-service-healthcheckconfiguration"></a>

Describes the settings for the health check that AWS App Runner performs to monitor the health of a service\.

## Syntax<a name="aws-properties-apprunner-service-healthcheckconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-apprunner-service-healthcheckconfiguration-syntax.json"></a>

```
{
  "[HealthyThreshold](#cfn-apprunner-service-healthcheckconfiguration-healthythreshold)" : Integer,
  "[Interval](#cfn-apprunner-service-healthcheckconfiguration-interval)" : Integer,
  "[Path](#cfn-apprunner-service-healthcheckconfiguration-path)" : String,
  "[Protocol](#cfn-apprunner-service-healthcheckconfiguration-protocol)" : String,
  "[Timeout](#cfn-apprunner-service-healthcheckconfiguration-timeout)" : Integer,
  "[UnhealthyThreshold](#cfn-apprunner-service-healthcheckconfiguration-unhealthythreshold)" : Integer
}
```

### YAML<a name="aws-properties-apprunner-service-healthcheckconfiguration-syntax.yaml"></a>

```
  [HealthyThreshold](#cfn-apprunner-service-healthcheckconfiguration-healthythreshold): Integer
  [Interval](#cfn-apprunner-service-healthcheckconfiguration-interval): Integer
  [Path](#cfn-apprunner-service-healthcheckconfiguration-path): String
  [Protocol](#cfn-apprunner-service-healthcheckconfiguration-protocol): String
  [Timeout](#cfn-apprunner-service-healthcheckconfiguration-timeout): Integer
  [UnhealthyThreshold](#cfn-apprunner-service-healthcheckconfiguration-unhealthythreshold): Integer
```

## Properties<a name="aws-properties-apprunner-service-healthcheckconfiguration-properties"></a>

`HealthyThreshold`  <a name="cfn-apprunner-service-healthcheckconfiguration-healthythreshold"></a>
The number of consecutive checks that must succeed before App Runner decides that the service is healthy\.  
Default: `1`   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-apprunner-service-healthcheckconfiguration-interval"></a>
The time interval, in seconds, between health checks\.  
Default: `5`   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-apprunner-service-healthcheckconfiguration-path"></a>
The URL that health check requests are sent to\.  
 `Path` is only applicable when you set `Protocol` to `HTTP`\.  
Default: `"/"`   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-apprunner-service-healthcheckconfiguration-protocol"></a>
The IP protocol that App Runner uses to perform health checks for your service\.  
If you set `Protocol` to `HTTP`, App Runner sends health check requests to the HTTP path specified by `Path`\.  
Default: `TCP`   
*Required*: No  
*Type*: String  
*Allowed values*: `HTTP | TCP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Timeout`  <a name="cfn-apprunner-service-healthcheckconfiguration-timeout"></a>
The time, in seconds, to wait for a health check response before deciding it failed\.  
Default: `2`   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnhealthyThreshold`  <a name="cfn-apprunner-service-healthcheckconfiguration-unhealthythreshold"></a>
The number of consecutive checks that must fail before App Runner decides that the service is unhealthy\.  
Default: `5`   
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `20`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)