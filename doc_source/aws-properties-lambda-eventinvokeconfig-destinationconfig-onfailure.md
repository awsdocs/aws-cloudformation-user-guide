# AWS::Lambda::EventInvokeConfig OnFailure<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure"></a>

A destination for events that failed processing\.

## Syntax<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure-syntax.json"></a>

```
{
  "[Destination](#cfn-lambda-eventinvokeconfig-destinationconfig-onfailure-destination)" : String
}
```

### YAML<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure-syntax.yaml"></a>

```
  [Destination](#cfn-lambda-eventinvokeconfig-destinationconfig-onfailure-destination): String
```

## Properties<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure-properties"></a>

`Destination`  <a name="cfn-lambda-eventinvokeconfig-destinationconfig-onfailure-destination"></a>
The Amazon Resource Name \(ARN\) of the destination resource\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `350`  
*Pattern*: `^$|arn:(aws[a-zA-Z0-9-]*):([a-zA-Z0-9\-])+:([a-z]{2}(-gov)?-[a-z]+-\d{1})?:(\d{12})?:(.*)`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure--examples"></a>



### On\-Failure Destination Configuration<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure--examples--On-Failure_Destination_Configuration"></a>

Configure a function to send a record of failed asynchronous invocations to an SQS queue\.

#### YAML<a name="aws-properties-lambda-eventinvokeconfig-destinationconfig-onfailure--examples--On-Failure_Destination_Configuration--yaml"></a>

```
          OnFailure:
            Destination: arn:aws:sqs:us-east-2:123456789012:dlq
```