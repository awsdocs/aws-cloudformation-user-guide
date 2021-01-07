# AWS CloudFormation template formats<a name="template-formats"></a>

You can author AWS CloudFormation templates in JSON or YAML formats\. We support all AWS CloudFormation features and functions for both formats, including in AWS CloudFormation Designer\.

When deciding which format to use, pick the format that you're most comfortable working in\. Also consider that YAML inherently provides some features, such as commenting, that aren't available in JSON\.

**Important**  
We recommend that you do not add `#` YAML comments to your templates in Designer\. If your YAML template has `#` comments, Designer does not preserve those comments when converting the template to JSON\. In addition, if you modify your template in Designer \(for example, if you move a resource on the canvas\), your comments are lost\. 

You can add comments to the AWS CloudFormation templates you create outside of Designer\. The following example shows a YAML template with inline comments\.

```
AWSTemplateFormatVersion: "2010-09-09"
Description: A sample template
Resources:
  MyEC2Instance: #An inline comment
    Type: "AWS::EC2::Instance"
    Properties: 
      ImageId: "ami-0ff8a91507f77f867" #Another comment -- This is a Linux AMI
      InstanceType: t2.micro
      KeyName: testkey
      BlockDeviceMappings:
        -
          DeviceName: /dev/sdm
          Ebs:
            VolumeType: io1
            Iops: 200
            DeleteOnTermination: false
            VolumeSize: 20
```

For more information about the template syntax for each format, see [Template anatomy](template-anatomy.md)\.

AWS CloudFormation supports the following JSON and YAML specifications:

JSON  
AWS CloudFormation follows the ECMA\-404 JSON standard\. For more information about the JSON format, see [http://www\.json\.org](http://www.json.org)\.

YAML  
AWS CloudFormation supports the YAML Version 1\.1 specification with a few exceptions\. AWS CloudFormation doesn't support the following features:  
+ The `binary`, `omap`, `pairs`, `set`, and `timestamp` tags
+ Aliases
+ Hash merges
For more information about YAML, see [http://www\.yaml\.org](http://www.yaml.org)\.
