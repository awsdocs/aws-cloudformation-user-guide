# AWS::Config::ConformancePack TemplateSSMDocumentDetails<a name="aws-properties-config-conformancepack-templatessmdocumentdetails"></a>

This API allows you to create a conformance pack template with an AWS Systems Manager document \(SSM document\)\. To deploy a conformance pack using an SSM document, first create an SSM document with conformance pack content, and then provide the `DocumentName` in the [PutConformancePack API](https://docs.aws.amazon.com/config/latest/APIReference/API_PutConformancePack.html)\. You can also provide the `DocumentVersion`\.

The `TemplateSSMDocumentDetails` object contains the name of the SSM document and the version of the SSM document\.

## Syntax<a name="aws-properties-config-conformancepack-templatessmdocumentdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-config-conformancepack-templatessmdocumentdetails-syntax.json"></a>

```
{
  "[DocumentName](#cfn-config-conformancepack-templatessmdocumentdetails-documentname)" : String,
  "[DocumentVersion](#cfn-config-conformancepack-templatessmdocumentdetails-documentversion)" : String
}
```

### YAML<a name="aws-properties-config-conformancepack-templatessmdocumentdetails-syntax.yaml"></a>

```
  [DocumentName](#cfn-config-conformancepack-templatessmdocumentdetails-documentname): String
  [DocumentVersion](#cfn-config-conformancepack-templatessmdocumentdetails-documentversion): String
```

## Properties<a name="aws-properties-config-conformancepack-templatessmdocumentdetails-properties"></a>

`DocumentName`  <a name="cfn-config-conformancepack-templatessmdocumentdetails-documentname"></a>
The name or Amazon Resource Name \(ARN\) of the SSM document to use to create a conformance pack\. If you use the document name, AWS Config checks only your account and AWS Region for the SSM document\. If you want to use an SSM document from another Region or account, you must provide the ARN\.  
*Required*: No  
*Type*: String  
*Pattern*: `^[a-zA-Z0-9_\-.:/]{3,200}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentVersion`  <a name="cfn-config-conformancepack-templatessmdocumentdetails-documentversion"></a>
The version of the SSM document to use to create a conformance pack\. By default, AWS Config uses the latest version\.  
This field is optional\.
*Required*: No  
*Type*: String  
*Pattern*: `([$]LATEST|[$]DEFAULT|^[1-9][0-9]*$)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)