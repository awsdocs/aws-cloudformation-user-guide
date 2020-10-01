# AWS::AppMesh::VirtualNode Duration<a name="aws-properties-appmesh-virtualnode-duration"></a>

An object that represents a duration of time\.

## Syntax<a name="aws-properties-appmesh-virtualnode-duration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-duration-syntax.json"></a>

```
{
  "[Unit](#cfn-appmesh-virtualnode-duration-unit)" : String,
  "[Value](#cfn-appmesh-virtualnode-duration-value)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-duration-syntax.yaml"></a>

```
  [Unit](#cfn-appmesh-virtualnode-duration-unit): String
  [Value](#cfn-appmesh-virtualnode-duration-value): Integer
```

## Properties<a name="aws-properties-appmesh-virtualnode-duration-properties"></a>

`Unit`  <a name="cfn-appmesh-virtualnode-duration-unit"></a>
A unit of time\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appmesh-virtualnode-duration-value"></a>
A number of time units\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)