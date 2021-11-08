# AWS::Redshift::ScheduledAction PauseClusterMessage<a name="aws-properties-redshift-scheduledaction-pauseclustermessage"></a>

Describes a pause cluster operation\. For example, a scheduled action to run the `PauseCluster` API operation\. 

## Syntax<a name="aws-properties-redshift-scheduledaction-pauseclustermessage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshift-scheduledaction-pauseclustermessage-syntax.json"></a>

```
{
  "[ClusterIdentifier](#cfn-redshift-scheduledaction-pauseclustermessage-clusteridentifier)" : String
}
```

### YAML<a name="aws-properties-redshift-scheduledaction-pauseclustermessage-syntax.yaml"></a>

```
  [ClusterIdentifier](#cfn-redshift-scheduledaction-pauseclustermessage-clusteridentifier): String
```

## Properties<a name="aws-properties-redshift-scheduledaction-pauseclustermessage-properties"></a>

`ClusterIdentifier`  <a name="cfn-redshift-scheduledaction-pauseclustermessage-clusteridentifier"></a>
The identifier of the cluster to be paused\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)