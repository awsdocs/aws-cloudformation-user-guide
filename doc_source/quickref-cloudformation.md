# AWS CloudFormation template snippets<a name="quickref-cloudformation"></a>

**Topics**
+ [Nested stacks](#w7739ab1c27c22c19b5)
+ [Wait condition](#w7739ab1c27c22c19b7)

## Nested stacks<a name="w7739ab1c27c22c19b5"></a>

### Nesting a stack in a template<a name="scenario-stack"></a>

This example template contains a nested stack resource called `myStack`\. When AWS CloudFormation creates a stack from the template, it creates the `myStack`, whose template is specified in the `TemplateURL` property\.  The output value `StackRef` returns the stack ID for `myStack` and the value `OutputFromNestedStack` returns the output value `BucketName` from within the `myStack` resource\. The Outputs\.*nestedstackoutputname* format is reserved for specifying output values from nested stacks and can be used anywhere within the containing template\.

For more information, see [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)\.

#### JSON<a name="quickref-cloudformation-example-1.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion" : "2010-09-09",
 3.     "Resources" : {
 4.         "myStack" : {
 5. 	       "Type" : "AWS::CloudFormation::Stack",
 6. 	       "Properties" : {
 7. 	        "TemplateURL" : "https://s3.amazonaws.com/cloudformation-templates-us-east-1/S3_Bucket.template",
 8.               "TimeoutInMinutes" : "60"
 9. 	       }
10.         }
11.     },
12.     "Outputs": {
13.        "StackRef": {"Value": { "Ref" : "myStack"}},
14.        "OutputFromNestedStack" : {
15.              "Value" : { "Fn::GetAtt" : [ "myStack", "Outputs.BucketName" ] }
16.        }
17.     }
18. }
```

#### YAML<a name="quickref-cloudformation-example-1.yaml"></a>

```
 1. AWSTemplateFormatVersion: '2010-09-09'
 2. Resources:
 3.   myStack:
 4.     Type: AWS::CloudFormation::Stack
 5.     Properties:
 6.       TemplateURL: https://s3.amazonaws.com/cloudformation-templates-us-east-1/S3_Bucket.template
 7.       TimeoutInMinutes: '60'
 8. Outputs:
 9.   StackRef:
10.     Value: !Ref myStack
11.   OutputFromNestedStack:
12.     Value: !GetAtt myStack.Outputs.BucketName
```

### Nesting a stack with input parameters in a template<a name="scenario-stack-parameters"></a>

This example template contains a stack resource that specifies input parameters\. When AWS CloudFormation creates a stack from this template, it uses the value pairs declared within the Parameters property as the input parameters for the template used to create the `myStackWithParams` stack\. In this example, the `InstanceType` and `KeyName` parameters are specified\.

For more information, see [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)\.

#### JSON<a name="quickref-cloudformation-example-2.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion" : "2010-09-09",
 3.     "Resources" : {
 4.         "myStackWithParams" : {
 5.   	       "Type" : "AWS::CloudFormation::Stack",
 6. 	       "Properties" : {
 7. 	           "TemplateURL" : "https://s3.amazonaws.com/cloudformation-templates-us-east-1/EC2ChooseAMI.template",
 8. 	           "Parameters" : {
 9. 	               "InstanceType" : "t2.micro",
10. 	               "KeyName" : "mykey"
11. 	           }
12.    	       }
13.         }
14.     }
15. }
```

#### YAML<a name="quickref-cloudformation-example-2.yaml"></a>

```
1. AWSTemplateFormatVersion: '2010-09-09'
2. Resources:
3.   myStackWithParams:
4.     Type: AWS::CloudFormation::Stack
5.     Properties:
6.       TemplateURL: https://s3.amazonaws.com/cloudformation-templates-us-east-1/EC2ChooseAMI.template
7.       Parameters:
8.         InstanceType: t2.micro
9.         KeyName: mykey
```

## Wait condition<a name="w7739ab1c27c22c19b7"></a>

### Using a wait condition with an Amazon EC2 instance<a name="scenario-waitcondition"></a>

**Important**  
For Amazon EC2 and Auto Scaling resources, we recommend that you use a CreationPolicy attribute instead of wait conditions\. Add a CreationPolicy attribute to those resources, and use the cfn\-signal helper script to signal when an instance creation process has completed successfully\.

If you can't use a creation policy, you view the following example template, which declares an Amazon EC2 instance with a wait condition\. The wait condition myWaitCondition uses myWaitConditionHandle for signaling, uses the [DependsOn attribute](aws-attribute-dependson.md) to specify that the wait condition will trigger after the Amazon EC2 instance resource has been created, and uses the Timeout property to specify a duration of 4500 seconds for the wait condition\. In addition, the presigned URL that signals the wait condition is passed to the Amazon EC2 instance with the UserData property of the Ec2Instance resource, thus enabling an application or script running on that Amazon EC2 instance to retrieve the pre\-signed URL and employ it to signal a success or failure to the wait condition\. Note that you need to use cfn\-signal or create the application or script that signals the wait condition\. The output value ApplicationData contains the data passed back from the wait condition signal\.

For more information, see [Creating wait conditions in a template](using-cfn-waitcondition.md), [AWS::CloudFormation::WaitCondition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitcondition.html), [AWS::CloudFormation::WaitConditionHandle](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitconditionhandle.html), and [cfn\-signal](cfn-signal.md)\.

#### JSON<a name="quickref-cloudformation-example-3.json"></a>

```
 1. {
 2.     "AWSTemplateFormatVersion" : "2010-09-09",
 3.     "Mappings" : {
 4.         "RegionMap" : {
 5.             "us-east-1" : {
 6.                 "AMI" : "ami-0ff8a91507f77f867"
 7.             },
 8.             "us-west-1" : {
 9.                 "AMI" : "ami-0bdb828fd58c52235"
10.             },
11.             "eu-west-1" : {
12.                 "AMI" : "ami-047bb4163c506cd98"
13.             },
14.             "ap-northeast-1" : {
15.                 "AMI" : "ami-06cd52961ce9f0d85"
16.             },
17.             "ap-southeast-1" : {
18.                 "AMI" : "ami-08569b978cc4dfa10"
19.             }
20.         }
21.     },
22.     "Resources" : {
23.         "Ec2Instance" : {
24.             "Type" : "AWS::EC2::Instance",
25.             "Properties" : {
26.                 "UserData" : { "Fn::Base64" : {"Ref" : "myWaitHandle"}},
27.                 "ImageId" : { "Fn::FindInMap" : [ "RegionMap", { "Ref" : "AWS::Region" }, "AMI" ]}
28.             }
29.         },
30.         "myWaitHandle" : {
31.             "Type" : "AWS::CloudFormation::WaitConditionHandle",
32.             "Properties" : {
33.             }
34.         },
35.         "myWaitCondition" : {
36.             "Type" : "AWS::CloudFormation::WaitCondition",
37.             "DependsOn" : "Ec2Instance",
38.             "Properties" : {
39.                 "Handle" : { "Ref" : "myWaitHandle" },
40.                 "Timeout" : "4500"
41.             }
42.         }
43.     },
44.     "Outputs" : {
45.         "ApplicationData" : {
46.             "Value" : { "Fn::GetAtt" : [ "myWaitCondition", "Data" ]},
47.             "Description" : "The data passed back as part of signalling the WaitCondition."
48.         }
49.     }
50. }
```

#### YAML<a name="quickref-cloudformation-example-3.yaml"></a>

```
 1. AWSTemplateFormatVersion: '2010-09-09'
 2. Mappings:
 3.   RegionMap:
 4.     us-east-1:
 5.       AMI: ami-0ff8a91507f77f867
 6.     us-west-1:
 7.       AMI: ami-0bdb828fd58c52235
 8.     eu-west-1:
 9.       AMI: ami-047bb4163c506cd98
10.     ap-northeast-1:
11.       AMI: ami-06cd52961ce9f0d85
12.     ap-southeast-1:
13.       AMI: ami-08569b978cc4dfa10
14. Resources:
15.   Ec2Instance:
16.     Type: AWS::EC2::Instance
17.     Properties:
18.       UserData:
19.         Fn::Base64: !Ref myWaitHandle
20.       ImageId:
21.         Fn::FindInMap:
22.         - RegionMap
23.         - Ref: AWS::Region
24.         - AMI
25.   myWaitHandle:
26.     Type: AWS::CloudFormation::WaitConditionHandle
27.     Properties: {}
28.   myWaitCondition:
29.     Type: AWS::CloudFormation::WaitCondition
30.     DependsOn: Ec2Instance
31.     Properties:
32.       Handle: !Ref myWaitHandle
33.       Timeout: '4500'
34. Outputs:
35.   ApplicationData:
36.     Value: !GetAtt myWaitCondition.Data
37.     Description: The data passed back as part of signalling the WaitCondition.
```

### Using the cfn\-signal helper script to signal a wait condition<a name="scenario-waitcondition-cfn-signal"></a>

This example shows a cfn\-signal command line that signals success to a wait condition\. You need to define the command line in the `UserData` property of the EC2 instance\.

#### JSON<a name="w7739ab1c27c22c19b7b4b4"></a>

```
"UserData": {
  "Fn::Base64": {
    "Fn::Join": [
      "", 
      [
         "#!/bin/bash -xe\n",
         "/opt/aws/bin/cfn-signal --exit-code 0 '", 
         {
           "Ref": "myWaitHandle"
         },
         "'\n"
      ]   
    ]
  }
}
```

#### YAML<a name="w7739ab1c27c22c19b7b4b6"></a>

```
UserData:
  'Fn::Base64':
    'Fn::Join':
      - ''
      - - |
          #!/bin/bash -xe
        - /opt/aws/bin/cfn-signal --exit-code 0 '
        - Ref: myWaitHandle
        - |
          '
```

### Using Curl to signal a wait condition<a name="scenario-waitcondition-curl"></a>

This example shows a Curl command line that signals success to a wait condition\.

```
1. curl -T /tmp/a "https://cloudformation-waitcondition-test.s3.amazonaws.com/arn%3Aaws%3Acloudformation%3Aus-east-1%3A034017226601%3Astack%2Fstack-gosar-20110427004224-test-stack-with-WaitCondition--VEYW%2Fe498ce60-70a1-11e0-81a7-5081d0136786%2FmyWaitConditionHandle?Expires=1303976584&AWSAccessKeyId=AKIAIOSFODNN7EXAMPLE&Signature=ik1twT6hpS4cgNAw7wyOoRejVoo%3D"
```

where the file /tmp/a contains the following JSON structure:

```
1. {
2.   "Status" : "SUCCESS",
3.   "Reason" : "Configuration Complete",
4.   "UniqueId" : "ID1234",
5.   "Data" : "Application has completed configuration."
6. }
```

This example shows a Curl command line that sends the same success signal except it sends the JSON as a parameter on the command line\.

```
1. curl -X PUT -H 'Content-Type:' --data-binary '{"Status" : "SUCCESS","Reason" : "Configuration Complete","UniqueId" : "ID1234","Data" : "Application has completed configuration."}' "https://cloudformation-waitcondition-test.s3.amazonaws.com/arn%3Aaws%3Acloudformation%3Aus-east-1%3A034017226601%3Astack%2Fstack-gosar-20110427004224-test-stack-with-WaitCondition--VEYW%2Fe498ce60-70a1-11e0-81a7-5081d0136786%2FmyWaitConditionHandle?Expires=1303976584&AWSAccessKeyId=AKIAIOSFODNN7EXAMPLE&Signature=ik1twT6hpS4cgNAw7wyOoRejVoo%3D"
```