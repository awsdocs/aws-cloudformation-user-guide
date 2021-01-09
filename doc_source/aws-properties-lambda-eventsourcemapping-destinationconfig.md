# AWS::Lambda::EventSourceMapping DestinationConfig<a name="aws-properties-lambda-eventsourcemapping-destinationconfig"></a>

\(Streams\) An Amazon SQS queue or Amazon SNS topic destination for discarded records\.

## Syntax<a name="aws-properties-lambda-eventsourcemapping-destinationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-eventsourcemapping-destinationconfig-syntax.json"></a>

```
{
  "[OnFailure](#cfn-lambda-eventsourcemapping-destinationconfig-onfailure)" : OnFailure
}
```

### YAML<a name="aws-properties-lambda-eventsourcemapping-destinationconfig-syntax.yaml"></a>

```
  [OnFailure](#cfn-lambda-eventsourcemapping-destinationconfig-onfailure): 
    OnFailure
```

## Properties<a name="aws-properties-lambda-eventsourcemapping-destinationconfig-properties"></a>

`OnFailure`  <a name="cfn-lambda-eventsourcemapping-destinationconfig-onfailure"></a>
The destination configuration for failed invocations\.  
*Required*: No  
*Type*: [OnFailure](aws-properties-lambda-eventsourcemapping-onfailure.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-eventsourcemapping-destinationconfig--examples"></a>



### On\-Failure Destination Configuration<a name="aws-properties-lambda-eventsourcemapping-destinationconfig--examples--On-Failure_Destination_Configuration"></a>

Configure a function to send a record of failed batches to an SQS queue\.

#### YAML<a name="aws-properties-lambda-eventsourcemapping-destinationconfig--examples--On-Failure_Destination_Configuration--yaml"></a>

```
      DestinationConfig:
          OnFailure:
            Destination: arn:aws:sqs:us-east-2:123456789012:dlq
```