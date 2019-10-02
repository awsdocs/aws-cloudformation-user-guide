# AWS::AppMesh::Route HeaderMatchMethod<a name="aws-properties-appmesh-route-headermatchmethod"></a>

An object representing the method and value to match the header value sent with a request\. Specify one match method\.

## Syntax<a name="aws-properties-appmesh-route-headermatchmethod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-headermatchmethod-syntax.json"></a>

```
{
  "[Exact](#cfn-appmesh-route-headermatchmethod-exact)" : String,
  "[Prefix](#cfn-appmesh-route-headermatchmethod-prefix)" : String,
  "[Range](#cfn-appmesh-route-headermatchmethod-range)" : [MatchRange](aws-properties-appmesh-route-matchrange.md),
  "[Regex](#cfn-appmesh-route-headermatchmethod-regex)" : String,
  "[Suffix](#cfn-appmesh-route-headermatchmethod-suffix)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-headermatchmethod-syntax.yaml"></a>

```
  [Exact](#cfn-appmesh-route-headermatchmethod-exact): String
  [Prefix](#cfn-appmesh-route-headermatchmethod-prefix): String
  [Range](#cfn-appmesh-route-headermatchmethod-range): 
    [MatchRange](aws-properties-appmesh-route-matchrange.md)
  [Regex](#cfn-appmesh-route-headermatchmethod-regex): String
  [Suffix](#cfn-appmesh-route-headermatchmethod-suffix): String
```

## Properties<a name="aws-properties-appmesh-route-headermatchmethod-properties"></a>

`Exact`  <a name="cfn-appmesh-route-headermatchmethod-exact"></a>
The header value sent by the client must match the specified value exactly\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-appmesh-route-headermatchmethod-prefix"></a>
The header value sent by the client must begin with the specified characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Range`  <a name="cfn-appmesh-route-headermatchmethod-range"></a>
The object that specifies the range of numbers that the header value sent by the client must be included in\.  
*Required*: No  
*Type*: [MatchRange](aws-properties-appmesh-route-matchrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regex`  <a name="cfn-appmesh-route-headermatchmethod-regex"></a>
The header value sent by the client must include the specified characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-appmesh-route-headermatchmethod-suffix"></a>
The header value sent by the client must end with the specified characters\.  
*Required*: No  
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
