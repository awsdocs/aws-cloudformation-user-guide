# AWS::DataSync::StorageSystem ServerConfiguration<a name="aws-properties-datasync-storagesystem-serverconfiguration"></a>

The network settings that DataSync Discovery uses to connect with your on\-premises storage system's management interface\.

## Syntax<a name="aws-properties-datasync-storagesystem-serverconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-storagesystem-serverconfiguration-syntax.json"></a>

```
{
  "[ServerHostname](#cfn-datasync-storagesystem-serverconfiguration-serverhostname)" : String,
  "[ServerPort](#cfn-datasync-storagesystem-serverconfiguration-serverport)" : Integer
}
```

### YAML<a name="aws-properties-datasync-storagesystem-serverconfiguration-syntax.yaml"></a>

```
  [ServerHostname](#cfn-datasync-storagesystem-serverconfiguration-serverhostname): String
  [ServerPort](#cfn-datasync-storagesystem-serverconfiguration-serverport): Integer
```

## Properties<a name="aws-properties-datasync-storagesystem-serverconfiguration-properties"></a>

`ServerHostname`  <a name="cfn-datasync-storagesystem-serverconfiguration-serverhostname"></a>
The domain name or IP address of your storage system's management interface\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `255`  
*Pattern*: `^(([a-zA-Z0-9\-]*[a-zA-Z0-9])\.)*([A-Za-z0-9\-]*[A-Za-z0-9])$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerPort`  <a name="cfn-datasync-storagesystem-serverconfiguration-serverport"></a>
The network port for accessing the storage system's management interface\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)