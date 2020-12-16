# AWS::ServiceDiscovery::Service<a name="aws-resource-servicediscovery-service"></a>

A complex type that contains information about a service, which defines the configuration of the following entities:
+ For public and private DNS namespaces, one of the following combinations of DNS records in Amazon Route 53:
  + A
  + AAAA
  + A and AAAA
  + SRV
  + CNAME
+ Optionally, a health check

## Syntax<a name="aws-resource-servicediscovery-service-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-service-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::Service",
  "Properties" : {
      "[Description](#cfn-servicediscovery-service-description)" : String,
      "[DnsConfig](#cfn-servicediscovery-service-dnsconfig)" : DnsConfig,
      "[HealthCheckConfig](#cfn-servicediscovery-service-healthcheckconfig)" : HealthCheckConfig,
      "[HealthCheckCustomConfig](#cfn-servicediscovery-service-healthcheckcustomconfig)" : HealthCheckCustomConfig,
      "[Name](#cfn-servicediscovery-service-name)" : String,
      "[NamespaceId](#cfn-servicediscovery-service-namespaceid)" : String,
      "[Tags](#cfn-servicediscovery-service-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-servicediscovery-service-syntax.yaml"></a>

```
Type: AWS::ServiceDiscovery::Service
Properties: 
  [Description](#cfn-servicediscovery-service-description): String
  [DnsConfig](#cfn-servicediscovery-service-dnsconfig): 
    DnsConfig
  [HealthCheckConfig](#cfn-servicediscovery-service-healthcheckconfig): 
    HealthCheckConfig
  [HealthCheckCustomConfig](#cfn-servicediscovery-service-healthcheckcustomconfig): 
    HealthCheckCustomConfig
  [Name](#cfn-servicediscovery-service-name): String
  [NamespaceId](#cfn-servicediscovery-service-namespaceid): String
  [Tags](#cfn-servicediscovery-service-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-servicediscovery-service-properties"></a>

`Description`  <a name="cfn-servicediscovery-service-description"></a>
The description of the service\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DnsConfig`  <a name="cfn-servicediscovery-service-dnsconfig"></a>
A complex type that contains information about the Route 53 DNS records that you want AWS Cloud Map to create when you register an instance\.  
*Required*: No  
*Type*: [DnsConfig](aws-properties-servicediscovery-service-dnsconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckConfig`  <a name="cfn-servicediscovery-service-healthcheckconfig"></a>
 *Public DNS and HTTP namespaces only\.* A complex type that contains settings for an optional health check\. If you specify settings for a health check, AWS Cloud Map associates the health check with the records that you specify in `DnsConfig`\.  
For information about the charges for health checks, see [Amazon Route 53 Pricing](http://aws.amazon.com/route53/pricing/)\.  
*Required*: No  
*Type*: [HealthCheckConfig](aws-properties-servicediscovery-service-healthcheckconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckCustomConfig`  <a name="cfn-servicediscovery-service-healthcheckcustomconfig"></a>
A complex type that contains information about an optional custom health check\.  
If you specify a health check configuration, you can specify either `HealthCheckCustomConfig` or `HealthCheckConfig` but not both\.
*Required*: No  
*Type*: [HealthCheckCustomConfig](aws-properties-servicediscovery-service-healthcheckcustomconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-servicediscovery-service-name"></a>
The name of the service\.  
*Required*: No  
*Type*: String  
*Pattern*: `((?=^.{1,127}$)^([a-zA-Z0-9_][a-zA-Z0-9-_]{0,61}[a-zA-Z0-9_]|[a-zA-Z0-9])(\.([a-zA-Z0-9_][a-zA-Z0-9-_]{0,61}[a-zA-Z0-9_]|[a-zA-Z0-9]))*$)|(^\.$)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NamespaceId`  <a name="cfn-servicediscovery-service-namespaceid"></a>
The ID of the namespace that was used to create the service\.  
You must specify a value for `NamespaceId` either for the service properties or for [DnsConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-servicediscovery-service-dnsconfig.html)\. Don't specify a value in both places\. 
*Required*: No  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-servicediscovery-service-tags"></a>
The tags for the service\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: Updates are not supported\.

## Return values<a name="aws-resource-servicediscovery-service-return-values"></a>

### Ref<a name="aws-resource-servicediscovery-service-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the value of `Id` for the service, such as `srv-e4anhexample0004`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicediscovery-service-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicediscovery-service-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the service\.

`Name`  <a name="Name-fn::getatt"></a>
The name that you assigned to the service\.

## Examples<a name="aws-resource-servicediscovery-service--examples"></a>



### Create a service<a name="aws-resource-servicediscovery-service--examples--Create_a_service"></a>

The following example creates a service based on a public DNS namespace\. The service includes settings for Amazon Route 53 A and AAAA records that have a routing policy of `WEIGHTED`\. It also includes a Route 53 health check\.

#### JSON<a name="aws-resource-servicediscovery-service--examples--Create_a_service--json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::Service",
  "Properties" : {
    "Description" : "Service based on a public DNS namespace",
    "DnsConfig" : {
      "DnsRecords" : [
        {
          "Type" : "A",
          "TTL" : 60
        },
        {
          "Type" : "AAAA",
          "TTL" : 60
        }
      ],
      "RoutingPolicy" : "WEIGHTED"
    },
    "HealthCheckConfig" : {
      "FailureThreshold" : 3,
      "ResourcePath" : "/",
      "Type" : "HTTPS"
    },
    "Name" : "example-public-DNS-service",
    "NamespaceId" : "ns-e4anhexample0004"
  }
}
```

#### YAML<a name="aws-resource-servicediscovery-service--examples--Create_a_service--yaml"></a>

```
Type: 'AWS::ServiceDiscovery::Service'
Properties:
  Description: Service based on a public DNS namespace
  DnsConfig:
    DnsRecords:
      - Type: A
        TTL: 60
      - Type: AAAA
        TTL: 60
    RoutingPolicy: WEIGHTED
  HealthCheckConfig:
    FailureThreshold: 3
    ResourcePath: /
    Type: HTTPS
  Name: example-public-DNS-service
  NamespaceId: ns-e4anhexample0004
```

## See also<a name="aws-resource-servicediscovery-service--seealso"></a>
+  [CreateService](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateService.html) in the *AWS Cloud Map API Reference* 

