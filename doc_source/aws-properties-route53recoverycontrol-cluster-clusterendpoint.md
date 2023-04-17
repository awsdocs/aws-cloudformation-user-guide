# AWS::Route53RecoveryControl::Cluster ClusterEndpoint<a name="aws-properties-route53recoverycontrol-cluster-clusterendpoint"></a>

A cluster endpoint\. You specify one of the five cluster endpoints, which consists of an endpoint URL and an AWS Region, when you want to get or update a routing control state in the cluster\. 

For more information, see [Code examples](https://docs.aws.amazon.com/r53recovery/latest/dg/service_code_examples.html) in the Amazon Route 53 Application Recovery Controller Developer Guide\.

## Syntax<a name="aws-properties-route53recoverycontrol-cluster-clusterendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-route53recoverycontrol-cluster-clusterendpoint-syntax.json"></a>

```
{
  "[Endpoint](#cfn-route53recoverycontrol-cluster-clusterendpoint-endpoint)" : String,
  "[Region](#cfn-route53recoverycontrol-cluster-clusterendpoint-region)" : String
}
```

### YAML<a name="aws-properties-route53recoverycontrol-cluster-clusterendpoint-syntax.yaml"></a>

```
  [Endpoint](#cfn-route53recoverycontrol-cluster-clusterendpoint-endpoint): String
  [Region](#cfn-route53recoverycontrol-cluster-clusterendpoint-region): String
```

## Properties<a name="aws-properties-route53recoverycontrol-cluster-clusterendpoint-properties"></a>

`Endpoint`  <a name="cfn-route53recoverycontrol-cluster-clusterendpoint-endpoint"></a>
A cluster endpoint URL for one of the five redundant clusters that you specify to set or retrieve a routing control state\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-route53recoverycontrol-cluster-clusterendpoint-region"></a>
The AWS Region for a cluster endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)