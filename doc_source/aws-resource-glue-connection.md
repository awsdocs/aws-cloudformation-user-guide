# AWS::Glue::Connection<a name="aws-resource-glue-connection"></a>

The `AWS::Glue::Connection` resource specifies an AWS Glue connection to a data source\. For more information, see [Adding a Connection to Your Data Store](https://docs.aws.amazon.com/glue/latest/dg/populate-add-connection.html) and [Connection Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-catalog-connections.html#aws-glue-api-catalog-connections-Connection) in the *AWS Glue Developer Guide*\.

## Syntax<a name="aws-resource-glue-connection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-connection-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Connection",
  "Properties" : {
      "[CatalogId](#cfn-glue-connection-catalogid)" : String,
      "[ConnectionInput](#cfn-glue-connection-connectioninput)" : ConnectionInput
    }
}
```

### YAML<a name="aws-resource-glue-connection-syntax.yaml"></a>

```
Type: AWS::Glue::Connection
Properties: 
  [CatalogId](#cfn-glue-connection-catalogid): String
  [ConnectionInput](#cfn-glue-connection-connectioninput): 
    ConnectionInput
```

## Properties<a name="aws-resource-glue-connection-properties"></a>

`CatalogId`  <a name="cfn-glue-connection-catalogid"></a>
The ID of the data catalog to create the catalog object in\. Currently, this should be the AWS account ID\.  
To specify the account ID, you can use the `Ref` intrinsic function with the `AWS::AccountId` pseudo parameter\. For example: `!Ref AWS::AccountId`\.
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectionInput`  <a name="cfn-glue-connection-connectioninput"></a>
The connection that you want to create\.  
*Required*: Yes  
*Type*: [ConnectionInput](aws-properties-glue-connection-connectioninput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-connection-return-values"></a>

### Ref<a name="aws-resource-glue-connection-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the connection name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.