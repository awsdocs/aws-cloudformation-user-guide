# AWS::SSM::Association<a name="aws-resource-ssm-association"></a>

The `AWS::SSM::Association` resource associates an Amazon EC2 Systems Manager \(SSM\) document with EC2 instances that contain a configuration agent to process the document\.


+ [Syntax](#aws-resource-ssm-association-syntax)
+ [Properties](#w3ab2c21c10e1005b9)
+ [Example](#w3ab2c21c10e1005c11)

## Syntax<a name="aws-resource-ssm-association-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssm-association-syntax.json"></a>

```
{
  "Type" : "AWS::SSM::Association",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-documentationversion)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-instanceid)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-parameters)" : { String: [String, ...] },
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-scheduleexpression)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-targets)" : [ Targets ]
  }
}
```

### YAML<a name="aws-resource-ssm-association-syntax.yaml"></a>

```
Type: "AWS::SSM::Association"
Properties: 
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-documentationversion): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-instanceid): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-parameters):
    String:
      - String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-scheduleexpression): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-ssm-association-targets):
    - Targets
```

## Properties<a name="w3ab2c21c10e1005b9"></a>

`DocumentVersion`  
The version of the SSM document to associate with the target\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`InstanceId`  
The ID of the instance that the SSM document is associated with\.  
*Required: *Conditional\. You must specify the `InstanceId` or `Targets` property\.  
*Type*: String  
*Update requires*: Replacement

`Name`  
The name of the SSM document\.  
*Required: *Yes  
*Type*: String  
*Update requires*: Replacement

`Parameters`  
Parameter values that the SSM document uses at runtime\.  
*Required: *No  
*Type*: String to list\-of\-strings map  
*Update requires*: No interruption

`ScheduleExpression`  
A Cron expression that specifies when the association is applied to the target\. For more on working with Cron expressions, see [Working with Cron and Rate Expressions for Systems Manager](http://docs.aws.amazon.com/systems-manager/latest/userguide/sysman-cron.html)\.  
*Required: *No  
*Type*: String  
*Update requires*: No interruption

`Targets`  
The targets that the SSM document sends commands to\.  
*Required: *Conditional\. You must specify the `InstanceId` or `Targets` property\.  
*Type*: List of [Amazon EC2 Systems Manager Association Targets](aws-properties-ssm-association-targets.md)  
*Update requires*: Replacement

## Example<a name="w3ab2c21c10e1005c11"></a>

### <a name="w3ab2c21c10e1005c11b2"></a>

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