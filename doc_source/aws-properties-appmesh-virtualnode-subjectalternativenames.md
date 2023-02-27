# AWS::AppMesh::VirtualNode SubjectAlternativeNames<a name="aws-properties-appmesh-virtualnode-subjectalternativenames"></a>

An object that represents the subject alternative names secured by the certificate\.

## Syntax<a name="aws-properties-appmesh-virtualnode-subjectalternativenames-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-subjectalternativenames-syntax.json"></a>

```
{
  "[Match](#cfn-appmesh-virtualnode-subjectalternativenames-match)" : SubjectAlternativeNameMatchers
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-subjectalternativenames-syntax.yaml"></a>

```
  [Match](#cfn-appmesh-virtualnode-subjectalternativenames-match): 
    SubjectAlternativeNameMatchers
```

## Properties<a name="aws-properties-appmesh-virtualnode-subjectalternativenames-properties"></a>

`Match`  <a name="cfn-appmesh-virtualnode-subjectalternativenames-match"></a>
An object that represents the criteria for determining a SANs match\.  
*Required*: Yes  
*Type*: [SubjectAlternativeNameMatchers](aws-properties-appmesh-virtualnode-subjectalternativenamematchers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)