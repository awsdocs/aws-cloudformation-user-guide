# AWS::StepFunctions::StateMachine<a name="aws-resource-stepfunctions-statemachine"></a>

Use the `AWS::StepFunctions::StateMachine` resource to create an AWS Step Functions state machine\.

For information about creating state machines, see [Tutorial: A Lambda State Machine](http://docs.aws.amazon.com/step-functions/latest/dg/hello-lambda.html) in the *AWS Step Functions Developer Guide* and `[CreateStateMachine](http://docs.aws.amazon.com/step-functions/latest/apireference/API_CreateStateMachine.html)` in the *AWS Step Functions API Reference*\.

## Syntax<a name="aws-resource-stepfunctions-statemachine-syntax"></a>

### JSON<a name="aws-resource-stepfunctions-statemachine-syntax-json"></a>

```
{
   "Type": "AWS::StepFunctions::StateMachine",
   "Properties": {
      "[StateMachineName](#cfn-stepfunctions-statemachine-definitionname)": String,
      "[DefinitionString](#cfn-stepfunctions-statemachine-definitionstring)": String,
      "[RoleArn](#cfn-stepfunctions-statemachine-rolearn)": String
    }
}
```

### YAML<a name="aws-resource-stepfunctions-statemachine-syntax-yaml"></a>

```
Type: "AWS::StepFunctions::StateMachine"
Properties:
  [StateMachineName](#cfn-stepfunctions-statemachine-definitionname): String
  [DefinitionString](#cfn-stepfunctions-statemachine-definitionstring): String
  [RoleArn](#cfn-stepfunctions-statemachine-rolearn): String
```

## Properties<a name="aws-resource-stepfunctions-statemachine-properties"></a>

`StateMachineName`  <a name="cfn-stepfunctions-statemachine-definitionname"></a>
The name of the state machine\. If you do not specify a name one will be generated that is similar to `MyStateMachine-1234abcdefgh`\. For more information on creating a valid name see [Request Parameters](http://docs.aws.amazon.com/step-functions/latest/apireference/API_CreateStateMachine.html#API_CreateStateMachine_RequestSyntax) in the *AWS Step Functions API Reference*\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`DefinitionString`  <a name="cfn-stepfunctions-statemachine-definitionstring"></a>
The Amazon States Language definition of the state machine\. For more information, see [Amazon States Language](http://docs.aws.amazon.com/step-functions/latest/dg/concepts-awl.html) in the *AWS Step Functions Developer Guide*\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RoleArn`  <a name="cfn-stepfunctions-statemachine-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role to use for this state machine\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-stepfunctions-statemachine-returnvalues"></a>

### Ref<a name="aws-resource-stepfunctions-statemachine-returnvalues-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` returns the ARN of the created state machine\. For example:

```
{ "Ref": "MyStateMachine" }
```

Returns a value similar to the following:

```
arn:aws:states:us-east-1:111122223333:stateMachine:HelloWorld-StateMachine
```

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-stepfunctions-statemachine-returnvalues-getatt"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Name`  
Returns the name of the state machine\. For example:  

```
{ "Fn::GetAtt": ["MyStateMachine", "Name"] }
```
Returns the name of your state machine:  

```
HelloWorld-StateMachine
```
If you did not specify the name it will be similar to the following:  

```
MyStateMachine-1234abcdefgh
```

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="aws-resource-stepfunctions-statemachine-examples"></a>

The following examples create a Step Functions state machine\.

### JSON<a name="aws-resource-stepfunctions-statemachine-specifying-example-json"></a>

#### Using a Single\-Line Property<a name="stepfunctions-statemachine-single-line-property"></a>

```
{
   "AWSTemplateFormatVersion" : "2010-09-09",
   "Description" : "An example template for a Step Functions state machine.",
   "Resources" : {
      "MyStateMachine" : {
         "Type" : "AWS::StepFunctions::StateMachine",
         "Properties" : {
            "StateMachineName" : "HelloWorld-StateMachine",
            "DefinitionString" : "{\"StartAt\": \"HelloWorld\", \"States\": {\"HelloWorld\": {\"Type\": \"Task\", \"Resource\": \"arn:aws:lambda:us-east-1:111122223333:function:HelloFunction\", \"End\": true}}}",
            "RoleArn" : "arn:aws:iam::111122223333:role/service-role/StatesExecutionRole-us-east-1"
         }
      }
   }
}
```

#### Using the Fn::Join Intrinsic Function<a name="stepfunctions-statemachine-join"></a>

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
   	      "RoleArn" : "arn:aws:iam::111122223333:role/service-role/StatesExecutionRole-us-east-1"
            }
        }
    }
}
```

### YAML<a name="aws-resource-stepfunctions-statemachine-specifying-example-yaml"></a>

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
```