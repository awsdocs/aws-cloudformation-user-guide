# AWS::IoTAnalytics::Dataset DeltaTimeSessionWindowConfiguration<a name="aws-properties-iotanalytics-dataset-deltatimesessionwindowconfiguration"></a>

A structure that contains the configuration information of a delta time session window\.

 [https://docs.aws.amazon.com/iotanalytics/latest/APIReference/API_DeltaTime.html](https://docs.aws.amazon.com/iotanalytics/latest/APIReference/API_DeltaTime.html) specifies a time interval\. You can use `DeltaTime` to create dataset contents with data that has arrived in the data store since the last execution\. For an example of `DeltaTime`, see [ Creating a SQL dataset with a delta window \(CLI\)](https://docs.aws.amazon.com/iotanalytics/latest/userguide/automate-create-dataset.html#automate-example6) in the * AWS IoT Analytics User Guide*\.

## Syntax<a name="aws-properties-iotanalytics-dataset-deltatimesessionwindowconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-dataset-deltatimesessionwindowconfiguration-syntax.json"></a>

```
{
  "[TimeoutInMinutes](#cfn-iotanalytics-dataset-deltatimesessionwindowconfiguration-timeoutinminutes)" : Integer
}
```

### YAML<a name="aws-properties-iotanalytics-dataset-deltatimesessionwindowconfiguration-syntax.yaml"></a>

```
  [TimeoutInMinutes](#cfn-iotanalytics-dataset-deltatimesessionwindowconfiguration-timeoutinminutes): Integer
```

## Properties<a name="aws-properties-iotanalytics-dataset-deltatimesessionwindowconfiguration-properties"></a>

`TimeoutInMinutes`  <a name="cfn-iotanalytics-dataset-deltatimesessionwindowconfiguration-timeoutinminutes"></a>
A time interval\. You can use `timeoutInMinutes` so that AWS IoT Analytics can batch up late data notifications that have been generated since the last execution\. AWS IoT Analytics sends one batch of notifications to Amazon CloudWatch Events at one time\.  
For more information about how to write a timestamp expression, see [Date and Time Functions and Operators](https://prestodb.io/docs/0.172/functions/datetime.html), in the *Presto 0\.172 Documentation*\.  
*Required*: Yes  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `60`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)