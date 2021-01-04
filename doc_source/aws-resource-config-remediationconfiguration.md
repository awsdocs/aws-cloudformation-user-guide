# AWS::Config::RemediationConfiguration<a name="aws-resource-config-remediationconfiguration"></a>

An object that represents the details about the remediation configuration that includes the remediation action, parameters, and data to execute the action\.

## Syntax<a name="aws-resource-config-remediationconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-remediationconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::Config::RemediationConfiguration",
  "Properties" : {
      "[Automatic](#cfn-config-remediationconfiguration-automatic)" : Boolean,
      "[ConfigRuleName](#cfn-config-remediationconfiguration-configrulename)" : String,
      "[ExecutionControls](#cfn-config-remediationconfiguration-executioncontrols)" : ExecutionControls,
      "[MaximumAutomaticAttempts](#cfn-config-remediationconfiguration-maximumautomaticattempts)" : Integer,
      "[Parameters](#cfn-config-remediationconfiguration-parameters)" : Json,
      "[ResourceType](#cfn-config-remediationconfiguration-resourcetype)" : String,
      "[RetryAttemptSeconds](#cfn-config-remediationconfiguration-retryattemptseconds)" : Integer,
      "[TargetId](#cfn-config-remediationconfiguration-targetid)" : String,
      "[TargetType](#cfn-config-remediationconfiguration-targettype)" : String,
      "[TargetVersion](#cfn-config-remediationconfiguration-targetversion)" : String
    }
}
```

### YAML<a name="aws-resource-config-remediationconfiguration-syntax.yaml"></a>

```
Type: AWS::Config::RemediationConfiguration
Properties: 
  [Automatic](#cfn-config-remediationconfiguration-automatic): Boolean
  [ConfigRuleName](#cfn-config-remediationconfiguration-configrulename): String
  [ExecutionControls](#cfn-config-remediationconfiguration-executioncontrols): 
    ExecutionControls
  [MaximumAutomaticAttempts](#cfn-config-remediationconfiguration-maximumautomaticattempts): Integer
  [Parameters](#cfn-config-remediationconfiguration-parameters): Json
  [ResourceType](#cfn-config-remediationconfiguration-resourcetype): String
  [RetryAttemptSeconds](#cfn-config-remediationconfiguration-retryattemptseconds): Integer
  [TargetId](#cfn-config-remediationconfiguration-targetid): String
  [TargetType](#cfn-config-remediationconfiguration-targettype): String
  [TargetVersion](#cfn-config-remediationconfiguration-targetversion): String
```

## Properties<a name="aws-resource-config-remediationconfiguration-properties"></a>

`Automatic`  <a name="cfn-config-remediationconfiguration-automatic"></a>
The remediation is triggered automatically\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConfigRuleName`  <a name="cfn-config-remediationconfiguration-configrulename"></a>
The name of the AWS Config rule\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ExecutionControls`  <a name="cfn-config-remediationconfiguration-executioncontrols"></a>
An ExecutionControls object\.  
*Required*: No  
*Type*: [ExecutionControls](aws-properties-config-remediationconfiguration-executioncontrols.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MaximumAutomaticAttempts`  <a name="cfn-config-remediationconfiguration-maximumautomaticattempts"></a>
The maximum number of failed attempts for auto\-remediation\. If you do not select a number, the default is 5\.  
For example, if you specify MaximumAutomaticAttempts as 5 with RetryAttemptSeconds as 50 seconds, AWS Config will put a RemediationException on your behalf for the failing resource after the 5th failed attempt within 50 seconds\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Parameters`  <a name="cfn-config-remediationconfiguration-parameters"></a>
An object of the RemediationParameterValue\.  
The type is a map of strings to RemediationParameterValue\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-config-remediationconfiguration-resourcetype"></a>
The type of a resource\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetryAttemptSeconds`  <a name="cfn-config-remediationconfiguration-retryattemptseconds"></a>
Maximum time in seconds that AWS Config runs auto\-remediation\. If you do not select a number, the default is 60 seconds\.   
For example, if you specify RetryAttemptSeconds as 50 seconds and MaximumAutomaticAttempts as 5, AWS Config will run auto\-remediations 5 times within 50 seconds before throwing an exception\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetId`  <a name="cfn-config-remediationconfiguration-targetid"></a>
Target ID is the name of the public document\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetType`  <a name="cfn-config-remediationconfiguration-targettype"></a>
The type of the target\. Target executes remediation\. For example, SSM document\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `SSM_DOCUMENT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetVersion`  <a name="cfn-config-remediationconfiguration-targetversion"></a>
Version of the target\. For example, version of the SSM document\.  
If you make backward incompatible changes to the SSM document, you must call PutRemediationConfiguration API again to ensure the remediations can run\.
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-config-remediationconfiguration-return-values"></a>

### Ref<a name="aws-resource-config-remediationconfiguration-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the remediation action with the associated SSM document\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-config-remediationconfiguration--examples"></a>



### Remeditation Configuration<a name="aws-resource-config-remediationconfiguration--examples--Remeditation_Configuration"></a>

The following example creates a remediation configuration using AWS Systems Manager document\.

#### JSON<a name="aws-resource-config-remediationconfiguration--examples--Remeditation_Configuration--json"></a>

```
{
    "BasicRemediationConfiguration": {
        "Type": "AWS::Config::RemediationConfiguration",
        "Properties": {
            "ConfigRuleName": "configRuleName",
            "Parameters": {
                "AutomationAssumeRole": {
                    "StaticValue": {
                        "Values": [
                            "automationAssumeRole"
                        ]
                    }
                },
                "InstanceId": {
                    "StaticValue": {
                        "Values": [
                            "instanceId"
                        ]
                    }
                }
            },
            "TargetId": "AWS-StartEC2Instance",
            "TargetType": "SSM_DOCUMENT",
            "TargetVersion": "1"
        }
    }
}
```

#### YAML<a name="aws-resource-config-remediationconfiguration--examples--Remeditation_Configuration--yaml"></a>

```
BasicRemediationConfiguration:
    Type: "AWS::Config::RemediationConfiguration"
    Properties:
        ConfigRuleName: configRuleName
        Parameters:
            AutomationAssumeRole:
                StaticValue:
                    Values: 
                    - automationAssumeRole
            InstanceId:
                StaticValue:
                    Values:
                        - instanceId
        TargetId: "AWS-StartEC2Instance"
        TargetType: "SSM_DOCUMENT"
        TargetVersion: "1"
```