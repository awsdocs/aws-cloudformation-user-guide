# AWS::SSM::Association<a name="aws-resource-ssm-association"></a>

The `AWS::SSM::Association` resource associates an SSM document in AWS Systems Manager with managed instances that contain a configuration agent to process the document\.

## Syntax<a name="aws-resource-ssm-association-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-association-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Association",
  "Properties" : {
      "[AssociationName](#cfn-ssm-association-associationname)" : String,
      "[DocumentVersion](#cfn-ssm-association-documentversion)" : String,
      "[InstanceId](#cfn-ssm-association-instanceid)" : String,
      "[Name](#cfn-ssm-association-name)" : String,
      "[OutputLocation](#cfn-ssm-association-outputlocation)" : [InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md),
      "[Parameters](#cfn-ssm-association-parameters)" : {Key : Value, ...},
      "[ScheduleExpression](#cfn-ssm-association-scheduleexpression)" : String,
      "[Targets](#cfn-ssm-association-targets)" : [ [Target](aws-properties-ssm-association-target.md), ... ]
    }
}
```

### YAML<a name="aws-resource-ssm-association-syntax.yaml"></a>

```
Type: AWS::SSM::Association
Properties:
  [AssociationName](#cfn-ssm-association-associationname): String
  [DocumentVersion](#cfn-ssm-association-documentversion): String
  [InstanceId](#cfn-ssm-association-instanceid): String
  [Name](#cfn-ssm-association-name): String
  [OutputLocation](#cfn-ssm-association-outputlocation):
    [InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md)
  [Parameters](#cfn-ssm-association-parameters):
    Key : Value
  [ScheduleExpression](#cfn-ssm-association-scheduleexpression): String
  [Targets](#cfn-ssm-association-targets):
    - [Target](aws-properties-ssm-association-target.md)
```

## Properties<a name="aws-resource-ssm-association-properties"></a>

`AssociationName`  <a name="cfn-ssm-association-associationname"></a>
The name of the association\.
*Required*: No
*Type*: String
*Pattern*: `^[a-zA-Z0-9_\-.]{3,128}$`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DocumentVersion`  <a name="cfn-ssm-association-documentversion"></a>
The version of the SSM document to associate with the target\.
*Required*: No
*Type*: String
*Pattern*: `([$]LATEST|[$]DEFAULT|^[1-9][0-9]*$)`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceId`  <a name="cfn-ssm-association-instanceid"></a>
The ID of the instance that the SSM document is associated with\.
You must specify the `InstanceId` or `Targets` property\.
*Required*: Conditional
*Type*: String
*Pattern*: `(^i-(\w{8}|\w{17})$)|(^mi-\w{17}$)`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-ssm-association-name"></a>
The name of the Systems Manager document\.
*Required*: Yes
*Type*: String
*Pattern*: `^[a-zA-Z0-9_\-.:/]{3,128}$`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutputLocation`  <a name="cfn-ssm-association-outputlocation"></a>
An Amazon S3 bucket where you want to store the output details of the request\.
*Required*: No
*Type*: [InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-ssm-association-parameters"></a>
The parameters for the runtime configuration of the document\.
*Required*: No
*Type*: Map of [ParameterValues](aws-properties-ssm-association-parametervalues.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-ssm-association-scheduleexpression"></a>
A cron expression that specifies a schedule when the association runs\.
*Required*: No
*Type*: String
*Minimum*: `1`
*Maximum*: `256`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-ssm-association-targets"></a>
The targets that the SSM document sends commands to\.
You must specify the `InstanceId` or `Targets` property\.
*Required*: Conditional
*Type*: List of [Target](aws-properties-ssm-association-target.md)
*Maximum*: `5`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Examples<a name="aws-resource-ssm-association--examples"></a>

### Associate a Systems Manager document with a specific instance<a name="aws-resource-ssm-association--examples--Associate_a_Systems_Manager_document_with_a_specific_instance"></a>

The following example associates an SSM document with a specific instance\. The ID of the instance is specified by the `myInstanceId` parameter\.

#### JSON<a name="aws-resource-ssm-association--examples--Associate_a_Systems_Manager_document_with_a_specific_instance--json"></a>

```
"association": {
  "Type": "AWS::SSM::Association",
  "Properties": {
    "Name": {
      "Ref": "document"
    },
    "Parameters": {
      "Directory": ["myWorkSpace"]
    },
    "Targets": [{
      "Key": "InstanceIds",
      "Values": [{
        "Ref": "myInstanceId"
      }]
    }]
  }
}
```

#### YAML<a name="aws-resource-ssm-association--examples--Associate_a_Systems_Manager_document_with_a_specific_instance--yaml"></a>

```
association:
  Type: AWS::SSM::Association
  Properties:
    Name: !Ref 'document'
    Parameters:
      Directory: ["myWorkSpace"]
    Targets:
    - Key: InstanceIds
      Values: [!Ref 'myInstanceId']
```

## See Also<a name="aws-resource-ssm-association--seealso"></a>
+  [Reference: Cron and Rate Expressions for Systems Manager](https://docs.aws.amazon.com/systems-manager/latest/userguide/reference-cron-and-rate-expressions.html)
