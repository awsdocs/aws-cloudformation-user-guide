# AWS::AppMesh::VirtualGateway SubjectAlternativeNameMatchers<a name="aws-properties-appmesh-virtualgateway-subjectalternativenamematchers"></a>

An object that represents the methods by which a subject alternative name on a peer Transport Layer Security \(TLS\) certificate can be matched\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-subjectalternativenamematchers-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-subjectalternativenamematchers-syntax.json"></a>

```
{
  "[Exact](#cfn-appmesh-virtualgateway-subjectalternativenamematchers-exact)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-subjectalternativenamematchers-syntax.yaml"></a>

```
  [Exact](#cfn-appmesh-virtualgateway-subjectalternativenamematchers-exact): 
    - String
```

## Properties<a name="aws-properties-appmesh-virtualgateway-subjectalternativenamematchers-properties"></a>

`Exact`  <a name="cfn-appmesh-virtualgateway-subjectalternativenamematchers-exact"></a>
The values sent must match the specified values exactly\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)