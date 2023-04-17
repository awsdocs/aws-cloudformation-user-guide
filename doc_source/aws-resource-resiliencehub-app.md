# AWS::ResilienceHub::App<a name="aws-resource-resiliencehub-app"></a>

Creates an AWS Resilience Hub application\. An AWS Resilience Hub application is a collection of AWS resources structured to prevent and recover AWS application disruptions\. To describe a AWS Resilience Hub application, you provide an application name, resources from one or more–up to 20–AWS CloudFormation stacks, and an appropriate resiliency policy\.

After you create an AWS Resilience Hub application, you publish it so that you can run a resiliency assessment on it\. You can then use recommendations from the assessment to improve resiliency by running another assessment, comparing results, and then iterating the process until you achieve your goals for recovery time objective \(RTO\) and recovery point objective \(RPO\)\.

## Syntax<a name="aws-resource-resiliencehub-app-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-resiliencehub-app-syntax.json"></a>

```
{
  "Type" : "AWS::ResilienceHub::App",
  "Properties" : {
      "[AppAssessmentSchedule](#cfn-resiliencehub-app-appassessmentschedule)" : String,
      "[AppTemplateBody](#cfn-resiliencehub-app-apptemplatebody)" : String,
      "[Description](#cfn-resiliencehub-app-description)" : String,
      "[Name](#cfn-resiliencehub-app-name)" : String,
      "[ResiliencyPolicyArn](#cfn-resiliencehub-app-resiliencypolicyarn)" : String,
      "[ResourceMappings](#cfn-resiliencehub-app-resourcemappings)" : [ ResourceMapping, ... ],
      "[Tags](#cfn-resiliencehub-app-tags)" : {Key : Value, ...}
    }
}
```

### YAML<a name="aws-resource-resiliencehub-app-syntax.yaml"></a>

```
Type: AWS::ResilienceHub::App
Properties: 
  [AppAssessmentSchedule](#cfn-resiliencehub-app-appassessmentschedule): String
  [AppTemplateBody](#cfn-resiliencehub-app-apptemplatebody): String
  [Description](#cfn-resiliencehub-app-description): String
  [Name](#cfn-resiliencehub-app-name): String
  [ResiliencyPolicyArn](#cfn-resiliencehub-app-resiliencypolicyarn): String
  [ResourceMappings](#cfn-resiliencehub-app-resourcemappings): 
    - ResourceMapping
  [Tags](#cfn-resiliencehub-app-tags): 
    Key : Value
```

## Properties<a name="aws-resource-resiliencehub-app-properties"></a>

