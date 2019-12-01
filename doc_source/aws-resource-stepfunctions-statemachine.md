# AWS::StepFunctions::StateMachine<a name="aws-resource-stepfunctions-statemachine"></a>

Provisions a state machine\. A state machine consists of a collection of states that can do work \(`Task` states\), determine to which states to transition next \(`Choice` states\), stop an execution with an error \(`Fail` states\), and so on\. State machines are specified using a JSON\-based, structured language\.

## Syntax<a name="aws-resource-stepfunctions-statemachine-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-stepfunctions-statemachine-syntax.json"></a>

```
{
  "Type" : "AWS::StepFunctions::StateMachine",
  "Properties" : {
      "[DefinitionString](#cfn-stepfunctions-statemachine-definitionstring)" : String,
      "[RoleArn](#cfn-stepfunctions-statemachine-rolearn)" : String,
      "[StateMachineName](#cfn-stepfunctions-statemachine-statemachinename)" : String,
      "[Tags](#cfn-stepfunctions-statemachine-tags)" : [ [TagsEntry](aws-properties-stepfunctions-statemachine-tagsentry.md), ... ]
    }
}
```

### YAML<a name="aws-resource-stepfunctions-statemachine-syntax.yaml"></a>

```
Type: AWS::StepFunctions::StateMachine
Properties: 
  [DefinitionString](#cfn-stepfunctions-statemachine-definitionstring): 
    String
  [RoleArn](#cfn-stepfunctions-statemachine-rolearn): String
  [StateMachineName](#cfn-stepfunctions-statemachine-statemachinename): String
  [Tags](#cfn-stepfunctions-statemachine-tags): 
    - [TagsEntry](aws-properties-stepfunctions-statemachine-tagsentry.md)
```

## Properties<a name="aws-resource-stepfunctions-statemachine-properties"></a>

`DefinitionString`  <a name="cfn-stepfunctions-statemachine-definitionstring"></a>
The Amazon States Language definition of the state machine\. See [Amazon States Language](https://docs.aws.amazon.com/step-functions/latest/dg/concepts-amazon-states-language.html)\.  
*Required*: Yes  
*Type*: String  
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
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-stepfunctions-statemachine-tags"></a>
The list of tags to add to a resource\.  
Tags may only contain Unicode letters, digits, white space, or these symbols: `_ . : / = + - @`\.  
*Required*: No  
*Type*: List of [TagsEntry](aws-properties-stepfunctions-statemachine-tagsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-stepfunctions-statemachine-return-values"></a>

### Ref<a name="aws-resource-stepfunctions-statemachine-return-values-ref"></a>

When you provide the logical ID of this resource to the Ref intrinsic function, Ref returns the ARN of the created state machine\. For example:

 `{ "Ref": "MyStateMachine" }`Guide 

Returns a value similar to the following:

 `arn:aws:states:us-east-1:111122223333:stateMachine:HelloWorld-StateMachine` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-stepfunctions-statemachine-return-values-fn--getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-stepfunctions-statemachine-return-values-fn--getatt-fn--getatt"></a>

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