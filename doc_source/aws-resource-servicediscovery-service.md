# AWS::ServiceDiscovery::Service<a name="aws-resource-servicediscovery-service"></a>

The `AWS::ServiceDiscovery::Service` resource defines a template for up to five records and an optional health check that you want Amazon Route 53 to create when you register an instance\. For more information, see [CreateService](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreateService.html) in the *Amazon Route 53 API Reference*\.

**Topics**
+ [Syntax](#aws-resource-servicediscovery-service-syntax)
+ [Properties](#aws-resource-servicediscovery-service-properties)
+ [Return Values](#aws-resource-servicediscovery-service-returnvalues)
+ [See Also](#aws-resource-servicediscovery-service-seealso)

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
    "[Name](#cfn-servicediscovery-service-name)" : String
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
  [Name](#cfn-servicediscovery-service-name): String
```

## Properties<a name="aws-resource-servicediscovery-service-properties"></a>

`Description`  <a name="cfn-servicediscovery-service-description"></a>
A description for the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DnsConfig`  <a name="cfn-servicediscovery-service-dnsconfig"></a>
A complex type that contains information about the resource record sets that you want Route 53 to create when you register an instance\.   
*Required*: Yes  
*Type*: [Amazon Route 53 ServiceDiscovery DnsConfig](aws-properties-servicediscovery-service-dnsconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`HealthCheckConfig`  <a name="cfn-servicediscovery-service-healthcheckconfig"></a>
A complex type that contains settings for an optional health check\. If you specify settings for a health check, Route 53 associates the health check with all the resource record sets that you specify in `DnsConfig`\.  
*Required*: No  
*Type*: [Amazon Route 53 ServiceDiscovery HealthCheckConfig](aws-properties-servicediscovery-service-healthcheckconfig.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Name`  <a name="cfn-servicediscovery-service-name"></a>
The name that you want to assign to the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicediscovery-service-returnvalues"></a>

### Ref<a name="aws-resource-servicediscovery-service-ref"></a>

When you pass the logical ID of an `AWS::ServiceDiscovery::Service` resource to the intrinsic `Ref` function, the function returns the value of `Id` for the service\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-servicediscovery-service-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Id`  
The ID of the service\.

`Arn`  
The Amazon Resource Name \(ARN\) of the service\.

`Name`  
The name that you assigned to the service\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## See Also<a name="aws-resource-servicediscovery-service-seealso"></a>
+ [Using Autonaming for Service Discovery](http://docs.aws.amazon.com/Route53/latest/APIReference/overview-service-discovery.html) in the *Amazon Route 53 API Reference*
+ [CreateService](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreateService.html) in the *Amazon Route 53 API Reference*