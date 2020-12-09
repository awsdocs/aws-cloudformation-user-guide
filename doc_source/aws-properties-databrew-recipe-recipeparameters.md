# AWS::DataBrew::Recipe RecipeParameters<a name="aws-properties-databrew-recipe-recipeparameters"></a>

Parameters that are used as inputs for various recipe actions\. The parameters are specific to the context in which they're used\.

## Syntax<a name="aws-properties-databrew-recipe-recipeparameters-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-databrew-recipe-recipeparameters-syntax.json"></a>

```
{
  "[AggregateFunction](#cfn-databrew-recipe-recipeparameters-aggregatefunction)" : String,
  "[Base](#cfn-databrew-recipe-recipeparameters-base)" : String,
  "[CaseStatement](#cfn-databrew-recipe-recipeparameters-casestatement)" : String,
  "[CategoryMap](#cfn-databrew-recipe-recipeparameters-categorymap)" : String,
  "[CharsToRemove](#cfn-databrew-recipe-recipeparameters-charstoremove)" : String,
  "[CollapseConsecutiveWhitespace](#cfn-databrew-recipe-recipeparameters-collapseconsecutivewhitespace)" : String,
  "[ColumnDataType](#cfn-databrew-recipe-recipeparameters-columndatatype)" : String,
  "[ColumnRange](#cfn-databrew-recipe-recipeparameters-columnrange)" : String,
  "[Count](#cfn-databrew-recipe-recipeparameters-count)" : String,
  "[CustomCharacters](#cfn-databrew-recipe-recipeparameters-customcharacters)" : String,
  "[CustomStopWords](#cfn-databrew-recipe-recipeparameters-customstopwords)" : String,
  "[CustomValue](#cfn-databrew-recipe-recipeparameters-customvalue)" : String,
  "[DatasetsColumns](#cfn-databrew-recipe-recipeparameters-datasetscolumns)" : String,
  "[DateAddValue](#cfn-databrew-recipe-recipeparameters-dateaddvalue)" : String,
  "[DateTimeFormat](#cfn-databrew-recipe-recipeparameters-datetimeformat)" : String,
  "[DateTimeParameters](#cfn-databrew-recipe-recipeparameters-datetimeparameters)" : String,
  "[DeleteOtherRows](#cfn-databrew-recipe-recipeparameters-deleteotherrows)" : String,
  "[Delimiter](#cfn-databrew-recipe-recipeparameters-delimiter)" : String,
  "[EndPattern](#cfn-databrew-recipe-recipeparameters-endpattern)" : String,
  "[EndPosition](#cfn-databrew-recipe-recipeparameters-endposition)" : String,
  "[EndValue](#cfn-databrew-recipe-recipeparameters-endvalue)" : String,
  "[ExpandContractions](#cfn-databrew-recipe-recipeparameters-expandcontractions)" : String,
  "[Exponent](#cfn-databrew-recipe-recipeparameters-exponent)" : String,
  "[FalseString](#cfn-databrew-recipe-recipeparameters-falsestring)" : String,
  "[GroupByAggFunctionOptions](#cfn-databrew-recipe-recipeparameters-groupbyaggfunctionoptions)" : String,
  "[GroupByColumns](#cfn-databrew-recipe-recipeparameters-groupbycolumns)" : String,
  "[HiddenColumns](#cfn-databrew-recipe-recipeparameters-hiddencolumns)" : String,
  "[IgnoreCase](#cfn-databrew-recipe-recipeparameters-ignorecase)" : String,
  "[IncludeInSplit](#cfn-databrew-recipe-recipeparameters-includeinsplit)" : String,
  "[Input](#cfn-databrew-recipe-recipeparameters-input)" : Json,
  "[Interval](#cfn-databrew-recipe-recipeparameters-interval)" : String,
  "[IsText](#cfn-databrew-recipe-recipeparameters-istext)" : String,
  "[JoinKeys](#cfn-databrew-recipe-recipeparameters-joinkeys)" : String,
  "[JoinType](#cfn-databrew-recipe-recipeparameters-jointype)" : String,
  "[LeftColumns](#cfn-databrew-recipe-recipeparameters-leftcolumns)" : String,
  "[Limit](#cfn-databrew-recipe-recipeparameters-limit)" : String,
  "[LowerBound](#cfn-databrew-recipe-recipeparameters-lowerbound)" : String,
  "[MapType](#cfn-databrew-recipe-recipeparameters-maptype)" : String,
  "[ModeType](#cfn-databrew-recipe-recipeparameters-modetype)" : String,
  "[MultiLine](#cfn-databrew-recipe-recipeparameters-multiline)" : Boolean,
  "[NumRows](#cfn-databrew-recipe-recipeparameters-numrows)" : String,
  "[NumRowsAfter](#cfn-databrew-recipe-recipeparameters-numrowsafter)" : String,
  "[NumRowsBefore](#cfn-databrew-recipe-recipeparameters-numrowsbefore)" : String,
  "[OrderByColumn](#cfn-databrew-recipe-recipeparameters-orderbycolumn)" : String,
  "[OrderByColumns](#cfn-databrew-recipe-recipeparameters-orderbycolumns)" : String,
  "[Other](#cfn-databrew-recipe-recipeparameters-other)" : String,
  "[Pattern](#cfn-databrew-recipe-recipeparameters-pattern)" : String,
  "[PatternOption1](#cfn-databrew-recipe-recipeparameters-patternoption1)" : String,
  "[PatternOption2](#cfn-databrew-recipe-recipeparameters-patternoption2)" : String,
  "[PatternOptions](#cfn-databrew-recipe-recipeparameters-patternoptions)" : String,
  "[Period](#cfn-databrew-recipe-recipeparameters-period)" : String,
  "[Position](#cfn-databrew-recipe-recipeparameters-position)" : String,
  "[RemoveAllPunctuation](#cfn-databrew-recipe-recipeparameters-removeallpunctuation)" : String,
  "[RemoveAllQuotes](#cfn-databrew-recipe-recipeparameters-removeallquotes)" : String,
  "[RemoveAllWhitespace](#cfn-databrew-recipe-recipeparameters-removeallwhitespace)" : String,
  "[RemoveCustomCharacters](#cfn-databrew-recipe-recipeparameters-removecustomcharacters)" : String,
  "[RemoveCustomValue](#cfn-databrew-recipe-recipeparameters-removecustomvalue)" : String,
  "[RemoveLeadingAndTrailingPunctuation](#cfn-databrew-recipe-recipeparameters-removeleadingandtrailingpunctuation)" : String,
  "[RemoveLeadingAndTrailingQuotes](#cfn-databrew-recipe-recipeparameters-removeleadingandtrailingquotes)" : String,
  "[RemoveLeadingAndTrailingWhitespace](#cfn-databrew-recipe-recipeparameters-removeleadingandtrailingwhitespace)" : String,
  "[RemoveLetters](#cfn-databrew-recipe-recipeparameters-removeletters)" : String,
  "[RemoveNumbers](#cfn-databrew-recipe-recipeparameters-removenumbers)" : String,
  "[RemoveSourceColumn](#cfn-databrew-recipe-recipeparameters-removesourcecolumn)" : String,
  "[RemoveSpecialCharacters](#cfn-databrew-recipe-recipeparameters-removespecialcharacters)" : String,
  "[RightColumns](#cfn-databrew-recipe-recipeparameters-rightcolumns)" : String,
  "[SampleSize](#cfn-databrew-recipe-recipeparameters-samplesize)" : String,
  "[SampleType](#cfn-databrew-recipe-recipeparameters-sampletype)" : String,
  "[SecondaryInputs](#cfn-databrew-recipe-recipeparameters-secondaryinputs)" : [ SecondaryInput, ... ],
  "[SecondInput](#cfn-databrew-recipe-recipeparameters-secondinput)" : String,
  "[SheetIndexes](#cfn-databrew-recipe-recipeparameters-sheetindexes)" : [ Integer, ... ],
  "[SheetNames](#cfn-databrew-recipe-recipeparameters-sheetnames)" : [ String, ... ],
  "[SourceColumn](#cfn-databrew-recipe-recipeparameters-sourcecolumn)" : String,
  "[SourceColumn1](#cfn-databrew-recipe-recipeparameters-sourcecolumn1)" : String,
  "[SourceColumn2](#cfn-databrew-recipe-recipeparameters-sourcecolumn2)" : String,
  "[SourceColumns](#cfn-databrew-recipe-recipeparameters-sourcecolumns)" : String,
  "[StartColumnIndex](#cfn-databrew-recipe-recipeparameters-startcolumnindex)" : String,
  "[StartPattern](#cfn-databrew-recipe-recipeparameters-startpattern)" : String,
  "[StartPosition](#cfn-databrew-recipe-recipeparameters-startposition)" : String,
  "[StartValue](#cfn-databrew-recipe-recipeparameters-startvalue)" : String,
  "[StemmingMode](#cfn-databrew-recipe-recipeparameters-stemmingmode)" : String,
  "[StepCount](#cfn-databrew-recipe-recipeparameters-stepcount)" : String,
  "[StepIndex](#cfn-databrew-recipe-recipeparameters-stepindex)" : String,
  "[StopWordsMode](#cfn-databrew-recipe-recipeparameters-stopwordsmode)" : String,
  "[Strategy](#cfn-databrew-recipe-recipeparameters-strategy)" : String,
  "[TargetColumn](#cfn-databrew-recipe-recipeparameters-targetcolumn)" : String,
  "[TargetColumnNames](#cfn-databrew-recipe-recipeparameters-targetcolumnnames)" : String,
  "[TargetDateFormat](#cfn-databrew-recipe-recipeparameters-targetdateformat)" : String,
  "[TargetIndex](#cfn-databrew-recipe-recipeparameters-targetindex)" : String,
  "[TimeZone](#cfn-databrew-recipe-recipeparameters-timezone)" : String,
  "[TokenizerPattern](#cfn-databrew-recipe-recipeparameters-tokenizerpattern)" : String,
  "[TrueString](#cfn-databrew-recipe-recipeparameters-truestring)" : String,
  "[UdfLang](#cfn-databrew-recipe-recipeparameters-udflang)" : String,
  "[Units](#cfn-databrew-recipe-recipeparameters-units)" : String,
  "[UnpivotColumn](#cfn-databrew-recipe-recipeparameters-unpivotcolumn)" : String,
  "[UpperBound](#cfn-databrew-recipe-recipeparameters-upperbound)" : String,
  "[UseNewDataFrame](#cfn-databrew-recipe-recipeparameters-usenewdataframe)" : String,
  "[Value](#cfn-databrew-recipe-recipeparameters-value)" : String,
  "[Value1](#cfn-databrew-recipe-recipeparameters-value1)" : String,
  "[Value2](#cfn-databrew-recipe-recipeparameters-value2)" : String,
  "[ValueColumn](#cfn-databrew-recipe-recipeparameters-valuecolumn)" : String,
  "[ViewFrame](#cfn-databrew-recipe-recipeparameters-viewframe)" : String
}
```

