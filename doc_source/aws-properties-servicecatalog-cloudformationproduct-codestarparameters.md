# AWS::ServiceCatalog::CloudFormationProduct CodeStarParameters<a name="aws-properties-servicecatalog-cloudformationproduct-codestarparameters"></a>

The subtype containing details about the Codestar connection `Type`\. 

## Syntax<a name="aws-properties-servicecatalog-cloudformationproduct-codestarparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicecatalog-cloudformationproduct-codestarparameters-syntax.json"></a>

```
{
  "[ArtifactPath](#cfn-servicecatalog-cloudformationproduct-codestarparameters-artifactpath)" : String,
  "[Branch](#cfn-servicecatalog-cloudformationproduct-codestarparameters-branch)" : String,
  "[ConnectionArn](#cfn-servicecatalog-cloudformationproduct-codestarparameters-connectionarn)" : String,
  "[Repository](#cfn-servicecatalog-cloudformationproduct-codestarparameters-repository)" : String
}
```

### YAML<a name="aws-properties-servicecatalog-cloudformationproduct-codestarparameters-syntax.yaml"></a>

```
  [ArtifactPath](#cfn-servicecatalog-cloudformationproduct-codestarparameters-artifactpath): String
  [Branch](#cfn-servicecatalog-cloudformationproduct-codestarparameters-branch): String
  [ConnectionArn](#cfn-servicecatalog-cloudformationproduct-codestarparameters-connectionarn): String
  [Repository](#cfn-servicecatalog-cloudformationproduct-codestarparameters-repository): String
```

## Properties<a name="aws-properties-servicecatalog-cloudformationproduct-codestarparameters-properties"></a>

`ArtifactPath`  <a name="cfn-servicecatalog-cloudformationproduct-codestarparameters-artifactpath"></a>
The absolute path wehre the artifact resides within the repo and branch, formatted as "folder/file\.json\."   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `4096`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Branch`  <a name="cfn-servicecatalog-cloudformationproduct-codestarparameters-branch"></a>
The specific branch where the artifact resides\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `250`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionArn`  <a name="cfn-servicecatalog-cloudformationproduct-codestarparameters-connectionarn"></a>
The CodeStar ARN, which is the connection between AWS Service Catalog and the external repository\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1224`  
*Pattern*: `arn:[a-z0-9][-.a-z0-9]{0,62}:codestar-connections:([a-z0-9][-.a-z0-9]{0,62})?:([a-z0-9][-.a-z0-9]{0,62})?:[^/].{0,1023}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Repository`  <a name="cfn-servicecatalog-cloudformationproduct-codestarparameters-repository"></a>
The specific repository where the product’s artifact\-to\-be\-synced resides, formatted as "Account/Repo\."   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)