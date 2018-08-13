# AWS::ECR::Repository<a name="aws-resource-ecr-repository"></a>

The `AWS::ECR::Repository` resource creates an Amazon Elastic Container Registry \(Amazon ECR\) repository, where users can push and pull Docker images\. For more information, see [Amazon ECR Repositories](http://docs.aws.amazon.com/AmazonECR/latest/userguide/Repositories.html) in the *Amazon Elastic Container Registry User Guide*\.

**Topics**
+ [Syntax](#aws-resource-ecr-repository-syntax)
+ [Properties](#aws-resource-ecr-repository-properties)
+ [Return Values](#aws-resource-ecr-repository-returnvalues)
+ [Examples](#aws-resource-ecr-repository-examples)

## Syntax<a name="aws-resource-ecr-repository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecr-repository-syntax.json"></a>

```
{
  "Type" : "AWS::ECR::Repository",
  "Properties" : {
    "[LifecyclePolicy](#cfn-ecr-repository-lifecyclepolicy)" : [*LifecyclePolicy*](aws-properties-ecr-repository-lifecyclepolicy.md),
    "[RepositoryName](#cfn-ecr-repository-repositoryname)" : String,
    "[RepositoryPolicyText](#cfn-ecr-repository-repositorypolicytext)" : JSON object
  }
}
```

### YAML<a name="aws-resource-ecr-repository-syntax.yaml"></a>

```
Type: "AWS::ECR::Repository"
Properties: 
  [LifecyclePolicy](#cfn-ecr-repository-lifecyclepolicy):
    [*LifecyclePolicy*](aws-properties-ecr-repository-lifecyclepolicy.md)
  [RepositoryName](#cfn-ecr-repository-repositoryname): String
  [RepositoryPolicyText](#cfn-ecr-repository-repositorypolicytext): JSON object
```

## Properties<a name="aws-resource-ecr-repository-properties"></a>

`LifecyclePolicy`  <a name="cfn-ecr-repository-lifecyclepolicy"></a>
A lifecycle policy for the repository\.  
*Required*: No  
*Type*: [Amazon ECR Repository LifecyclePolicy](aws-properties-ecr-repository-lifecyclepolicy.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`RepositoryName`  <a name="cfn-ecr-repository-repositoryname"></a>
A name for the image repository\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the repository name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`RepositoryPolicyText`  <a name="cfn-ecr-repository-repositorypolicytext"></a>
A policy that controls who has access to the repository and which actions they can perform on it\. For more information, see [Amazon ECR Repository Policies](http://docs.aws.amazon.com/AmazonECR/latest/userguide/RepositoryPolicies.html) in the *Amazon Elastic Container Registry User Guide*\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="aws-resource-ecr-repository-returnvalues"></a>

### Ref<a name="w3ab2c21c10d555c11b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name, such as `test-repository`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

## Examples<a name="aws-resource-ecr-repository-examples"></a>

### <a name="aws-resource-ecr-repository-example1"></a>

The following example creates a repository named `test-repository`\. Its policy permits the users `Bob` and `Alice` to push and pull images\. Note that the IAM users actually need to exist, or stack creation will fail\.

#### JSON<a name="aws-resource-ecr-repository-example1.json"></a>

```
"MyRepository": {
  "Type": "AWS::ECR::Repository",
  "Properties": {
    "RepositoryName" : "test-repository",
    "RepositoryPolicyText" : {
      "Version": "2008-10-17",
      "Statement": [
        {
          "Sid": "AllowPushPull",
          "Effect": "Allow",
          "Principal": {
            "AWS": [
              "arn:aws:iam::123456789012:user/Bob",
              "arn:aws:iam::123456789012:user/Alice"
            ]
          },
          "Action": [
            "ecr:GetDownloadUrlForLayer",
            "ecr:BatchGetImage",
            "ecr:BatchCheckLayerAvailability",
            "ecr:PutImage",
            "ecr:InitiateLayerUpload",
            "ecr:UploadLayerPart",
            "ecr:CompleteLayerUpload"
          ]
        }
      ]
    }
  }
}
```

#### YAML<a name="aws-resource-ecr-repository-example1.yaml"></a>

```
MyRepository: 
  Type: "AWS::ECR::Repository"
  Properties: 
    RepositoryName: "test-repository"
    RepositoryPolicyText: 
      Version: "2012-10-17"
      Statement: 
        - 
          Sid: AllowPushPull
          Effect: Allow
          Principal: 
            AWS: 
              - "arn:aws:iam::123456789012:user/Bob"
              - "arn:aws:iam::123456789012:user/Alice"
          Action: 
            - "ecr:GetDownloadUrlForLayer"
            - "ecr:BatchGetImage"
            - "ecr:BatchCheckLayerAvailability"
            - "ecr:PutImage"
            - "ecr:InitiateLayerUpload"
            - "ecr:UploadLayerPart"
            - "ecr:CompleteLayerUpload"
```

### <a name="aws-resource-ecr-repository-example2"></a>

The following example creates a repository with a lifecycle policy\.

#### JSON<a name="aws-resource-ecr-repository-example2.json"></a>

```
{
  "Parameters": {
    "lifecyclePolicyText": {
      "Type": "String"
    },
    "repositoryName": {
      "Type": "String"
    },
    "registryId": {
      "Type": "String"
    }
  },
  "Resources": {
    "MyRepository": {
      "Type": "AWS::ECR::Repository",
      "Properties": {
        "LifecyclePolicy": {
          "LifecyclePolicyText": {
            "Ref": "lifecyclePolicyText"
          },
          "RegistryId": {
            "Ref": "registryId"
          }
        },
        "RepositoryName": {
          "Ref": "repositoryName"
        }
      }
    }
  },
  "Outputs": {
    "Arn": {
      "Value": {
        "Fn::GetAtt": [
          "MyRepository",
          "Arn"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-ecr-repository-example2.yaml"></a>

```
Parameters:    
  lifecyclePolicyText:
    Type: String
  repositoryName:
    Type: String
  registryId:
    Type: String
Resources:
  MyRepository:
    Type: AWS::ECR::Repository
    Properties:
      LifecyclePolicy:
        LifecyclePolicyText: !Ref lifecyclePolicyText
        RegistryId: !Ref registryId
      RepositoryName: !Ref repositoryName
Outputs:    
  Arn:
    Value: !GetAtt MyRepository.Arn
```