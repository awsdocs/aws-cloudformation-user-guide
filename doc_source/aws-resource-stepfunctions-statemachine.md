# AWS::StepFunctions::StateMachine<a name="aws-resource-stepfunctions-statemachine"></a>

Provisions a state machine\. A state machine consists of a collection of states that can do work \(`Task` states\), determine to which states to transition next \(`Choice` states\), stop an execution with an error \(`Fail` states\), and so on\. State machines are specified using a JSON\-based, structured language\.

## Syntax<a name="aws-resource-stepfunctions-statemachine-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-stepfunctions-statemachine-syntax.json"></a>

```
{
  "Type" : "AWS::StepFunctions::StateMachine",
  "Properties" : {
      "[DefinitionS3Location](#cfn-stepfunctions-statemachine-definitions3location)" : S3Location,
      "[DefinitionString](#cfn-stepfunctions-statemachine-definitionstring)" : String,
      "[DefinitionSubstitutions](#cfn-stepfunctions-statemachine-definitionsubstitutions)" : DefinitionSubstitutions,
      "[LoggingConfiguration](#cfn-stepfunctions-statemachine-loggingconfiguration)" : LoggingConfiguration,
      "[RoleArn](#cfn-stepfunctions-statemachine-rolearn)" : String,
      "[StateMachineName](#cfn-stepfunctions-statemachine-statemachinename)" : String,
      "[StateMachineType](#cfn-stepfunctions-statemachine-statemachinetype)" : String,
      "[Tags](#cfn-stepfunctions-statemachine-tags)" : [ TagsEntry, ... ],
      "[TracingConfiguration](#cfn-stepfunctions-statemachine-tracingconfiguration)" : TracingConfiguration
    }
}
```

### YAML<a name="aws-resource-stepfunctions-statemachine-syntax.yaml"></a>

```
Type: AWS::StepFunctions::StateMachine
Properties: 
  [DefinitionS3Location](#cfn-stepfunctions-statemachine-definitions3location): 
    S3Location
  [DefinitionString](#cfn-stepfunctions-statemachine-definitionstring): 
    String
  [DefinitionSubstitutions](#cfn-stepfunctions-statemachine-definitionsubstitutions): 
    DefinitionSubstitutions
  [LoggingConfiguration](#cfn-stepfunctions-statemachine-loggingconfiguration): 
    LoggingConfiguration
  [RoleArn](#cfn-stepfunctions-statemachine-rolearn): String
  [StateMachineName](#cfn-stepfunctions-statemachine-statemachinename): String
  [StateMachineType](#cfn-stepfunctions-statemachine-statemachinetype): String
  [Tags](#cfn-stepfunctions-statemachine-tags): 
    - TagsEntry
  [TracingConfiguration](#cfn-stepfunctions-statemachine-tracingconfiguration): 
    TracingConfiguration
```

## Properties<a name="aws-resource-stepfunctions-statemachine-properties"></a>

