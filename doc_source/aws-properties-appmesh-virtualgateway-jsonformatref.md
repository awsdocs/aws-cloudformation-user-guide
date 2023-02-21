# AWS::AppMesh::VirtualGateway JsonFormatRef<a name="aws-properties-appmesh-virtualgateway-jsonformatref"></a>

An object that represents the key value pairs for the JSON\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-jsonformatref-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-jsonformatref-syntax.json"></a>

```
{
  "[Key](#cfn-appmesh-virtualgateway-jsonformatref-key)" : String,
  "[Value](#cfn-appmesh-virtualgateway-jsonformatref-value)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-jsonformatref-syntax.yaml"></a>

```
  [Key](#cfn-appmesh-virtualgateway-jsonformatref-key): String
  [Value](#cfn-appmesh-virtualgateway-jsonformatref-value): String
```

## Properties<a name="aws-properties-appmesh-virtualgateway-jsonformatref-properties"></a>

`Key`  <a name="cfn-appmesh-virtualgateway-jsonformatref-key"></a>
The specified key for the JSON\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-appmesh-virtualgateway-jsonformatref-value"></a>
The specified value for the JSON\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)