# AWS::Kendra::DataSource ServiceNowConfiguration<a name="aws-properties-kendra-datasource-servicenowconfiguration"></a>

Provides configuration information required to connect to a ServiceNow data source\.

## Syntax<a name="aws-properties-kendra-datasource-servicenowconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kendra-datasource-servicenowconfiguration-syntax.json"></a>

```
{
  "[HostUrl](#cfn-kendra-datasource-servicenowconfiguration-hosturl)" : String,
  "[KnowledgeArticleConfiguration](#cfn-kendra-datasource-servicenowconfiguration-knowledgearticleconfiguration)" : ServiceNowKnowledgeArticleConfiguration,
  "[SecretArn](#cfn-kendra-datasource-servicenowconfiguration-secretarn)" : String,
  "[ServiceCatalogConfiguration](#cfn-kendra-datasource-servicenowconfiguration-servicecatalogconfiguration)" : ServiceNowServiceCatalogConfiguration,
  "[ServiceNowBuildVersion](#cfn-kendra-datasource-servicenowconfiguration-servicenowbuildversion)" : String
}
```

### YAML<a name="aws-properties-kendra-datasource-servicenowconfiguration-syntax.yaml"></a>

```
  [HostUrl](#cfn-kendra-datasource-servicenowconfiguration-hosturl): String
  [KnowledgeArticleConfiguration](#cfn-kendra-datasource-servicenowconfiguration-knowledgearticleconfiguration): 
    ServiceNowKnowledgeArticleConfiguration
  [SecretArn](#cfn-kendra-datasource-servicenowconfiguration-secretarn): String
  [ServiceCatalogConfiguration](#cfn-kendra-datasource-servicenowconfiguration-servicecatalogconfiguration): 
    ServiceNowServiceCatalogConfiguration
  [ServiceNowBuildVersion](#cfn-kendra-datasource-servicenowconfiguration-servicenowbuildversion): String
```

## Properties<a name="aws-properties-kendra-datasource-servicenowconfiguration-properties"></a>

`HostUrl`  <a name="cfn-kendra-datasource-servicenowconfiguration-hosturl"></a>
The ServiceNow instance that the data source connects to\. The host endpoint should look like the following: `{instance}.service-now.com.`   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `^(?!(^(https?|ftp|file):\/\/))[a-z0-9-]+(\.service-now\.com)$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KnowledgeArticleConfiguration`  <a name="cfn-kendra-datasource-servicenowconfiguration-knowledgearticleconfiguration"></a>
Provides configuration information for crawling knowledge articles in the ServiceNow site\.  
*Required*: No  
*Type*: [ServiceNowKnowledgeArticleConfiguration](aws-properties-kendra-datasource-servicenowknowledgearticleconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecretArn`  <a name="cfn-kendra-datasource-servicenowconfiguration-secretarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Secret Manager secret that contains the user name and password required to connect to the ServiceNow instance\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1284`  
*Pattern*: `arn:[a-z0-9-\.]{1,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[a-z0-9-\.]{0,63}:[^/].{0,1023}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceCatalogConfiguration`  <a name="cfn-kendra-datasource-servicenowconfiguration-servicecatalogconfiguration"></a>
Provides configuration information for crawling service catalogs in the ServiceNow site\.  
*Required*: No  
*Type*: [ServiceNowServiceCatalogConfiguration](aws-properties-kendra-datasource-servicenowservicecatalogconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceNowBuildVersion`  <a name="cfn-kendra-datasource-servicenowconfiguration-servicenowbuildversion"></a>
The identifier of the release that the ServiceNow host is running\. If the host is not running the `LONDON` release, use `OTHERS`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `LONDON | OTHERS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)