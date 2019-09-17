# AWS::LakeFormation::DataLakeSettings Admins<a name="aws-properties-lakeformation-datalakesettings-admins"></a>

A list of AWS Lake Formation principals\.

## Syntax<a name="aws-resource-lakeformation-datalakesettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-datalakesettings-syntax.json"></a>

```
{
      [
          "[DataLakePrincipalIdentifier](aws-properties-lakeformation-datalakesettings-datalakeprincipal.md)" : String)
      ]
}
```

### YAML<a name="aws-resource-lakeformation-datalakesettings-syntax.yaml"></a>

```
  [Admins](#cfn-lakeformation-datalakesettings-admins): 
    - [DataLakePrincipalIdentifier](aws-properties-lakeformation-datalakesettings-datalakeprincipal.md): String
```
`DataLakePrincipalIdentifier` 
A list of Amazon Resource Names \(ARNs\) of the Lake Formation Administrtor Principals that you want to make Lake Formation Administrators\.  
For more information about ARNs, see [Amazon Resource Names \(ARNs\) and AWS Service Namespaces](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *AWS General Reference*\.  
*Required*: No  
*Type*: List of DataLakePrincipal  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
