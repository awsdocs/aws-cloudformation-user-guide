# AWS::SageMaker::MonitoringSchedule NetworkConfig<a name="aws-properties-sagemaker-monitoringschedule-networkconfig"></a>

Networking options for a job, such as network traffic encryption between containers, whether to allow inbound and outbound network calls to and from containers, and the VPC subnets and security groups to use for VPC\-enabled jobs\.

## Syntax<a name="aws-properties-sagemaker-monitoringschedule-networkconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-sagemaker-monitoringschedule-networkconfig-syntax.json"></a>

```
{
  "[EnableInterContainerTrafficEncryption](#cfn-sagemaker-monitoringschedule-networkconfig-enableintercontainertrafficencryption)" : Boolean,
  "[EnableNetworkIsolation](#cfn-sagemaker-monitoringschedule-networkconfig-enablenetworkisolation)" : Boolean,
  "[VpcConfig](#cfn-sagemaker-monitoringschedule-networkconfig-vpcconfig)" : VpcConfig
}
```

### YAML<a name="aws-properties-sagemaker-monitoringschedule-networkconfig-syntax.yaml"></a>

```
  [EnableInterContainerTrafficEncryption](#cfn-sagemaker-monitoringschedule-networkconfig-enableintercontainertrafficencryption): Boolean
  [EnableNetworkIsolation](#cfn-sagemaker-monitoringschedule-networkconfig-enablenetworkisolation): Boolean
  [VpcConfig](#cfn-sagemaker-monitoringschedule-networkconfig-vpcconfig): 
    VpcConfig
```

## Properties<a name="aws-properties-sagemaker-monitoringschedule-networkconfig-properties"></a>

`EnableInterContainerTrafficEncryption`  <a name="cfn-sagemaker-monitoringschedule-networkconfig-enableintercontainertrafficencryption"></a>
Whether to encrypt all communications between distributed processing jobs\. Choose `True` to encrypt communications\. Encryption provides greater security for distributed processing jobs, but the processing might take longer\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EnableNetworkIsolation`  <a name="cfn-sagemaker-monitoringschedule-networkconfig-enablenetworkisolation"></a>
Whether to allow inbound and outbound network calls to and from the containers used for the processing job\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcConfig`  <a name="cfn-sagemaker-monitoringschedule-networkconfig-vpcconfig"></a>
Specifies a VPC that your training jobs and hosted models have access to\. Control access to and from your training and model containers by configuring the VPC\. For more information, see [Protect Endpoints by Using an Amazon Virtual Private Cloud](https://docs.aws.amazon.com/sagemaker/latest/dg/host-vpc.html) and [Protect Training Jobs by Using an Amazon Virtual Private Cloud](https://docs.aws.amazon.com/sagemaker/latest/dg/train-vpc.html)\.  
*Required*: No  
*Type*: [VpcConfig](aws-properties-sagemaker-monitoringschedule-vpcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)