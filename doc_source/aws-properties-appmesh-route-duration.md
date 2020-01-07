# AWS::AppMesh::Route Duration<a name="aws-properties-appmesh-route-duration"></a>

An object representing the duration between retry attempts\.

## Syntax<a name="aws-properties-appmesh-route-duration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-duration-syntax.json"></a>

```
{
  "[Unit](#cfn-appmesh-route-duration-unit)" : String,
  "[Value](#cfn-appmesh-route-duration-value)" : Integer
}
```

### YAML<a name="aws-properties-appmesh-route-duration-syntax.yaml"></a>

```
  [Unit](#cfn-appmesh-route-duration-unit): String
  [Value](#cfn-appmesh-route-duration-value): Integer
```

## Properties<a name="aws-properties-appmesh-route-duration-properties"></a>

`Unit`  <a name="cfn-appmesh-route-duration-unit"></a>
The unit of time between retry attempts\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appmesh-route-duration-value"></a>
The duration of time between retry attempts\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)