`AppAssessmentSchedule`  <a name="cfn-resiliencehub-app-appassessmentschedule"></a>
 Assessment execution schedule with 'Daily' or 'Disabled' values\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AppTemplateBody`  <a name="cfn-resiliencehub-app-apptemplatebody"></a>
A JSON string that provides information about your application structure\. To learn more about the `appTemplateBody` template, see the sample template provided in the *Examples* section\.  
The `appTemplateBody` JSON string has the following structure:  
+ **`resources`**

  The list of logical resources that needs to be included in the AWS Resilience Hub application\.

  Type: Array
**Note**  
Don't add the resources that you want to exclude\.

  Each `resources` array item includes the following fields:
  + *`logicalResourceId`* 

    The logical identifier of the resource\.

    Type: Object

    Each `logicalResourceId` object includes the following fields:
    + `identifier`

      The identifier of the resource\.

      Type: String
    + `logicalStackName`

      The name of the AWS CloudFormation stack this resource belongs to\.

      Type: String
    + `resourceGroupName`

      The name of the resource group this resource belongs to\.

      Type: String
    + `terraformSourceName` 

      The name of the Terraform S3 state file this resource belongs to\.

      Type: String
    + `eksSourceName` 

      The name of the Amazon Elastic Kubernetes Service cluster and namespace this resource belongs to\.
**Note**  
This parameter accepts values in "eks\-cluster/namespace" format\.

      Type: String
  + *`type`*

    The type of resource\.

    Type: string
  + *`name`*

    The name of the resource\.

    Type: String
  + `additionalInfo`

    Additional configuration parameters for an AWS Resilience Hub application\. If you want to implement `additionalInfo` through the AWS Resilience Hub console rather than using an API call, see [Configure the application configuration parameters](https://docs.aws.amazon.com/resilience-hub/latest/userguide/app-config-param.html)\.
**Note**  
Currently, this parameter accepts a key\-value mapping \(in a string format\) of only one failover region and one associated account\.  
Key: `"failover-regions"`  
Value: `"[{"region":"<REGION>", "accounts":[{"id":"<ACCOUNT_ID>"}]}]"`
+ **`appComponents`**

  The list of Application Components \(AppComponent\) that this resource belongs to\. If an AppComponent is not part of the AWS Resilience Hub application, it will be added\.

  Type: Array

  Each `appComponents` array item includes the following fields:
  + `name`

    The name of the AppComponent\.

    Type: String
  + `type`

    The type of AppComponent\. For more information about the types of AppComponent, see [Grouping resources in an AppComponent](https://docs.aws.amazon.com/resilience-hub/latest/userguide/AppComponent.grouping.html)\.

    Type: String
  + `resourceNames`

    The list of included resources that are assigned to the AppComponent\.

    Type: Array of strings
  + `additionalInfo`

    Additional configuration parameters for an AWS Resilience Hub application\. If you want to implement `additionalInfo` through the AWS Resilience Hub console rather than using an API call, see [Configure the application configuration parameters](https://docs.aws.amazon.com/resilience-hub/latest/userguide/app-config-param.html)\.
**Note**  
Currently, this parameter accepts a key\-value mapping \(in a string format\) of only one failover region and one associated account\.  
Key: `"failover-regions"`  
Value: `"[{"region":"<REGION>", "accounts":[{"id":"<ACCOUNT_ID>"}]}]"`
+ **`excludedResources`**

  The list of logical resource identifiers to be excluded from the application\.

  Type: Array
**Note**  
Don't add the resources that you want to include\.

  Each `excludedResources` array item includes the following fields:
  + *`logicalResourceIds`* 

    The logical identifier of the resource\.

    Type: Object
**Note**  
You can configure only one of the following fields:  
`logicalStackName`
`resourceGroupName`
`terraformSourceName`
`eksSourceName`

    Each `logicalResourceIds` object includes the following fields:
    + `identifier`

      The identifier of the resource\.

      Type: String
    + `logicalStackName`

      The name of the AWS CloudFormation stack this resource belongs to\.

      Type: String
    + `resourceGroupName`

      The name of the resource group this resource belongs to\.

      Type: String
    + `terraformSourceName` 

      The name of the Terraform S3 state file this resource belongs to\.

      Type: String
    + `eksSourceName` 

      The name of the Amazon Elastic Kubernetes Service cluster and namespace this resource belongs to\.
**Note**  
This parameter accepts values in "eks\-cluster/namespace" format\.

      Type: String
+ **`version`**

  The AWS Resilience Hub application version\.
+ `additionalInfo`

  Additional configuration parameters for an AWS Resilience Hub application\. If you want to implement `additionalInfo` through the AWS Resilience Hub console rather than using an API call, see [Configure the application configuration parameters](https://docs.aws.amazon.com/resilience-hub/latest/userguide/app-config-param.html)\.
**Note**  
Currently, this parameter accepts a key\-value mapping \(in a string format\) of only one failover region and one associated account\.  
Key: `"failover-regions"`  
Value: `"[{"region":"<REGION>", "accounts":[{"id":"<ACCOUNT_ID>"}]}]"`
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-resiliencehub-app-description"></a>
The optional description for an app\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-resiliencehub-app-name"></a>
The name for the application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResiliencyPolicyArn`  <a name="cfn-resiliencehub-app-resiliencypolicyarn"></a>
The Amazon Resource Name \(ARN\) of the resiliency policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceMappings`  <a name="cfn-resiliencehub-app-resourcemappings"></a>
An array of ResourceMapping objects\.  
*Required*: Yes  
*Type*: List of [ResourceMapping](aws-properties-resiliencehub-app-resourcemapping.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-resiliencehub-app-tags"></a>
The tags assigned to the resource\. A tag is a label that you assign to an AWS resource\. Each tag consists of a key/value pair\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-resiliencehub-app-return-values"></a>

### Ref<a name="aws-resource-resiliencehub-app-return-values-ref"></a>

The returned Amazon Resource Name \(ARN\) for the app\.

### Fn::GetAtt<a name="aws-resource-resiliencehub-app-return-values-fn--getatt"></a>

The Amazon Resource Name \(ARN\) for the app\.

#### <a name="aws-resource-resiliencehub-app-return-values-fn--getatt-fn--getatt"></a>

`AppArn`  <a name="AppArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the app\.