# AWS::Kendra::DataSource DocumentAttributeTarget<a name="aws-properties-kendra-datasource-documentattributetarget"></a>

The target document attribute or metadata field you want to alter when ingesting documents into Amazon Kendra\.

For example, you can delete customer identification numbers associated with the documents, stored in the document metadata field called 'Customer\_ID'\. You set the target key as 'Customer\_ID' and the deletion flag to `TRUE`\. This removes all customer ID values in the field 'Customer\_ID'\. This would scrub personally identifiable information from each document's metadata\.

Amazon Kendra cannot create a target field if it has not already been created as an index field\. After you create your index field, you can create a document metadata field using `DocumentAttributeTarget`\. Amazon Kendra then will map your newly created metadata field to your index field\.

You can also use this with [DocumentAttributeCondition](https://docs.aws.amazon.com/kendra/latest/dg/API_DocumentAttributeCondition.html)\.

## Syntax<a name="aws-properties-kendra-datasource-documentattributetarget-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-documentattributetarget-syntax.json"></a>

```
{
  "[TargetDocumentAttributeKey](#cfn-kendra-datasource-documentattributetarget-targetdocumentattributekey)" : String,
  "[TargetDocumentAttributeValue](#cfn-kendra-datasource-documentattributetarget-targetdocumentattributevalue)" : DocumentAttributeValue,
  "[TargetDocumentAttributeValueDeletion](#cfn-kendra-datasource-documentattributetarget-targetdocumentattributevaluedeletion)" : Boolean
}
```

### YAML<a name="aws-properties-kendra-datasource-documentattributetarget-syntax.yaml"></a>

```
  [TargetDocumentAttributeKey](#cfn-kendra-datasource-documentattributetarget-targetdocumentattributekey): String
  [TargetDocumentAttributeValue](#cfn-kendra-datasource-documentattributetarget-targetdocumentattributevalue): 
    DocumentAttributeValue
  [TargetDocumentAttributeValueDeletion](#cfn-kendra-datasource-documentattributetarget-targetdocumentattributevaluedeletion): Boolean
```

## Properties<a name="aws-properties-kendra-datasource-documentattributetarget-properties"></a>

`TargetDocumentAttributeKey`  <a name="cfn-kendra-datasource-documentattributetarget-targetdocumentattributekey"></a>
The identifier of the target document attribute or metadata field\.  
For example, 'Department' could be an identifier for the target attribute or metadata field that includes the department names associated with the documents\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `200`  
*Pattern*: `[a-zA-Z0-9_][a-zA-Z0-9_-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetDocumentAttributeValue`  <a name="cfn-kendra-datasource-documentattributetarget-targetdocumentattributevalue"></a>
The target value you want to create for the target attribute\.  
For example, 'Finance' could be the target value for the target attribute key 'Department'\.  
*Required*: No  
*Type*: [DocumentAttributeValue](aws-properties-kendra-datasource-documentattributevalue.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetDocumentAttributeValueDeletion`  <a name="cfn-kendra-datasource-documentattributetarget-targetdocumentattributevaluedeletion"></a>
 `TRUE` to delete the existing target value for your specified target attribute key\. You cannot create a target value and set this to `TRUE`\. To create a target value \(`TargetDocumentAttributeValue`\), set this to `FALSE`\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)