### YAML<a name="aws-properties-databrew-recipe-recipeparameters-syntax.yaml"></a>

```
  [AggregateFunction](#cfn-databrew-recipe-recipeparameters-aggregatefunction): String
  [Base](#cfn-databrew-recipe-recipeparameters-base): String
  [CaseStatement](#cfn-databrew-recipe-recipeparameters-casestatement): String
  [CategoryMap](#cfn-databrew-recipe-recipeparameters-categorymap): String
  [CharsToRemove](#cfn-databrew-recipe-recipeparameters-charstoremove): String
  [CollapseConsecutiveWhitespace](#cfn-databrew-recipe-recipeparameters-collapseconsecutivewhitespace): String
  [ColumnDataType](#cfn-databrew-recipe-recipeparameters-columndatatype): String
  [ColumnRange](#cfn-databrew-recipe-recipeparameters-columnrange): String
  [Count](#cfn-databrew-recipe-recipeparameters-count): String
  [CustomCharacters](#cfn-databrew-recipe-recipeparameters-customcharacters): String
  [CustomStopWords](#cfn-databrew-recipe-recipeparameters-customstopwords): String
  [CustomValue](#cfn-databrew-recipe-recipeparameters-customvalue): String
  [DatasetsColumns](#cfn-databrew-recipe-recipeparameters-datasetscolumns): String
  [DateAddValue](#cfn-databrew-recipe-recipeparameters-dateaddvalue): String
  [DateTimeFormat](#cfn-databrew-recipe-recipeparameters-datetimeformat): String
  [DateTimeParameters](#cfn-databrew-recipe-recipeparameters-datetimeparameters): String
  [DeleteOtherRows](#cfn-databrew-recipe-recipeparameters-deleteotherrows): String
  [Delimiter](#cfn-databrew-recipe-recipeparameters-delimiter): String
  [EndPattern](#cfn-databrew-recipe-recipeparameters-endpattern): String
  [EndPosition](#cfn-databrew-recipe-recipeparameters-endposition): String
  [EndValue](#cfn-databrew-recipe-recipeparameters-endvalue): String
  [ExpandContractions](#cfn-databrew-recipe-recipeparameters-expandcontractions): String
  [Exponent](#cfn-databrew-recipe-recipeparameters-exponent): String
  [FalseString](#cfn-databrew-recipe-recipeparameters-falsestring): 
    String
  [GroupByAggFunctionOptions](#cfn-databrew-recipe-recipeparameters-groupbyaggfunctionoptions): String
  [GroupByColumns](#cfn-databrew-recipe-recipeparameters-groupbycolumns): String
  [HiddenColumns](#cfn-databrew-recipe-recipeparameters-hiddencolumns): String
  [IgnoreCase](#cfn-databrew-recipe-recipeparameters-ignorecase): String
  [IncludeInSplit](#cfn-databrew-recipe-recipeparameters-includeinsplit): String
  [Input](#cfn-databrew-recipe-recipeparameters-input): Json
  [Interval](#cfn-databrew-recipe-recipeparameters-interval): String
  [IsText](#cfn-databrew-recipe-recipeparameters-istext): String
  [JoinKeys](#cfn-databrew-recipe-recipeparameters-joinkeys): String
  [JoinType](#cfn-databrew-recipe-recipeparameters-jointype): String
  [LeftColumns](#cfn-databrew-recipe-recipeparameters-leftcolumns): String
  [Limit](#cfn-databrew-recipe-recipeparameters-limit): String
  [LowerBound](#cfn-databrew-recipe-recipeparameters-lowerbound): String
  [MapType](#cfn-databrew-recipe-recipeparameters-maptype): String
  [ModeType](#cfn-databrew-recipe-recipeparameters-modetype): String
  [MultiLine](#cfn-databrew-recipe-recipeparameters-multiline): Boolean
  [NumRows](#cfn-databrew-recipe-recipeparameters-numrows): String
  [NumRowsAfter](#cfn-databrew-recipe-recipeparameters-numrowsafter): String
  [NumRowsBefore](#cfn-databrew-recipe-recipeparameters-numrowsbefore): String
  [OrderByColumn](#cfn-databrew-recipe-recipeparameters-orderbycolumn): String
  [OrderByColumns](#cfn-databrew-recipe-recipeparameters-orderbycolumns): String
  [Other](#cfn-databrew-recipe-recipeparameters-other): String
  [Pattern](#cfn-databrew-recipe-recipeparameters-pattern): String
  [PatternOption1](#cfn-databrew-recipe-recipeparameters-patternoption1): String
  [PatternOption2](#cfn-databrew-recipe-recipeparameters-patternoption2): String
  [PatternOptions](#cfn-databrew-recipe-recipeparameters-patternoptions): String
  [Period](#cfn-databrew-recipe-recipeparameters-period): String
  [Position](#cfn-databrew-recipe-recipeparameters-position): String
  [RemoveAllPunctuation](#cfn-databrew-recipe-recipeparameters-removeallpunctuation): String
  [RemoveAllQuotes](#cfn-databrew-recipe-recipeparameters-removeallquotes): String
  [RemoveAllWhitespace](#cfn-databrew-recipe-recipeparameters-removeallwhitespace): String
  [RemoveCustomCharacters](#cfn-databrew-recipe-recipeparameters-removecustomcharacters): String
  [RemoveCustomValue](#cfn-databrew-recipe-recipeparameters-removecustomvalue): String
  [RemoveLeadingAndTrailingPunctuation](#cfn-databrew-recipe-recipeparameters-removeleadingandtrailingpunctuation): String
  [RemoveLeadingAndTrailingQuotes](#cfn-databrew-recipe-recipeparameters-removeleadingandtrailingquotes): String
  [RemoveLeadingAndTrailingWhitespace](#cfn-databrew-recipe-recipeparameters-removeleadingandtrailingwhitespace): String
  [RemoveLetters](#cfn-databrew-recipe-recipeparameters-removeletters): String
  [RemoveNumbers](#cfn-databrew-recipe-recipeparameters-removenumbers): String
  [RemoveSourceColumn](#cfn-databrew-recipe-recipeparameters-removesourcecolumn): String
  [RemoveSpecialCharacters](#cfn-databrew-recipe-recipeparameters-removespecialcharacters): String
  [RightColumns](#cfn-databrew-recipe-recipeparameters-rightcolumns): String
  [SampleSize](#cfn-databrew-recipe-recipeparameters-samplesize): String
  [SampleType](#cfn-databrew-recipe-recipeparameters-sampletype): String
  [SecondaryInputs](#cfn-databrew-recipe-recipeparameters-secondaryinputs): 
    - SecondaryInput
  [SecondInput](#cfn-databrew-recipe-recipeparameters-secondinput): String
  [SheetIndexes](#cfn-databrew-recipe-recipeparameters-sheetindexes): 
    - Integer
  [SheetNames](#cfn-databrew-recipe-recipeparameters-sheetnames): 
    - String
  [SourceColumn](#cfn-databrew-recipe-recipeparameters-sourcecolumn): String
  [SourceColumn1](#cfn-databrew-recipe-recipeparameters-sourcecolumn1): String
  [SourceColumn2](#cfn-databrew-recipe-recipeparameters-sourcecolumn2): String
  [SourceColumns](#cfn-databrew-recipe-recipeparameters-sourcecolumns): String
  [StartColumnIndex](#cfn-databrew-recipe-recipeparameters-startcolumnindex): String
  [StartPattern](#cfn-databrew-recipe-recipeparameters-startpattern): String
  [StartPosition](#cfn-databrew-recipe-recipeparameters-startposition): String
  [StartValue](#cfn-databrew-recipe-recipeparameters-startvalue): String
  [StemmingMode](#cfn-databrew-recipe-recipeparameters-stemmingmode): String
  [StepCount](#cfn-databrew-recipe-recipeparameters-stepcount): String
  [StepIndex](#cfn-databrew-recipe-recipeparameters-stepindex): String
  [StopWordsMode](#cfn-databrew-recipe-recipeparameters-stopwordsmode): String
  [Strategy](#cfn-databrew-recipe-recipeparameters-strategy): String
  [TargetColumn](#cfn-databrew-recipe-recipeparameters-targetcolumn): String
  [TargetColumnNames](#cfn-databrew-recipe-recipeparameters-targetcolumnnames): String
  [TargetDateFormat](#cfn-databrew-recipe-recipeparameters-targetdateformat): String
  [TargetIndex](#cfn-databrew-recipe-recipeparameters-targetindex): String
  [TimeZone](#cfn-databrew-recipe-recipeparameters-timezone): String
  [TokenizerPattern](#cfn-databrew-recipe-recipeparameters-tokenizerpattern): String
  [TrueString](#cfn-databrew-recipe-recipeparameters-truestring): 
    String
  [UdfLang](#cfn-databrew-recipe-recipeparameters-udflang): String
  [Units](#cfn-databrew-recipe-recipeparameters-units): String
  [UnpivotColumn](#cfn-databrew-recipe-recipeparameters-unpivotcolumn): String
  [UpperBound](#cfn-databrew-recipe-recipeparameters-upperbound): String
  [UseNewDataFrame](#cfn-databrew-recipe-recipeparameters-usenewdataframe): String
  [Value](#cfn-databrew-recipe-recipeparameters-value): String
  [Value1](#cfn-databrew-recipe-recipeparameters-value1): String
  [Value2](#cfn-databrew-recipe-recipeparameters-value2): String
  [ValueColumn](#cfn-databrew-recipe-recipeparameters-valuecolumn): String
  [ViewFrame](#cfn-databrew-recipe-recipeparameters-viewframe): String
```

