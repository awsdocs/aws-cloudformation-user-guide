# AWS::ACMPCA::Certificate Validity<a name="aws-properties-acmpca-certificate-validity"></a>

The period of time during which a certificate issued by your private certificate authority \(CA\) is valid\. The expiration can be absolute \(expressed as an explicit date and time\) or relative \(expressed as a period of time after issuance in days, months, or years\)\. For more information, see [Validity](https://tools.ietf.org/html/rfc5280#section-4.1.2.5) in RFC 5280\.

You can issue a certificate by calling the IssueCertificate action\.

## Syntax<a name="aws-properties-acmpca-certificate-validity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-validity-syntax.json"></a>

```
{
  "[Type](#cfn-acmpca-certificate-validity-type)" : String,
  "[Value](#cfn-acmpca-certificate-validity-value)" : Integer
}
```

### YAML<a name="aws-properties-acmpca-certificate-validity-syntax.yaml"></a>

```
  [Type](#cfn-acmpca-certificate-validity-type): String
  [Value](#cfn-acmpca-certificate-validity-value): Integer
```

## Properties<a name="aws-properties-acmpca-certificate-validity-properties"></a>

`Type`  <a name="cfn-acmpca-certificate-validity-type"></a>
Determines how *ACM Private CA* interprets the `Value` parameter, an integer\. Supported validity types include those listed below\. Type definitions with absolute values include a sample input value and the resulting output\.   
 `END_DATE`: Absolute value, using UTCTime \(YYMMDDHHMMSS\) or GeneralizedTime \(YYYYMMDDHHMMSS\) format\.  
+ Sample input value: 491231235959 \(UTCTime format\)
+ Output date: 12/31/2049 23:59:59
 `ABSOLUTE`: Absolute value, expressed as the number of seconds since the Unix epoch\.  
+ Sample input value: 2524608000
+ Output date: 01/01/2050 00:00:00
 `DAYS`, `MONTHS`, `YEARS`: Relative values, setting expiration as a number of days, months, or years after certificate issuance\.  
Note: When UTCTime is used, if the year field \(YY\) is greater than or equal to 50, the year is interpreted as 19YY\. If the year field is less than 50, the year is interpreted as 20YY\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `ABSOLUTE | DAYS | END_DATE | MONTHS | YEARS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-acmpca-certificate-validity-value"></a>
Time period\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)