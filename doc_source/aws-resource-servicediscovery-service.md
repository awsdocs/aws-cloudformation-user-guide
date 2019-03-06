# AWS::ServiceDiscovery::Service<a name="aws-resource-servicediscovery-service"></a>

The `AWS::ServiceDiscovery::Service` resource defines a template that your application uses to register service instances\. For more information, see [CreateService](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateService.html) in the *AWS Cloud Map API Reference*\.

## Syntax<a name="aws-resource-servicediscovery-service-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-service-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::Service",
  "Properties" : {
    "[Description](#cfn-servicediscovery-service-description)" : String,
    "[DnsConfig](#cfn-servicediscovery-service-dnsconfig)" : [*DnsConfig*](aws-properties-servicediscovery-service-dnsconfig.md),
    "[HealthCheckConfig](#cfn-servicediscovery-service-healthcheckconfig)" : [*HealthCheckConfig*](aws-properties-servicediscovery-service-healthcheckconfig.md),
    "[HealthCheckCustomConfig](#cfn-servicediscovery-service-healthcheckcustomconfig)" : [*HealthCheckCustomConfig*](aws-properties-servicediscovery-service-healthcheckcustomconfig.md),
    "[Name](#cfn-servicediscovery-service-name)" : String,
    "[NamespaceId](#cfn-servicediscovery-service-namespaceid)" : String
  }
}
```

### YAML<a name="aws-resource-servicediscovery-service-syntax.yaml"></a>

```
Type: "AWS::ServiceDiscovery::Service"
Properties:
  [Description](#cfn-servicediscovery-service-description): String
  [DnsConfig](#cfn-servicediscovery-service-dnsconfig): 
    [*DnsConfig*](aws-properties-servicediscovery-service-dnsconfig.md)
  [HealthCheckConfig](#cfn-servicediscovery-service-healthcheckconfig): 
    [*HealthCheckConfig*](aws-properties-servicediscovery-service-healthcheckconfig.md)
  [HealthCheckCustomConfig](#cfn-servicediscovery-service-healthcheckcustomconfig): 
    [*HealthCheckCustomConfig*](aws-properties-servicediscovery-service-healthcheckcustomconfig.md)
  [Name](#cfn-servicediscovery-service-name): String,
  [NamespaceId](#cfn-servicediscovery-service-namespaceid): String
```

## Properties<a name="aws-resource-servicediscovery-service-properties"></a>

`Description`  <a name="cfn-servicediscovery-service-description"></a>
A description for the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DnsConfig`  <a name="cfn-servicediscovery-service-dnsconfig"></a>
An optional complex type that contains information about the DNS records that you want AWS Cloud Map to create when you register an instance\.  
*Required*: No  
*Type*: [DnsConfig](aws-properties-servicediscovery-service-dnsconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckConfig`  <a name="cfn-servicediscovery-service-healthcheckconfig"></a>
A complex type that contains settings for an optional Route 53 health check\. If you specify settings for a health check, AWS Cloud Map associates the health check with all the records that you specify in `DnsConfig`\.  
If you specify a health check configuration, you can specify either `HealthCheckCustomConfig` or `HealthCheckConfig` but not both\.  
*Required*: No  
*Type*: [HealthCheckConfig](aws-properties-servicediscovery-service-healthcheckconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckCustomConfig`  <a name="cfn-servicediscovery-service-healthcheckcustomconfig"></a>
Specifies information about an optional custom health check\.  
If you specify a health check configuration, you can specify either `HealthCheckCustomConfig` or `HealthCheckConfig` but not both\.  
*Required*: No  
*Type*: [HealthCheckCustomConfig](aws-properties-servicediscovery-service-healthcheckcustomconfig.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-servicediscovery-service-name"></a>
The name that you want to assign to the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`NamespaceId`  <a name="cfn-servicediscovery-service-namespaceid"></a>
The ID of the namespace that you want to use to create the service\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-servicediscovery-service-returnvalues"></a>

### Ref<a name="aws-resource-servicediscovery-service-ref"></a>

When you pass the logical ID of an `AWS::ServiceDiscovery::Service` resource to the intrinsic `Ref` function, the function returns the value of `Id` for the service\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-servicediscovery-service-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the service\.

`Id`  
The ID of the service\.

`Name`  
The name that you assigned to the service\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## See Also<a name="aws-resource-servicediscovery-service-seealso"></a>
+ [CreateService](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateService.html) in the *AWS Cloud Map API Reference*