# AWS::SSM::Association<a name="aws-resource-ssm-association"></a>

The `AWS::SSM::Association` resource associates an SSM document in AWS Systems Manager with EC2 instances that contain a configuration agent to process the document\.

**Topics**
+ [Syntax](#aws-resource-ssm-association-syntax)
+ [Properties](#w3ab2c21c10e1148b9)
+ [Example](#w3ab2c21c10e1148c11)

## Syntax<a name="aws-resource-ssm-association-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-association-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Association",
  "Properties" : {
    "[AssociationName](#cfn-ssm-association-associationname)" : String,
    "[DocumentVersion](#cfn-ssm-association-documentationversion)" : String,
    "[InstanceId](#cfn-ssm-association-instanceid)" : String,
    "[Name](#cfn-ssm-association-name)" : String,   
    "[OutputLocation](#cfn-ssm-association-outputlocation)" : [*InstanceAssociationOutputLocation*](aws-properties-ssm-association-instanceassociationoutputlocation.md) ,
    "[Parameters](#cfn-ssm-association-parameters)" : { String: [String, ...] },
    "[ScheduleExpression](#cfn-ssm-association-scheduleexpression)" : String,
    "[Targets](#cfn-ssm-association-targets)" : [ [*Targets*](aws-properties-ssm-association-targets.md) ]
  }
}
```

### YAML<a name="aws-resource-ssm-association-syntax.yaml"></a>

```
Type: "AWS::SSM::Association"
Properties: 
  [AssociationName](#cfn-ssm-association-associationname): String
  [DocumentVersion](#cfn-ssm-association-documentationversion): String
  [InstanceId](#cfn-ssm-association-instanceid): String
  [Name](#cfn-ssm-association-name): String
  [OutputLocation](#cfn-ssm-association-outputlocation): [*InstanceAssociationOutputLocation*](aws-properties-ssm-association-instanceassociationoutputlocation.md)
  [Parameters](#cfn-ssm-association-parameters):
    String:
      - String
  [ScheduleExpression](#cfn-ssm-association-scheduleexpression): String
  [Targets](#cfn-ssm-association-targets):
    - [*Targets*](aws-properties-ssm-association-targets.md)
```

## Properties<a name="w3ab2c21c10e1148b9"></a>

`AssociationName`  <a name="cfn-ssm-association-associationname"></a>
The name of the association\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`DocumentVersion`  <a name="cfn-ssm-association-documentationversion"></a>
The version of the SSM document to associate with the target\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InstanceId`  <a name="cfn-ssm-association-instanceid"></a>
The ID of the instance that the SSM document is associated with\.  
*Required*: Conditional\. You must specify the `InstanceId` or `Targets` property\.  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-ssm-association-name"></a>
The name of the SSM document\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`OutputLocation`  <a name="cfn-ssm-association-outputlocation"></a>
An Amazon S3 bucket where you want to store the results of this request\.  
*Required*: No  
*Type*: [Systems Manager Association InstanceAssociationOutputLocation](aws-properties-ssm-association-instanceassociationoutputlocation.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Parameters`  <a name="cfn-ssm-association-parameters"></a>
Parameter values that the SSM document uses at runtime\.  
*Required*: No  
*Type*: String to list\-of\-strings map  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ScheduleExpression`  <a name="cfn-ssm-association-scheduleexpression"></a>
A Cron expression that specifies when the association is applied to the target\. For more on working with Cron expressions, see [Working with Cron and Rate Expressions for Systems Manager](http://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-cron.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Targets`  <a name="cfn-ssm-association-targets"></a>
The targets that the SSM document sends commands to\.  
*Required*: Conditional\. You must specify the `InstanceId` or `Targets` property\.  
*Type*: List of [AWS Systems Manager Association Targets](aws-properties-ssm-association-targets.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Example<a name="w3ab2c21c10e1148c11"></a>

### <a name="w3ab2c21c10e1148c11b3"></a>

The following example associates an SSM document with a specific instance\. The ID of the instance is specified by the `myInstanceId` parameter\.

#### JSON<a name="aws-resource-ssm-association-example.json"></a>

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

#### YAML<a name="aws-resource-ssm-association-example.yaml"></a>

```
association:
  Type: AWS::SSM::Association
  Properties:
    Name: !Ref 'document'
    Parameters:
      Directory: [FakeDirectory]
    Targets:
    - Key: InstanceIds
      Values: [!Ref 'myInstanceId']
```