# AWS::ImageBuilder::InfrastructureConfiguration<a name="aws-resource-imagebuilder-infrastructureconfiguration"></a>

 The infrastructure configuration allows you to specify the infrastructure within which to build and test your image\. In the infrastructure configuration, you can specify instance types, subnets, and security groups to associate with your instance\. You can also associate an Amazon EC2 key pair with the instance used to build your image\. This allows you to log on to your instance to troubleshoot if your build fails and you set terminateInstanceOnFailure to false\. 

## Syntax<a name="aws-resource-imagebuilder-infrastructureconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-imagebuilder-infrastructureconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::ImageBuilder::InfrastructureConfiguration",
  "Properties" : {
      "[Description](#cfn-imagebuilder-infrastructureconfiguration-description)" : String,
      "[InstanceProfileName](#cfn-imagebuilder-infrastructureconfiguration-instanceprofilename)" : String,
      "[InstanceTypes](#cfn-imagebuilder-infrastructureconfiguration-instancetypes)" : [ String, ... ],
      "[KeyPair](#cfn-imagebuilder-infrastructureconfiguration-keypair)" : String,
      "[Logging](#cfn-imagebuilder-infrastructureconfiguration-logging)" : Logging,
      "[Name](#cfn-imagebuilder-infrastructureconfiguration-name)" : String,
      "[ResourceTags](#cfn-imagebuilder-infrastructureconfiguration-resourcetags)" : {Key : Value, ...},
      "[SecurityGroupIds](#cfn-imagebuilder-infrastructureconfiguration-securitygroupids)" : [ String, ... ],
      "[SnsTopicArn](#cfn-imagebuilder-infrastructureconfiguration-snstopicarn)" : String,
      "[SubnetId](#cfn-imagebuilder-infrastructureconfiguration-subnetid)" : String,
      "[Tags](#cfn-imagebuilder-infrastructureconfiguration-tags)" : {Key : Value, ...},
      "[TerminateInstanceOnFailure](#cfn-imagebuilder-infrastructureconfiguration-terminateinstanceonfailure)" : Boolean
    }
}
```

### YAML<a name="aws-resource-imagebuilder-infrastructureconfiguration-syntax.yaml"></a>

```
Type: AWS::ImageBuilder::InfrastructureConfiguration
Properties: 
  [Description](#cfn-imagebuilder-infrastructureconfiguration-description): String
  [InstanceProfileName](#cfn-imagebuilder-infrastructureconfiguration-instanceprofilename): String
  [InstanceTypes](#cfn-imagebuilder-infrastructureconfiguration-instancetypes): 
    - String
  [KeyPair](#cfn-imagebuilder-infrastructureconfiguration-keypair): String
  [Logging](#cfn-imagebuilder-infrastructureconfiguration-logging): 
    Logging
  [Name](#cfn-imagebuilder-infrastructureconfiguration-name): String
  [ResourceTags](#cfn-imagebuilder-infrastructureconfiguration-resourcetags): 
    Key : Value
  [SecurityGroupIds](#cfn-imagebuilder-infrastructureconfiguration-securitygroupids): 
    - String
  [SnsTopicArn](#cfn-imagebuilder-infrastructureconfiguration-snstopicarn): String
  [SubnetId](#cfn-imagebuilder-infrastructureconfiguration-subnetid): String
  [Tags](#cfn-imagebuilder-infrastructureconfiguration-tags): 
    Key : Value
  [TerminateInstanceOnFailure](#cfn-imagebuilder-infrastructureconfiguration-terminateinstanceonfailure): Boolean
```

## Properties<a name="aws-resource-imagebuilder-infrastructureconfiguration-properties"></a>

`Description`  <a name="cfn-imagebuilder-infrastructureconfiguration-description"></a>
The description of the infrastructure configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceProfileName`  <a name="cfn-imagebuilder-infrastructureconfiguration-instanceprofilename"></a>
The instance profile of the infrastructure configuration\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InstanceTypes`  <a name="cfn-imagebuilder-infrastructureconfiguration-instancetypes"></a>
The instance types of the infrastructure configuration\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeyPair`  <a name="cfn-imagebuilder-infrastructureconfiguration-keypair"></a>
The EC2 key pair of the infrastructure configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Logging`  <a name="cfn-imagebuilder-infrastructureconfiguration-logging"></a>
The logging configuration of the infrastructure configuration\.  
*Required*: No  
*Type*: [Logging](aws-properties-imagebuilder-infrastructureconfiguration-logging.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-imagebuilder-infrastructureconfiguration-name"></a>
The name of the infrastructure configuration\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `^[-_A-Za-z-0-9][-_A-Za-z0-9 ]{1,126}[-_A-Za-z-0-9]$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourceTags`  <a name="cfn-imagebuilder-infrastructureconfiguration-resourcetags"></a>
The tags attached to the resource created by Image Builder\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityGroupIds`  <a name="cfn-imagebuilder-infrastructureconfiguration-securitygroupids"></a>
The security group IDs of the infrastructure configuration\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SnsTopicArn`  <a name="cfn-imagebuilder-infrastructureconfiguration-snstopicarn"></a>
The Amazon Resource Name \(ARN\) of the SNS topic for the infrastructure configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetId`  <a name="cfn-imagebuilder-infrastructureconfiguration-subnetid"></a>
The subnet ID of the infrastructure configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-imagebuilder-infrastructureconfiguration-tags"></a>
The tags of the infrastructure configuration\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminateInstanceOnFailure`  <a name="cfn-imagebuilder-infrastructureconfiguration-terminateinstanceonfailure"></a>
The terminate instance on failure configuration of the infrastructure configuration\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-imagebuilder-infrastructureconfiguration-return-values"></a>

### Ref<a name="aws-resource-imagebuilder-infrastructureconfiguration-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource ARN, such as `arn:aws:imagebuilder:us-west-2:123456789012:infrastructure-configuration/my-example-infrastructure`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-imagebuilder-infrastructureconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-imagebuilder-infrastructureconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the infrastructure configuration\. The following pattern is applied: `^arn:aws[^:]*:imagebuilder:[^:]+:(?:\d{12}|aws):(?:image-recipe|infrastructure-configuration|distribution-configuration|component|image|image-pipeline)/[a-z0-9-_]+(?:/(?:(?:x|\d+)\.(?:x|\d+)\.(?:x|\d+))(?:/\d+)?)?$`\.

## Examples<a name="aws-resource-imagebuilder-infrastructureconfiguration--examples"></a>



### Create an infrastructure configuration<a name="aws-resource-imagebuilder-infrastructureconfiguration--examples--Create_an_infrastructure_configuration"></a>

The following example shows the schema for all of the parameters of the InfrastructureConfiguration resource document in both YAML and JSON format \.

#### YAML<a name="aws-resource-imagebuilder-infrastructureconfiguration--examples--Create_an_infrastructure_configuration--yaml"></a>

```
Resources:
  InfrastructureConfigurationAll:
    Type: 'AWS::ImageBuilder::InfrastructureConfiguration'
    Properties:
      Name: 'infrastructure-configuration-name'
      InstanceProfileName: 'instance-profile-name'
      Description: 'description'
      InstanceTypes:
        - 'm4.large'
        - 'm5.large'
      KeyPair: 'key-pair'
      Logging:
        S3Logs:
          S3BucketName: 'imagebuilder-logging-bucket'
          S3KeyPrefix: 'imagebuilder-bucket-prefix'
      SnsTopicArn: !Ref SnsTopicArn
      TerminateInstanceOnFailure: true
      SecurityGroupIds:
        - 'security-group-id-1'
        - 'security-group-id-2'
      SubnetId: 'subnet-id'
      Tags:
        CustomerInfraConfigTagKey1: 'CustomerInfraConfigTagValue1'
        CustomerInfraConfigTagKey2: 'CustomerInfraConfigTagValue2'
```

#### JSON<a name="aws-resource-imagebuilder-infrastructureconfiguration--examples--Create_an_infrastructure_configuration--json"></a>

```
{
    "Resources": {
        "InfrastructureConfigurationAll": {
            "Type": "AWS::ImageBuilder::InfrastructureConfiguration",
            "Properties": {
                "Name": "infrastructure-configuration-name",
                "InstanceProfileName": "instance-profile-name",
                "Description": "description",
                "InstanceTypes": [
                    "m4.large",
                    "m5.large"
                ],
                "KeyPair": "key-pair",
                "Logging": {
                    "S3Logs": {
                        "S3BucketName": "imagebuilder-logging-bucket",
                        "S3KeyPrefix": "imagebuilder-bucket-prefix"
                    }
                },
                "SnsTopicArn": {
                    "Ref": "SnsTopicArn"
                },
                "TerminateInstanceOnFailure": true,
                "SecurityGroupIds": [
                    "security-group-id-1",
                    "security-group-id-2"
                ],
                "SubnetId": "subnet-id",
                "Tags": {
                    "CustomerInfraConfigTagKey1": "CustomerInfraConfigTagValue1",
                    "CustomerInfraConfigTagKey2": "CustomerInfraConfigTagValue2"
                }
            }
        }
    }
}
```