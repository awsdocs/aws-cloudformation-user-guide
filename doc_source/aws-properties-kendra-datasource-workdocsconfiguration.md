# AWS::Kendra::DataSource WorkDocsConfiguration<a name="aws-properties-kendra-datasource-workdocsconfiguration"></a>

<a name="aws-properties-kendra-datasource-workdocsconfiguration-description"></a>The `WorkDocsConfiguration` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::Kendra::DataSource](aws-resource-kendra-datasource.md)\.

## Syntax<a name="aws-properties-kendra-datasource-workdocsconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-workdocsconfiguration-syntax.json"></a>

```
{
  "[CrawlComments](#cfn-kendra-datasource-workdocsconfiguration-crawlcomments)" : Boolean,
  "[ExclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-exclusionpatterns)" : [ String, ... ],
  "[FieldMappings](#cfn-kendra-datasource-workdocsconfiguration-fieldmappings)" : [ DataSourceToIndexFieldMapping, ... ],
  "[InclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-inclusionpatterns)" : [ String, ... ],
  "[OrganizationId](#cfn-kendra-datasource-workdocsconfiguration-organizationid)" : String,
  "[UseChangeLog](#cfn-kendra-datasource-workdocsconfiguration-usechangelog)" : Boolean
}
```

### YAML<a name="aws-properties-kendra-datasource-workdocsconfiguration-syntax.yaml"></a>

```
  [CrawlComments](#cfn-kendra-datasource-workdocsconfiguration-crawlcomments): Boolean
  [ExclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-exclusionpatterns): 
    - String
  [FieldMappings](#cfn-kendra-datasource-workdocsconfiguration-fieldmappings): 
    - DataSourceToIndexFieldMapping
  [InclusionPatterns](#cfn-kendra-datasource-workdocsconfiguration-inclusionpatterns): 
    - String
  [OrganizationId](#cfn-kendra-datasource-workdocsconfiguration-organizationid): String
  [UseChangeLog](#cfn-kendra-datasource-workdocsconfiguration-usechangelog): Boolean
```

## Properties<a name="aws-properties-kendra-datasource-workdocsconfiguration-properties"></a>

`CrawlComments`  <a name="cfn-kendra-datasource-workdocsconfiguration-crawlcomments"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-workdocsconfiguration-exclusionpatterns"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FieldMappings`  <a name="cfn-kendra-datasource-workdocsconfiguration-fieldmappings"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [DataSourceToIndexFieldMapping](aws-properties-kendra-datasource-datasourcetoindexfieldmapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-workdocsconfiguration-inclusionpatterns"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationId`  <a name="cfn-kendra-datasource-workdocsconfiguration-organizationid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseChangeLog`  <a name="cfn-kendra-datasource-workdocsconfiguration-usechangelog"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)