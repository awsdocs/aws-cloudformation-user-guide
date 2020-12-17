# AWS::ServiceDiscovery::Service HealthCheckCustomConfig<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig"></a>

A complex type that contains information about an optional custom health check\. A custom health check, which requires that you use a third\-party health checker to evaluate the health of your resources, is useful in the following circumstances:
+ You can't use a health check that is defined by `HealthCheckConfig` because the resource isn't available over the internet\. For example, you can use a custom health check when the instance is in an Amazon VPC\. \(To check the health of resources in a VPC, the health checker must also be in the VPC\.\)
+ You want to use a third\-party health checker regardless of where your resources are\.

**Important**  
If you specify a health check configuration, you can specify either `HealthCheckCustomConfig` or `HealthCheckConfig` but not both\.

To change the status of a custom health check, submit an `UpdateInstanceCustomHealthStatus` request\. AWS Cloud Map doesn't monitor the status of the resource, it just keeps a record of the status specified in the most recent `UpdateInstanceCustomHealthStatus` request\.

Here's how custom health checks work:

1. You create a service and specify a value for `FailureThreshold`\. 

   The failure threshold indicates the number of 30\-second intervals you want AWS Cloud Map to wait between the time that your application sends an [UpdateInstanceCustomHealthStatus](https://docs.aws.amazon.com/cloud-map/latest/api/API_UpdateInstanceCustomHealthStatus.html) request and the time that AWS Cloud Map stops routing internet traffic to the corresponding resource\.

1. You register an instance\.

1. You configure a third\-party health checker to monitor the resource that is associated with the new instance\. 
**Note**  
AWS Cloud Map doesn't check the health of the resource directly\. 

1. The third\-party health\-checker determines that the resource is unhealthy and notifies your application\.

1. Your application submits an `UpdateInstanceCustomHealthStatus` request\.

1. AWS Cloud Map waits for \(`FailureThreshold` x 30\) seconds\.

1. If another `UpdateInstanceCustomHealthStatus` request doesn't arrive during that time to change the status back to healthy, AWS Cloud Map stops routing traffic to the resource\.

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
This parameter has been deprecated and is always set to 1\. AWS Cloud Map waits for approximately 30 seconds after receiving an `UpdateInstanceCustomHealthStatus` request before changing the status of the service instance\.
The number of 30\-second intervals that you want AWS Cloud Map to wait after receiving an `UpdateInstanceCustomHealthStatus` request before it changes the health status of a service instance\.  
Sending a second or subsequent `UpdateInstanceCustomHealthStatus` request with the same value before 30 seconds has passed doesn't accelerate the change\. AWS Cloud Map still waits `30` seconds after the first request to make the change\.  
*Required*: No  
*Type*: Double  
*Minimum*: `1`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## See also<a name="aws-properties-servicediscovery-service-healthcheckcustomconfig--seealso"></a>
+  [Return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html#aws-resource-servicediscovery-service-return-values) in the topic [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html) 
+  [HealthCheckCustomConfig](https://docs.aws.amazon.com/cloud-map/latest/api/API_HealthCheckCustomConfig.html) in the *AWS Cloud Map API Reference* 

