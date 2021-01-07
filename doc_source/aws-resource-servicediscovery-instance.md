# AWS::ServiceDiscovery::Instance<a name="aws-resource-servicediscovery-instance"></a>

A complex type that contains information about an instance that AWS Cloud Map creates when you submit a `RegisterInstance` request\.

## Syntax<a name="aws-resource-servicediscovery-instance-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-instance-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::Instance",
  "Properties" : {
      "[InstanceAttributes](#cfn-servicediscovery-instance-instanceattributes)" : Json,
      "[InstanceId](#cfn-servicediscovery-instance-instanceid)" : String,
      "[ServiceId](#cfn-servicediscovery-instance-serviceid)" : String
    }
}
```

### YAML<a name="aws-resource-servicediscovery-instance-syntax.yaml"></a>

```
Type: AWS::ServiceDiscovery::Instance
Properties: 
  [InstanceAttributes](#cfn-servicediscovery-instance-instanceattributes): Json
  [InstanceId](#cfn-servicediscovery-instance-instanceid): String
  [ServiceId](#cfn-servicediscovery-instance-serviceid): String
```

## Properties<a name="aws-resource-servicediscovery-instance-properties"></a>

`InstanceAttributes`  <a name="cfn-servicediscovery-instance-instanceattributes"></a>
A string map that contains the following information for the service that you specify in `ServiceId`:  
+ The attributes that apply to the records that are defined in the service\. 
+ For each attribute, the applicable value\.
Supported attribute keys include the following:  
**AWS\_ALIAS\_DNS\_NAME**  
If you want AWS Cloud Map to create a Route 53 alias record that routes traffic to an Elastic Load Balancing load balancer, specify the DNS name that is associated with the load balancer\. For information about how to get the DNS name, see "DNSName" in the topic [AliasTarget](https://docs.aws.amazon.com/Route53/latest/APIReference/API_AliasTarget.html)\.  
Note the following:  
+ The configuration for the service that is specified by `ServiceId` must include settings for an `A` record, an `AAAA` record, or both\.
+ In the service that is specified by `ServiceId`, the value of `RoutingPolicy` must be `WEIGHTED`\.
+ If the service that is specified by `ServiceId` includes `HealthCheckConfig` settings, AWS Cloud Map will create the health check, but it won't associate the health check with the alias record\.
+ Auto naming currently doesn't support creating alias records that route traffic to AWS resources other than ELB load balancers\.
+ If you specify a value for `AWS_ALIAS_DNS_NAME`, don't specify values for any of the `AWS_INSTANCE` attributes\.  
AWS\_EC2\_INSTANCE\_ID  
 *HTTP namespaces only\.* The Amazon EC2 instance ID for the instance\. When creating resources with a type of [AWS::ServiceDiscovery::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-instance.html), if the `AWS_EC2_INSTANCE_ID` attribute is specified, the only other attribute that can be specified is `AWS_INIT_HEALTH_STATUS`\. After the resource has been created, the `AWS_INSTANCE_IPV4` attribute contains the primary private IPv4 address\.  
AWS\_INIT\_HEALTH\_STATUS  
If the service configuration includes `HealthCheckCustomConfig`, when creating resources with a type of [AWS::ServiceDiscovery::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-instance.html) you can optionally use `AWS_INIT_HEALTH_STATUS` to specify the initial status of the custom health check, `HEALTHY` or `UNHEALTHY`\. If you don't specify a value for `AWS_INIT_HEALTH_STATUS`, the initial status is `HEALTHY`\. This attribute can only be used when creating resources and will not be seen on existing resources\.  
AWS\_INSTANCE\_CNAME  
If the service configuration includes a `CNAME` record, the domain name that you want Route 53 to return in response to DNS queries, for example, `example.com`\.  
This value is required if the service specified by `ServiceId` includes settings for an `CNAME` record\.  
AWS\_INSTANCE\_IPV4  
If the service configuration includes an `A` record, the IPv4 address that you want Route 53 to return in response to DNS queries, for example, `192.0.2.44`\.  
This value is required if the service specified by `ServiceId` includes settings for an `A` record\. If the service includes settings for an `SRV` record, you must specify a value for `AWS_INSTANCE_IPV4`, `AWS_INSTANCE_IPV6`, or both\.  
AWS\_INSTANCE\_IPV6  
If the service configuration includes an `AAAA` record, the IPv6 address that you want Route 53 to return in response to DNS queries, for example, `2001:0db8:85a3:0000:0000:abcd:0001:2345`\.  
This value is required if the service specified by `ServiceId` includes settings for an `AAAA` record\. If the service includes settings for an `SRV` record, you must specify a value for `AWS_INSTANCE_IPV4`, `AWS_INSTANCE_IPV6`, or both\.  
AWS\_INSTANCE\_PORT  
If the service includes an `SRV` record, the value that you want Route 53 to return for the port\.  
If the service includes `HealthCheckConfig`, the port on the endpoint that you want Route 53 to send requests to\.  
This value is required if you specified settings for an `SRV` record or a Route 53 health check when you created the service\.
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-servicediscovery-instance-instanceid"></a>
An identifier that you want to associate with the instance\. Note the following:  
+ If the service that is specified by `ServiceId` includes settings for an `SRV` record, the value of `InstanceId` is automatically included as part of the value for the `SRV` record\. For more information, see [DnsRecord > Type](https://docs.aws.amazon.com/cloud-map/latest/api/API_DnsRecord.html#cloudmap-Type-DnsRecord-Type)\.
+ You can use this value to update an existing instance\.
+ To register a new instance, you must specify a value that is unique among instances that you register by using the same service\. 
+ If you specify an existing `InstanceId` and `ServiceId`, AWS Cloud Map updates the existing DNS records\. If there's also an existing health check, AWS Cloud Map deletes the old health check and creates a new one\. 
**Note**  
The health check isn't deleted immediately, so it will still appear for a while if you submit a `ListHealthChecks` request, for example\.
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceId`  <a name="cfn-servicediscovery-instance-serviceid"></a>
The ID of the service that you want to use for settings for the instance\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicediscovery-instance-return-values"></a>

### Ref<a name="aws-resource-servicediscovery-instance-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the value of `Id` for the instance, such as `i-abcd1234`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-servicediscovery-instance--examples"></a>



### Provide IP addresses for an instance<a name="aws-resource-servicediscovery-instance--examples--Provide_IP_addresses_for_an_instance"></a>

The following example provides IPv4 and IPV6 IP addresses for the instance that has an ID of `i-abcd1234`\. The instance was registered using the service that has an ID of `srv-e4anhexample0004`\.

#### JSON<a name="aws-resource-servicediscovery-instance--examples--Provide_IP_addresses_for_an_instance--json"></a>

```
{
    "Type": "AWS::ServiceDiscovery::Instance",
    "Properties": {
        "InstanceAttributes": {
            "AWS_INSTANCE_IPV4": "192.0.2.44",
            "AWS_INSTANCE_IPV6": "2001:0db8:85a3:0000:0000:abcd:0001:2345"
        },
        "InstanceId": "i-abcd1234",
        "ServiceId": "srv-e4anhexample0004"
    }
}
```

#### YAML<a name="aws-resource-servicediscovery-instance--examples--Provide_IP_addresses_for_an_instance--yaml"></a>

```
Type: AWS::ServiceDiscovery::Instance
Properties:
  InstanceAttributes:
    AWS_INSTANCE_IPV4: 192.0.2.44
    AWS_INSTANCE_IPV6: 2001:0db8:85a3:0000:0000:abcd:0001:2345
  InstanceId: i-abcd1234
  ServiceId: srv-e4anhexample0004
```

## See also<a name="aws-resource-servicediscovery-instance--seealso"></a>
+  [RegisterInstance](https://docs.aws.amazon.com/cloud-map/latest/api/API_RegisterInstance.html) in the *AWS Cloud Map API Reference* 

