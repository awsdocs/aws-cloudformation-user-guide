# AWS::ServiceCatalog::CloudFormationProduct SourceConnection<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection"></a>

A top level `ProductViewDetail` response containing details about the product’s connection\. AWS Service Catalog returns this field for the `CreateProduct`, `UpdateProduct`, `DescribeProductAsAdmin`, and `SearchProductAsAdmin` APIs\. This response contains the same fields as the `ConnectionParameters` request, with the addition of the `LastSync` response\.

## Syntax<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-syntax.json"></a>

```
{
  "[ConnectionParameters](#cfn-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters)" : ConnectionParameters,
  "[Type](#cfn-servicecatalog-cloudformationproduct-sourceconnection-type)" : String
}
```

### YAML<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-syntax.yaml"></a>

```
  [ConnectionParameters](#cfn-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters): 
    ConnectionParameters
  [Type](#cfn-servicecatalog-cloudformationproduct-sourceconnection-type): String
```

## Properties<a name="aws-properties-servicecatalog-cloudformationproduct-sourceconnection-properties"></a>

`ConnectionParameters`  <a name="cfn-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters"></a>
The connection details based on the connection `Type`\.   
*Required*: Yes  
*Type*: [ConnectionParameters](aws-properties-servicecatalog-cloudformationproduct-sourceconnection-connectionparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-servicecatalog-cloudformationproduct-sourceconnection-type"></a>
The only supported `SourceConnection` type is Codestar\.   
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)