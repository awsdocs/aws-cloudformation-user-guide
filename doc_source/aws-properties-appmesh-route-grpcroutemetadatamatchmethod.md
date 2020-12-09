# AWS::AppMesh::Route GrpcRouteMetadataMatchMethod<a name="aws-properties-appmesh-route-grpcroutemetadatamatchmethod"></a>

An object that represents the match method\. Specify one of the match values\.

## Syntax<a name="aws-properties-appmesh-route-grpcroutemetadatamatchmethod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-grpcroutemetadatamatchmethod-syntax.json"></a>

```
{
  "[Exact](#cfn-appmesh-route-grpcroutemetadatamatchmethod-exact)" : String,
  "[Prefix](#cfn-appmesh-route-grpcroutemetadatamatchmethod-prefix)" : String,
  "[Range](#cfn-appmesh-route-grpcroutemetadatamatchmethod-range)" : MatchRange,
  "[Regex](#cfn-appmesh-route-grpcroutemetadatamatchmethod-regex)" : String,
  "[Suffix](#cfn-appmesh-route-grpcroutemetadatamatchmethod-suffix)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-grpcroutemetadatamatchmethod-syntax.yaml"></a>

```
  [Exact](#cfn-appmesh-route-grpcroutemetadatamatchmethod-exact): String
  [Prefix](#cfn-appmesh-route-grpcroutemetadatamatchmethod-prefix): String
  [Range](#cfn-appmesh-route-grpcroutemetadatamatchmethod-range): 
    MatchRange
  [Regex](#cfn-appmesh-route-grpcroutemetadatamatchmethod-regex): String
  [Suffix](#cfn-appmesh-route-grpcroutemetadatamatchmethod-suffix): String
```

## Properties<a name="aws-properties-appmesh-route-grpcroutemetadatamatchmethod-properties"></a>

`Exact`  <a name="cfn-appmesh-route-grpcroutemetadatamatchmethod-exact"></a>
The value sent by the client must match the specified value exactly\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Prefix`  <a name="cfn-appmesh-route-grpcroutemetadatamatchmethod-prefix"></a>
The value sent by the client must begin with the specified characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Range`  <a name="cfn-appmesh-route-grpcroutemetadatamatchmethod-range"></a>
An object that represents the range of values to match on\.  
*Required*: No  
*Type*: [MatchRange](aws-properties-appmesh-route-matchrange.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Regex`  <a name="cfn-appmesh-route-grpcroutemetadatamatchmethod-regex"></a>
The value sent by the client must include the specified characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Suffix`  <a name="cfn-appmesh-route-grpcroutemetadatamatchmethod-suffix"></a>
The value sent by the client must end with the specified characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)