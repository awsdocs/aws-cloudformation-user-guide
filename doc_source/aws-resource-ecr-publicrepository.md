# AWS::ECR::PublicRepository<a name="aws-resource-ecr-publicrepository"></a>

The `AWS::ECR::PublicRepository` resource specifies an Amazon Elastic Container Registry Public \(Amazon ECR Public\) repository, where users can push and pull Docker images, Open Container Initiative \(OCI\) images, and OCI compatible artifacts\. For more information, see [Amazon ECR public repositories](https://docs.aws.amazon.com/AmazonECR/latest/public/public-repositories.html) in the *Amazon ECR Public User Guide*\.

## Syntax<a name="aws-resource-ecr-publicrepository-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ecr-publicrepository-syntax.json"></a>

```
{
  "Type" : "AWS::ECR::PublicRepository",
  "Properties" : {
      "[RepositoryCatalogData](#cfn-ecr-publicrepository-repositorycatalogdata)" : Json,
      "[RepositoryName](#cfn-ecr-publicrepository-repositoryname)" : String,
      "[RepositoryPolicyText](#cfn-ecr-publicrepository-repositorypolicytext)" : 
    }
}
```

### YAML<a name="aws-resource-ecr-publicrepository-syntax.yaml"></a>

```
Type: AWS::ECR::PublicRepository
Properties: 
  [RepositoryCatalogData](#cfn-ecr-publicrepository-repositorycatalogdata): Json
  [RepositoryName](#cfn-ecr-publicrepository-repositoryname): String
  [RepositoryPolicyText](#cfn-ecr-publicrepository-repositorypolicytext):
```

## Properties<a name="aws-resource-ecr-publicrepository-properties"></a>

`RepositoryCatalogData`  <a name="cfn-ecr-publicrepository-repositorycatalogdata"></a>
The details about the repository that are publicly visible in the Amazon ECR Public Gallery\. For more information, see [Amazon ECR Public repository catalog data](https://docs.aws.amazon.com/AmazonECR/latest/public/public-repository-catalog-data.html) in the *Amazon ECR Public User Guide*\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepositoryName`  <a name="cfn-ecr-publicrepository-repositoryname"></a>
The name to use for the public repository\. The repository name may be specified on its own \(such as `nginx-web-app`\) or it can be prepended with a namespace to group the repository into a category \(such as `project-a/nginx-web-app`\)\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the repository name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RepositoryPolicyText`  <a name="cfn-ecr-publicrepository-repositorypolicytext"></a>
The JSON repository policy text to apply to the public repository\. For more information, see [Amazon ECR Public repository policies](https://docs.aws.amazon.com/AmazonECR/latest/public/public-repository-policies.html) in the *Amazon ECR Public User Guide*\.  
*Required*: No  
*Type*:   
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ecr-publicrepository-return-values"></a>

### Ref<a name="aws-resource-ecr-publicrepository-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name, such as `test-repository`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ecr-publicrepository-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ecr-publicrepository-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) for the specified `AWS::ECR::PublicRepository` resource\. For example, `arn:aws:ecr-public::123456789012:repository/test-repository `\.

## Examples<a name="aws-resource-ecr-publicrepository--examples"></a>



### Specify a public repository<a name="aws-resource-ecr-publicrepository--examples--Specify_a_public_repository"></a>

The following example specifies a public repository named `test-repository`\. The repository catalog data appears publicly on the Amazon ECR Public Gallery\.

#### JSON<a name="aws-resource-ecr-publicrepository--examples--Specify_a_public_repository--json"></a>

```
"MyPublicRepository": {
  "Type": "AWS::ECR::PublicRepository",
  "Properties": {
    "RepositoryName" : "test-repository",
    "RepositoryCatalogData" : {
      "UsageText": "This is a sample usage text.",
      "AboutText": "This is a sample about text.",
      "OperatingSystems": [
           "Linux",
           "Windows"
       ],
       "Architectures": [
           "x86",
           "ARM"
       ],
      "RepositoryDescription": "This is a sample repository description."
    }
  }
}
```

#### YAML<a name="aws-resource-ecr-publicrepository--examples--Specify_a_public_repository--yaml"></a>

```
Resources:
  MyPublicRepositry:
    Type: AWS::ECR::PublicRepository
    Properties:
      RepositoryName: "test-repository"
      RepositoryCatalogData:
        UsageText: "This is a sample usage text."
        AboutText: "This is a sample about text."
        OperatingSystems:
          - "Linux"
          - "Windows"
        Architectures:
          - "x86"
          - "ARM"
        RepositoryDescription: "This is a sample repository description."
```