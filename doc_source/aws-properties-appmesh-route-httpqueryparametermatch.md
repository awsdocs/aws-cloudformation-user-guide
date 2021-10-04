# AWS::AppMesh::Route HttpQueryParameterMatch<a name="aws-properties-appmesh-route-httpqueryparametermatch"></a>

An object representing the query parameter to match\.

## Syntax<a name="aws-properties-appmesh-route-httpqueryparametermatch-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-route-httpqueryparametermatch-syntax.json"></a>

```
{
  "[Exact](#cfn-appmesh-route-httpqueryparametermatch-exact)" : String
}
```

### YAML<a name="aws-properties-appmesh-route-httpqueryparametermatch-syntax.yaml"></a>

```
  [Exact](#cfn-appmesh-route-httpqueryparametermatch-exact): String
```

## Properties<a name="aws-properties-appmesh-route-httpqueryparametermatch-properties"></a>

`Exact`  <a name="cfn-appmesh-route-httpqueryparametermatch-exact"></a>
The exact query parameter to match on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)