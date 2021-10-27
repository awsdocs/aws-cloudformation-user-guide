# AWS::ECR::ReplicationConfiguration ReplicationDestination<a name="aws-properties-ecr-replicationconfiguration-replicationdestination"></a>

An array of objects representing the destination for a replication rule\.

## Syntax<a name="aws-properties-ecr-replicationconfiguration-replicationdestination-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ecr-replicationconfiguration-replicationdestination-syntax.json"></a>

```
{
  "[Region](#cfn-ecr-replicationconfiguration-replicationdestination-region)" : String,
  "[RegistryId](#cfn-ecr-replicationconfiguration-replicationdestination-registryid)" : String
}
```

### YAML<a name="aws-properties-ecr-replicationconfiguration-replicationdestination-syntax.yaml"></a>

```
  [Region](#cfn-ecr-replicationconfiguration-replicationdestination-region): String
  [RegistryId](#cfn-ecr-replicationconfiguration-replicationdestination-registryid): String
```

## Properties<a name="aws-properties-ecr-replicationconfiguration-replicationdestination-properties"></a>

`Region`  <a name="cfn-ecr-replicationconfiguration-replicationdestination-region"></a>
The Region to replicate to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `25`  
*Pattern*: `[0-9a-z-]{2,25}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistryId`  <a name="cfn-ecr-replicationconfiguration-replicationdestination-registryid"></a>
The AWS account ID of the Amazon ECR private registry to replicate to\. When configuring cross\-Region replication within your own registry, specify your own account ID\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[0-9]{12}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)