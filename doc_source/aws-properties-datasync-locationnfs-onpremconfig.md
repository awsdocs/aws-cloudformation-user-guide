# AWS::DataSync::LocationNFS OnPremConfig<a name="aws-properties-datasync-locationnfs-onpremconfig"></a>

The AWS DataSync agents that are connecting to a Network File System \(NFS\) location\.

## Syntax<a name="aws-properties-datasync-locationnfs-onpremconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationnfs-onpremconfig-syntax.json"></a>

```
{
  "[AgentArns](#cfn-datasync-locationnfs-onpremconfig-agentarns)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-datasync-locationnfs-onpremconfig-syntax.yaml"></a>

```
  [AgentArns](#cfn-datasync-locationnfs-onpremconfig-agentarns): 
    - String
```

## Properties<a name="aws-properties-datasync-locationnfs-onpremconfig-properties"></a>

`AgentArns`  <a name="cfn-datasync-locationnfs-onpremconfig-agentarns"></a>
The Amazon Resource Names \(ARNs\) of the agents connecting to a transfer location\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)