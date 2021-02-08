# AWS::Batch::JobDefinition NetworkConfiguration<a name="aws-properties-batch-jobdefinition-containerproperties-networkconfiguration"></a>

The network configuration for jobs running on Fargate resources\. Jobs running on EC2 resources must not specify this parameter\.

## Syntax<a name="aws-properties-batch-jobdefinition-containerproperties-networkconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-batch-jobdefinition-containerproperties-networkconfiguration-syntax.json"></a>

```
{
  "[AssignPublicIp](#cfn-batch-jobdefinition-containerproperties-networkconfiguration-assignpublicip)" : String
}
```

### YAML<a name="aws-properties-batch-jobdefinition-containerproperties-networkconfiguration-syntax.yaml"></a>

```
  [AssignPublicIp](#cfn-batch-jobdefinition-containerproperties-networkconfiguration-assignpublicip): String
```

## Properties<a name="aws-properties-batch-jobdefinition-containerproperties-networkconfiguration-properties"></a>

`AssignPublicIp`  <a name="cfn-batch-jobdefinition-containerproperties-networkconfiguration-assignpublicip"></a>
Indicates whether the job should have a public IP address\. For a job running on Fargate resources in a private subnet to send outbound traffic to the internet \(for example, in order to pull container images\), the private subnet requires a NAT gateway be attached to route requests to the internet\. For more information, see [Amazon ECS task networking](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task-networking.html)\. The default value is "DISABLED"\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)