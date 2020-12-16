# AWS::Lambda::CodeSigningConfig CodeSigningPolicies<a name="aws-properties-lambda-codesigningconfig-codesigningpolicies"></a>

Code signing configuration policies specifies the validation failure action for signature mismatch or expiry\.

## Syntax<a name="aws-properties-lambda-codesigningconfig-codesigningpolicies-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-codesigningconfig-codesigningpolicies-syntax.json"></a>

```
{
  "[UntrustedArtifactOnDeployment](#cfn-lambda-codesigningconfig-codesigningpolicies-untrustedartifactondeployment)" : String
}
```

### YAML<a name="aws-properties-lambda-codesigningconfig-codesigningpolicies-syntax.yaml"></a>

```
  [UntrustedArtifactOnDeployment](#cfn-lambda-codesigningconfig-codesigningpolicies-untrustedartifactondeployment): String
```

## Properties<a name="aws-properties-lambda-codesigningconfig-codesigningpolicies-properties"></a>

`UntrustedArtifactOnDeployment`  <a name="cfn-lambda-codesigningconfig-codesigningpolicies-untrustedartifactondeployment"></a>
Code signing configuration policy for deployment validation failure\. If you set the policy to `Enforce`, Lambda blocks the deployment request if signature validation checks fail\. If you set the policy to `Warn`, Lambda allows the deployment and creates a CloudWatch log\.   
Default value: `Warn`   
*Required*: Yes  
*Type*: String  
*Allowed values*: `Enforce | Warn`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)