`DefinitionS3Location`  <a name="cfn-stepfunctions-statemachine-definitions3location"></a>
The name of the S3 bucket where the state machine definition is stored\. The state machine definition must be a JSON file\.  
*Required*: No  
*Type*: [S3Location](aws-properties-stepfunctions-statemachine-s3location.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefinitionString`  <a name="cfn-stepfunctions-statemachine-definitionstring"></a>
The Amazon States Language definition of the state machine\. See [Amazon States Language](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-amazon-states-language.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefinitionSubstitutions`  <a name="cfn-stepfunctions-statemachine-definitionsubstitutions"></a>
A map \(string to string\) that specifies the mappings for placeholder variables in the state machine definition\. This enables the customer to inject values obtained at runtime, for example from intrinsic functions, in the state machine definition\. Variables can be template parameter names, resource logical IDs, resource attributes, or a variable in a key\-value map\.   
*Required*: No  
*Type*: [DefinitionSubstitutions](aws-properties-stepfunctions-statemachine-definitionsubstitutions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingConfiguration`  <a name="cfn-stepfunctions-statemachine-loggingconfiguration"></a>
Defines what execution history events are logged and where they are logged\.  
By default, the `level` is set to `OFF`\. For more information see [Log Levels](https://docs.aws.amazon.com/step-functions/latest/dg/cloudwatch-log-level.html) in the AWS Step Functions User Guide\.
*Required*: No  
*Type*: [LoggingConfiguration](aws-properties-stepfunctions-statemachine-loggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-stepfunctions-statemachine-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to use for this state machine\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StateMachineName`  <a name="cfn-stepfunctions-statemachine-statemachinename"></a>
The name of the state machine\.   
A name must *not* contain:  
+ white space
+ brackets `< > { } [ ]` 
+ wildcard characters `? *` 
+ special characters `" # % \ ^ | ~ ` $ & , ; : /` 
+ control characters \(`U+0000-001F`, `U+007F-009F`\)
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StateMachineType`  <a name="cfn-stepfunctions-statemachine-statemachinetype"></a>
Determines whether a `STANDARD` or `EXPRESS` state machine is created\. The default is `STANDARD`\. You cannot update the `type` of a state machine once it has been created\. For more information on `STANDARD` and `EXPRESS` workflows, see [Standard Versus Express Workflows](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-standard-vs-express.html) in the AWS Step Functions Developer Guide\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-stepfunctions-statemachine-tags"></a>
The list of tags to add to a resource\.  
Tags may only contain Unicode letters, digits, white space, or these symbols: `_ . : / = + - @`\.  
*Required*: No  
*Type*: List of [TagsEntry](aws-properties-stepfunctions-statemachine-tagsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TracingConfiguration`  <a name="cfn-stepfunctions-statemachine-tracingconfiguration"></a>
Selects whether or not the state machine's AWS X\-Ray tracing is enabled\.  
*Required*: No  
*Type*: [TracingConfiguration](aws-properties-stepfunctions-statemachine-tracingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-stepfunctions-statemachine-return-values"></a>

### Ref<a name="aws-resource-stepfunctions-statemachine-return-values-ref"></a>

When you provide the logical ID of this resource to the Ref intrinsic function, Ref returns the ARN of the created state machine\. For example:

 `{ "Ref": "MyStateMachine" }`Guide 

Returns a value similar to the following:

 `arn:aws:states:us-east-1:111122223333:stateMachine:HelloWorld-StateMachine` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-stepfunctions-statemachine-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-stepfunctions-statemachine-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.

`Name`  <a name="Name-fn::getatt"></a>
Returns the name of the state machine\. For example:  
 `{ "Fn::GetAtt": ["MyStateMachine", "Name"] }`   
Returns the name of your state machine:  
 `HelloWorld-StateMachine`   
If you did not specify the name it will be similar to the following:  
 `MyStateMachine-1234abcdefgh`   
For more information about using `Fn::GetAtt`, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

## Examples<a name="aws-resource-stepfunctions-statemachine--examples"></a>

The following examples create a Step Functions state machine\.

### Using a Single\-Line Property<a name="aws-resource-stepfunctions-statemachine--examples--Using_a_Single-Line_Property"></a>

#### JSON<a name="aws-resource-stepfunctions-statemachine--examples--Using_a_Single-Line_Property--json"></a>

```
{  
   "AWSTemplateFormatVersion":"2010-09-09",
   "Description":"An example template for a Step Functions state machine.",
   "Resources":{  
      "MyStateMachine":{  
         "Type":"AWS::StepFunctions::StateMachine",
         "Properties":{  
            "StateMachineName":"HelloWorld-StateMachine",
            "StateMachineType":"STANDARD",
            "DefinitionString":"{\"StartAt\": \"HelloWorld\", 
            \"States\": {\"HelloWorld\": {\"Type\": \"Task\", \"Resource\": 
            \"arn:aws:lambda:us-east-1:111122223333;:function:HelloFunction\", \"End\": true}}}",
            "RoleArn":"arn:aws:iam::111122223333:role/service-role/StatesExecutionRole-us-east-1;"
         }
      }
   }
}
```

### Using the Fn::Join Intrinsic Function<a name="aws-resource-stepfunctions-statemachine--examples--Using_the_Fn::Join_Intrinsic_Function"></a>

#### JSON<a name="aws-resource-stepfunctions-statemachine--examples--Using_the_Fn::Join_Intrinsic_Function--json"></a>

```
{
    "AWSTemplateFormatVersion" : "2010-09-09",
    "Description" : "An example template for a Step Functions state machine.",
    "Resources": {
       "MyStateMachine": {
          "Type": "AWS::StepFunctions::StateMachine",
             "Properties": {
                "StateMachineName" : "HelloWorld-StateMachine",
                "StateMachineType":"STANDARD",
                "DefinitionString" : {
                   "Fn::Join": [
                      "\n",
                      [
                         "{",
                         "    \"StartAt\": \"HelloWorld\",",
                         "    \"States\" : {",
                         "        \"HelloWorld\" : {",
                         "            \"Type\" : \"Task\", ",
                         "            \"Resource\" : \"arn:aws:lambda:us-east-1:111122223333:function:HelloFunction\",",
                         "            \"End\" : true",
                         "        }",
                         "    }",
                         "}"
                      ]
                   ]
                },
   	      "RoleArn" : "arn:aws:iam::111122223333:role/service-role/StatesExecutionRole-us-east-1",
            "Tags": [
                    {
                        "Key": "keyname1",
                        "Value": "value1"
                    },
                    {
                        "Key": "keyname2",
                        "Value": "value2"
                    }
                ] 
            }
        }
    }
}
```

### Including Tags<a name="aws-resource-stepfunctions-statemachine--examples--Including_Tags"></a>

#### YAML<a name="aws-resource-stepfunctions-statemachine--examples--Including_Tags--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: An example template for a Step Functions state machine.
Resources:
  MyStateMachine:
    Type: AWS::StepFunctions::StateMachine
    Properties:
      StateMachineName: HelloWorld-StateMachine
      DefinitionString: |-
        {
          "StartAt": "HelloWorld",
          "States": {
            "HelloWorld": {
              "Type": "Task",
              "Resource": "arn:aws:lambda:us-east-1:111122223333:function:HelloFunction",
              "End": true
            }
          }
        }
      RoleArn: arn:aws:iam::111122223333:role/service-role/StatesExecutionRole-us-east-1
      Tags:
        -
          Key: "keyname1"
          Value: "value1"
        -
          Key: "keyname2"
          Value: "value2"
```

### Using DefinitionSubstitutions<a name="aws-resource-stepfunctions-statemachine--examples--Using_DefinitionSubstitutions"></a>

In this example template, `HelloFunction:` is defined for the `DefinitionSubstitutions` property\. In the `hello_world.json` definition file, that follows`${HelloFunction}` will be replaced by `arn:aws:lambda:us-east-1:111122223333:function:HelloFunction`\.

#### YAML<a name="aws-resource-stepfunctions-statemachine--examples--Using_DefinitionSubstitutions--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Description: An example template for a Step Functions state machine.
  Resources:
    MyStateMachine:
      Type: AWS::StepFunctions::StateMachine
      Properties:
        StateMachineName: HelloWorld-StateMachine
        DefinitionS3Location:
          Bucket: example_bucket
          Key: hello_world.json
        DefinitionSubstitutions:
          HelloFunction: arn:aws:lambda:us-east-1:111122223333:function:HelloFunction
        RoleArn: arn:aws:iam::111122223333:role/service-role/StatesExecutionRole-us-east-1
```

### hello\_world\.json<a name="aws-resource-stepfunctions-statemachine--examples--hello_world.json"></a>

 A definition file where `${HelloFunction}` will be replaced by `arn:aws:lambda:us-east-1:111122223333:function:HelloFunction`\. from the preceding example template\.

#### JSON<a name="aws-resource-stepfunctions-statemachine--examples--hello_world.json--json"></a>

```
{
  "StartAt": "HelloWorld",
  "States": {
    "HelloWorld": {
      "Type": "Task",
      "Resource": "${HelloFunction}",
      "End": true
    }
  }
}
```