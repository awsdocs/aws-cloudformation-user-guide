# AWS::Glue::Connection<a name="aws-resource-glue-connection"></a>

The `AWS::Glue::Connection` resource specifies an AWS Glue connection to a data source\. For more information, see [Adding a Connection to Your Data Store](http://docs.aws.amazon.com/glue/latest/dg/populate-add-connection.html) and [Connection Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-connections.html#aws-glue-api-catalog-connections-Connection) in the *AWS Glue Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-glue-connection-syntax)
+ [Properties](#aws-resource-glue-connection-properties)
+ [Return Values](#aws-resource-glue-connection-returnvalues)

## Syntax<a name="aws-resource-glue-connection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-connection-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Connection",
  "Properties" : {
    "[ConnectionInput](#cfn-glue-connection-connectioninput)" : [*ConnectionInput*](aws-properties-glue-connection-connectioninput.md),
    "[CatalogId](#cfn-glue-connection-catalogid)" : String
  }
}
```

### YAML<a name="aws-resource-glue-connection-syntax.yaml"></a>

```
Type: "AWS::Glue::Connection"
Properties:
  [ConnectionInput](#cfn-glue-connection-connectioninput): 
    [*ConnectionInput*](aws-properties-glue-connection-connectioninput.md)
  [CatalogId](#cfn-glue-connection-catalogid): String
```

## Properties<a name="aws-resource-glue-connection-properties"></a>

`ConnectionInput`  <a name="cfn-glue-connection-connectioninput"></a>
The connection that you want to create\.  
 *Required*: Yes  
 *Type*: [AWS Glue Connection ConnectionInput](aws-properties-glue-connection-connectioninput.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`CatalogId`  <a name="cfn-glue-connection-catalogid"></a>
The ID of the data catalog to create the catalog object in\. Currently, this should be the AWS account ID\.  
To specify the account ID, you can use the `Ref` intrinsic function with the `AWS::AccountId` pseudo parameter—for example `!Ref AWS::AccountId`\.
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Return Values<a name="aws-resource-glue-connection-returnvalues"></a>

### Ref<a name="w3ab2c21c10d701c10b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the `ConnectionInput` name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 