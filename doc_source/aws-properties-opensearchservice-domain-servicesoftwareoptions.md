# AWS::OpenSearchService::Domain ServiceSoftwareOptions<a name="aws-properties-opensearchservice-domain-servicesoftwareoptions"></a>

The current status of the service software for an Amazon OpenSearch Service domain\. For more information, see [Service software updates in Amazon OpenSearch Service](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/service-software.html)\.

## Syntax<a name="aws-properties-opensearchservice-domain-servicesoftwareoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-opensearchservice-domain-servicesoftwareoptions-syntax.json"></a>

```
{
  "[AutomatedUpdateDate](#cfn-opensearchservice-domain-servicesoftwareoptions-automatedupdatedate)" : String,
  "[Cancellable](#cfn-opensearchservice-domain-servicesoftwareoptions-cancellable)" : Boolean,
  "[CurrentVersion](#cfn-opensearchservice-domain-servicesoftwareoptions-currentversion)" : String,
  "[Description](#cfn-opensearchservice-domain-servicesoftwareoptions-description)" : String,
  "[NewVersion](#cfn-opensearchservice-domain-servicesoftwareoptions-newversion)" : String,
  "[OptionalDeployment](#cfn-opensearchservice-domain-servicesoftwareoptions-optionaldeployment)" : Boolean,
  "[UpdateAvailable](#cfn-opensearchservice-domain-servicesoftwareoptions-updateavailable)" : Boolean,
  "[UpdateStatus](#cfn-opensearchservice-domain-servicesoftwareoptions-updatestatus)" : String
}
```

### YAML<a name="aws-properties-opensearchservice-domain-servicesoftwareoptions-syntax.yaml"></a>

```
  [AutomatedUpdateDate](#cfn-opensearchservice-domain-servicesoftwareoptions-automatedupdatedate): String
  [Cancellable](#cfn-opensearchservice-domain-servicesoftwareoptions-cancellable): Boolean
  [CurrentVersion](#cfn-opensearchservice-domain-servicesoftwareoptions-currentversion): String
  [Description](#cfn-opensearchservice-domain-servicesoftwareoptions-description): String
  [NewVersion](#cfn-opensearchservice-domain-servicesoftwareoptions-newversion): String
  [OptionalDeployment](#cfn-opensearchservice-domain-servicesoftwareoptions-optionaldeployment): Boolean
  [UpdateAvailable](#cfn-opensearchservice-domain-servicesoftwareoptions-updateavailable): Boolean
  [UpdateStatus](#cfn-opensearchservice-domain-servicesoftwareoptions-updatestatus): String
```

## Properties<a name="aws-properties-opensearchservice-domain-servicesoftwareoptions-properties"></a>

`AutomatedUpdateDate`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-automatedupdatedate"></a>
The timestamp, in Epoch time, until which you can manually request a service software update\. After this date, we automatically update your service software\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Cancellable`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-cancellable"></a>
 True if you're able to cancel your service software version update\. False if you can't cancel your service software update\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CurrentVersion`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-currentversion"></a>
The current service software version present on the domain\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-description"></a>
A description of the service software update status\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NewVersion`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-newversion"></a>
The new service software version, if one is available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OptionalDeployment`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-optionaldeployment"></a>
True if a service software is never automatically updated\. False if a service software is automatically updated after the automated update date\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateAvailable`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-updateavailable"></a>
True if you're able to update your service software version\. False if you can't update your service software version\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdateStatus`  <a name="cfn-opensearchservice-domain-servicesoftwareoptions-updatestatus"></a>
The status of your service software update\.  
*Required*: No  
*Type*: String  
*Allowed values*: `COMPLETED | ELIGIBLE | IN_PROGRESS | NOT_ELIGIBLE | PENDING_UPDATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)