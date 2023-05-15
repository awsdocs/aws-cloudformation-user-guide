# AWS::Route53RecoveryReadiness::ResourceSet<a name="aws-resource-route53recoveryreadiness-resourceset"></a>

Creates a resource set in Amazon Route 53 Application Recovery Controller\. A resource set is a set of resources of one type, such as Network Load Balancers, that span multiple cells\. You can associate a resource set with a readiness check to have Route 53 ARC continually monitor the resources in the set for failover readiness\.

You typically create a resource set and a readiness check for each supported type of AWS resource in your application\.

For more information, see [Readiness checks, resource sets, and readiness scopes](https://docs.aws.amazon.com/r53recovery/latest/dg/recovery-readiness.recovery-groups.readiness-scope.html) in the Amazon Route 53 Application Recovery Controller Developer Guide\.

Route 53 ARC Readiness supports us\-east\-1 and us\-west\-2 AWS Regions only\.

## Syntax<a name="aws-resource-route53recoveryreadiness-resourceset-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53recoveryreadiness-resourceset-syntax.json"></a>

```
{
  "Type" : "AWS::Route53RecoveryReadiness::ResourceSet",
  "Properties" : {
      "[Resources](#cfn-route53recoveryreadiness-resourceset-resources)" : [ Resource, ... ],
      "[ResourceSetName](#cfn-route53recoveryreadiness-resourceset-resourcesetname)" : String,
      "[ResourceSetType](#cfn-route53recoveryreadiness-resourceset-resourcesettype)" : String,
      "[Tags](#cfn-route53recoveryreadiness-resourceset-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53recoveryreadiness-resourceset-syntax.yaml"></a>

```
Type: AWS::Route53RecoveryReadiness::ResourceSet
Properties: 
  [Resources](#cfn-route53recoveryreadiness-resourceset-resources): 
    - Resource
  [ResourceSetName](#cfn-route53recoveryreadiness-resourceset-resourcesetname): String
  [ResourceSetType](#cfn-route53recoveryreadiness-resourceset-resourcesettype): String
  [Tags](#cfn-route53recoveryreadiness-resourceset-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53recoveryreadiness-resourceset-properties"></a>

`Resources`  <a name="cfn-route53recoveryreadiness-resourceset-resources"></a>
A list of resource objects in the resource set\.  
*Required*: Yes  
*Type*: List of [Resource](aws-properties-route53recoveryreadiness-resourceset-resource.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceSetName`  <a name="cfn-route53recoveryreadiness-resourceset-resourcesetname"></a>
The name of the resource set to create\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceSetType`  <a name="cfn-route53recoveryreadiness-resourceset-resourcesettype"></a>
The resource type of the resources in the resource set\. Enter one of the following values for resource type:  
 AWS::ApiGateway::Stage, AWS::ApiGatewayV2::Stage, AWS::AutoScaling::AutoScalingGroup, AWS::CloudWatch::Alarm, AWS::EC2::CustomerGateway, AWS::DynamoDB::Table, AWS::EC2::Volume, AWS::ElasticLoadBalancing::LoadBalancer, AWS::ElasticLoadBalancingV2::LoadBalancer, AWS::Lambda::Function, AWS::MSK::Cluster, AWS::RDS::DBCluster, AWS::Route53::HealthCheck, AWS::SQS::Queue, AWS::SNS::Topic, AWS::SNS::Subscription, AWS::EC2::VPC, AWS::EC2::VPNConnection, AWS::EC2::VPNGateway, AWS::Route53RecoveryReadiness::DNSTargetResource\.   
Note that AWS::Route53RecoveryReadiness::DNSTargetResource is only used for this setting\. It isn't an actual AWS CloudFormation resource type\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-route53recoveryreadiness-resourceset-tags"></a>
A tag to associate with the parameters for a resource set\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-route53recoveryreadiness-resourceset-return-values"></a>

### Ref<a name="aws-resource-route53recoveryreadiness-resourceset-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the `ResourceSetName` object\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53recoveryreadiness-resourceset-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53recoveryreadiness-resourceset-return-values-fn--getatt-fn--getatt"></a>

`ResourceSetArn`  <a name="ResourceSetArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the resource set\. 