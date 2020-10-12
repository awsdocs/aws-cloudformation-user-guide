# AWS::WAFv2::WebACL StatementThree<a name="aws-properties-wafv2-webacl-statementthree"></a>

Rules statement\. 

## Syntax<a name="aws-properties-wafv2-webacl-statementthree-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-statementthree-syntax.json"></a>

```
{
  "[ByteMatchStatement](#cfn-wafv2-webacl-statementthree-bytematchstatement)" : ByteMatchStatement,
  "[GeoMatchStatement](#cfn-wafv2-webacl-statementthree-geomatchstatement)" : GeoMatchStatement,
  "[IPSetReferenceStatement](#cfn-wafv2-webacl-statementthree-ipsetreferencestatement)" : IPSetReferenceStatement,
  "[ManagedRuleGroupStatement](#cfn-wafv2-webacl-statementthree-managedrulegroupstatement)" : ManagedRuleGroupStatement,
  "[RegexPatternSetReferenceStatement](#cfn-wafv2-webacl-statementthree-regexpatternsetreferencestatement)" : RegexPatternSetReferenceStatement,
  "[RuleGroupReferenceStatement](#cfn-wafv2-webacl-statementthree-rulegroupreferencestatement)" : RuleGroupReferenceStatement,
  "[SizeConstraintStatement](#cfn-wafv2-webacl-statementthree-sizeconstraintstatement)" : SizeConstraintStatement,
  "[SqliMatchStatement](#cfn-wafv2-webacl-statementthree-sqlimatchstatement)" : SqliMatchStatement,
  "[XssMatchStatement](#cfn-wafv2-webacl-statementthree-xssmatchstatement)" : XssMatchStatement
}
```

### YAML<a name="aws-properties-wafv2-webacl-statementthree-syntax.yaml"></a>

```
  [ByteMatchStatement](#cfn-wafv2-webacl-statementthree-bytematchstatement): 
    ByteMatchStatement
  [GeoMatchStatement](#cfn-wafv2-webacl-statementthree-geomatchstatement): 
    GeoMatchStatement
  [IPSetReferenceStatement](#cfn-wafv2-webacl-statementthree-ipsetreferencestatement): 
    IPSetReferenceStatement
  [ManagedRuleGroupStatement](#cfn-wafv2-webacl-statementthree-managedrulegroupstatement): 
    ManagedRuleGroupStatement
  [RegexPatternSetReferenceStatement](#cfn-wafv2-webacl-statementthree-regexpatternsetreferencestatement): 
    RegexPatternSetReferenceStatement
  [RuleGroupReferenceStatement](#cfn-wafv2-webacl-statementthree-rulegroupreferencestatement): 
    RuleGroupReferenceStatement
  [SizeConstraintStatement](#cfn-wafv2-webacl-statementthree-sizeconstraintstatement): 
    SizeConstraintStatement
  [SqliMatchStatement](#cfn-wafv2-webacl-statementthree-sqlimatchstatement): 
    SqliMatchStatement
  [XssMatchStatement](#cfn-wafv2-webacl-statementthree-xssmatchstatement): 
    XssMatchStatement
```

## Properties<a name="aws-properties-wafv2-webacl-statementthree-properties"></a>

`ByteMatchStatement`  <a name="cfn-wafv2-webacl-statementthree-bytematchstatement"></a>
A rule statement that defines a string match search for AWS WAF to apply to web requests\. The byte match statement provides the bytes to search for, the location in requests that you want AWS WAF to search, and other settings\. The bytes to search for are typically a string that corresponds with ASCII characters\. In the AWS WAF console and the developer guide, this is refered to as a string match statement\.  
*Required*: No  
*Type*: [ByteMatchStatement](aws-properties-wafv2-webacl-bytematchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeoMatchStatement`  <a name="cfn-wafv2-webacl-statementthree-geomatchstatement"></a>
Statement used to identify web requests based on country of origin\.  
*Required*: No  
*Type*: [GeoMatchStatement](aws-properties-wafv2-webacl-geomatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPSetReferenceStatement`  <a name="cfn-wafv2-webacl-statementthree-ipsetreferencestatement"></a>
Statement that references a set of IP addresses to compare to incoming requests\.   
*Required*: No  
*Type*: [IPSetReferenceStatement](aws-properties-wafv2-webacl-ipsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedRuleGroupStatement`  <a name="cfn-wafv2-webacl-statementthree-managedrulegroupstatement"></a>
Statement that references a managed rule group\.  
*Required*: No  
*Type*: [ManagedRuleGroupStatement](aws-properties-wafv2-webacl-managedrulegroupstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexPatternSetReferenceStatement`  <a name="cfn-wafv2-webacl-statementthree-regexpatternsetreferencestatement"></a>
A rule statement used to search web request components for matches with regular expressions\. To use this, create a RegexPatternSet with the expressions that you want to detect, then use that set in this statement\. A web request matches the pattern set rule statement if the request component matches any of the patterns in the set\.  
*Required*: No  
*Type*: [RegexPatternSetReferenceStatement](aws-properties-wafv2-webacl-regexpatternsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleGroupReferenceStatement`  <a name="cfn-wafv2-webacl-statementthree-rulegroupreferencestatement"></a>
A rule statement used to run the rules that are defined in a RuleGroup\. To use this, create a rule group with your rules, then provide the ARN of the rule group in this statement\. You can't nest this type of statement within another\.  
*Required*: No  
*Type*: [RuleGroupReferenceStatement](aws-properties-wafv2-webacl-rulegroupreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeConstraintStatement`  <a name="cfn-wafv2-webacl-statementthree-sizeconstraintstatement"></a>
A rule statement that compares a number of bytes against the size of a request component, using a comparison operator, such as greater than or less than\. For example, you can use a size constraint statement to look for query strings that are longer than 100 bytes\.  
If you configure AWS WAF to inspect the request body, AWS WAF inspects only the first 8192 bytes \(8 KB\)\. If the request body for your web requests never exceeds 8192 bytes, you can create a size constraint condition and block requests that have a request body greater than 8192 bytes\.  
If you choose URI for the value of Part of the request to filter on, the slash \(/\) in the URI counts as one character\. For example, the URI /logo\.jpg is nine characters long\.  
*Required*: No  
*Type*: [SizeConstraintStatement](aws-properties-wafv2-webacl-sizeconstraintstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqliMatchStatement`  <a name="cfn-wafv2-webacl-statementthree-sqlimatchstatement"></a>
Attackers sometimes insert malicious SQL code into web requests in an effort to extract data from your database\. To allow or block web requests that appear to contain malicious SQL code, create one or more SQL injection match conditions\. An SQL injection match condition identifies the part of web requests, such as the URI or the query string, that you want AWS WAF to inspect\. Later in the process, when you create a web ACL, you specify whether to allow or block requests that appear to contain malicious SQL code\.  
*Required*: No  
*Type*: [SqliMatchStatement](aws-properties-wafv2-webacl-sqlimatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XssMatchStatement`  <a name="cfn-wafv2-webacl-statementthree-xssmatchstatement"></a>
A rule statement that defines a cross\-site scripting \(XSS\) match search for AWS WAF to apply to web requests\. XSS attacks are those where the attacker uses vulnerabilities in a benign website as a vehicle to inject malicious client\-site scripts into other legitimate web browsers\. The XSS match statement provides the location in requests that you want AWS WAF to search and text transformations to use on the search area before AWS WAF searches for character sequences that are likely to be malicious strings\.  
*Required*: No  
*Type*: [XssMatchStatement](aws-properties-wafv2-webacl-xssmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)