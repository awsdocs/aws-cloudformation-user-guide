# AWS::EMRContainers::VirtualCluster ContainerProvider<a name="aws-properties-emrcontainers-virtualcluster-containerprovider"></a>

The information about the container provider\.

## Syntax<a name="aws-properties-emrcontainers-virtualcluster-containerprovider-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrcontainers-virtualcluster-containerprovider-syntax.json"></a>

```
{
  "[Id](#cfn-emrcontainers-virtualcluster-containerprovider-id)" : String,
  "[Info](#cfn-emrcontainers-virtualcluster-containerprovider-info)" : ContainerInfo,
  "[Type](#cfn-emrcontainers-virtualcluster-containerprovider-type)" : String
}
```

### YAML<a name="aws-properties-emrcontainers-virtualcluster-containerprovider-syntax.yaml"></a>

```
  [Id](#cfn-emrcontainers-virtualcluster-containerprovider-id): String
  [Info](#cfn-emrcontainers-virtualcluster-containerprovider-info): 
    ContainerInfo
  [Type](#cfn-emrcontainers-virtualcluster-containerprovider-type): String
```

## Properties<a name="aws-properties-emrcontainers-virtualcluster-containerprovider-properties"></a>

`Id`  <a name="cfn-emrcontainers-virtualcluster-containerprovider-id"></a>
The ID of the container cluster\.  
*Minimum*: 1  
*Maximum*: 100  
*Pattern*: `^[0-9A-Za-z][A-Za-z0-9\-_]*`  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Info`  <a name="cfn-emrcontainers-virtualcluster-containerprovider-info"></a>
The information about the container cluster\.  
*Required*: Yes  
*Type*: [ContainerInfo](aws-properties-emrcontainers-virtualcluster-containerinfo.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Type`  <a name="cfn-emrcontainers-virtualcluster-containerprovider-type"></a>
The type of the container provider\. Amazon EKS is the only supported type as of now\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EKS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)