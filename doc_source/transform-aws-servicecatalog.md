# AWS::ServiceCatalog transform<a name="transform-aws-servicecatalog"></a>

The `AWS::ServiceCatalog` transform enables Service Catalog users to reference outputs from an existing Service Catalog provisioned product in their CloudFormation template\.

To reference an output from an existing provisioned product, you must include the `AWS::ServiceCatalog` transform at the top of your template\. Where an output value is required, you provide the name of the provisioned product and the output key name\.

You can reference multiple provisioned products and key names in your template, a maximum of 20 per template\. During provisioning, the transform retrieves the value from each referenced provisioned product and key, substituting the output value in your CloudFormation template\. 

## Usage<a name="tbd"></a>

Use the `AWS::ServiceCatalog` transform at the top of the template\. You cannot use `AWS::ServiceCatalog` as a transform embedded in any other template section\. 

The value for the transform declaration must be a literal string\. You cannot use a parameter or function to specify a transform value\.

### Syntax at the top level of a template<a name="servicecatalog-top-level-syntax"></a>

To include `AWS::ServiceCatalog` at the top level of a template, in the Transform section, use the following syntax:

#### JSON<a name="servicecatalog-top-level-syntax.json"></a>

```
{
"Transform": "AWS::ServiceCatalog",
. . .
}
```

#### YAML<a name="servicecatalog-top-level-syntax.yaml"></a>

```
Transform: AWS::ServiceCatalog
```

## Parameters<a name="servicecatalog-parameters"></a>

The `AWS::ServiceCatalog` transform does not accept any parameters\.

## Example<a name="servicecatalog-example-json"></a>

The JSON and YAML examples below show how a user can reference outputs from an existing Service Catalog provisioned product in a CloudFormation template\.

In these examples, `SampleProvisionedProduct` is a previously created provisioned product\. `SampleOutputKey` is an output key of this provisioned product\.

### JSON<a name="servicecatalog-json-transform"></a>

This example is a working version\.

Template versions that don't wrap the value as a string literal will fail\.

```
    {
        "AWSTemplateFormatVersion": "2010-09-09",
        "Transform": "AWS::ServiceCatalog",
        "Resources": {
            "ExampleParameter": {
                "Type": "AWS::SSM::Parameter",
                "Properties": {
                    "Type": "String",
                    "Value": "[[servicecatalog:provisionedproduct:SampleProvisionedProduct:SampleOutputKey]]"
                }
            }
        }
    }
```

### YAML<a name="servicecatalog-yaml-transform"></a>

Examples 1\-4 are valid templates\. In Examples 1 and 2, the transform and value are string literals\.

Example 5 is not a valid template\. The value must be wrapped in a string ' or " or >\- \. If not, the user receives an error\.

```
     // Example 1 
    AWSTemplateFormatVersion: 2010-09-09
    Transform: 'AWS::ServiceCatalog'
    Resources:
      ExampleParameter:
        Type: 'AWS::SSM::Parameter'
        Properties:
          Type: String
          Value: '[[servicecatalog:provisionedproduct:SampleProvisionedProduct:SampleOutputKey]]'
     
    // Example 2 
    AWSTemplateFormatVersion: 2010-09-09
    Transform: 'AWS::ServiceCatalog'
    Resources:
      ExampleParameter:
        Type: 'AWS::SSM::Parameter'
        Properties:
          Type: String
          Value: '[[servicecatalog:provisionedproduct:SampleProvisionedProduct:SampleOutputKey]]'
     
     
    // Example 3 
    AWSTemplateFormatVersion: 2010-09-09
    Transform: AWS::ServiceCatalog
    Resources:
      ExampleParameter:
        Type: 'AWS::SSM::Parameter'
        Properties:
          Type: String
          Value: "[[servicecatalog:provisionedproduct:SampleProvisionedProduct:SampleOutputKey]]"
     
     
    // Example 4 
     
    AWSTemplateFormatVersion: 2010-09-09
    Transform: AWS::ServiceCatalog
    Resources:
      ExampleParameter:
        Type: 'AWS::SSM::Parameter'
        Properties:
          Type: String
          Value: >-
            [[servicecatalog:provisionedproduct:SampleProvisionedProduct:SampleOutputKey]]
     
     
    // Example 5 
    AWSTemplateFormatVersion: 2010-09-09
    Transform: AWS::ServiceCatalog
    Resources:
      ExampleParameter2:
        Type: 'AWS::SSM::Parameter'
        Properties:
          Type: String
          Value: [[servicecatalog:provisionedproduct:SSMProductProvisionedProduct:SampleOutputKey]]
```