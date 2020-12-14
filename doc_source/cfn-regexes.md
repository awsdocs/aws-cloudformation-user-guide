# Using regular expressions in AWS CloudFormation templates<a name="cfn-regexes"></a>

Regular expressions \(commonly known as regexes\) can be specified in a number of places within an AWS CloudFormation template, such as for the `AllowedPattern` property when creating a template [parameter](parameters-section-structure.md)\.

Regular expressions in AWS CloudFormation conform to the Java regular expression syntax\. A full description of this syntax and its constructs can be viewed in the Java documentation, here: [java\.util\.regex\.Pattern](http://docs.oracle.com/javase/6/docs/api/java/util/regex/Pattern.html)\.

**Important**  
Since AWS CloudFormation templates use the JSON syntax for specifying objects and data, you will need to add an additional backslash to any backslash characters in your regular expression, or JSON will interpret these as escape characters\.  
For example, if you include a `\d` in your regular expression to match a digit character, you will need to write it as `\\d` in your JSON template\.