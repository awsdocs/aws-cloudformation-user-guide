# AWS::Cloud9::EnvironmentEC2<a name="aws-resource-cloud9-environmentec2"></a>

The `AWS::Cloud9::EnvironmentEC2` resource creates an Amazon EC2 development environment in AWS Cloud9\. For more information, see [Creating an Environment](http://docs.aws.amazon.com/cloud9/latest/user-guide/create-environment.html) in the *AWS Cloud9 User Guide*\. 


+ [Syntax](#aws-resource-cloud9-environmentec2-syntax)
+ [Properties](#aws-resource-cloud9-environmentec2-properties)
+ [Return Values](#aws-resource-cloud9-environmentec2-returnvalues)

## Syntax<a name="aws-resource-cloud9-environmentec2-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloud9-environmentec2-syntax.json"></a>

```
{
  "Type" : "AWS::Cloud9::EnvironmentEC2",
  "Properties" : {
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-repositories)" : [ Repository, ... ],
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-ownerarn)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-description)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-automaticstoptimeminutes)" : Integer,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-instancetype)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-name)" : String,
    "[[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-subnetid)" : String          
  }
}
```

### YAML<a name="aws-resource-cloud9-environmentec2-syntax.yaml"></a>

```
Type: "AWS::Cloud9::EnvironmentEC2"
Properties:
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-repositories): 
    - Repository
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-ownerarn): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-description): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-automaticstoptimeminutes): Integer
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-instancetype): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-name): String
  [[ERROR] BAD/MISSING LINK TEXT](#cfn-cloud9-environmentec2-subnetid): String
```

## Properties<a name="aws-resource-cloud9-environmentec2-properties"></a>

`Repositories`  
Any AWS CodeCommit source code repositories to be cloned into the development environment\.  
 *Required*: No  
 *Type*: List of [AWS Cloud9 EnvironmentEC2 Repository](aws-properties-cloud9-environmentec2-repository.md)  
 *Update requires*: No interruption 

`OwnerArn`  
The Amazon Resource Name \(ARN\) of the environment owner\. If this value is not specified, the ARN defaults to this environment's creator\.   
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`Description`  
The description of the environment to create\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: Replacement 

`AutomaticStopTimeMinutes`  
The number of minutes until the running instance is shut down after the environment has last been used\.  
 *Required*: No  
 *Type*: Integer  
 *Update requires*: Replacement 

`InstanceType`  
The type of instance to host the environment on \(for example, `t2.micro`\)\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`Name`  
The name of the environment to create\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

`SubnetId`  
The ID of the subnet in Amazon Virtual Private Cloud \(Amazon VPC\) to use\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: Replacement 

## Return Values<a name="aws-resource-cloud9-environmentec2-returnvalues"></a>

### Ref<a name="aws-resource-cloud9-environmentec2-ref"></a>

When you pass the logical ID of an `AWS::Cloud9::EnvironmentEC2` resource to the intrinsic `Ref` function, the function returns the ID of the development environment, such as `2bc3642873c342e485f7e0c561234567`\. 

For more information about using the `Ref` function, see Ref\. 

### Fn::GetAtt<a name="aws-resource-cloud9-environmentec2-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the development environment, such as `arn:aws:cloud9:us-east-2:123456789012:environment:2bc3642873c342e485f7e0c561234567`\. 

`Name`  
The name of the development environment, such as `my-demo-environment`\. 

For more information about using `Fn::GetAtt`, see Fn::GetAtt\. 