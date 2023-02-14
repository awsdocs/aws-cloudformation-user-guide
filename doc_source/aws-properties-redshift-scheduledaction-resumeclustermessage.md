# AWS::Redshift::ScheduledAction ResumeClusterMessage<a name="aws-properties-redshift-scheduledaction-resumeclustermessage"></a>

Describes a resume cluster operation\. For example, a scheduled action to run the `ResumeCluster` API operation\. 

## Syntax<a name="aws-properties-redshift-scheduledaction-resumeclustermessage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-redshift-scheduledaction-resumeclustermessage-syntax.json"></a>

```
{
  "[ClusterIdentifier](#cfn-redshift-scheduledaction-resumeclustermessage-clusteridentifier)" : String
}
```

### YAML<a name="aws-properties-redshift-scheduledaction-resumeclustermessage-syntax.yaml"></a>

```
  [ClusterIdentifier](#cfn-redshift-scheduledaction-resumeclustermessage-clusteridentifier): String
```

## Properties<a name="aws-properties-redshift-scheduledaction-resumeclustermessage-properties"></a>

`ClusterIdentifier`  <a name="cfn-redshift-scheduledaction-resumeclustermessage-clusteridentifier"></a>
The identifier of the cluster to be resumed\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)