## Properties<a name="aws-properties-databrew-recipe-recipeparameters-properties"></a>

`AggregateFunction`  <a name="cfn-databrew-recipe-recipeparameters-aggregatefunction"></a>
The name of an aggregation function to apply\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Base`  <a name="cfn-databrew-recipe-recipeparameters-base"></a>
The number of digits used in a counting system\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CaseStatement`  <a name="cfn-databrew-recipe-recipeparameters-casestatement"></a>
A case statement associated with a recipe\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CategoryMap`  <a name="cfn-databrew-recipe-recipeparameters-categorymap"></a>
A category map used for one\-hot encoding\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CharsToRemove`  <a name="cfn-databrew-recipe-recipeparameters-charstoremove"></a>
Characters to remove from a step that applies one\-hot encoding or tokenization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CollapseConsecutiveWhitespace`  <a name="cfn-databrew-recipe-recipeparameters-collapseconsecutivewhitespace"></a>
Remove any non\-word non\-punctuation character\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnDataType`  <a name="cfn-databrew-recipe-recipeparameters-columndatatype"></a>
The data type of the column\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ColumnRange`  <a name="cfn-databrew-recipe-recipeparameters-columnrange"></a>
 A range of columns to which a step is applied\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Count`  <a name="cfn-databrew-recipe-recipeparameters-count"></a>
