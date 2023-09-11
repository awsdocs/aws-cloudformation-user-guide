# AWS::VpcLattice::Rule FixedResponse<a name="aws-properties-vpclattice-rule-fixedresponse"></a>

Describes an action that returns a custom HTTP response\.

## Syntax<a name="aws-properties-vpclattice-rule-fixedresponse-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-rule-fixedresponse-syntax.json"></a>

```
{
  "[StatusCode](#cfn-vpclattice-rule-fixedresponse-statuscode)" : Integer
}
```

### YAML<a name="aws-properties-vpclattice-rule-fixedresponse-syntax.yaml"></a>

```
  [StatusCode](#cfn-vpclattice-rule-fixedresponse-statuscode): Integer
```

## Properties<a name="aws-properties-vpclattice-rule-fixedresponse-properties"></a>

`StatusCode`  <a name="cfn-vpclattice-rule-fixedresponse-statuscode"></a>
The HTTP response code\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)