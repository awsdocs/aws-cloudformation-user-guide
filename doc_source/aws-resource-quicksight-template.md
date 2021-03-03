# AWS::QuickSight::Template<a name="aws-resource-quicksight-template"></a>

Creates a template from an existing QuickSight analysis or template\. You can use the resulting template to create a dashboard\.

A *template* is an entity in QuickSight that encapsulates the metadata required to create an analysis and that you can use to create s dashboard\. A template adds a layer of abstraction by using placeholders to replace the dataset associated with the analysis\. You can use templates to create dashboards by replacing dataset placeholders with datasets that follow the same schema that was used to create the source analysis and template\.

## Syntax<a name="aws-resource-quicksight-template-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-quicksight-template-syntax.json"></a>

```
{
  "Type" : "AWS::QuickSight::Template",
  "Properties" : {
      "[AwsAccountId](#cfn-quicksight-template-awsaccountid)" : String,
      "[Name](#cfn-quicksight-template-name)" : String,
      "[Permissions](#cfn-quicksight-template-permissions)" : [ ResourcePermission, ... ],
      "[SourceEntity](#cfn-quicksight-template-sourceentity)" : TemplateSourceEntity,
      "[Tags](#cfn-quicksight-template-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TemplateId](#cfn-quicksight-template-templateid)" : String,
      "[VersionDescription](#cfn-quicksight-template-versiondescription)" : String
    }
}
```

### YAML<a name="aws-resource-quicksight-template-syntax.yaml"></a>

```
Type: AWS::QuickSight::Template
Properties: 
  [AwsAccountId](#cfn-quicksight-template-awsaccountid): String
  [Name](#cfn-quicksight-template-name): String
  [Permissions](#cfn-quicksight-template-permissions): 
    - ResourcePermission
  [SourceEntity](#cfn-quicksight-template-sourceentity): 
    TemplateSourceEntity
  [Tags](#cfn-quicksight-template-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TemplateId](#cfn-quicksight-template-templateid): String
  [VersionDescription](#cfn-quicksight-template-versiondescription): String
```

## Properties<a name="aws-resource-quicksight-template-properties"></a>

`AwsAccountId`  <a name="cfn-quicksight-template-awsaccountid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-quicksight-template-name"></a>
A display name for the template\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\u0020-\u00FF]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Permissions`  <a name="cfn-quicksight-template-permissions"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [ResourcePermission](aws-properties-quicksight-template-resourcepermission.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceEntity`  <a name="cfn-quicksight-template-sourceentity"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: [TemplateSourceEntity](aws-properties-quicksight-template-templatesourceentity.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-quicksight-template-tags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TemplateId`  <a name="cfn-quicksight-template-templateid"></a>
The ID of the template\. This ID is unique per AWS Region for each AWS account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `[\w\-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VersionDescription`  <a name="cfn-quicksight-template-versiondescription"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-quicksight-template-return-values"></a>

### Ref<a name="aws-resource-quicksight-template-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-quicksight-template-return-values-fn--getatt"></a>

#### <a name="aws-resource-quicksight-template-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`CreatedTime`  <a name="CreatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`LastUpdatedTime`  <a name="LastUpdatedTime-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.