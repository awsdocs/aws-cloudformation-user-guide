# AWS::LakeFormation::DataLakeSettings Admins<a name="aws-properties-lakeformation-datalakesettings-admins"></a>

A list of AWS Lake Formation principals\.

## Examples<a name="aws-properties-lakeformation-datalakesettings-admins--examples"></a>

### Input format for Admins resource<a name="aws-properties-lakeformation-datalakesettings-admins--examples--Input_format_for_Admins_resource"></a>

#### JSON<a name="aws-properties-lakeformation-datalakesettings-admins--examples--Input_format_for_Admins_resource--json"></a>

```
{
    "SampleDataLakeSettings": {
      "Type": "AWS::LakeFormation::DataLakeSettings",
      "Properties": {
        "Admins": [
            DataLakePrincipalIdentifier: "arn:sample_principal_1",
            DataLakePrincipalIdentifier: "arn:sample_principal_2"
        ],
        "TrustedResourceOwners": [
            "12345678910",
            "23456789101" 
        ]
      }
    }
  }
```

#### YAML<a name="aws-properties-lakeformation-datalakesettings-admins--examples--Input_format_for_Admins_resource--yaml"></a>

```
SampleDataLakeSettings  
  Type: AWS::LakeFormation::DataLakeSettings
    Properties:
      Admins:
        - DataLakePrincipalIdentifier: 'arn:sample_principal_1'
        - DataLakePrincipalIdentifier: 'arn:sample_principal_2'
      TrustedResourceOwners:
        - '12345678910'
        - '23456789101'
```

## See also<a name="aws-properties-lakeformation-datalakesettings-admins--seealso"></a>

[AWS::LakeFormation::DataLakeSettings DataLakePrincipal ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lakeformation-datalakesettings-datalakeprincipal.html)