# AWS::Route53::HealthCheck<a name="aws-resource-route53-healthcheck"></a>

The `AWS::Route53::HealthCheck` resource is a Route 53 resource type that contains settings for a Route 53 health check\.

For information about associating health checks with records, see [HealthCheckId](https://docs.aws.amazon.com/Route53/latest/APIReference/API_ResourceRecordSet.html#Route53-Type-ResourceRecordSet-HealthCheckId) in [ChangeResourceRecordSets](https://docs.aws.amazon.com/Route53/latest/APIReference/API_ChangeResourceRecordSets.html)\. 

**ELB Load Balancers**

If you're registering EC2 instances with an Elastic Load Balancing \(ELB\) load balancer, do not create Amazon Route 53 health checks for the EC2 instances\. When you register an EC2 instance with a load balancer, you configure settings for an ELB health check, which performs a similar function to a Route 53 health check\.

**Private Hosted Zones**

You can associate health checks with failover records in a private hosted zone\. Note the following:
+ Route 53 health checkers are outside the VPC\. To check the health of an endpoint within a VPC by IP address, you must assign a public IP address to the instance in the VPC\.
+ You can configure a health checker to check the health of an external resource that the instance relies on, such as a database server\.
+ You can create a CloudWatch metric, associate an alarm with the metric, and then create a health check that is based on the state of the alarm\. For example, you might create a CloudWatch metric that checks the status of the Amazon EC2 `StatusCheckFailed` metric, add an alarm to the metric, and then create a health check that is based on the state of the alarm\. For information about creating CloudWatch metrics and alarms by using the CloudWatch console, see the [Amazon CloudWatch User Guide](https://docs.aws.amazon.com/AmazonCloudWatch/latest/DeveloperGuide/WhatIsCloudWatch.html)\.

## Syntax<a name="aws-resource-route53-healthcheck-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53-healthcheck-syntax.json"></a>

```
{
  "Type" : "AWS::Route53::HealthCheck",
  "Properties" : {
      "[HealthCheckConfig](#cfn-route53-healthcheck-healthcheckconfig)" : Json,
      "[HealthCheckTags](#cfn-route53-healthcheck-healthchecktags)" : [ HealthCheckTag, ... ]
    }
}
```

### YAML<a name="aws-resource-route53-healthcheck-syntax.yaml"></a>

```
Type: AWS::Route53::HealthCheck
Properties: 
  [HealthCheckConfig](#cfn-route53-healthcheck-healthcheckconfig): Json
  [HealthCheckTags](#cfn-route53-healthcheck-healthchecktags): 
    - HealthCheckTag
```

## Properties<a name="aws-resource-route53-healthcheck-properties"></a>

`HealthCheckConfig`  <a name="cfn-route53-healthcheck-healthcheckconfig"></a>
A complex type that contains detailed information about one health check\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckTags`  <a name="cfn-route53-healthcheck-healthchecktags"></a>
The `HealthCheckTags` property describes key\-value pairs that are associated with an `AWS::Route53::HealthCheck` resource\.   
*Required*: No  
*Type*: List of [HealthCheckTag](aws-properties-route53-healthcheck-healthchecktag.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53-healthcheck-return-values"></a>

### Ref<a name="aws-resource-route53-healthcheck-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the health check ID, such as `e0a123b4-4dba-4650-935e-example`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53-healthcheck-return-values-fn--getatt"></a>

#### <a name="aws-resource-route53-healthcheck-return-values-fn--getatt-fn--getatt"></a>

`HealthCheckId`  <a name="HealthCheckId-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

## Examples<a name="aws-resource-route53-healthcheck--examples"></a>



### Create health check<a name="aws-resource-route53-healthcheck--examples--Create_health_check"></a>

The following example creates an Amazon Route 53 health check that sends HTTP requests to the specified endpoint\.

#### JSON<a name="aws-resource-route53-healthcheck--examples--Create_health_check--json"></a>

```
{
   "myHealthCheck": {
      "Type": "AWS::Route53::HealthCheck",
      "Properties": {
         "HealthCheckConfig": {
            "IPAddress": "192.0.2.44",
            "Port": "80",
            "Type": "HTTP",
            "ResourcePath": "/example/index.html",
            "FullyQualifiedDomainName": "example.com",
            "RequestInterval": "30",
            "FailureThreshold": "3"
         },
         "HealthCheckTags": [
            {
               "Key": "SampleKey1",
               "Value": "SampleValue1"
            },
            {
               "Key": "SampleKey2",
               "Value": "SampleValue2"
            }
         ]
      }
   }
}
```

#### YAML<a name="aws-resource-route53-healthcheck--examples--Create_health_check--yaml"></a>

```
myHealthCheck: 
  Type: 'AWS::Route53::HealthCheck'
  Properties: 
    HealthCheckConfig: 
      IPAddress: 192.0.2.44
      Port: 80
      Type: HTTP
      ResourcePath: '/example/index.html'
      FullyQualifiedDomainName: example.com
      RequestInterval: 30
      FailureThreshold: 3
    HealthCheckTags: 
      - 
        Key: SampleKey1
        Value: SampleValue1
      - 
        Key: SampleKey2
        Value: SampleValue2
```

## See also<a name="aws-resource-route53-healthcheck--seealso"></a>
+  [CreateHealthCheck](https://docs.aws.amazon.com/Route53/latest/APIReference/API_CreateHealthCheck.html) in the *Amazon Route 53 API Reference*

