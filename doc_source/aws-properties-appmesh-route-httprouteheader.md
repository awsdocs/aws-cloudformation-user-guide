# AWS::AppMesh::Route HttpRouteHeader<a name="aws-properties-appmesh-route-httprouteheader"></a>

An object representing the HTTP header in the request\.

## Syntax<a name="aws-properties-appmesh-route-httprouteheader-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httprouteheader-syntax.json"></a>

```
{
  "[Invert](#cfn-appmesh-route-httprouteheader-invert)" : Boolean,
  "[Match](#cfn-appmesh-route-httprouteheader-match)" : [HeaderMatchMethod](aws-properties-appmesh-route-headermatchmethod.md),
  "[Name](#cfn-appmesh-route-httprouteheader-name)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-httprouteheader-syntax.yaml"></a>

```
  [Invert](#cfn-appmesh-route-httprouteheader-invert): Boolean
  [Match](#cfn-appmesh-route-httprouteheader-match): 
    [HeaderMatchMethod](aws-properties-appmesh-route-headermatchmethod.md)
  [Name](#cfn-appmesh-route-httprouteheader-name): String
```

## Properties<a name="aws-properties-appmesh-route-httprouteheader-properties"></a>

`Invert`  <a name="cfn-appmesh-route-httprouteheader-invert"></a>
Specify `True` to match the opposite of the `HeaderMatchMethod` method and value\. The default value is `False`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Match`  <a name="cfn-appmesh-route-httprouteheader-match"></a>
The `HeaderMatchMethod` object\.  
*Required*: No  
*Type*: [HeaderMatchMethod](aws-properties-appmesh-route-headermatchmethod.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-appmesh-route-httprouteheader-name"></a>
A name for the HTTP header in the client request that will be matched on\.  
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
