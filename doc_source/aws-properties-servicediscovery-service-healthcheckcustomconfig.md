# AWS Cloud Map ServiceDiscovery Service HealthCheckCustomConfig<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig"></a>

<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig-description"></a>The `HealthCheckCustomConfig` property type specifies information about an optional custom health check\.

<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig-inheritance"></a> `HealthCheckCustomConfig` is a property of the [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md) resource\.

## Syntax<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig-syntax.json"></a>

```
{
  "[FailureThreshold](#cfn-servicediscovery-service-healthcheckcustomconfig-failurethreshold)" : Double
}
```

### YAML<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig-syntax.yaml"></a>

```
[FailureThreshold](#cfn-servicediscovery-service-healthcheckcustomconfig-failurethreshold): Double
```

## Properties<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig-properties"></a>

`FailureThreshold`  <a name="cfn-servicediscovery-service-healthcheckcustomconfig-failurethreshold"></a>
The number of 30\-second intervals that you want service discovery to wait after receiving an `UpdateInstanceCustomHealthStatus` request before it changes the health status of a service instance\. For example, suppose you specify a value of 2 for `FailureTheshold` , and then your application sends an `UpdateInstanceCustomHealthStatus` request\. Service discovery waits for approximately 60 seconds \(2 x 30\) before changing the status of the service instance based on that request\.  
Sending a second or subsequent `UpdateInstanceCustomHealthStatus` request with the same value before `FailureThreshold` x 30 seconds has passed doesn't accelerate the change\. Service discovery still waits `FailureThreshold` x 30 seconds after the first request to make the change\.  
Minimum value of 1\. Maximum value of 10\.  
 *Required*: No  
 *Type*: Double  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## See Also<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig-seealso"></a>
+ [HealthCheckCustomConfig](https://docs.aws.amazon.com/cloud-map/latest/api/API_HealthCheckCustomConfig.html) in the *AWS Cloud Map API Reference*