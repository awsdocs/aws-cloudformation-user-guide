# AWS CloudFormation concepts<a name="cfn-whatis-concepts"></a>

When you use AWS CloudFormation, you work with *templates* and *stacks*\. You create templates to describe your AWS resources and their properties\. Whenever you create a stack, CloudFormation provisions the resources that are described in your template\.

**Topics**
+ [Templates](#cfn-concepts-templates)
+ [Stacks](#w2ab1b5c15b9)
+ [Change sets](#cfn-concepts-change-sets)

## Templates<a name="cfn-concepts-templates"></a>

A CloudFormation template is a JSON or YAML formatted text file\. You can save these files with any extension, such as `.json`, `.yaml`, `.template`, or `.txt`\. CloudFormation uses these templates as blueprints for building your AWS resources\. For example, in a template, you can describe an Amazon EC2 instance, such as the instance type, the AMI ID, block device mappings, and its Amazon EC2 key pair name\. Whenever you create a stack, you also specify a template that CloudFormation uses to create whatever you described in the template\.

For example, if you created a stack with the following template, CloudFormation provisions an instance with an `ami-0ff8a91507f77f867` AMI ID, `t2.micro` instance type, `testkey` key pair name, and an Amazon EBS volume\.

### JSON<a name="t2-micro-example.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "A sample template",
    "Resources": {
        "MyEC2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "ImageId": "ami-0ff8a91507f77f867",
                "InstanceType": "t2.micro",
                "KeyName": "testkey",
                "BlockDeviceMappings": [
                    {
                        "DeviceName": "/dev/sdm",
                        "Ebs": {
                            "VolumeType": "io1",
                            "Iops": 200,
                            "DeleteOnTermination": false,
                            "VolumeSize": 20
                        }
                    }
                ]
            }
        }
    }
}
```

### YAML<a name="t2-micro-example.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: A sample template
Resources:
  MyEC2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      ImageId: ami-0ff8a91507f77f867
      InstanceType: t2.micro
      KeyName: testkey
      BlockDeviceMappings:
        - DeviceName: /dev/sdm
          Ebs:
            VolumeType: io1
            Iops: 200
            DeleteOnTermination: false
            VolumeSize: 20
```

You can also specify multiple resources in a single template and configure these resources to work together\. For example, you can modify the previous template to include an Elastic IP address \(EIP\) and associate it with the Amazon EC2 instance, as shown in the following example:

### JSON<a name="multiple-resources-single-template.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "A sample template",
    "Resources": {
        "MyEC2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "ImageId": "ami-0ff8a91507f77f867",
                "InstanceType": "t2.micro",
                "KeyName": "testkey",
                "BlockDeviceMappings": [
                    {
                        "DeviceName": "/dev/sdm",
                        "Ebs": {
                            "VolumeType": "io1",
                            "Iops": 200,
                            "DeleteOnTermination": false,
                            "VolumeSize": 20
                        }
                    }
                ]
            }
        },
        "MyEIP": {
            "Type": "AWS::EC2::EIP",
            "Properties": {
                "InstanceId": {
                    "Ref": "MyEC2Instance"
                }
            }
        }
    }
}
```

### YAML<a name="multiple-resources-single-template.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: A sample template
Resources:
  MyEC2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      ImageId: ami-0ff8a91507f77f867
      InstanceType: t2.micro
      KeyName: testkey
      BlockDeviceMappings:
        - DeviceName: /dev/sdm
          Ebs:
            VolumeType: io1
            Iops: 200
            DeleteOnTermination: false
            VolumeSize: 20
  MyEIP:
    Type: 'AWS::EC2::EIP'
    Properties:
      InstanceId: !Ref MyEC2Instance
```

The previous templates are centered around a single Amazon EC2 instance; however, CloudFormation templates have additional capabilities that you can use to build complex sets of resources and reuse those templates in multiple contexts\. For example, you can add input parameters whose values are specified when you create a CloudFormation stack\. In other words, you can specify a value like the instance type when you create a stack instead of when you create the template, making the template easier to reuse in different situations\.

For more information about template creation and capabilities, see [Template anatomy](template-anatomy.md)\.

For more information about declaring specific resources, see [AWS resource and property types reference](aws-template-resource-type-ref.md)\.

To start designing your own templates with AWS CloudFormation Designer, go to [https://console\.aws\.amazon\.com/cloudformation/designer](https://console.aws.amazon.com/cloudformation/designer)\.

## Stacks<a name="w2ab1b5c15b9"></a>

When you use CloudFormation, you manage related resources as a single unit called a stack\. You create, update, and delete a collection of resources by creating, updating, and deleting stacks\. All the resources in a stack are defined by the stack's CloudFormation template\. Suppose you created a template that includes an Auto Scaling group, Elastic Load Balancing load balancer, and an Amazon Relational Database Service \(Amazon RDS\) database instance\. To create those resources, you create a stack by submitting the template that you created, and CloudFormation provisions all those resources for you\. You can work with stacks by using the CloudFormation [console](https://console.aws.amazon.com/cloudformation/), [API](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/), or [AWS CLI](https://docs.aws.amazon.com/cli/latest/reference/cloudformation)\.

For more information about creating, updating, or deleting stacks, see [Working with stacks](stacks.md)\.

## Change sets<a name="cfn-concepts-change-sets"></a>

If you need to make changes to the running resources in a stack, you update the stack\. Before making changes to your resources, you can generate a change set, which is a summary of your proposed changes\. Change sets allow you to see how your changes might impact your running resources, especially for critical resources, before implementing them\.

For example, if you change the name of an Amazon RDS database instance, CloudFormation will create a new database and delete the old one\. You will lose the data in the old database unless you've already backed it up\. If you generate a change set, you will see that your change will cause your database to be replaced, and you will be able to plan accordingly before you update your stack\. For more information, see [Updating stacks using change sets](using-cfn-updating-stacks-changesets.md)\.