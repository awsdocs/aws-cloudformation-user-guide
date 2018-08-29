# AWS::ServiceDiscovery::Instance<a name="aws-resource-servicediscovery-instance"></a>

The `AWS::ServiceDiscovery::Instance` resource specifies information about an instance that Amazon Route 53 creates\. For more information, see [Instance](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_Instance.html) in the *Amazon Route 53 API Reference*\.

**Topics**
+ [Syntax](#aws-resource-servicediscovery-instance-syntax)
+ [Properties](#aws-resource-servicediscovery-instance-properties)
+ [Return Values](#aws-resource-servicediscovery-instance-returnvalues)
+ [See Also](#aws-resource-servicediscovery-instance-seealso)

## Syntax<a name="aws-resource-servicediscovery-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-instance-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::Instance",
  "Properties" : {
    "[InstanceAttributes](#cfn-servicediscovery-instance-instanceattributes)" : JSON object,
    "[InstanceId](#cfn-servicediscovery-instance-instanceid)" : String,
    "[ServiceId](#cfn-servicediscovery-instance-serviceid)" : String
  }
}
```

### YAML<a name="aws-resource-servicediscovery-instance-syntax.yaml"></a>

```
Type: "AWS::ServiceDiscovery::Instance"
Properties:
  [InstanceAttributes](#cfn-servicediscovery-instance-instanceattributes): JSON object
  [InstanceId](#cfn-servicediscovery-instance-instanceid): String
  [ServiceId](#cfn-servicediscovery-instance-serviceid): String
```

## Properties<a name="aws-resource-servicediscovery-instance-properties"></a>

`InstanceAttributes`  <a name="cfn-servicediscovery-instance-instanceattributes"></a>
A string map that contains attribute keys and values\. Supported attribute keys include the following:  
+ `AWS_INSTANCE_PORT`: The port on the endpoint that you want Route 53 to perform health checks on\. This value is also used for the port value in an SRV record if the service that you specify includes an SRV record\. You can also specify a default port that is applied to all instances in the `Service` configuration\. For more information, see [CreateService](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreateService.html) in the *Amazon Route 53 API Reference*\.
+ `AWS_INSTANCE_IPV4`: If the service that you specify contains a resource record set template for an A record, the IPv4 address that you want Route 53 to use for the value of the A record\.
+ `AWS_INSTANCE_IPV6`: If the service that you specify contains a resource record set template for an AAAA record, the IPv6 address that you want Route 53 to use for the value of the AAAA record\.
*Required*: Yes  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceId`  <a name="cfn-servicediscovery-instance-instanceid"></a>
An identifier that you want to associate with the instance\. Note the following:  
+ You can use this value to update an existing instance\.
+ To associate a new instance, you must specify a value that is unique among instances that you associate by using the same service\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`ServiceId`  <a name="cfn-servicediscovery-instance-serviceid"></a>
The ID of the service that you want to use for settings for the resource record sets and health check that Route 53 will create\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicediscovery-instance-returnvalues"></a>

### Ref<a name="aws-resource-servicediscovery-instance-ref"></a>

When you pass the logical ID of an `AWS::ServiceDiscovery::Instance` resource to the intrinsic `Ref` function, the function returns the value of `Id` for the instance\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## See Also<a name="aws-resource-servicediscovery-instance-seealso"></a>
+ [Using Autonaming for Service Discovery](http://docs.aws.amazon.com/Route53/latest/APIReference/overview-service-discovery.html) in the *Amazon Route 53 API Reference*
+ [RegisterInstance](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_RegisterInstance.html) in the *Amazon Route 53 API Reference*
+ [CreateService](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreateService.html) in the *Amazon Route 53 API Reference*