# AWS::EMR::Cluster AutoTerminationPolicy<a name="aws-properties-elasticmapreduce-cluster-autoterminationpolicy"></a>

An auto\-termination policy for an Amazon EMR cluster\. An auto\-termination policy defines the amount of idle time in seconds after which a cluster automatically terminates\. For alternative cluster termination options, see [Control cluster termination](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-plan-termination.html)\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-autoterminationpolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-autoterminationpolicy-syntax.json"></a>

```
{
  "[IdleTimeout](#cfn-elasticmapreduce-cluster-autoterminationpolicy-idletimeout)" : Long
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-autoterminationpolicy-syntax.yaml"></a>

```
  [IdleTimeout](#cfn-elasticmapreduce-cluster-autoterminationpolicy-idletimeout): Long
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-autoterminationpolicy-properties"></a>

`IdleTimeout`  <a name="cfn-elasticmapreduce-cluster-autoterminationpolicy-idletimeout"></a>
Specifies the amount of idle time in seconds after which the cluster automatically terminates\. You can specify a minimum of 60 seconds and a maximum of 604800 seconds \(seven days\)\.  
*Required*: No  
*Type*: Long  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)