# AWS::IoTAnalytics::Datastore IotSiteWiseMultiLayerStorage<a name="aws-properties-iotanalytics-datastore-iotsitewisemultilayerstorage"></a>

Stores data used by AWS IoT SiteWise in an Amazon S3 bucket that you manage\. You can't change the choice of Amazon S3 storage after your data store is created\. 

## Syntax<a name="aws-properties-iotanalytics-datastore-iotsitewisemultilayerstorage-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-iotanalytics-datastore-iotsitewisemultilayerstorage-syntax.json"></a>

```
{
  "[CustomerManagedS3Storage](#cfn-iotanalytics-datastore-iotsitewisemultilayerstorage-customermanageds3storage)" : CustomerManagedS3Storage
}
```

### YAML<a name="aws-properties-iotanalytics-datastore-iotsitewisemultilayerstorage-syntax.yaml"></a>

```
  [CustomerManagedS3Storage](#cfn-iotanalytics-datastore-iotsitewisemultilayerstorage-customermanageds3storage): 
    CustomerManagedS3Storage
```

## Properties<a name="aws-properties-iotanalytics-datastore-iotsitewisemultilayerstorage-properties"></a>

`CustomerManagedS3Storage`  <a name="cfn-iotanalytics-datastore-iotsitewisemultilayerstorage-customermanageds3storage"></a>
Stores data used by AWS IoT SiteWise in an Amazon S3 bucket that you manage\.  
*Required*: No  
*Type*: [CustomerManagedS3Storage](aws-properties-iotanalytics-datastore-customermanageds3storage.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)