# AWS::Pipes::Pipe<a name="aws-resource-pipes-pipe"></a>

Create a pipe\. Amazon EventBridge Pipes connect event sources to targets and reduces the need for specialized knowledge and integration code\.

## Syntax<a name="aws-resource-pipes-pipe-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-pipes-pipe-syntax.json"></a>

```
{
  "Type" : "AWS::Pipes::Pipe",
  "Properties" : {
      "[Description](#cfn-pipes-pipe-description)" : String,
      "[DesiredState](#cfn-pipes-pipe-desiredstate)" : String,
      "[Enrichment](#cfn-pipes-pipe-enrichment)" : String,
      "[EnrichmentParameters](#cfn-pipes-pipe-enrichmentparameters)" : PipeEnrichmentParameters,
      "[Name](#cfn-pipes-pipe-name)" : String,
      "[RoleArn](#cfn-pipes-pipe-rolearn)" : String,
      "[Source](#cfn-pipes-pipe-source)" : String,
      "[SourceParameters](#cfn-pipes-pipe-sourceparameters)" : PipeSourceParameters,
      "[Tags](#cfn-pipes-pipe-tags)" : {Key : Value, ...},
      "[Target](#cfn-pipes-pipe-target)" : String,
      "[TargetParameters](#cfn-pipes-pipe-targetparameters)" : PipeTargetParameters
    }
}
```

### YAML<a name="aws-resource-pipes-pipe-syntax.yaml"></a>

```
Type: AWS::Pipes::Pipe
Properties: 
  [Description](#cfn-pipes-pipe-description): String
  [DesiredState](#cfn-pipes-pipe-desiredstate): String
  [Enrichment](#cfn-pipes-pipe-enrichment): String
  [EnrichmentParameters](#cfn-pipes-pipe-enrichmentparameters): 
    PipeEnrichmentParameters
  [Name](#cfn-pipes-pipe-name): String
  [RoleArn](#cfn-pipes-pipe-rolearn): String
  [Source](#cfn-pipes-pipe-source): String
  [SourceParameters](#cfn-pipes-pipe-sourceparameters): 
    PipeSourceParameters
  [Tags](#cfn-pipes-pipe-tags): 
    Key : Value
  [Target](#cfn-pipes-pipe-target): String
  [TargetParameters](#cfn-pipes-pipe-targetparameters): 
    PipeTargetParameters
```

## Properties<a name="aws-resource-pipes-pipe-properties"></a>

`Description`  <a name="cfn-pipes-pipe-description"></a>
A description of the pipe\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DesiredState`  <a name="cfn-pipes-pipe-desiredstate"></a>
The state the pipe should be in\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Enrichment`  <a name="cfn-pipes-pipe-enrichment"></a>
The ARN of the enrichment resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnrichmentParameters`  <a name="cfn-pipes-pipe-enrichmentparameters"></a>
The parameters required to set up enrichment on your pipe\.  
*Required*: No  
*Type*: [PipeEnrichmentParameters](aws-properties-pipes-pipe-pipeenrichmentparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-pipes-pipe-name"></a>
The name of the pipe\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-pipes-pipe-rolearn"></a>
The ARN of the role that allows the pipe to send data to the target\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Source`  <a name="cfn-pipes-pipe-source"></a>
The ARN of the source resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceParameters`  <a name="cfn-pipes-pipe-sourceparameters"></a>
The parameters required to set up a source for your pipe\.  
*Required*: No  
*Type*: [PipeSourceParameters](aws-properties-pipes-pipe-pipesourceparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-pipes-pipe-tags"></a>
The list of key\-value pairs to associate with the pipe\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Target`  <a name="cfn-pipes-pipe-target"></a>
The ARN of the target resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetParameters`  <a name="cfn-pipes-pipe-targetparameters"></a>
The parameters required to set up a target for your pipe\.  
For more information about pipe target parameters, including how to use dynamic path parameters, see [Target parameters](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-pipes-event-target.html) in the *Amazon EventBridge User Guide*\.  
*Required*: No  
*Type*: [PipeTargetParameters](aws-properties-pipes-pipe-pipetargetparameters.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-pipes-pipe-return-values"></a>

### Ref<a name="aws-resource-pipes-pipe-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the pipe that was created by the request\.

### Fn::GetAtt<a name="aws-resource-pipes-pipe-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-pipes-pipe-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the pipe\.

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The time the pipe was created\.

`CurrentState`  <a name="CurrentState-fn::getatt"></a>
The state the pipe is in\.

`LastModifiedTime`  <a name="LastModifiedTime-fn::getatt"></a>
When the pipe was last updated, in [ISO\-8601 format](https://www.w3.org/TR/NOTE-datetime) \(YYYY\-MM\-DDThh:mm:ss\.sTZD\)\.

`StateReason`  <a name="StateReason-fn::getatt"></a>
The reason the pipe is in its current state\.

## Examples<a name="aws-resource-pipes-pipe--examples"></a>



### Create a Pipe with an enrichment<a name="aws-resource-pipes-pipe--examples--Create_a_Pipe_with_an_enrichment"></a>

Create a Pipe with an Amazon SQS source, an API Gateway enrichment, and a Step Functions state machine target\.

#### JSON<a name="aws-resource-pipes-pipe--examples--Create_a_Pipe_with_an_enrichment--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources": {
    "TestPipe": {
      "Type": "AWS::Pipes::Pipe",
      "Properties": {
        "Name": "PipeCfnExample",
        "RoleArn": "arn:aws:iam::123456789123:role/Pipe-Dev-All-Targets-Dummy-Execution-Role",
        "Source": "arn:aws:sqs:us-east-1:123456789123:pipeDemoSource",
        "Enrichment": "arn:aws:execute-api:us-east-1:123456789123:53eo2i89p9/*/POST/pets",
        "Target": "arn:aws:states:us-east-1:123456789123:stateMachine:PipeTargetStateMachine"
      }
    }
  }
}
```

#### YAML<a name="aws-resource-pipes-pipe--examples--Create_a_Pipe_with_an_enrichment--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  TestPipe:
    Type: AWS::Pipes::Pipe
    Properties:
      Name:  PipeCfnExample
      RoleArn: arn:aws:iam::123456789123:role/Pipe-Dev-All-Targets-Dummy-Execution-Role
      Source: arn:aws:sqs:us-east-1:123456789123:pipeDemoSource
      Enrichment: arn:aws:execute-api:us-east-1:123456789123:53eo2i89p9/*/POST/pets
      Target: arn:aws:states:us-east-1:123456789123:stateMachine:PipeTargetStateMachine
```