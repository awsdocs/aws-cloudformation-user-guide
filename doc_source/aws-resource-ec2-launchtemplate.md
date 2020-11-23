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

### Launch Template with an IAM Instance Profile<a name="aws-resource-ec2-launchtemplate--examples--Launch_Template_with_an_IAM_Instance_Profile"></a>

#### YAML<a name="aws-resource-ec2-launchtemplate--examples--Launch_Template_with_an_IAM_Instance_Profile--yaml"></a>

```
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
      LaunchTemplateData:
        InstanceType: c4.large
        DisableApiTermination: 'true'
        KeyName: MyKeyPair
        ImageId: ami-04d5cc9b88example
        IamInstanceProfile:
          Arn:
            Fn::GetAtt:
            - MyIamInstanceProfile
            - Arn
        SecurityGroupIds:
        - sg-083cd3bfb8example
      LaunchTemplateName: MyLaunchTemplate
```

### <a name="aws-resource-ec2-launchtemplate--examples--"></a>

#### JSON<a name="aws-resource-ec2-launchtemplate--examples----json"></a>

```
{
    "Resources": {
        "MyIamInstanceProfile": {
            "Type": "AWS::IAM::InstanceProfile",
            "Properties": {
                "InstanceProfileName" : "MyIamInstanceProfile",
                    "Path" : "/",
                    "Roles" : ["MyAdminRole"]
            }
        },
        "MyLaunchTemplate": {
            "Type": "AWS::EC2::LaunchTemplate",
            "Properties": {
                "LaunchTemplateData" : {
                    "InstanceType" : "c4.large",
                    "DisableApiTermination" : "true",
                    "KeyName" : "MyKeyPair",
                    "ImageId" : "ami-04d5cc9b88example",
                    "IamInstanceProfile" : {
                    "Arn" : {"Fn::GetAtt": ["MyIamInstanceProfile", "Arn"]}
                    },
                    "SecurityGroupIds" : ["sg-083cd3bfb8example"]
                },
                "LaunchTemplateName" : "MyLaunchTemplate"
            }
        }		
    }
}
```

## See also<a name="aws-resource-ec2-launchtemplate--seealso"></a>
+ [ CreateLaunchTemplate](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateLaunchTemplate.html) in the *Amazon EC2 API Reference* 