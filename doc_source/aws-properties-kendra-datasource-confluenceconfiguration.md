# AWS::Kendra::DataSource ConfluenceConfiguration<a name="aws-properties-kendra-datasource-confluenceconfiguration"></a>

Provides the configuration information to connect to Confluence as your data source\.

## Syntax<a name="aws-properties-kendra-datasource-confluenceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-confluenceconfiguration-syntax.json"></a>

```
{
  "[AttachmentConfiguration](#cfn-kendra-datasource-confluenceconfiguration-attachmentconfiguration)" : ConfluenceAttachmentConfiguration,
  "[BlogConfiguration](#cfn-kendra-datasource-confluenceconfiguration-blogconfiguration)" : ConfluenceBlogConfiguration,
  "[ExclusionPatterns](#cfn-kendra-datasource-confluenceconfiguration-exclusionpatterns)" : [ String, ... ],
  "[InclusionPatterns](#cfn-kendra-datasource-confluenceconfiguration-inclusionpatterns)" : [ String, ... ],
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
    - String
  [InclusionPatterns](#cfn-kendra-datasource-confluenceconfiguration-inclusionpatterns): 
    - String
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
Configuration information for indexing attachments to Confluence blogs and pages\.  
*Required*: No  
*Type*: [ConfluenceAttachmentConfiguration](aws-properties-kendra-datasource-confluenceattachmentconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BlogConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-blogconfiguration"></a>
Configuration information for indexing Confluence blogs\.  
*Required*: No  
*Type*: [ConfluenceBlogConfiguration](aws-properties-kendra-datasource-confluenceblogconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExclusionPatterns`  <a name="cfn-kendra-datasource-confluenceconfiguration-exclusionpatterns"></a>
A list of regular expression patterns to exclude certain blog posts, pages, spaces, or attachments in your Confluence\. Content that matches the patterns are excluded from the index\. Content that doesn't match the patterns is included in the index\. If content matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the content isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InclusionPatterns`  <a name="cfn-kendra-datasource-confluenceconfiguration-inclusionpatterns"></a>
A list of regular expression patterns to include certain blog posts, pages, spaces, or attachments in your Confluence\. Content that matches the patterns are included in the index\. Content that doesn't match the patterns is excluded from the index\. If content matches both an inclusion and exclusion pattern, the exclusion pattern takes precedence and the content isn't included in the index\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PageConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-pageconfiguration"></a>
Configuration information for indexing Confluence pages\.  
*Required*: No  
*Type*: [ConfluencePageConfiguration](aws-properties-kendra-datasource-confluencepageconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-confluenceconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of an AWS Secrets Manager secret that contains the user name and password required to connect to the Confluence instance\. If you use Confluence Cloud, you use a generated API token as the password\.  
You can also provide authentication credentials in the form of a personal access token\. For more information, see [Using a Confluence data source](https://docs.aws.amazon.com/kendra/latest/dg/data-source-confluence.html)\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerUrl`  <a name="cfn-kendra-datasource-confluenceconfiguration-serverurl"></a>
The URL of your Confluence instance\. Use the full URL of the server\. For example, *https://server\.example\.com:port/*\. You can also use an IP address, for example, *https://192\.168\.1\.113/*\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^(https?|ftp|file):\/\/([^\s]*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SpaceConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-spaceconfiguration"></a>
Configuration information for indexing Confluence spaces\.  
*Required*: No  
*Type*: [ConfluenceSpaceConfiguration](aws-properties-kendra-datasource-confluencespaceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-kendra-datasource-confluenceconfiguration-version"></a>
The version or the type of Confluence installation to connect to\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `CLOUD | SERVER`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfiguration`  <a name="cfn-kendra-datasource-confluenceconfiguration-vpcconfiguration"></a>
Configuration information for an Amazon Virtual Private Cloud to connect to your Confluence\. For more information, see [Configuring a VPC](https://docs.aws.amazon.com/kendra/latest/dg/vpc-configuration.html)\.  
*Required*: No  
*Type*: [DataSourceVpcConfiguration](aws-properties-kendra-datasource-datasourcevpcconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)