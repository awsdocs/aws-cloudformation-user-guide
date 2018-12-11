# AWS Cloud Map ServiceDiscovery HealthCheckConfig<a name="aws-properties-servicediscovery-service-healthcheckconfig"></a>

<a name="aws-properties-servicediscovery-service-healthcheckconfig-description"></a>The `HealthCheckConfig` property type specifies settings for an optional Amazon Route 53 health check\. If you specify settings for a health check, AWS Cloud Map associates the health check with all the records that you specify in `DnsConfig`\.

<a name="aws-properties-servicediscovery-service-healthcheckconfig-inheritance"></a>`HealthCheckConfig` is a property of the [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md) resource\.

## Syntax<a name="aws-properties-servicediscovery-service-healthcheckconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicediscovery-service-healthcheckconfig-syntax.json"></a>

```
{
  "[Type](#cfn-servicediscovery-service-healthcheckconfig-type)" : String,
  "[ResourcePath](#cfn-servicediscovery-service-healthcheckconfig-resourcepath)" : String,
  "[FailureThreshold](#cfn-servicediscovery-service-healthcheckconfig-failurethreshold)" : Double
}
```

### YAML<a name="aws-properties-servicediscovery-service-healthcheckconfig-syntax.yaml"></a>

```
[Type](#cfn-servicediscovery-service-healthcheckconfig-type): String
[ResourcePath](#cfn-servicediscovery-service-healthcheckconfig-resourcepath): String
[FailureThreshold](#cfn-servicediscovery-service-healthcheckconfig-failurethreshold): Double
```

## Properties<a name="aws-properties-servicediscovery-service-healthcheckconfig-properties"></a>

`Type`  <a name="cfn-servicediscovery-service-healthcheckconfig-type"></a>
The type of health check that you want to create, which indicates how Route 53 determines whether an endpoint is healthy\. Valid types include `HTTP`, `HTTPS`, and `TCP`\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ResourcePath`  <a name="cfn-servicediscovery-service-healthcheckconfig-resourcepath"></a>
The path that you want Route 53 to request when performing health checks\. The path can be any value for which your endpoint will return an HTTP status code of 2xx or 3xx when the endpoint is healthy, such as the file `/docs/route53-health-check.html`\. Route 53 automatically adds the DNS name for the service and a leading forward slash \(/\) character\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`FailureThreshold`  <a name="cfn-servicediscovery-service-healthcheckconfig-failurethreshold"></a>
The number of consecutive health checks that an endpoint must pass or fail for Route 53 to change the current status of the endpoint from unhealthy to healthy or vice versa\. For more information, see [How Route 53 Determines Whether a Health Check Is Healthy](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/dns-failover-determining-health-of-endpoints.html) in the *Amazon Route 53 Developer Guide*  
*Required*: No  
*Type*: Double  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-servicediscovery-service-healthcheckconfig-seealso"></a>
+ [CreateService](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateService.html) in the *AWS Cloud Map API Reference*