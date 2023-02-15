# AWS::Route53RecoveryControl::Cluster ClusterEndpoint<a name="aws-properties-route53recoverycontrol-cluster-clusterendpoint"></a>

A cluster endpoint\. Specify an endpoint when you want to set or retrieve a routing control state in the cluster\.

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
A cluster endpoint\. Specify an endpoint and AWS Region when you want to set or retrieve a routing control state in the cluster\.  
To get or update the routing control state, see the Amazon Route 53 Application Recovery Controller Routing Control Actions\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Region`  <a name="cfn-route53recoverycontrol-cluster-clusterendpoint-region"></a>
The AWS Region for a cluster endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)