# AWS::IoTFleetWise::Campaign DataDestinationConfig<a name="aws-properties-iotfleetwise-campaign-datadestinationconfig"></a>

The destination where the AWS IoT FleetWise campaign sends data\. You can send data to be stored in Amazon S3 or Amazon Timestream\.

## Syntax<a name="aws-properties-iotfleetwise-campaign-datadestinationconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotfleetwise-campaign-datadestinationconfig-syntax.json"></a>

```
{
  "[S3Config](#cfn-iotfleetwise-campaign-datadestinationconfig-s3config)" : S3Config,
  "[TimestreamConfig](#cfn-iotfleetwise-campaign-datadestinationconfig-timestreamconfig)" : TimestreamConfig
}
```

### YAML<a name="aws-properties-iotfleetwise-campaign-datadestinationconfig-syntax.yaml"></a>

```
  [S3Config](#cfn-iotfleetwise-campaign-datadestinationconfig-s3config): 
    S3Config
  [TimestreamConfig](#cfn-iotfleetwise-campaign-datadestinationconfig-timestreamconfig): 
    TimestreamConfig
```

## Properties<a name="aws-properties-iotfleetwise-campaign-datadestinationconfig-properties"></a>

`S3Config`  <a name="cfn-iotfleetwise-campaign-datadestinationconfig-s3config"></a>
\(Optional\) The Amazon S3 bucket where the AWS IoT FleetWise campaign sends data\.  
*Required*: No  
*Type*: [S3Config](aws-properties-iotfleetwise-campaign-s3config.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimestreamConfig`  <a name="cfn-iotfleetwise-campaign-datadestinationconfig-timestreamconfig"></a>
\(Optional\) The Amazon Timestream table where the campaign sends data\.  
*Required*: No  
*Type*: [TimestreamConfig](aws-properties-iotfleetwise-campaign-timestreamconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)