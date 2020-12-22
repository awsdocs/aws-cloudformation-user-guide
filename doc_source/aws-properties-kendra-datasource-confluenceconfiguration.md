# AWS::Kendra::DataSource ConfluenceConfiguration<a name="aws-properties-kendra-datasource-confluenceconfiguration"></a>

Provides configuration information for data sources that connect to Confluence\.

## Syntax<a name="aws-properties-kendra-datasource-confluenceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluenceconfiguration-syntax.json"></a>

```
{
  "[AttachmentConfiguration](#cfn-kendra-datasource-confluenceconfiguration-attachmentconfiguration)" : ConfluenceAttachmentConfiguration,
  "[BlogConfiguration](#cfn-kendra-datasource-confluenceconfiguration-blogconfiguration)" : ConfluenceBlogConfiguration,
  "[ExclusionPatterns](#cfn-kendra-datasource-confluenceconfiguration-exclusionpatterns)" : DataSourceInclusionsExclusionsStrings,
  "[InclusionPatterns](#cfn-kendra-datasource-confluenceconfiguration-inclusionpatterns)" : DataSourceInclusionsExclusionsStrings,
  "[PageConfiguration](#cfn-kendra-datasource-confluenceconfiguration-pageconfiguration)" : ConfluencePageConfiguration,
  "[SecretArn](#cfn-kendra-datasource-confluenceconfiguration-secretarn)" : String,
  "[ServerUrl](#cfn-kendra-datasource-confluenceconfiguration-serverurl)" : String,
  "[SpaceConfiguration](#cfn-kendra-datasource-confluenceconfiguration-spaceconfiguration)" : ConfluenceSpaceConfiguration,
  "[Version](#cfn-kendra-datasource-confluenceconfiguration-version)" : String,
  "[VpcConfiguration](#cfn-kendra-datasource-confluenceconfiguration-vpcconfiguration)" : DataSourceVpcConfiguration
}
```

### YAML<a name="aws-properties-kendra-datasource-confluenceconfiguration-syntax.yaml"></a>

```
  [AttachmentConfiguration](#cfn-kendra-datasource-confluenceconfiguration-attachmentconfiguration): 
    ConfluenceAttachmentConfiguration
  [BlogConfiguration](#cfn-kendra-datasource-confluenceconfiguration-blogconfiguration): 
    ConfluenceBlogConfiguration
  [ExclusionPatterns](#cfn-kendra-datasource-confluenceconfiguration-exclusionpatterns): 
    DataSourceInclusionsExclusionsStrings
  [InclusionPatterns](#cfn-kendra-datasource-confluenceconfiguration-inclusionpatterns): 
    DataSourceInclusionsExclusionsStrings
  [PageConfiguration](#cfn-kendra-datasource-confluenceconfiguration-pageconfiguration): 
    ConfluencePageConfiguration
  [SecretArn](#cfn-kendra-datasource-confluenceconfiguration-secretarn): String
  [ServerUrl](#cfn-kendra-datasource-confluenceconfiguration-serverurl): String
  [SpaceConfiguration](#cfn-kendra-datasource-confluenceconfiguration-spaceconfiguration): 
    ConfluenceSpaceConfiguration
  [Version](#cfn-kendra-datasource-confluenceconfiguration-version): String
  [VpcConfiguration](#cfn-kendra-datasource-confluenceconfiguration-vpcconfiguration): 
    DataSourceVpcConfiguration
```

## Properties<a name="aws-properties-kendra-datasource-confluenceconfiguration-properties"></a>

`AttachmentConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-attachmentconfiguration"></a>
Specifies configuration information for indexing attachments to Confluence blogs and pages\.  
*Required*: No  
*Type*: [ConfluenceAttachmentConfiguration](aws-properties-kendra-datasource-confluenceattachmentconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlogConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-blogconfiguration"></a>
 Specifies configuration information for indexing Confluence blogs\.  
*Required*: No  
*Type*: [ConfluenceBlogConfiguration](aws-properties-kendra-datasource-confluenceblogconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-confluenceconfiguration-exclusionpatterns"></a>
A list of regular expression patterns that apply to a URL on the Confluence server\. An exclusion pattern can apply to a blog post, a page, a space, or an attachment\. Items that match the pattern are excluded from the index\. Items that don't match the pattern are included in the index\. If a item matches both an exclusion pattern and an inclusion pattern, the item isn't included in the index\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-confluenceconfiguration-inclusionpatterns"></a>
A list of regular expression patterns that apply to a URL on the Confluence server\. An inclusion pattern can apply to a blog post, a page, a space, or an attachment\. Items that match the patterns are included in the index\. Items that don't match the pattern are excluded from the index\. If an item matches both an inclusion pattern and an exclusion pattern, the item isn't included in the index\.  
*Required*: No  
*Type*: [DataSourceInclusionsExclusionsStrings](aws-properties-kendra-datasource-datasourceinclusionsexclusionsstrings.md)  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PageConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-pageconfiguration"></a>
Specifies configuration information for indexing Confluence pages\.  
*Required*: No  
*Type*: [ConfluencePageConfiguration](aws-properties-kendra-datasource-confluencepageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-confluenceconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Secrets Manager secret that contains the key/value pairs required to connect to your Confluence server\. The secret must contain a JSON structure with the following keys:  
+ username \- The user name or email address of a user with administrative privileges for the Confluence server\.
+ password \- The password associated with the user logging in to the Confluence server\.
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerUrl`  <a name="cfn-kendra-datasource-confluenceconfiguration-serverurl"></a>
The URL of your Confluence instance\. Use the full URL of the server\. For example, `https://server.example.com:port/`\. You can also use an IP address, for example, `https://192.168.1.113/`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^(https?|ftp|file):\/\/([^\s]*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpaceConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-spaceconfiguration"></a>
Specifies configuration information for indexing Confluence spaces\.  
*Required*: No  
*Type*: [ConfluenceSpaceConfiguration](aws-properties-kendra-datasource-confluencespaceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-kendra-datasource-confluenceconfiguration-version"></a>
Specifies the version of the Confluence installation that you are connecting to\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CLOUD | SERVER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-vpcconfiguration"></a>
Specifies the information for connecting to an Amazon VPC\.  
*Required*: No  
*Type*: [DataSourceVpcConfiguration](aws-properties-kendra-datasource-datasourcevpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)