The number of times a string needs to be repeated\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomCharacters`  <a name="cfn-databrew-recipe-recipeparameters-customcharacters"></a>
One or more characters that can be substituted or removed, depending on the context\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomStopWords`  <a name="cfn-databrew-recipe-recipeparameters-customstopwords"></a>
A list of words to ignore in a step that applies word tokenization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomValue`  <a name="cfn-databrew-recipe-recipeparameters-customvalue"></a>
A list of custom values to use in a step that requires that you provide a value to finish the operation\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatasetsColumns`  <a name="cfn-databrew-recipe-recipeparameters-datasetscolumns"></a>
A list of the dataset columns included in a project\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateAddValue`  <a name="cfn-databrew-recipe-recipeparameters-dateaddvalue"></a>
A value that specifies how many units of time to add or subtract for a date math operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateTimeFormat`  <a name="cfn-databrew-recipe-recipeparameters-datetimeformat"></a>
A date format to apply to a date\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DateTimeParameters`  <a name="cfn-databrew-recipe-recipeparameters-datetimeparameters"></a>
A set of parameters associated with a datetime\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeleteOtherRows`  <a name="cfn-databrew-recipe-recipeparameters-deleteotherrows"></a>
Determines whether unmapped rows in a categorical mapping should be deleted  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Delimiter`  <a name="cfn-databrew-recipe-recipeparameters-delimiter"></a>
The delimiter to use when parsing separated values in a text file\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndPattern`  <a name="cfn-databrew-recipe-recipeparameters-endpattern"></a>
The end pattern to locate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndPosition`  <a name="cfn-databrew-recipe-recipeparameters-endposition"></a>
The end position to locate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndValue`  <a name="cfn-databrew-recipe-recipeparameters-endvalue"></a>
The end value to locate\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ExpandContractions`  <a name="cfn-databrew-recipe-recipeparameters-expandcontractions"></a>
A list of word contractions and what they expand to\. For eample: *can't*; *cannot*; *can not*\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Exponent`  <a name="cfn-databrew-recipe-recipeparameters-exponent"></a>
The exponent to apply in an exponential operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FalseString`  <a name="cfn-databrew-recipe-recipeparameters-falsestring"></a>
A value that represents `FALSE`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupByAggFunctionOptions`  <a name="cfn-databrew-recipe-recipeparameters-groupbyaggfunctionoptions"></a>
Specifies options to apply to the `GROUP BY` used in an aggregation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GroupByColumns`  <a name="cfn-databrew-recipe-recipeparameters-groupbycolumns"></a>
The columns to use in the `GROUP BY` clause\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HiddenColumns`  <a name="cfn-databrew-recipe-recipeparameters-hiddencolumns"></a>
A list of columns to hide\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IgnoreCase`  <a name="cfn-databrew-recipe-recipeparameters-ignorecase"></a>
Indicates that lower and upper case letters are treated equally\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IncludeInSplit`  <a name="cfn-databrew-recipe-recipeparameters-includeinsplit"></a>
Indicates if this column is participating in a split transform\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Input`  <a name="cfn-databrew-recipe-recipeparameters-input"></a>
The input location to load the dataset from \- Amazon S3 or Data Catalog\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Interval`  <a name="cfn-databrew-recipe-recipeparameters-interval"></a>
The number of characters to split by\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsText`  <a name="cfn-databrew-recipe-recipeparameters-istext"></a>
Indicates if the content is text\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JoinKeys`  <a name="cfn-databrew-recipe-recipeparameters-joinkeys"></a>
The keys or columns involved in a join\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`JoinType`  <a name="cfn-databrew-recipe-recipeparameters-jointype"></a>
The type of join to use, for example, `INNER JOIN`, `OUTER JOIN`, and so on\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LeftColumns`  <a name="cfn-databrew-recipe-recipeparameters-leftcolumns"></a>
The columns on the left side of the join\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Limit`  <a name="cfn-databrew-recipe-recipeparameters-limit"></a>
The number of times to perform `split` or `replaceBy` in a string  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LowerBound`  <a name="cfn-databrew-recipe-recipeparameters-lowerbound"></a>
The lower boundary for a value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MapType`  <a name="cfn-databrew-recipe-recipeparameters-maptype"></a>
The type of mappings to apply to construct a new dynamic frame\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ModeType`  <a name="cfn-databrew-recipe-recipeparameters-modetype"></a>
Determines the manner in which mode value is calculated, in case there is more than one mode value\. Valid values: `NONE` \| `AVERAGE` \| `MINIMUM` \| `MAXIMUM`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiLine`  <a name="cfn-databrew-recipe-recipeparameters-multiline"></a>
Specifies whether JSON input contains embedded new line characters\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRows`  <a name="cfn-databrew-recipe-recipeparameters-numrows"></a>
The number of rows to consider in a window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRowsAfter`  <a name="cfn-databrew-recipe-recipeparameters-numrowsafter"></a>
The number of rows to consider after the current row in a window  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NumRowsBefore`  <a name="cfn-databrew-recipe-recipeparameters-numrowsbefore"></a>
The number of rows to consider before the current row in a window  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrderByColumn`  <a name="cfn-databrew-recipe-recipeparameters-orderbycolumn"></a>
A column to sort the results by\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrderByColumns`  <a name="cfn-databrew-recipe-recipeparameters-orderbycolumns"></a>
The columns to sort the results by\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Other`  <a name="cfn-databrew-recipe-recipeparameters-other"></a>
The value to assign to unmapped cells, in categorical mapping  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Pattern`  <a name="cfn-databrew-recipe-recipeparameters-pattern"></a>
The pattern to locate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatternOption1`  <a name="cfn-databrew-recipe-recipeparameters-patternoption1"></a>
The starting pattern to split between\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatternOption2`  <a name="cfn-databrew-recipe-recipeparameters-patternoption2"></a>
The ending pattern to split between\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PatternOptions`  <a name="cfn-databrew-recipe-recipeparameters-patternoptions"></a>
For splitting by multiple delimiters: A JSON\-encoded string that lists the patterns inte format\. For example: `[{\"pattern\":\"1\",\"includeInSplit\":true}]`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Period`  <a name="cfn-databrew-recipe-recipeparameters-period"></a>
The size of the rolling window\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Position`  <a name="cfn-databrew-recipe-recipeparameters-position"></a>
The character index within a string  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveAllPunctuation`  <a name="cfn-databrew-recipe-recipeparameters-removeallpunctuation"></a>
If `true`, removes all of the following characters: `.` `.!` `.,` `.?`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveAllQuotes`  <a name="cfn-databrew-recipe-recipeparameters-removeallquotes"></a>
If `true`, removes all single quotes and double quotes\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveAllWhitespace`  <a name="cfn-databrew-recipe-recipeparameters-removeallwhitespace"></a>
If `true`, removes all whitespaces from the value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveCustomCharacters`  <a name="cfn-databrew-recipe-recipeparameters-removecustomcharacters"></a>
If `true`, removes all chraracters specified by `CustomCharacters`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveCustomValue`  <a name="cfn-databrew-recipe-recipeparameters-removecustomvalue"></a>
If `true`, removes all chraracters specified by `CustomValue`\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveLeadingAndTrailingPunctuation`  <a name="cfn-databrew-recipe-recipeparameters-removeleadingandtrailingpunctuation"></a>
If `true`, removes the following characters if they occur at the start or end of the value: `.` `!` `,` `?`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveLeadingAndTrailingQuotes`  <a name="cfn-databrew-recipe-recipeparameters-removeleadingandtrailingquotes"></a>
If `true`, removes single quotes and double quotes from the beginning and end of the value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveLeadingAndTrailingWhitespace`  <a name="cfn-databrew-recipe-recipeparameters-removeleadingandtrailingwhitespace"></a>
If `true`, removes all whitespaces from the beginning and end of the value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveLetters`  <a name="cfn-databrew-recipe-recipeparameters-removeletters"></a>
If `true`, removes all uppercase and lowercase alphabetic characters \(A through Z; a through z\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveNumbers`  <a name="cfn-databrew-recipe-recipeparameters-removenumbers"></a>
If `true`, removes all numeric characters \(0 through 9\)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveSourceColumn`  <a name="cfn-databrew-recipe-recipeparameters-removesourcecolumn"></a>
If `true`, the source column will be removed after un\-nesting that column\. \(Used with nested column types, such as Map, Struct, or Array\.\)  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RemoveSpecialCharacters`  <a name="cfn-databrew-recipe-recipeparameters-removespecialcharacters"></a>
If `true`, removes all of the following characters: `! " # $ % & ' ( ) * + , - . / : ; < = > ? @ [ \ ] ^ _ ` { | } ~`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RightColumns`  <a name="cfn-databrew-recipe-recipeparameters-rightcolumns"></a>
The columns on the right side of a join\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampleSize`  <a name="cfn-databrew-recipe-recipeparameters-samplesize"></a>
The number of rows in the sample\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SampleType`  <a name="cfn-databrew-recipe-recipeparameters-sampletype"></a>
The sampling type to apply to the dataset\. Valid values: `FIRST_N` \| `LAST_N` \| `RANDOM`  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryInputs`  <a name="cfn-databrew-recipe-recipeparameters-secondaryinputs"></a>
A list of secondary inputs in a UNION transform  
*Required*: No  
*Type*: List of [SecondaryInput](aws-properties-databrew-recipe-secondaryinput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondInput`  <a name="cfn-databrew-recipe-recipeparameters-secondinput"></a>
A object value to indicate the second dataset used in a join\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SheetIndexes`  <a name="cfn-databrew-recipe-recipeparameters-sheetindexes"></a>
One or more sheet numbers in the Excel file, which will be included in a dataset\.  
*Required*: No  
*Type*: List of Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SheetNames`  <a name="cfn-databrew-recipe-recipeparameters-sheetnames"></a>
Oone or more named sheets in the Excel file, which will be included in a dataset\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceColumn`  <a name="cfn-databrew-recipe-recipeparameters-sourcecolumn"></a>
A source column needed for an operation, step, or transform\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceColumn1`  <a name="cfn-databrew-recipe-recipeparameters-sourcecolumn1"></a>
A source column needed for an operation, step, or transform\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceColumn2`  <a name="cfn-databrew-recipe-recipeparameters-sourcecolumn2"></a>
A source column needed for an operation, step, or transform\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceColumns`  <a name="cfn-databrew-recipe-recipeparameters-sourcecolumns"></a>
A list of source columns needed for an operation, step, or transform\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartColumnIndex`  <a name="cfn-databrew-recipe-recipeparameters-startcolumnindex"></a>
The index number of the first column used by an operation, step, or transform\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartPattern`  <a name="cfn-databrew-recipe-recipeparameters-startpattern"></a>
The starting pattern to locate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartPosition`  <a name="cfn-databrew-recipe-recipeparameters-startposition"></a>
The starting position to locate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartValue`  <a name="cfn-databrew-recipe-recipeparameters-startvalue"></a>
The starting value to locate\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StemmingMode`  <a name="cfn-databrew-recipe-recipeparameters-stemmingmode"></a>
Indicates this operation uses stems and lemmas \(base words\) for word tokenization\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepCount`  <a name="cfn-databrew-recipe-recipeparameters-stepcount"></a>
The total number of transforms in this recipe\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StepIndex`  <a name="cfn-databrew-recipe-recipeparameters-stepindex"></a>
The index ID of a step\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StopWordsMode`  <a name="cfn-databrew-recipe-recipeparameters-stopwordsmode"></a>
Indicates this operation uses stop words as part of word tokenization\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Strategy`  <a name="cfn-databrew-recipe-recipeparameters-strategy"></a>
The resolution strategy to apply in resolving ambiguities\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetColumn`  <a name="cfn-databrew-recipe-recipeparameters-targetcolumn"></a>
The column targeted by this operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetColumnNames`  <a name="cfn-databrew-recipe-recipeparameters-targetcolumnnames"></a>
The names to give columns altered by this operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetDateFormat`  <a name="cfn-databrew-recipe-recipeparameters-targetdateformat"></a>
The date format to convert to\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetIndex`  <a name="cfn-databrew-recipe-recipeparameters-targetindex"></a>
The index number of an object that is targeted by this operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZone`  <a name="cfn-databrew-recipe-recipeparameters-timezone"></a>
The current timezone that you want to use for dates\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TokenizerPattern`  <a name="cfn-databrew-recipe-recipeparameters-tokenizerpattern"></a>
A regex expression to use when splitting text into terms, also called words or tokens\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TrueString`  <a name="cfn-databrew-recipe-recipeparameters-truestring"></a>
A value to use to represent `TRUE`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UdfLang`  <a name="cfn-databrew-recipe-recipeparameters-udflang"></a>
The language that's used in the user\-defined function\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Units`  <a name="cfn-databrew-recipe-recipeparameters-units"></a>
Specifies a unit of time\. For example: `MINUTES`; `SECONDS`; `HOURS`; etc\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnpivotColumn`  <a name="cfn-databrew-recipe-recipeparameters-unpivotcolumn"></a>
Cast columns as rows, so that each value is a different row in a single column\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpperBound`  <a name="cfn-databrew-recipe-recipeparameters-upperbound"></a>
The upper boundary for a value\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseNewDataFrame`  <a name="cfn-databrew-recipe-recipeparameters-usenewdataframe"></a>
Create a new container to hold a dataset\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-databrew-recipe-recipeparameters-value"></a>
A static value that can be used in a comparison, a substitution, or in another context\-specific way\. A `Value` can be a number, string, or other datatype, depending on the recipe action in which it's used\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value1`  <a name="cfn-databrew-recipe-recipeparameters-value1"></a>
A value that's used by this operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value2`  <a name="cfn-databrew-recipe-recipeparameters-value2"></a>
A value that's used by this operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ValueColumn`  <a name="cfn-databrew-recipe-recipeparameters-valuecolumn"></a>
The column that is provided as a value that's used by this operation\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ViewFrame`  <a name="cfn-databrew-recipe-recipeparameters-viewframe"></a>
The subset of rows currently available for viewing\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)