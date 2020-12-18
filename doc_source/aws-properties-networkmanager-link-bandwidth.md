# AWS::NetworkManager::Link Bandwidth<a name="aws-properties-networkmanager-link-bandwidth"></a>

Describes bandwidth information\.

## Syntax<a name="aws-properties-networkmanager-link-bandwidth-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-networkmanager-link-bandwidth-syntax.json"></a>

```
{
  "[DownloadSpeed](#cfn-networkmanager-link-bandwidth-downloadspeed)" : Integer,
  "[UploadSpeed](#cfn-networkmanager-link-bandwidth-uploadspeed)" : Integer
}
```

### YAML<a name="aws-properties-networkmanager-link-bandwidth-syntax.yaml"></a>

```
  [DownloadSpeed](#cfn-networkmanager-link-bandwidth-downloadspeed): Integer
  [UploadSpeed](#cfn-networkmanager-link-bandwidth-uploadspeed): Integer
```

## Properties<a name="aws-properties-networkmanager-link-bandwidth-properties"></a>

`DownloadSpeed`  <a name="cfn-networkmanager-link-bandwidth-downloadspeed"></a>
Download speed in Mbps\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UploadSpeed`  <a name="cfn-networkmanager-link-bandwidth-uploadspeed"></a>
Upload speed in Mbps\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)