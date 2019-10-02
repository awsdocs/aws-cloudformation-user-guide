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
