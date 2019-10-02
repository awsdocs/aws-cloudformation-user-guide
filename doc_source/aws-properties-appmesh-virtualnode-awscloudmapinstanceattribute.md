# AWS::AppMesh::VirtualNode AwsCloudMapInstanceAttribute<a name="aws-properties-appmesh-virtualnode-awscloudmapinstanceattribute"></a>

An object representing the AWS Cloud Map attribute information for your virtual node\.

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

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-northeast-2`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `ca-central-1`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-1`
- `us-west-2`
