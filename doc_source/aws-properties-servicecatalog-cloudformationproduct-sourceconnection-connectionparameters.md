# AWS::ServiceCatalog::CloudFormationProduct ConnectionParameters<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters"></a>

Provides connection details\.

## Syntax<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters-syntax.json"></a>

```
{
  "[CodeStar](#cfn-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters-codestar)" : CodeStarParameters
}
```

### YAML<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters-syntax.yaml"></a>

```
  [CodeStar](#cfn-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters-codestar): 
    CodeStarParameters
```

## Properties<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters-properties"></a>

`CodeStar`  <a name="cfn-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters-codestar"></a>
Provides `ConnectionType` details\.  
*Required*: No  
*Type*: [CodeStarParameters](aws-properties-servicecatalog-cloudformationproduct-codestarparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)