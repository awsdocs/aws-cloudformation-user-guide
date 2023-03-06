# AWS::ResilienceHub::App<a name="aws-resource-resiliencehub-app"></a>

Creates an AWS Resilience Hub application\. An AWS Resilience Hub application is a collection of AWS resources structured to prevent and recover AWS application disruptions\. To describe a AWS Resilience Hub application, you provide an application name, resources from one or more–up to five–AWS CloudFormation stacks, and an appropriate resiliency policy\.

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
A string containing a full AWS Resilience Hub app template body\.  
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