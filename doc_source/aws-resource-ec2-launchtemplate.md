# AWS::EC2::LaunchTemplate<a name="aws-resource-ec2-launchtemplate"></a>

Specifies a launch template for an Amazon EC2 instance\. A launch template contains the parameters to launch an instance\. For more information, see [Launching an instance from a launch template](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/ec2-launch-templates.html) in the *Amazon Elastic Compute Cloud User Guide*\.

## Syntax<a name="aws-resource-ec2-launchtemplate-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-launchtemplate-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::LaunchTemplate",
  "Properties" : {
      "[LaunchTemplateData](#cfn-ec2-launchtemplate-launchtemplatedata)" : LaunchTemplateData,
      "[LaunchTemplateName](#cfn-ec2-launchtemplate-launchtemplatename)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-launchtemplate-syntax.yaml"></a>

```
Type: AWS::EC2::LaunchTemplate
Properties: 
  [LaunchTemplateData](#cfn-ec2-launchtemplate-launchtemplatedata): 
    LaunchTemplateData
  [LaunchTemplateName](#cfn-ec2-launchtemplate-launchtemplatename): String
```

## Properties<a name="aws-resource-ec2-launchtemplate-properties"></a>

`LaunchTemplateData`  <a name="cfn-ec2-launchtemplate-launchtemplatedata"></a>
The information for the launch template\.  
*Required*: No  
*Type*: [LaunchTemplateData](aws-properties-ec2-launchtemplate-launchtemplatedata.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LaunchTemplateName`  <a name="cfn-ec2-launchtemplate-launchtemplatename"></a>
A name for the launch template\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9\(\)\.\-/_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-launchtemplate-return-values"></a>

### Ref<a name="aws-resource-ec2-launchtemplate-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the launch template, for example, `lt-01238c059e3466abc`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ec2-launchtemplate-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ec2-launchtemplate-return-values-fn--getatt-fn--getatt"></a>

`DefaultVersionNumber`  <a name="DefaultVersionNumber-fn::getatt"></a>
The default version of the launch template, such as 2\.  
The default version of a launch template cannot be specified in AWS CloudFormation\. The default version can be set in the Amazon EC2 Console or by using the `modify-launch-template` AWS CLI command\.

`LatestVersionNumber`  <a name="LatestVersionNumber-fn::getatt"></a>
The latest version of the launch template, such as `5`\.

## Examples<a name="aws-resource-ec2-launchtemplate--examples"></a>

### Launch template with an IAM instance profile<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_an_IAM_instance_profile"></a>

The following example creates a launch template and an instance profile\. The instance profile contains the IAM role named `MyAdminRole` and can provide the role's temporary credentials to an application that runs on the instances created by this launch template\.

The launch template also prevents accidental instance termination when using the Amazon EC2 console, CLI, or API, by specifying `true` for the `DisableApiTermination` property\. If the instances created by this launch template are launched in a default VPC, they receive a public IP address by default\. If the instances are launched in a nondefault VPC, they do not receive a public IP address by default\.

#### JSON<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_an_IAM_instance_profile--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Resources":{
    "MyIamInstanceProfile":{
      "Type":"AWS::IAM::InstanceProfile",
      "Properties":{
        "InstanceProfileName":"MyIamInstanceProfile",
        "Path":"/",
        "Roles":["MyAdminRole"]
      }
    },
    "MyLaunchTemplate":{
      "Type":"AWS::EC2::LaunchTemplate",
      "Properties":{
        "LaunchTemplateName":"MyLaunchTemplate",
        "LaunchTemplateData":{
          "IamInstanceProfile":{
          "Arn":{"Fn::GetAtt": ["MyIamInstanceProfile", "Arn"]}
          },
          "DisableApiTermination":"true",
          "ImageId":"ami-04d5cc9b88example",
          "InstanceType":"t2.micro",
          "KeyName":"MyKeyPair",
          "SecurityGroupIds":[
            "sg-083cd3bfb8example"
          ]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_an_IAM_instance_profile--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  MyIamInstanceProfile:
    Type: AWS::IAM::InstanceProfile
    Properties:
      InstanceProfileName: MyIamInstanceProfile
      Path: "/"
      Roles:
      - MyAdminRole
  MyLaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties:
      LaunchTemplateName: MyLaunchTemplate
      LaunchTemplateData:
        IamInstanceProfile:
          Arn: !GetAtt
            - MyIamInstanceProfile
            - Arn
        DisableApiTermination: true
        ImageId: ami-04d5cc9b88example
        InstanceType: t2.micro
        KeyName: MyKeyPair
        SecurityGroupIds:
          - sg-083cd3bfb8example
```

### Launch template with defined block device mapping<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_defined_block_device_mapping"></a>

The following example creates a launch template with a block device mapping: an encrypted 22 gigabyte EBS volume mapped to /dev/xvdcz\. The /dev/xvdcz volume uses the General Purpose SSD \(gp2\) volume type and is deleted when terminating the instance it is attached to\. This example uses the Fn::Sub function to customize the name of the launch template to include the stack name\.

The launch template also provisions T2 instances in unlimited mode by specifying a value of `unlimited` for the `CPUCredits` property\. Because `Monitoring` is enabled, EC2 metric data will be available at 1\-minute intervals \(known as detailed monitoring\) through CloudWatch\.

#### JSON<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_defined_block_device_mapping--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Resources":{
    "myLaunchTemplate":{
      "Type":"AWS::EC2::LaunchTemplate",
      "Properties":{
        "LaunchTemplateName":{"Fn::Sub":"${AWS::StackName}-launch-template"},
        "LaunchTemplateData":{
          "BlockDeviceMappings":[{
            "Ebs":{
              "VolumeSize":"22",
              "VolumeType":"gp2",
              "DeleteOnTermination": true,
              "Encrypted": true
            },
            "DeviceName":"/dev/xvdcz"
          }],
          "CreditSpecification":{
            "CpuCredits":"unlimited"
          },
          "Monitoring":{"Enabled":true},
          "ImageId":"ami-04d5cc9b88example",
          "InstanceType":"t2.micro",
          "KeyName":"MyKeyPair",
          "SecurityGroupIds":["sg-7c2270198example", "sg-903004f88example"]
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_defined_block_device_mapping--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  myLaunchTemplate:
    Type: AWS::EC2::LaunchTemplate
    Properties: 
      LaunchTemplateName: !Sub ${AWS::StackName}-launch-template
      LaunchTemplateData: 
        BlockDeviceMappings: 
          - Ebs:
              VolumeSize: 22
              VolumeType: gp2
              DeleteOnTermination: true
              Encrypted: true
            DeviceName: /dev/xvdcz
        CreditSpecification: 
          CpuCredits: Unlimited
        Monitoring: 
          Enabled: true
        ImageId: ami-04d5cc9b88example
        InstanceType: t2.micro
        KeyName: MyKeyPair
        SecurityGroupIds: 
          - sg-7c2270198example
          - sg-903004f88example
```

### Launch template with public IP addresses for Amazon EC2 Auto Scaling<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_public_IP_addresses_for_Amazon_EC2_Auto_Scaling"></a>

The following example creates and configures a launch template to assign public IP addresses to instances launched in a nondefault VPC\. Note that when you specify a network interface for Amazon EC2 Auto Scaling, specify the VPC subnets as properties of the Auto Scaling group, and not in the launch template \(because they will be ignored\)\.

This example launch template also sets the instance placement tenancy to `dedicated`\.

For more information about creating launch templates for Amazon EC2 Auto Scaling, see [Creating a launch template for an Auto Scaling group](https://docs.aws.amazon.com/autoscaling/ec2/userguide/create-launch-template.html) in the *Amazon EC2 Auto Scaling User Guide*\.

#### JSON<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_public_IP_addresses_for_Amazon_EC2_Auto_Scaling--json"></a>

```
{
  "AWSTemplateFormatVersion":"2010-09-09",
  "Resources":{
    "myLaunchTemplate":{
      "Type":"AWS::EC2::LaunchTemplate",
      "Properties":{
        "LaunchTemplateName":{
          "Fn::Sub":"${AWS::StackName}-launch-template-for-auto-scaling"
        },
        "LaunchTemplateData":{
          "NetworkInterfaces":[
            {
              "DeviceIndex":0,
              "AssociatePublicIpAddress":true,
              "Groups":[
                "sg-7c2270198example",
                "sg-903004f88example"
              ],
              "DeleteOnTermination":true
            }
          ],
          "Placement":{
            "Tenancy": "dedicated"
          },
          "ImageId":"ami-04d5cc9b88example",
          "InstanceType":"t2.micro",
          "KeyName":"MyKeyPair"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ec2-launchtemplate--examples--Launch_template_with_public_IP_addresses_for_Amazon_EC2_Auto_Scaling--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myLaunchTemplate:
    Type: 'AWS::EC2::LaunchTemplate'
    Properties:
      LaunchTemplateName: !Sub '${AWS::StackName}-launch-template-for-auto-scaling'
      LaunchTemplateData:
        NetworkInterfaces:
          - DeviceIndex: 0
            AssociatePublicIpAddress: true
            Groups:
              - sg-7c2270198example
              - sg-903004f88example
            DeleteOnTermination: true
        Placement:
          Tenancy: dedicated
        ImageId: ami-04d5cc9b88example
        InstanceType: t2.micro
        KeyName: MyKeyPair
```

## See also<a name="aws-resource-ec2-launchtemplate--seealso"></a>
+ [ CreateLaunchTemplate](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLaunchTemplate.html) in the *Amazon EC2 API Reference* 