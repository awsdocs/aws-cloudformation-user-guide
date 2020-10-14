# Learn template basics<a name="gettingstarted.templatebasics"></a>

**Topics**
+ [What is an AWS CloudFormation template?](#gettingstarted.templatebasics.what)
+ [Resources: Hello Bucket\!](#gettingstarted.templatebasics.simple)
+ [Resource properties and using resources together](#gettingstarted.templatebasics.multiple)
+ [Receiving user input using input parameters](#gettingstarted.templatebasics.parameters)
+ [Specifying conditional values using mappings](#gettingstarted.templatebasics.mappings)
+ [Constructed values and output values](#gettingstarted.templatebasics.outputs)
+ [Next steps](#gettingstarted.templatebasics.learnmore)

In [Get started](GettingStarted.Walkthrough.md), you learned how to use a template to create a stack\. You saw resources declared in a template and how they map to resources in the stack\. We also touched on input parameters and how they enable you to pass in specific values when you create a stack from a template\. In this section, we'll go deeper into resources and parameters\. We'll also cover the other components of templates so that you'll know how to use these components together to create templates that produce the AWS resources you want\.

## What is an AWS CloudFormation template?<a name="gettingstarted.templatebasics.what"></a>

A template is a declaration of the AWS resources that make up a stack\. The template is stored as a text file whose format complies with the JavaScript Object Notation \(JSON\) or YAML standard\. Because they are just text files, you can create and edit them in any text editor and manage them in your source control system with the rest of your source code\. For more information about the template formats, see [AWS CloudFormation template formats](template-formats.md)\.

In the template, you declare the AWS resources you want to create and configure\. You declare an object as a name\-value pair or a pairing of a name with a set of child objects enclosed\. The syntax depends on the format you use\. For more information, see the [Template anatomy](template-anatomy.md)\. The only required top\-level object is the Resources object, which must declare at least one resource\. Let's start with the most basic template containing only a Resources object, which contains a single resource declaration\.

## Resources: Hello Bucket\!<a name="gettingstarted.templatebasics.simple"></a>

The Resources object contains a list of resource objects\. A resource declaration contains the resource's attributes, which are themselves declared as child objects\. A resource must have a `Type` attribute, which defines the kind of AWS resource you want to create\. The `Type` attribute has a special format:

```
AWS::ProductIdentifier::ResourceType
```

For example, the resource type for an Amazon S3 bucket is [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)\. For a full list of resource types, see [Template reference](template-reference.md)\.

Let's take a look at a very basic template\. The following template declares a single resource of type AWS::S3::Bucket: with the name HelloBucket\.

**Example JSON**  

```
{
    "Resources" : {
        "HelloBucket" : {
            "Type" : "AWS::S3::Bucket"
        }
    }
}
```

**Example YAML**  

```
Resources:
  HelloBucket:
    Type: AWS::S3::Bucket
```

If you use this template to create a stack, AWS CloudFormation will create an Amazon S3 bucket\. Creating a bucket is simple, because AWS CloudFormation can create a bucket with default settings\. For other resources, such as an Auto Scaling group or EC2 instance, AWS CloudFormation requires more information\. Resource declarations use a `Properties` attribute to specify the information used to create a resource\.

 Depending on the resource type, some properties are required, such as the ImageId property for an [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource, and others are optional\. Some properties have default values, such as the AccessControl property of the AWS::S3::Bucket resource, so specifying a value for those properties is optional\. Other properties are not required but may add functionality that you want, such as the WebsiteConfiguration property of the AWS::S3::Bucket resource\. Specifying a value for such properties is entirely optional and based on your needs\. In the example above, because the AWS::S3::Bucket resource has only optional properties and we didn't need any of the optional features, we could accept the defaults and omit the Properties attribute\. 

 To view the properties for each resource type, see the topics in [AWS resource and property types reference](aws-template-resource-type-ref.md)\.

## Resource properties and using resources together<a name="gettingstarted.templatebasics.multiple"></a>

Usually, a property for a resource is simply a string value\. For example, the following template specifies a canned ACL \(PublicRead\) for the AccessControl property of the bucket\.

**Example JSON**  

```
{
    "Resources" : {
        "HelloBucket" : {
            "Type" : "AWS::S3::Bucket",
            "Properties" : {
               "AccessControl" : "PublicRead"               
            }
        }
    }
}
```

**Example YAML**  

```
Resources:
  HelloBucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: PublicRead
```

Some resources can have multiple properties, and some properties can have one or more subproperties\. For example, the [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html) resource has two properties, AccessControl and WebsiteConfiguration\. The WebsiteConfiguration property has two subproperties, IndexDocument and ErrorDocument\. The following template shows our original bucket resource with the additional properties\.

**Example JSON**  

```
{
    "Resources" : {
        "HelloBucket" : {
            "Type" : "AWS::S3::Bucket",
            "Properties" : {
               "AccessControl" : "PublicRead",
               "WebsiteConfiguration" : {
                    "IndexDocument" : "index.html",
                    "ErrorDocument" : "error.html"            
               }               
            }
        }
    }
}
```

**Example YAML**  

```
Resources:
  HelloBucket:
    Type: AWS::S3::Bucket
    Properties:
      AccessControl: PublicRead
      WebsiteConfiguration:
        IndexDocument: index.html
        ErrorDocument: error.html
```

One of the greatest benefits of templates and AWS CloudFormation is the ability to create a set of resources that work together to create an application or solution\. The name used for a resource within the template is a logical name\. When AWS CloudFormation creates the resource, it generates a physical name that is based on the combination of the logical name, the stack name, and a unique ID\.

 You're probably wondering how you set properties on one resource based on the name or property of another resource\. For example, you can create a CloudFront distribution backed by an S3 bucket or  an EC2 instance that uses EC2 security groups, and all of these resources can be created in the same template\. AWS CloudFormation has a number of intrinsic functions that you can use to refer to other resources and their properties\. You can use the [Ref function](intrinsic-function-reference-ref.md) to refer to an identifying property of a resource\. Frequently, this is the physical name of the resource; however, sometimes it can be an identifier, such as the IP address for an [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html) resource or an Amazon Resource Name \(ARN\) for an Amazon SNS topic\. For a list of values returned by the Ref function, see [Ref function](intrinsic-function-reference-ref.md)\. The following template contains an [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) resource\. The resource's SecurityGroups property calls the Ref function to refer to the AWS::EC2::SecurityGroup resource InstanceSecurityGroup\.

**Example JSON**  

```
{
    "Resources": {
        "Ec2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "SecurityGroups": [
                    {
                        "Ref": "InstanceSecurityGroup"
                    }
                ],
                "KeyName": "mykey",
                "ImageId": ""
            }
        },
        "InstanceSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable SSH access via port 22",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": "22",
                        "ToPort": "22",
                        "CidrIp": "0.0.0.0/0"
                    }
                ]
            }
        }
    }
}
```

**Example YAML**  

```
Resources:
  Ec2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      SecurityGroups:
        - !Ref InstanceSecurityGroup
      KeyName: mykey
      ImageId: ''
  InstanceSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access via port 22
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '22'
          ToPort: '22'
          CidrIp: 0.0.0.0/0
```

The SecurityGroups property is a list of security groups, and in the previous example we have only one item in the list\. The following template has an additional item in the SecurityGroups property list\. 

**Example JSON**  

```
{
    "Resources": {
        "Ec2Instance": {
            "Type": "AWS::EC2::Instance",
            "Properties": {
                "SecurityGroups": [
                    {
                        "Ref": "InstanceSecurityGroup"
                    },
                    "MyExistingSecurityGroup"
                ],
                "KeyName": "mykey",
                "ImageId": "ami-7a11e213"
            }
        },
        "InstanceSecurityGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "Enable SSH access via port 22",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": "22",
                        "ToPort": "22",
                        "CidrIp": "0.0.0.0/0"
                    }
                ]
            }
        }
    }
}
```

**Example YAML**  

```
Resources:
  Ec2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      SecurityGroups:
        - !Ref InstanceSecurityGroup
        - MyExistingSecurityGroup
      KeyName: mykey
      ImageId: ami-7a11e213
  InstanceSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access via port 22
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '22'
          ToPort: '22'
          CidrIp: 0.0.0.0/0
```

MyExistingSecurityGroup is a string that refers to an existing EC2 security group instead of a security group declared in a template\. You use literal strings to refer to existing AWS resources\.

In the example above, the KeyName property of the [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) is the literal string mykey\. This means that a key pair with the name mykey must exist in the region where the stack is being created; otherwise, stack creation will fail because the key pair does not exist\. The key pair you use can vary with the region where you are creating the stack, or you may want to share the template with someone else so that they can use it with their AWS account\. If so, you can use an input parameter so that the key pair name can be specified when the stack is created\. The Ref function can refer to input parameters that are specified at stack creation time\. The following template adds a Parameters object containing the KeyName parameter, which is used to specify the KeyName property for the AWS::EC2::Instance resource\. The parameter type is `AWS::EC2::KeyPair::KeyName`, which ensures a user specifies a valid key pair name in his or her account and in the region where the stack is being created\.

**Example JSON**  

```
{
  "Parameters": {
    "KeyName": {
      "Description": "The EC2 Key Pair to allow SSH access to the instance",
      "Type": "AWS::EC2::KeyPair::KeyName"
    }
  },
  "Resources": {
    "Ec2Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "SecurityGroups": [
          {
            "Ref": "InstanceSecurityGroup"
          },
          "MyExistingSecurityGroup"
        ],
        "KeyName": {
          "Ref": "KeyName"
        },
        "ImageId": "ami-7a11e213"
      }
    },
    "InstanceSecurityGroup": {
      "Type": "AWS::EC2::SecurityGroup",
      "Properties": {
        "GroupDescription": "Enable SSH access via port 22",
        "SecurityGroupIngress": [
          {
            "IpProtocol": "tcp",
            "FromPort": "22",
            "ToPort": "22",
            "CidrIp": "0.0.0.0/0"
          }
        ]
      }
    }
  }
}
```

**Example YAML**  

```
Parameters:
  KeyName:
    Description: The EC2 Key Pair to allow SSH access to the instance
    Type: 'AWS::EC2::KeyPair::KeyName'
Resources:
  Ec2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      SecurityGroups:
        - !Ref InstanceSecurityGroup
        - MyExistingSecurityGroup
      KeyName: !Ref KeyName
      ImageId: ami-7a11e213
  InstanceSecurityGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: Enable SSH access via port 22
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '22'
          ToPort: '22'
          CidrIp: 0.0.0.0/0
```

The Ref function is handy if the parameter or the value returned for a resource is exactly what you want; however, you may need other attributes of a resource\. For example, if you want to create a CloudFront distribution with an S3 origin, you need to specify the bucket location by using a DNS\-style address\. A number of resources have additional attributes whose values you can use in your template\. To get these attributes, you use the [Fn::GetAtt](intrinsic-function-reference-getatt.md) function\. The following template creates a CloudFront distribution resource that specifies the DNS name of an S3 bucket resource using Fn::GetAtt function to get the bucket's DomainName attribute\. 

**Example JSON**  

```
{
  "Resources": {
    "myBucket": {
      "Type": "AWS::S3::Bucket"
    },
    "myDistribution": {
      "Type": "AWS::CloudFront::Distribution",
      "Properties": {
        "DistributionConfig": {
          "Origins": [
            {
              "DomainName": {
                "Fn::GetAtt": [
                  "myBucket",
                  "DomainName"
                ]
              },
              "Id": "myS3Origin",
              "S3OriginConfig": {}
            }
          ],
          "Enabled": "true",
          "DefaultCacheBehavior": {
            "TargetOriginId": "myS3Origin",
            "ForwardedValues": {
              "QueryString": "false"
            },
            "ViewerProtocolPolicy": "allow-all"
          }
        }
      }
    }
  }
}
```

**Example YAML**  

```
Resources:
  myBucket:
    Type: 'AWS::S3::Bucket'
  myDistribution:
    Type: 'AWS::CloudFront::Distribution'
    Properties:
      DistributionConfig:
        Origins:
          - DomainName: !GetAtt 
              - myBucket
              - DomainName
            Id: myS3Origin
            S3OriginConfig: {}
        Enabled: 'true'
        DefaultCacheBehavior:
          TargetOriginId: myS3Origin
          ForwardedValues:
            QueryString: 'false'
          ViewerProtocolPolicy: allow-all
```

The Fn::GetAtt function takes two parameters, the logical name of the resource and the name of the attribute to be retrieved\. For a full list of available attributes for resources, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. You'll notice that the Fn::GetAtt function lists its two parameters in an array\. For functions that take multiple parameters, you use an array to specify their parameters\.

## Receiving user input using input parameters<a name="gettingstarted.templatebasics.parameters"></a>

So far, you've learned about resources and a little bit about how to use them together within a template\. You've learned how to refer to input parameters, but we haven't gone deeply into how to define the input parameters themselves\. Let's take a look at parameter declarations and how you can restrict and validate user input\.

You declare parameters in a template's Parameters object\. A parameter contains a list of attributes that define its value and constraints against its value\. The only required attribute is Type, which can be String, Number, or an AWS\-specific type\. You can also add a Description attribute that tells a user more about what kind of value they should specify\. The parameter's name and description appear in the Specify Parameters page when a user uses the template in the Create Stack wizard\.

The following template fragment is a Parameters object that declares the parameters used in the Specify Parameters page above\. 

**Example JSON**  

```
  "Parameters": {
    "KeyName": {
      "Description" : "Name of an existing EC2 KeyPair to enable SSH access into the WordPress web server",
      "Type": "AWS::EC2::KeyPair::KeyName"
    },
    "WordPressUser": {
      "Default": "admin",
      "NoEcho": "true",
      "Description" : "The WordPress database admin account user name",
      "Type": "String",
      "MinLength": "1",
      "MaxLength": "16",
      "AllowedPattern" : "[a-zA-Z][a-zA-Z0-9]*"
    },
    "WebServerPort": {
      "Default": "8888",
      "Description" : "TCP/IP port for the WordPress web server",
      "Type": "Number",
      "MinValue": "1",
      "MaxValue": "65535"
    }
  }
```

**Example YAML**  

```
Parameters:
  KeyName:
    Description: Name of an existing EC2 KeyPair to enable SSH access into the WordPress web server
    Type: AWS::EC2::KeyPair::KeyName
  WordPressUser:
    Default: admin
    NoEcho: true
    Description: The WordPress database admin account user name
    Type: String
    MinLength: 1
    MaxLength: 16
    AllowedPattern: "[a-zA-Z][a-zA-Z0-9]*"
  WebServerPort:
    Default: 8888
    Description: TCP/IP port for the WordPress web server
    Type: Number
    MinValue: 1
    MaxValue: 65535
```

For parameters with default values, AWS CloudFormation uses the default values unless users specify another value\. If you omit the default attribute, users are required to specify a value for that parameter; however, requiring the user to input a value does not ensure that the value is valid\. To validate the value of a parameter, you can declare constraints or specify an AWS\-specific parameter type\.

You'll notice that the `KeyName` parameter has no `Default` attribute and the other parameters do\. For example, the `WordPress` parameter has the attribute `Default: admin`, but the `KeyName` parameter has none\. Users must specify a key name value at stack creation\. If they don’t, AWS CloudFormation fails to create the stack and throws an exception: `Parameters: [KeyName] must have values`\.

For AWS\-specific parameter types, AWS CloudFormation validates input values against existing values in the user's AWS account and in the region where he or she is creating the stack *before* creating any stack resources\. In the sample template, the `KeyName` parameter is an AWS\-specific parameter type of `AWS::EC2::KeyPair::KeyName`\. AWS CloudFormation checks that users specify a valid EC2 key pair name before creating the stack\. Another example of an AWS\-specific parameter type is `AWS::EC2::VPC::Id`, which requires users to specify a valid VPC ID\. In addition to upfront validation, the AWS console shows a drop\-down list of valid values for AWS\-specific parameter types, such as valid EC2 key pair names or VPC IDs, when users use the Create Stack wizard\.

 For the `String` type, you can use the following attributes to declare constraints: `MinLength`, `MaxLength`, `Default`, `AllowedValues`, and `AllowedPattern`\. In the example above, the `WordPressUser` parameter has three constraints: the parameter value must be 1 to 16 character long \(`MinLength`, `MaxLength`\) and must begin with a letter followed by any combination of letters and numbers \(`AllowedPattern`\)\. 

 For the `Number` type, you can declare the following constraints: `MinValue`, `MaxValue`, `Default`, and `AllowedValues`\. A number can be an integer or a float value\. In the example above, the `WebServerPort` parameter must be a number between 1 and 65535 inclusive \(`MinValue`, `MaxValue`\)\. 

Earlier in this section, we mentioned that parameters are a good way to specify sensitive or implementation\-specific data, such as passwords or user names, that you need to use but do not want to embed in the template itself\. If you set the `NoEcho` attribute to `true`, CloudFormation returns the parameter value masked as asterisks \(\*\*\*\*\*\) for any calls that describe the stack or stack events, except for information stored in the locations specified below\. In the example above, the `WordPressUser` parameter value is not visible to anyone viewing the stack's settings, and its value is returned as asterisks\. 

**Important**  
Using the `NoEcho` attribute does not mask any information stored in the following:  
The `Metadata` template section\. CloudFormation does not transform, modify, or redact any information you include in the `Metadata` section\. For more information, see [Metadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)\.
The `Outputs` template section\. For more information, see [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)\.
The `Metadata` attribute of a resource definition\. For more information, [Metadata attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-metadata.html)\.
We strongly recommend you do not use these mechanisms to include sensitive information, such as passwords or secrets\.

**Important**  
Rather than embedding sensitive information directly in your AWS CloudFormation templates, we recommend you use dynamic parameters in the stack template to reference sensitive information that is stored and managed outside of CloudFormation, such as in the AWS Systems Manager Parameter Store or AWS Secrets Manager\.  
For more information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.

## Specifying conditional values using mappings<a name="gettingstarted.templatebasics.mappings"></a>

Parameters are a great way to enable users to specify unique or sensitive values for use in the properties of stack resources; however, there may be settings that are region dependent or are somewhat complex for users to figure out because of other conditions or dependencies\. In these cases, you would want to put some logic in the template itself so that users can specify simpler values \(or none at all\) to get the results that they want\. In an earlier example, we hardcoded the AMI ID for the ImageId property of our EC2 instance\. This works fine in the US\-East region, where it represents the AMI that we want\. However, if the user tries to build the stack in a different region he or she will get the wrong AMI or no AMI at all\. \(AMI IDs are unique to a region, so the same AMI ID in a different region may not represent any AMI or a completely different one\.\) 

 To avoid this problem, you need a way to specify the right AMI ID based on a conditional input \(in this example, the region where the stack is created\)\. There are two template features that can help, the Mappings object and the AWS::Region pseudo parameter\.

The AWS::Region pseudo parameter is a value that AWS CloudFormation resolves as the region where the stack is created\. Pseudo parameters are resolved by AWS CloudFormation when you create the stack\. Mappings enable you to use an input value as a condition that determines another value\. Similar to a switch statement, a mapping associates one set of values with another\. Using the AWS::Region parameter together with a mapping, you can ensure that an AMI ID appropriate to the region is specified\. The following template contains a Mappings object with a mapping named RegionMap that is used to map an AMI ID to the appropriate region\. 

**Example JSON**  

```
{
  "Parameters": {
    "KeyName": {
      "Description": "Name of an existing EC2 KeyPair to enable SSH access to the instance",
      "Type": "String"
    }
  },
  "Mappings": {
    "RegionMap": {
      "us-east-1": {
        "AMI": "ami-76f0061f"
      },
      "us-west-1": {
        "AMI": "ami-655a0a20"
      },
      "eu-west-1": {
        "AMI": "ami-7fd4e10b"
      },
      "ap-southeast-1": {
        "AMI": "ami-72621c20"
      },
      "ap-northeast-1": {
        "AMI": "ami-8e08a38f"
      }
    }
  },
  "Resources": {
    "Ec2Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "KeyName": {
          "Ref": "KeyName"
        },
        "ImageId": {
          "Fn::FindInMap": [
            "RegionMap",
            {
              "Ref": "AWS::Region"
            },
            "AMI"
          ]
        },
        "UserData": {
          "Fn::Base64": "80"
        }
      }
    }
  }
}
```

**Example YAML**  

```
Parameters:
  KeyName:
    Description: Name of an existing EC2 KeyPair to enable SSH access to the instance
    Type: String
Mappings:
  RegionMap:
    us-east-1:
      AMI: ami-76f0061f
    us-west-1:
      AMI: ami-655a0a20
    eu-west-1:
      AMI: ami-7fd4e10b
    ap-southeast-1:
      AMI: ami-72621c20
    ap-northeast-1:
      AMI: ami-8e08a38f
Resources:
  Ec2Instance:
    Type: 'AWS::EC2::Instance'
    Properties:
      KeyName: !Ref KeyName
      ImageId: !FindInMap 
        - RegionMap
        - !Ref 'AWS::Region'
        - AMI
      UserData: !Base64 '80'
```

In the RegionMap, each region is mapped to a name\-value pair\. The name\-value pair is a label, and the value to map\. In the RegionMap, AMI is the label and the AMI ID is the value\. To use a map to return a value, you use the [Fn::FindInMap](intrinsic-function-reference-findinmap.md) function, passing the name of the map, the value used to find the mapped value, and the label of the mapped value you want to return\. In the example above, the ImageId property of the resource Ec2Instance uses the Fn::FindInMap function to determine its value by specifying RegionMap as the map to use, AWS::Region as the input value to map from, and AMI as the label to identify the value to map to\. For example, if this template were used to create a stack in the us\-west\-1 region, ImageId would be set to ami\-655a0a20\. 

**Tip**  
The AWS::Region pseudo parameter enables you to get the region where the stack is created\. Some resources, such as [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html), [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html), and [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html), have a property that specifies availability zones\. You can use the [Fn::GetAZs function](intrinsic-function-reference-getavailabilityzones.md) to get the list of all availability zones in a region\.

## Constructed values and output values<a name="gettingstarted.templatebasics.outputs"></a>

Parameters and mappings are an excellent way to pass or determine specific values at stack creation time, but there can be situations where a value from a parameter or other resource attribute is only part of the value you need\. For example, in the following fragment from the WordPress template, the Fn::Join function constructs the Target subproperty of the HealthCheck property for the ElasticLoadBalancer resource by concatenating the WebServerPort parameter with other literal strings to form the value needed\.

**Example JSON**  

```
{
  "Resources": {
    "ElasticLoadBalancer": {
      "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
      "Properties": {
        "AvailabilityZones": {
          "Fn::GetAZs": ""
        },
        "Instances": [
          {
            "Ref": "Ec2Instance1"
          },
          {
            "Ref": "Ec2Instance2"
          }
        ],
        "Listeners": [
          {
            "LoadBalancerPort": "80",
            "InstancePort": {
              "Ref": "WebServerPort"
            },
            "Protocol": "HTTP"
          }
        ],
        "HealthCheck": {
          "Target": {
            "Fn::Join": [
              "",
              [
                "HTTP:",
                {
                  "Ref": "WebServerPort"
                },
                "/"
              ]
            ]
          },
          "HealthyThreshold": "3",
          "UnhealthyThreshold": "5",
          "Interval": "30",
          "Timeout": "5"
        }
      }
    }
  }
}
```

**Example YAML**  

```
Resources:
  ElasticLoadBalancer:
    Type: 'AWS::ElasticLoadBalancing::LoadBalancer'
    Properties:
      AvailabilityZones: !GetAZs ''
      Instances:
        - !Ref Ec2Instance1
        - !Ref Ec2Instance2
      Listeners:
        - LoadBalancerPort: '80'
          InstancePort: !Ref WebServerPort
          Protocol: HTTP
      HealthCheck:
        Target: !Join 
          - ''
          - - 'HTTP:'
            - !Ref WebServerPort
            - /
        HealthyThreshold: '3'
        UnhealthyThreshold: '5'
        Interval: '30'
        Timeout: '5'
```

The Fn::Join function takes two parameters, a delimiter that separates the values you want to concatenate and an array of values in the order that you want them to appear\. In the example above, the Fn::Join function specifies an empty string as the delimiter and HTTP:, the value of the WebServerPort parameter, and a / character as the values to concatenate\. If WebServerPort had a value of 8888, the Target property would be set to the following value: 

```
HTTP:8888/
```

The Fn::Join function is also useful for declaring output values for the stack\. The Outputs object in the template contains declarations for the values that you want to have available after the stack is created\. An output is a convenient way to capture important information about your resources or input parameters\. For example, in the WordPress template, we declare the following Outputs object\.

**Example JSON**  

```
"Outputs": {
  "InstallURL": {
    "Value": {
      "Fn::Join": [
        "",
        [
          "http://",
          {
            "Fn::GetAtt": [
              "ElasticLoadBalancer",
              "DNSName"
            ]
          },
          "/wp-admin/install.php"
        ]
      ]
    },
    "Description": "Installation URL of the WordPress website"
  },
  "WebsiteURL": {
    "Value": {
      "Fn::Join": [
        "",
        [
          "http://",
          {
            "Fn::GetAtt": [
              "ElasticLoadBalancer",
              "DNSName"
            ]
          }
        ]
      ]
    }
  }
}
```

**Example YAML**  

```
Outputs:
  InstallURL:
    Value: !Join 
      - ''
      - - 'http://'
        - !GetAtt 
          - ElasticLoadBalancer
          - DNSName
        - /wp-admin/install.php
    Description: Installation URL of the WordPress website
  WebsiteURL:
    Value: !Join 
      - ''
      - - 'http://'
        - !GetAtt 
          - ElasticLoadBalancer
          - DNSName
```

Each output value has a name, a Value attribute that contains declaration of the value returned as the output value, and optionally a description of the value\. In the previous example, InstallURL is the string returned by a Fn::Join function call that concatenates http://, the DNS name of the resource ElasticLoadBalancer, and /wp\-admin/install\.php\. The output value would be similar to the following:

```
http://mywptests-elasticl-1gb51l6sl8y5v-206169572.us-east-2.elb.amazonaws.com/wp-admin/install.php
```

In the Get Started tutorial, we used this link to conveniently go to the installation page for the WordPress blog that we created\. AWS CloudFormation generates the output values after it finishes creating the stack\. You can view output values in the Outputs tab of the AWS CloudFormation console or by using the aws cloudformation describe\-stacks command\.

## Next steps<a name="gettingstarted.templatebasics.learnmore"></a>

We just walked through the basic parts of a template and how to use them\. You learned the following about templates:
+ Declaring resources and their properties
+ Referencing other resources with the Ref function and resource attributes using the Fn::GetAtt function
+ Using parameters to enable users to specify values at stack creation time and using constraints to validate parameter input
+ Using mappings to determine conditional values
+ Using the Fn::Join function to construct values based on parameters, resource attributes, and other strings
+ Using output values to capture information about the stack's resources\.

We didn't cover two top level objects in a template: AWSTemplateFormatVersion and Description\. AWSTemplateFormatVersion is simply the version of the template format—if you don't specify it, AWS CloudFormation will use the latest version\. The Description is any valid JSON or YAML string\. This description appears in the Specify Parameters page of the Create Stack wizard\. For more information, see [Format version](format-version-structure.md) and [Description](template-description-structure.md)\.

Of course, there are more advanced template and stack features\. Here is a list of a few important ones that you'll want to learn more about:

*Optional attributes* that can be used with any resource:
+ [DependsOn attribute](aws-attribute-dependson.md) enables you to specify that one resource must be created after another\.
+ [DeletionPolicy attribute](aws-attribute-deletionpolicy.md) enables you to specify how AWS CloudFormation should handle the deletion of a resource\.
+ [Metadata](aws-attribute-metadata.md) attribute enables you to specify structured data with a resource\.

[https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html) enables you to nest another stack as a resource within your template\.