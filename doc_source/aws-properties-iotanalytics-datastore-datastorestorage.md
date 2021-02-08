# AWS::IoTAnalytics::Datastore DatastoreStorage<a name="aws-properties-iotanalytics-datastore-datastorestorage"></a>

Where data store data is stored\.

## Syntax<a name="aws-properties-iotanalytics-datastore-datastorestorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-datastorestorage-syntax.json"></a>

```
{
  "[CustomerManagedS3](#cfn-iotanalytics-datastore-datastorestorage-customermanageds3)" : CustomerManagedS3,
  "[ServiceManagedS3](#cfn-iotanalytics-datastore-datastorestorage-servicemanageds3)" : ServiceManagedS3
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-datastorestorage-syntax.yaml"></a>

```
  [CustomerManagedS3](#cfn-iotanalytics-datastore-datastorestorage-customermanageds3): 
    CustomerManagedS3
  [ServiceManagedS3](#cfn-iotanalytics-datastore-datastorestorage-servicemanageds3): 
    ServiceManagedS3
```

## Properties<a name="aws-properties-iotanalytics-datastore-datastorestorage-properties"></a>

`CustomerManagedS3`  <a name="cfn-iotanalytics-datastore-datastorestorage-customermanageds3"></a>
Use this to store data store data in an S3 bucket that you manage\. The choice of service\-managed or customer\-managed S3 storage cannot be changed after creation of the data store\.  
*Required*: No  
*Type*: [CustomerManagedS3](aws-properties-iotanalytics-datastore-customermanageds3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceManagedS3`  <a name="cfn-iotanalytics-datastore-datastorestorage-servicemanageds3"></a>
Use this to store data store data in an S3 bucket managed by the AWS IoT Analytics service\. The choice of service\-managed or customer\-managed S3 storage cannot be changed after creation of the data store\.  
*Required*: No  
*Type*: [ServiceManagedS3](aws-properties-iotanalytics-datastore-servicemanageds3.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)