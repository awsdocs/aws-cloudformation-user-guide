# AWS::ECR::Repository<a name="aws-resource-ecr-repository"></a>

The `AWS::ECR::Repository` resource specifies an Amazon Elastic Container Registry \(Amazon ECR\) repository, where users can push and pull Docker images, Open Container Initiative \(OCI\) images, and OCI compatible artifacts\. For more information, see [Amazon ECR private repositories](https://docs.aws.amazon.com/AmazonECR/latest/userguide/Repositories.html) in the *Amazon ECR User Guide*\.

## Syntax<a name="aws-resource-ecr-repository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecr-repository-syntax.json"></a>

```
{
  "Type" : "AWS::ECR::Repository",
  "Properties" : {
      "[ImageScanningConfiguration](#cfn-ecr-repository-imagescanningconfiguration)" : Json,
      "[ImageTagMutability](#cfn-ecr-repository-imagetagmutability)" : String,
      "[LifecyclePolicy](#cfn-ecr-repository-lifecyclepolicy)" : LifecyclePolicy,
      "[RepositoryName](#cfn-ecr-repository-repositoryname)" : String,
      "[RepositoryPolicyText](#cfn-ecr-repository-repositorypolicytext)" : ,
      "[Tags](#cfn-ecr-repository-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ecr-repository-syntax.yaml"></a>

```
Type: AWS::ECR::Repository
Properties: 
  [ImageScanningConfiguration](#cfn-ecr-repository-imagescanningconfiguration): Json
  [ImageTagMutability](#cfn-ecr-repository-imagetagmutability): String
  [LifecyclePolicy](#cfn-ecr-repository-lifecyclepolicy): 
    LifecyclePolicy
  [RepositoryName](#cfn-ecr-repository-repositoryname): String
  [RepositoryPolicyText](#cfn-ecr-repository-repositorypolicytext): 
  [Tags](#cfn-ecr-repository-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ecr-repository-properties"></a>

`ImageScanningConfiguration`  <a name="cfn-ecr-repository-imagescanningconfiguration"></a>
The image scanning configuration for the repository\. This determines whether images are scanned for known vulnerabilities after being pushed to the repository\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ImageTagMutability`  <a name="cfn-ecr-repository-imagetagmutability"></a>
The tag mutability setting for the repository\. If this parameter is omitted, the default setting of `MUTABLE` will be used which will allow image tags to be overwritten\. If `IMMUTABLE` is specified, all image tags within the repository will be immutable which will prevent them from being overwritten\.  
*Required*: No  
*Type*: String  
*Allowed values*: `IMMUTABLE | MUTABLE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LifecyclePolicy`  <a name="cfn-ecr-repository-lifecyclepolicy"></a>
Creates or updates a lifecycle policy\. For information about lifecycle policy syntax, see [Lifecycle policy template](https://docs.aws.amazon.com/AmazonECR/latest/userguide/LifecyclePolicies.html)\.  
*Required*: No  
*Type*: [LifecyclePolicy](aws-properties-ecr-repository-lifecyclepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepositoryName`  <a name="cfn-ecr-repository-repositoryname"></a>
The name to use for the repository\. The repository name may be specified on its own \(such as `nginx-web-app`\) or it can be prepended with a namespace to group the repository into a category \(such as `project-a/nginx-web-app`\)\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the repository name\. For more information, see [Name type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Minimum*: `2`  
*Maximum*: `256`  
*Pattern*: `(?:[a-z0-9]+(?:[._-][a-z0-9]+)*/)*[a-z0-9]+(?:[._-][a-z0-9]+)*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RepositoryPolicyText`  <a name="cfn-ecr-repository-repositorypolicytext"></a>
The JSON repository policy text to apply to the repository\. For more information, see [Amazon ECR Repository Policies](https://docs.aws.amazon.com/AmazonECR/latest/userguide/repository-policy-examples.html) in the *Amazon Elastic Container Registry User Guide*\.  
*Required*: No  
*Type*:   
*Minimum*: `0`  
*Maximum*: `10240`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ecr-repository-tags"></a>
An array of key\-value pairs to apply to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecr-repository-return-values"></a>

### Ref<a name="aws-resource-ecr-repository-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name, such as `test-repository`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ecr-repository-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ecr-repository-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the specified `AWS::ECR::Repository` resource\. For example, `arn:aws:ecr:eu-west-1:123456789012:repository/test-repository `\.

## Examples<a name="aws-resource-ecr-repository--examples"></a>



### Specify a repository<a name="aws-resource-ecr-repository--examples--Specify_a_repository"></a>

The following example specifies a repository named `test-repository`\. Its policy permits the users `Bob` and `Alice` to push and pull images\. Note that the IAM users actually need to exist, or stack creation will fail\.

#### JSON<a name="aws-resource-ecr-repository--examples--Specify_a_repository--json"></a>

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

#### YAML<a name="aws-resource-ecr-repository--examples--Specify_a_repository--yaml"></a>

```
MyRepository: 
  Type: AWS::ECR::Repository
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

### Specify a repository with a lifecycle policy<a name="aws-resource-ecr-repository--examples--Specify_a_repository_with_a_lifecycle_policy"></a>

The following example creates a repository with a lifecycle policy\.

#### JSON<a name="aws-resource-ecr-repository--examples--Specify_a_repository_with_a_lifecycle_policy--json"></a>

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

#### YAML<a name="aws-resource-ecr-repository--examples--Specify_a_repository_with_a_lifecycle_policy--yaml"></a>

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

### Specify a repository with an image scanning configuration<a name="aws-resource-ecr-repository--examples--Specify_a_repository_with_an_image_scanning_configuration"></a>

The following example creates a repository named `test-repository` with image scanning enabled\. For more information on image scanning, see [Image scanning](https://docs.aws.amazon.com/AmazonECR/latest/userguide/image-scanning.html) in the *Amazon ECR User Guide*\.

#### JSON<a name="aws-resource-ecr-repository--examples--Specify_a_repository_with_an_image_scanning_configuration--json"></a>

```
"MyRepository": {
  "Type": "AWS::ECR::Repository",
  "Properties": {
    "RepositoryName" : "test-repository",
    "ImageScanningConfiguration" : {
      "scanOnPush": "true"
    }
  }
}
```

#### YAML<a name="aws-resource-ecr-repository--examples--Specify_a_repository_with_an_image_scanning_configuration--yaml"></a>

```
MyRepository: 
  Type: AWS::ECR::Repository
  Properties: 
    RepositoryName: "test-repository"
    ImageScanningConfiguration: 
      scanOnPush: "true"
```

## See also<a name="aws-resource-ecr-repository--seealso"></a>
+  [Creating a lifecycle policy](https://docs.aws.amazon.com/AmazonECR/latest/userguide/lp_creation.html) in the *Amazon ECR User Guide* 
+  [PutLifecyclePolicy](https://docs.aws.amazon.com/AmazonECR/latest/APIReference/API_PutLifecyclePolicy.html) in the *Amazon ECR API Reference* 

