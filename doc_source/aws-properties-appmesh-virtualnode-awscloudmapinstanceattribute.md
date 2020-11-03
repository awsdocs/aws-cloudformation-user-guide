# AWS::AppMesh::VirtualNode AwsCloudMapInstanceAttribute<a name="aws-properties-appmesh-virtualnode-awscloudmapinstanceattribute"></a>

An object that represents the AWS Cloud Map attribute information for your virtual node\.

**Note**  
AWS Cloud Map is not available in the eu\-south\-1 Region\.

## Syntax<a name="aws-properties-appmesh-virtualnode-awscloudmapinstanceattribute-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-awscloudmapinstanceattribute-syntax.json"></a>

```
{
  "[Key](#cfn-appmesh-virtualnode-awscloudmapinstanceattribute-key)" : String,
  "[Value](#cfn-appmesh-virtualnode-awscloudmapinstanceattribute-value)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-awscloudmapinstanceattribute-syntax.yaml"></a>

```
  [Key](#cfn-appmesh-virtualnode-awscloudmapinstanceattribute-key): String
  [Value](#cfn-appmesh-virtualnode-awscloudmapinstanceattribute-value): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-awscloudmapinstanceattribute-properties"></a>

`Key`  <a name="cfn-appmesh-virtualnode-awscloudmapinstanceattribute-key"></a>
The name of an AWS Cloud Map service instance attribute key\. Any AWS Cloud Map service instance that contains the specified key and value is returned\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appmesh-virtualnode-awscloudmapinstanceattribute-value"></a>
The value of an AWS Cloud Map service instance attribute key\. Any AWS Cloud Map service instance that contains the specified key and value is returned\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)