# AWS::Kinesis::Stream StreamModeDetails<a name="aws-properties-kinesis-stream-streammodedetails"></a>

 Specifies the capacity mode to which you want to set your data stream\. Currently, in Kinesis Data Streams, you can choose between an **on\-demand** capacity mode and a **provisioned** capacity mode for your data streams\. 

## Syntax<a name="aws-properties-kinesis-stream-streammodedetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-kinesis-stream-streammodedetails-syntax.json"></a>

```
{
  "[StreamMode](#cfn-kinesis-stream-streammodedetails-streammode)" : String
}
```

### YAML<a name="aws-properties-kinesis-stream-streammodedetails-syntax.yaml"></a>

```
  [StreamMode](#cfn-kinesis-stream-streammodedetails-streammode): String
```

## Properties<a name="aws-properties-kinesis-stream-streammodedetails-properties"></a>

`StreamMode`  <a name="cfn-kinesis-stream-streammodedetails-streammode"></a>
 Specifies the capacity mode to which you want to set your data stream\. Currently, in Kinesis Data Streams, you can choose between an **on\-demand** capacity mode and a **provisioned** capacity mode for your data streams\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `ON_DEMAND | PROVISIONED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)