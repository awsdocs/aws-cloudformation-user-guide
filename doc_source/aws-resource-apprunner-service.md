# AWS::AppRunner::Service<a name="aws-resource-apprunner-service"></a>

The `AWS::AppRunner::Service` resource is an AWS App Runner resource type that specifies an App Runner service\.

## Syntax<a name="aws-resource-apprunner-service-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-apprunner-service-syntax.json"></a>

```
{
  "Type" : "AWS::AppRunner::Service",
  "Properties" : {
      "[AutoScalingConfigurationArn](#cfn-apprunner-service-autoscalingconfigurationarn)" : String,
      "[EncryptionConfiguration](#cfn-apprunner-service-encryptionconfiguration)" : EncryptionConfiguration,
      "[HealthCheckConfiguration](#cfn-apprunner-service-healthcheckconfiguration)" : HealthCheckConfiguration,
      "[InstanceConfiguration](#cfn-apprunner-service-instanceconfiguration)" : InstanceConfiguration,
      "[NetworkConfiguration](#cfn-apprunner-service-networkconfiguration)" : NetworkConfiguration,
      "[ObservabilityConfiguration](#cfn-apprunner-service-observabilityconfiguration)" : ServiceObservabilityConfiguration,
      "[ServiceName](#cfn-apprunner-service-servicename)" : String,
      "[SourceConfiguration](#cfn-apprunner-service-sourceconfiguration)" : SourceConfiguration,
      "[Tags](#cfn-apprunner-service-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-apprunner-service-syntax.yaml"></a>

```
Type: AWS::AppRunner::Service
Properties: 
  [AutoScalingConfigurationArn](#cfn-apprunner-service-autoscalingconfigurationarn): String
  [EncryptionConfiguration](#cfn-apprunner-service-encryptionconfiguration): 
    EncryptionConfiguration
  [HealthCheckConfiguration](#cfn-apprunner-service-healthcheckconfiguration): 
    HealthCheckConfiguration
  [InstanceConfiguration](#cfn-apprunner-service-instanceconfiguration): 
    InstanceConfiguration
  [NetworkConfiguration](#cfn-apprunner-service-networkconfiguration): 
    NetworkConfiguration
  [ObservabilityConfiguration](#cfn-apprunner-service-observabilityconfiguration): 
    ServiceObservabilityConfiguration
  [ServiceName](#cfn-apprunner-service-servicename): String
  [SourceConfiguration](#cfn-apprunner-service-sourceconfiguration): 
    SourceConfiguration
  [Tags](#cfn-apprunner-service-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-apprunner-service-properties"></a>

`AutoScalingConfigurationArn`  <a name="cfn-apprunner-service-autoscalingconfigurationarn"></a>
The Amazon Resource Name \(ARN\) of an App Runner automatic scaling configuration resource that you want to associate with your service\. If not provided, App Runner associates the latest revision of a default auto scaling configuration\.  
Specify an ARN with a name and a revision number to associate that revision\. For example: `arn:aws:apprunner:us-east-1:123456789012:autoscalingconfiguration/high-availability/3`   
Specify just the name to associate the latest revision\. For example: `arn:aws:apprunner:us-east-1:123456789012:autoscalingconfiguration/high-availability`   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1011`  
*Pattern*: `arn:aws(-[\w]+)*:[a-z0-9-\\.]{0,63}:[a-z0-9-\\.]{0,63}:[0-9]{12}:(\w|\/|-){1,1011}`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EncryptionConfiguration`  <a name="cfn-apprunner-service-encryptionconfiguration"></a>
An optional custom encryption key that App Runner uses to encrypt the copy of your source repository that it maintains and your service logs\. By default, App Runner uses an AWS managed key\.  
*Required*: No  
*Type*: [EncryptionConfiguration](aws-properties-apprunner-service-encryptionconfiguration.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`HealthCheckConfiguration`  <a name="cfn-apprunner-service-healthcheckconfiguration"></a>
The settings for the health check that AWS App Runner performs to monitor the health of the App Runner service\.  
*Required*: No  
*Type*: [HealthCheckConfiguration](aws-properties-apprunner-service-healthcheckconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceConfiguration`  <a name="cfn-apprunner-service-instanceconfiguration"></a>
The runtime configuration of instances \(scaling units\) of your service\.  
*Required*: No  
*Type*: [InstanceConfiguration](aws-properties-apprunner-service-instanceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkConfiguration`  <a name="cfn-apprunner-service-networkconfiguration"></a>
Configuration settings related to network traffic of the web application that the App Runner service runs\.  
*Required*: No  
*Type*: [NetworkConfiguration](aws-properties-apprunner-service-networkconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObservabilityConfiguration`  <a name="cfn-apprunner-service-observabilityconfiguration"></a>
The observability configuration of your service\.  
*Required*: No  
*Type*: [ServiceObservabilityConfiguration](aws-properties-apprunner-service-serviceobservabilityconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-apprunner-service-servicename"></a>
A name for the App Runner service\. It must be unique across all the running App Runner services in your AWS account in the AWS Region\.  
If you don't specify a name, AWS CloudFormation generates a name for your service\.  
*Required*: No  
*Type*: String  
*Minimum*: `4`  
*Maximum*: `40`  
*Pattern*: `[A-Za-z0-9][A-Za-z0-9-_]{3,39}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceConfiguration`  <a name="cfn-apprunner-service-sourceconfiguration"></a>
The source to deploy to the App Runner service\. It can be a code or an image repository\.  
*Required*: Yes  
*Type*: [SourceConfiguration](aws-properties-apprunner-service-sourceconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-apprunner-service-tags"></a>
An optional list of metadata items that you can associate with the App Runner service resource\. A tag is a key\-value pair\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-apprunner-service-return-values"></a>

### Ref<a name="aws-resource-apprunner-service-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the ARN of the App Runner service\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-apprunner-service-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-apprunner-service-return-values-fn--getatt-fn--getatt"></a>

`ServiceArn`  <a name="ServiceArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of this service\.

`ServiceId`  <a name="ServiceId-fn::getatt"></a>
An ID that App Runner generated for this service\. It's unique within the AWS Region\.

`ServiceUrl`  <a name="ServiceUrl-fn::getatt"></a>
A subdomain URL that App Runner generated for this service\. You can use this URL to access your service web application\.

`Status`  <a name="Status-fn::getatt"></a>
The current state of the App Runner service\. These particular values mean the following\.  
+  `CREATE_FAILED` – The service failed to create\. To troubleshoot this failure, read the failure events and logs, change any parameters that need to be fixed, and retry the call to create the service\.

  The failed service isn't usable, and still counts towards your service quota\. When you're done analyzing the failure, delete the service\.
+  `DELETE_FAILED` – The service failed to delete and can't be successfully recovered\. Retry the service deletion call to ensure that all related resources are removed\.

## Examples<a name="aws-resource-apprunner-service--examples"></a>

### Service based on source code<a name="aws-resource-apprunner-service--examples--Service_based_on_source_code"></a>

This example illustrates creating a service based on a Python source code repository\.

#### JSON<a name="aws-resource-apprunner-service--examples--Service_based_on_source_code--json"></a>

```
{
  "Type": "AWS::AppRunner::Service",
  "Properties": {
    "ServiceName": "python-app",
    "SourceConfiguration": {
      "AuthenticationConfiguration": {
        "ConnectionArn": "arn:aws:apprunner:us-east-1:123456789012:connection/my-github-connection/e7656250f67242d7819feade6800f59e"
      },
      "AutoDeploymentsEnabled": true,
      "CodeRepository": {
        "RepositoryUrl": "https://github.com/my-account/python-hello",
        "SourceCodeVersion": {
          "Type": "BRANCH",
          "Value": "main"
        },
        "CodeConfiguration": {
          "ConfigurationSource": "API",
          "CodeConfigurationValues": {
            "Runtime": "PYTHON_3",
            "BuildCommand": "pip install -r requirements.txt",
            "StartCommand": "python server.py",
            "Port": "8080",
            "RuntimeEnvironmentVariables": [
              {
                "Name": "NAME",
                "Value": "Jane"
              }
            ]
          }
        }
      }
    },
    "InstanceConfiguration": {
      "Cpu": "1 vCPU",
      "Memory": "3 GB"
    }
  }
}
```

#### YAML<a name="aws-resource-apprunner-service--examples--Service_based_on_source_code--yaml"></a>

```
Type: AWS::AppRunner::Service
Properties:
  ServiceName: python-app
  SourceConfiguration:
    AuthenticationConfiguration:
      ConnectionArn: "arn:aws:apprunner:us-east-1:123456789012:connection/my-github-connection/e7656250f67242d7819feade6800f59e"
    AutoDeploymentsEnabled: true
    CodeRepository:
      RepositoryUrl: "https://github.com/my-account/python-hello"
      SourceCodeVersion:
        Type: BRANCH
        Value: main
      CodeConfiguration:
        ConfigurationSource: API
        CodeConfigurationValues:
          Runtime: PYTHON_3
          BuildCommand: "pip install -r requirements.txt"
          StartCommand: "python server.py"
          Port: 8080
          RuntimeEnvironmentVariables:
            -
              Name: NAME
              Value: Jane
  InstanceConfiguration:
    Cpu: 1 vCPU
    Memory: 3 GB
```

### Service based on source image<a name="aws-resource-apprunner-service--examples--Service_based_on_source_image"></a>

This example illustrates creating a service based on an image stored in Amazon Elastic Container Registry \(Amazon ECR\)\.

#### JSON<a name="aws-resource-apprunner-service--examples--Service_based_on_source_image--json"></a>

```
{
  "Type": "AWS::AppRunner::Service",
  "Properties": {
    "ServiceName": "golang-container-app",
    "SourceConfiguration": {
      "AuthenticationConfiguration": {
        "AccessRoleArn": "arn:aws:iam::123456789012:role/my-ecr-role"
      },
      "AutoDeploymentsEnabled": true,
      "ImageRepository": {
        "ImageIdentifier": "123456789012.dkr.ecr.us-east-1.amazonaws.com/golang-app:latest",
        "ImageRepositoryType": "ECR",
        "ImageConfiguration": {
          "Port": "8080",
          "RuntimeEnvironmentVariables": [
            {
              "Name": "NAME",
              "Value": "Jane"
            }
          ]
        }
      }
    },
    "InstanceConfiguration": {
      "Cpu": "1 vCPU",
      "Memory": "3 GB"
    }
  }
}
```

#### YAML<a name="aws-resource-apprunner-service--examples--Service_based_on_source_image--yaml"></a>

```
Type: AWS::AppRunner::Service
Properties:
  ServiceName: golang-container-app
  SourceConfiguration:
    AuthenticationConfiguration:
      AccessRoleArn: "arn:aws:iam::123456789012:role/my-ecr-role"
    AutoDeploymentsEnabled: true
    ImageRepository:
      ImageIdentifier: "123456789012.dkr.ecr.us-east-1.amazonaws.com/golang-app:latest"
      ImageRepositoryType: ECR
      ImageConfiguration:
        Port: 8080
        RuntimeEnvironmentVariables:
          -
            Name: NAME
            Value: Jane
  InstanceConfiguration:
    Cpu: 1 vCPU
    Memory: 3 GB
```

## See also<a name="aws-resource-apprunner-service--seealso"></a>
+ [Creating an App Runner service](https://docs.aws.amazon.com/apprunner/latest/dg/manage-create.html) in the *AWS App Runner Developer Guide*
+ [Deploying a new application version to App Runner](https://docs.aws.amazon.com/apprunner/latest/dg/manage-deploy.html) in the *AWS App Runner Developer Guide*
+ [Configuring an App Runner service](https://docs.aws.amazon.com/apprunner/latest/dg/manage-configure.html) in the *AWS App Runner Developer Guide*