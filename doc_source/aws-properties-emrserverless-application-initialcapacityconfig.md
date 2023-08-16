# AWS::EMRServerless::Application InitialCapacityConfig<a name="aws-properties-emrserverless-application-initialcapacityconfig"></a>

The initial capacity configuration per worker\.

## Syntax<a name="aws-properties-emrserverless-application-initialcapacityconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-emrserverless-application-initialcapacityconfig-syntax.json"></a>

```
{
  "[WorkerConfiguration](#cfn-emrserverless-application-initialcapacityconfig-workerconfiguration)" : WorkerConfiguration,
  "[WorkerCount](#cfn-emrserverless-application-initialcapacityconfig-workercount)" : Integer
}
```

### YAML<a name="aws-properties-emrserverless-application-initialcapacityconfig-syntax.yaml"></a>

```
  [WorkerConfiguration](#cfn-emrserverless-application-initialcapacityconfig-workerconfiguration): 
    WorkerConfiguration
  [WorkerCount](#cfn-emrserverless-application-initialcapacityconfig-workercount): Integer
```

## Properties<a name="aws-properties-emrserverless-application-initialcapacityconfig-properties"></a>

`WorkerConfiguration`  <a name="cfn-emrserverless-application-initialcapacityconfig-workerconfiguration"></a>
The resource configuration of the initial capacity configuration\.  
*Required*: Yes  
*Type*: [WorkerConfiguration](aws-properties-emrserverless-application-workerconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkerCount`  <a name="cfn-emrserverless-application-initialcapacityconfig-workercount"></a>
The number of workers in the initial capacity configuration\.  
*Minimum*: 1  
*Maximum*: 1000000  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)