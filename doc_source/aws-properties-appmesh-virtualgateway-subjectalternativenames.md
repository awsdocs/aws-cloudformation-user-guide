# AWS::AppMesh::VirtualGateway SubjectAlternativeNames<a name="aws-properties-appmesh-virtualgateway-subjectalternativenames"></a>

An object that represents the subject alternative names secured by the certificate\.

## Syntax<a name="aws-properties-appmesh-virtualgateway-subjectalternativenames-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualgateway-subjectalternativenames-syntax.json"></a>

```
{
  "[Match](#cfn-appmesh-virtualgateway-subjectalternativenames-match)" : SubjectAlternativeNameMatchers
}
```

### YAML<a name="aws-properties-appmesh-virtualgateway-subjectalternativenames-syntax.yaml"></a>

```
  [Match](#cfn-appmesh-virtualgateway-subjectalternativenames-match): 
    SubjectAlternativeNameMatchers
```

## Properties<a name="aws-properties-appmesh-virtualgateway-subjectalternativenames-properties"></a>

`Match`  <a name="cfn-appmesh-virtualgateway-subjectalternativenames-match"></a>
An object that represents the criteria for determining a SANs match\.  
*Required*: Yes  
*Type*: [SubjectAlternativeNameMatchers](aws-properties-appmesh-virtualgateway-subjectalternativenamematchers.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)