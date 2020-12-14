# AWS::Lambda::EventSourceMapping OnFailure<a name="aws-properties-lambda-eventsourcemapping-onfailure"></a>

A destination for events that failed processing\.

## Syntax<a name="aws-properties-lambda-eventsourcemapping-onfailure-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-onfailure-syntax.json"></a>

```
{
  "[Destination](#cfn-lambda-eventsourcemapping-onfailure-destination)" : String
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-onfailure-syntax.yaml"></a>

```
  [Destination](#cfn-lambda-eventsourcemapping-onfailure-destination): String
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-onfailure-properties"></a>

`Destination`  <a name="cfn-lambda-eventsourcemapping-onfailure-destination"></a>
The Amazon Resource Name \(ARN\) of the destination resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-eventsourcemapping-onfailure--examples"></a>



### On\-Failure Destination Configuration<a name="aws-properties-lambda-eventsourcemapping-onfailure--examples--On-Failure_Destination_Configuration"></a>

Configure a function to send a record of failed batches to an SQS queue\.

#### YAML<a name="aws-properties-lambda-eventsourcemapping-onfailure--examples--On-Failure_Destination_Configuration--yaml"></a>

```
          OnFailure:
            Destination: arn:aws:sqs:us-east-2:123456789012:dlq
```