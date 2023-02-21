# AWS::Backup::ReportPlan<a name="aws-resource-backup-reportplan"></a>

Creates a report plan\. A report plan is a document that contains information about the contents of the report and where AWS Backup will deliver it\.

If you call `CreateReportPlan` with a plan that already exists, you receive an `AlreadyExistsException` exception\.

For a sample AWS CloudFormation template, see the [AWS Backup Developer Guide](https://docs.aws.amazon.com/aws-backup/latest/devguide/assigning-resources.html#assigning-resources-cfn)\.

## Syntax<a name="aws-resource-backup-reportplan-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-backup-reportplan-syntax.json"></a>

```
{
  "Type" : "AWS::Backup::ReportPlan",
  "Properties" : {
      "[ReportDeliveryChannel](#cfn-backup-reportplan-reportdeliverychannel)" : ReportDeliveryChannel,
      "[ReportPlanDescription](#cfn-backup-reportplan-reportplandescription)" : String,
      "[ReportPlanName](#cfn-backup-reportplan-reportplanname)" : String,
      "[ReportPlanTags](#cfn-backup-reportplan-reportplantags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[ReportSetting](#cfn-backup-reportplan-reportsetting)" : ReportSetting
    }
}
```

### YAML<a name="aws-resource-backup-reportplan-syntax.yaml"></a>

```
Type: AWS::Backup::ReportPlan
Properties: 
  [ReportDeliveryChannel](#cfn-backup-reportplan-reportdeliverychannel): 
    ReportDeliveryChannel
  [ReportPlanDescription](#cfn-backup-reportplan-reportplandescription): String
  [ReportPlanName](#cfn-backup-reportplan-reportplanname): String
  [ReportPlanTags](#cfn-backup-reportplan-reportplantags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [ReportSetting](#cfn-backup-reportplan-reportsetting): 
    ReportSetting
```

## Properties<a name="aws-resource-backup-reportplan-properties"></a>

`ReportDeliveryChannel`  <a name="cfn-backup-reportplan-reportdeliverychannel"></a>
Contains information about where and how to deliver your reports, specifically your Amazon S3 bucket name, S3 key prefix, and the formats of your reports\.  
*Required*: Yes  
*Type*: [ReportDeliveryChannel](aws-properties-backup-reportplan-reportdeliverychannel.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportPlanDescription`  <a name="cfn-backup-reportplan-reportplandescription"></a>
An optional description of the report plan with a maximum 1,024 characters\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportPlanName`  <a name="cfn-backup-reportplan-reportplanname"></a>
The unique name of the report plan\. This name is between 1 and 256 characters starting with a letter, and consisting of letters \(a\-z, A\-Z\), numbers \(0\-9\), and underscores \(\_\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z][_a-zA-Z0-9]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ReportPlanTags`  <a name="cfn-backup-reportplan-reportplantags"></a>
A list of tags to tag your report plan\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReportSetting`  <a name="cfn-backup-reportplan-reportsetting"></a>
Identifies the report template for the report\. Reports are built using a report template\. The report templates are:  
 `RESOURCE_COMPLIANCE_REPORT | CONTROL_COMPLIANCE_REPORT | BACKUP_JOB_REPORT | COPY_JOB_REPORT | RESTORE_JOB_REPORT`   
If the report template is `RESOURCE_COMPLIANCE_REPORT` or `CONTROL_COMPLIANCE_REPORT`, this API resource also describes the report coverage by AWS Regions and frameworks\.  
*Required*: Yes  
*Type*: [ReportSetting](aws-properties-backup-reportplan-reportsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-backup-reportplan-return-values"></a>

### Ref<a name="aws-resource-backup-reportplan-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-backup-reportplan-return-values-fn--getatt"></a>

#### <a name="aws-resource-backup-reportplan-return-values-fn--getatt-fn--getatt"></a>

`ReportPlanArn`  <a name="ReportPlanArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of your report plan\.