# WeBWorK PG Macro Library Knowledge Base

Welcome to the complete, categorized reference guide for WeBWorK PG 2.20 macro tracking profiles.

## 🗺️ Table of Contents
* [📈 Statistics & Probability](#statistics-&-probability)
  * [`deprecated/regrfnsPG.pl`](#-deprecatedregrfnspgpl)
  * [`graph/PGstatisticsGraphMacros.pl`](#-graphpgstatisticsgraphmacrospl)
  * [`math/PGnauSet.pl`](#-mathpgnausetpl)
  * [`math/PGnauStats.pl`](#-mathpgnaustatspl)
  * [`math/PGstatisticsmacros.pl`](#-mathpgstatisticsmacrospl)
* [📐 Calculus & Differential Equations](#calculus-&-differential-equations)
  * [`math/PGdiffeqmacros.pl`](#-mathpgdiffeqmacrospl)
  * [`parsers/parserSolutionFor.pl`](#-parsersparsersolutionforpl)
  * [`parsers/parserFormulaUpToConstant.pl`](#-parsersparserformulauptoconstantpl)
  * [`parsers/parserParametricPlane.pl`](#-parsersparserparametricplanepl)
  * [`parsers/parserLinearRelation.pl`](#-parsersparserlinearrelationpl)
  * [`parsers/parserImplicitEquation.pl`](#-parsersparserimplicitequationpl)
  * [`parsers/parserParametricLine.pl`](#-parsersparserparametriclinepl)
  * [`parsers/parserFunctionPrime.pl`](#-parsersparserfunctionprimepl)
* [⚙️ Core Framework & Parsers](#core-framework-&-parsers)
  * [`PG.pl`](#-pgpl)
  * [`ui/text2PG.pl`](#-uitext2pgpl)
  * [`deprecated/parserUtils.pl`](#-deprecatedparserutilspl)
  * [`core/Parser.pl`](#-coreparserpl)
  * [`core/PGessaymacros.pl`](#-corepgessaymacrospl)
  * [`core/PGML.pl`](#-corepgmlpl)
  * [`core/Value.pl`](#-corevaluepl)
  * [`core/scaffold.pl`](#-corescaffoldpl)
  * [`core/RserveClient.pl`](#-corerserveclientpl)
  * [`core/PGanswermacros.pl`](#-corepganswermacrospl)
  * [`core/PGbasicmacros.pl`](#-corepgbasicmacrospl)
  * [`core/PGcommonFunctions.pl`](#-corepgcommonfunctionspl)
  * [`core/PGauxiliaryFunctions.pl`](#-corepgauxiliaryfunctionspl)
  * [`core/sage.pl`](#-coresagepl)
  * [`core/MathObjects.pl`](#-coremathobjectspl)
  * [`graph/parserGraphTool.pl`](#-graphparsergraphtoolpl)
  * [`parsers/parserCheckboxList.pl`](#-parsersparsercheckboxlistpl)
  * [`parsers/parserRadioButtons.pl`](#-parsersparserradiobuttonspl)
  * [`parsers/parserLogb.pl`](#-parsersparserlogbpl)
  * [`parsers/parserAutoStrings.pl`](#-parsersparserautostringspl)
  * [`parsers/parserWordCompletion.pl`](#-parsersparserwordcompletionpl)
  * [`parsers/parserLinearInequality.pl`](#-parsersparserlinearinequalitypl)
  * [`parsers/parserRoot.pl`](#-parsersparserrootpl)
  * [`parsers/parserFunction.pl`](#-parsersparserfunctionpl)
  * [`parsers/parserFormulaAnyVar.pl`](#-parsersparserformulaanyvarpl)
  * [`parsers/parserMultiAnswer.pl`](#-parsersparsermultianswerpl)
  * [`parsers/parserPopUp.pl`](#-parsersparserpopuppl)
  * [`parsers/parserPrime.pl`](#-parsersparserprimepl)
  * [`parsers/parserOneOf.pl`](#-parsersparseroneofpl)
  * [`parsers/parserImplicitPlane.pl`](#-parsersparserimplicitplanepl)
  * [`parsers/parserRadioMultiAnswer.pl`](#-parsersparserradiomultianswerpl)
  * [`parsers/parserFormulaWithUnits.pl`](#-parsersparserformulawithunitspl)
  * [`parsers/parserAssignment.pl`](#-parsersparserassignmentpl)
* [🛠️ Advanced Modules, Graphics & Legacy](#advanced-modules,-graphics-&-legacy)
  * [`answers/PGfunctionevaluators.pl`](#-answerspgfunctionevaluatorspl)
  * [`answers/PGnumericevaluators.pl`](#-answerspgnumericevaluatorspl)
  * [`answers/Generic.pl`](#-answersgenericpl)
  * [`answers/answerCustom.pl`](#-answersanswercustompl)
  * [`answers/PGstringevaluators.pl`](#-answerspgstringevaluatorspl)
  * [`answers/answerHints.pl`](#-answersanswerhintspl)
  * [`answers/weightedGrader.pl`](#-answersweightedgraderpl)
  * [`answers/PGmiscevaluators.pl`](#-answerspgmiscevaluatorspl)
  * [`answers/extraAnswerEvaluators.pl`](#-answersextraanswerevaluatorspl)
  * [`answers/unorderedAnswer.pl`](#-answersunorderedanswerpl)
  * [`answers/PGasu.pl`](#-answerspgasupl)
  * [`capa/PG_CAPAmacros.pl`](#-capapg_capamacrospl)
  * [`ui/PGchoicemacros.pl`](#-uipgchoicemacrospl)
  * [`ui/unionTables.pl`](#-uiuniontablespl)
  * [`ui/unionLists.pl`](#-uiunionlistspl)
  * [`ui/choiceUtils.pl`](#-uichoiceutilspl)
  * [`ui/alignedChoice.pl`](#-uialignedchoicepl)
  * [`ui/niceTables.pl`](#-uinicetablespl)
  * [`ui/pccTables.pl`](#-uipcctablespl)
  * [`ui/quickMatrixEntry.pl`](#-uiquickmatrixentrypl)
  * [`ui/problemPanic.pl`](#-uiproblempanicpl)
  * [`deprecated/hhAdditionalMacros.pl`](#-deprecatedhhadditionalmacrospl)
  * [`deprecated/unionProblem.pl`](#-deprecatedunionproblempl)
  * [`deprecated/unionMacros.pl`](#-deprecatedunionmacrospl)
  * [`deprecated/CanvasObject.pl`](#-deprecatedcanvasobjectpl)
  * [`deprecated/PGunion.pl`](#-deprecatedpgunionpl)
  * [`deprecated/freemanMacros.pl`](#-deprecatedfreemanmacrospl)
  * [`deprecated/PeriodicRerandomization.pl`](#-deprecatedperiodicrerandomizationpl)
  * [`deprecated/unionMessages.pl`](#-deprecatedunionmessagespl)
  * [`deprecated/unionUtils.pl`](#-deprecatedunionutilspl)
  * [`deprecated/problemPreserveAnswers.pl`](#-deprecatedproblempreserveanswerspl)
  * [`deprecated/Dartmouthmacros.pl`](#-deprecateddartmouthmacrospl)
  * [`deprecated/BrockPhysicsMacros.pl`](#-deprecatedbrockphysicsmacrospl)
  * [`deprecated/compoundProblem.pl`](#-deprecatedcompoundproblempl)
  * [`deprecated/PGcomplexmacros.pl`](#-deprecatedpgcomplexmacrospl)
  * [`deprecated/CofIdaho_macros.pl`](#-deprecatedcofidaho_macrospl)
  * [`deprecated/unionInclude.pl`](#-deprecatedunionincludepl)
  * [`deprecated/problemRandomize.pl`](#-deprecatedproblemrandomizepl)
  * [`deprecated/compoundProblem5.pl`](#-deprecatedcompoundproblem5pl)
  * [`deprecated/answerUtils.pl`](#-deprecatedanswerutilspl)
  * [`deprecated/Alfredmacros.pl`](#-deprecatedalfredmacrospl)
  * [`deprecated/answerDiscussion.pl`](#-deprecatedanswerdiscussionpl)
  * [`deprecated/compoundProblem2.pl`](#-deprecatedcompoundproblem2pl)
  * [`deprecated/PGtextevaluators.pl`](#-deprecatedpgtextevaluatorspl)
  * [`deprecated/littleneck.pl`](#-deprecatedlittleneckpl)
  * [`deprecated/PGcomplexmacros2.pl`](#-deprecatedpgcomplexmacros2pl)
  * [`deprecated/MUHelp.pl`](#-deprecatedmuhelppl)
  * [`misc/PCCmacros.pl`](#-miscpccmacrospl)
  * [`graph/PGtikz.pl`](#-graphpgtikzpl)
  * [`graph/PGlateximage.pl`](#-graphpglateximagepl)
  * [`graph/LiveGraphics3D.pl`](#-graphlivegraphics3dpl)
  * [`graph/PGnauGraphics.pl`](#-graphpgnaugraphicspl)
  * [`graph/AppletObjects.pl`](#-graphappletobjectspl)
  * [`graph/plotly3D.pl`](#-graphplotly3dpl)
  * [`graph/imageChoice.pl`](#-graphimagechoicepl)
  * [`graph/PCCgraphMacros.pl`](#-graphpccgraphmacrospl)
  * [`graph/unionImage.pl`](#-graphunionimagepl)
  * [`math/algebraMacros.pl`](#-mathalgebramacrospl)
  * [`math/MatrixReduce.pl`](#-mathmatrixreducepl)
  * [`math/SI_property_tables.pl`](#-mathsi_property_tablespl)
  * [`math/PGpolynomialmacros.pl`](#-mathpgpolynomialmacrospl)
  * [`math/tableau.pl`](#-mathtableaupl)
  * [`math/bizarroArithmetic.pl`](#-mathbizarroarithmeticpl)
  * [`math/PGnumericalmacros.pl`](#-mathpgnumericalmacrospl)
  * [`math/tableau_main_subroutines.pl`](#-mathtableau_main_subroutinespl)
  * [`math/SolveLinearEquationPCC.pl`](#-mathsolvelinearequationpccpl)
  * [`math/SystemsOfLinearEquationsProblemPCC.pl`](#-mathsystemsoflinearequationsproblempccpl)
  * [`math/PCCfactor.pl`](#-mathpccfactorpl)
  * [`math/PGmatrixmacros.pl`](#-mathpgmatrixmacrospl)
  * [`math/draggableProof.pl`](#-mathdraggableproofpl)
  * [`math/customizeLaTeX.pl`](#-mathcustomizelatexpl)
  * [`math/PGnauScheduling.pl`](#-mathpgnauschedulingpl)
  * [`math/MatrixUnimodular.pl`](#-mathmatrixunimodularpl)
  * [`math/draggableSubsets.pl`](#-mathdraggablesubsetspl)
  * [`math/LinearProgramming.pl`](#-mathlinearprogrammingpl)
  * [`math/PGnauGraphCatalog.pl`](#-mathpgnaugraphcatalogpl)
  * [`math/PGnauGraphtheory.pl`](#-mathpgnaugraphtheorypl)
  * [`math/MatrixUnits.pl`](#-mathmatrixunitspl)
  * [`math/PGmorematrixmacros.pl`](#-mathpgmorematrixmacrospl)
  * [`math/VectorListCheckers.pl`](#-mathvectorlistcheckerspl)
  * [`PGcourse.pl`](#-pgcoursepl)
  * [`contexts/contextRationalFunction.pl`](#-contextscontextrationalfunctionpl)
  * [`contexts/contextForm.pl`](#-contextscontextformpl)
  * [`contexts/contextLimitedVector.pl`](#-contextscontextlimitedvectorpl)
  * [`contexts/contextInteger.pl`](#-contextscontextintegerpl)
  * [`contexts/contextTrigDegrees.pl`](#-contextscontexttrigdegreespl)
  * [`contexts/contextComplexJ.pl`](#-contextscontextcomplexjpl)
  * [`contexts/contextLimitedPoint.pl`](#-contextscontextlimitedpointpl)
  * [`contexts/contextFraction.pl`](#-contextscontextfractionpl)
  * [`contexts/contextRationalExponent.pl`](#-contextscontextrationalexponentpl)
  * [`contexts/contextFiniteSolutionSets.pl`](#-contextscontextfinitesolutionsetspl)
  * [`contexts/legacyFraction.pl`](#-contextslegacyfractionpl)
  * [`contexts/contextLimitedPowers.pl`](#-contextscontextlimitedpowerspl)
  * [`contexts/contextPartition.pl`](#-contextscontextpartitionpl)
  * [`contexts/contextPiecewiseFunction.pl`](#-contextscontextpiecewisefunctionpl)
  * [`contexts/contextComplexExtras.pl`](#-contextscontextcomplexextraspl)
  * [`contexts/contextPolynomialFactors.pl`](#-contextscontextpolynomialfactorspl)
  * [`contexts/contextPermutation.pl`](#-contextscontextpermutationpl)
  * [`contexts/contextInequalitySetBuilder.pl`](#-contextscontextinequalitysetbuilderpl)
  * [`contexts/contextMatrixExtras.pl`](#-contextscontextmatrixextraspl)
  * [`contexts/contextLimitedComplex.pl`](#-contextscontextlimitedcomplexpl)
  * [`contexts/contextLimitedFactor.pl`](#-contextscontextlimitedfactorpl)
  * [`contexts/contextCurrency.pl`](#-contextscontextcurrencypl)
  * [`contexts/contextReaction.pl`](#-contextscontextreactionpl)
  * [`contexts/contextAlternateDecimal.pl`](#-contextscontextalternatedecimalpl)
  * [`contexts/contextArbitraryString.pl`](#-contextscontextarbitrarystringpl)
  * [`contexts/contextRestrictedDomains.pl`](#-contextscontextrestricteddomainspl)
  * [`contexts/contextExtensions.pl`](#-contextscontextextensionspl)
  * [`contexts/contextOrdering.pl`](#-contextscontextorderingpl)
  * [`contexts/contextPercent.pl`](#-contextscontextpercentpl)
  * [`contexts/contextLimitedRadicalComplex.pl`](#-contextscontextlimitedradicalcomplexpl)
  * [`contexts/contextAlternateIntervals.pl`](#-contextscontextalternateintervalspl)
  * [`contexts/contextLimitedRadical.pl`](#-contextscontextlimitedradicalpl)
  * [`contexts/contextCongruence.pl`](#-contextscontextcongruencepl)
  * [`contexts/contextUnits.pl`](#-contextscontextunitspl)
  * [`contexts/contextInequalities.pl`](#-contextscontextinequalitiespl)
  * [`contexts/contextString.pl`](#-contextscontextstringpl)
  * [`contexts/contextPermutationUBC.pl`](#-contextscontextpermutationubcpl)
  * [`contexts/contextBaseN.pl`](#-contextscontextbasenpl)
  * [`contexts/contextBoolean.pl`](#-contextscontextbooleanpl)
  * [`contexts/contextLimitedPolynomial.pl`](#-contextscontextlimitedpolynomialpl)
  * [`contexts/contextScientificNotation.pl`](#-contextscontextscientificnotationpl)
  * [`contexts/contextTypeset.pl`](#-contextscontexttypesetpl)


## 📈 Statistics & Probability

### 📄 `deprecated/regrfnsPG.pl`
```perl
# functions for simple linear regression in perl
#/* "a","b" are the two endpoints of the range of
#   random integers to be produced. */
# inputs $a,$b are integers
#sub rndgen
#{ local($a,$b,$r);
#  $a=$_[0]; $b=$_[1];
#  $r=rand($b-$a+1); # in (0,b-a+1)
#  #print $a," ",$b," ",$r,"\n";
#  $r=int($r)+$a; # between a,b inclusive
#  $r;
#}
# N (size of population) and ssize (sample size) are inputs
# simple linear regression
# input xvec, yvec : assumed as one vector here
# output ($n,$xbar,$ybar,$sx2,$sy2,$sxy,$b0,$b1,$sse,$mse,$x0);
# subpopulation mean at x0
#sqrt(mse*(1/n+(x0-xbar)^2/((n-1)*sx2)))
# input : output of lsreg, plus x0
#  or ($n,$xbar,$ybar,$sx2,$sy2,$sxy,$b0,$b1,$sse,$mse,$x0);
# output: point estimate and SE
#prediction interval at x=x0
#sqrt(mse*(1+1/n+(x0-xbar)^2/((n-1)*sx2)))
# input : output of lsreg, plus x0
# ($n,$xbar,$ybar,$sx2,$sy2,$sxy,$b0,$b1,$sse,$mse,$x0);
# output: point estimate and SE
```

---

### 📄 `graph/PGstatisticsGraphMacros.pl`
```perl
#my $User = $main::studentLogin;
#my $psvn = $main::psvn; #$main::in{'probSetKey'};  #in{'probSetNumber'}; #$main::probSetNumber;
#my $setNumber     = $main::setNumber;
#my $probNum       = $main::probNum;
##############################################################################################
# this accomplishes the following:
#   a) clears the accumulated statistical data,
#   b) Create three random, normally distributed, and one exponentially dist. data sets.
#   c) Add the data set to the collection of data
#   d) initializes a statistical graph object
#   e) adds the relevant box plots.
##############################################################################################
#   clear_stat_graph_data();         # (a)
#
#   @data1 = urand(10.0,2.0,10,2);   # (b) - mean=10, sd=2.0, N=10, 2 dec places
#   @data2 = urand(12.0,2.0,10,2);   # (b) - mean=12, sd=2.0
#   @data3 = urand(14.0,4.0,10,2);   # (b) - mean=14, sd=4.0
#   @data4 = exprand(0.1,10,2);      # (b) - lambda=0.1, N=10, and 2 dec places (exp)
#
#   push_stat_data_set(~~@data1);    # (c)
#   push_stat_data_set(~~@data2);    # (c)
#   push_stat_data_set(~~@data3);    # (c)
#   push_stat_data_set(~~@data4);    # (c)
#
#   # Now initialize the graph (d) and add the box plots (e)
#   $graph = init_statistics_graph(axes=>[0,0.0],ticks=>[10]);
#   $bounds = add_boxplot($graph,{"outliers"=>1});
#   # or #
#   $bounds = add_histogram($graph,10,1);  # add a histogram with 10 bins and a multipler of 1.
#                                          # The multiplier is for the height of the frequencies.
#                                          # ex: if the multiplier is 2 the graph is twice as tall
#
###############################################################################################
```

---

### 📄 `math/PGnauSet.pl`
```perl
#######################################################################################################
#
# Name : DrawVenn2
#
# Input		:
#
#			$input_word 	=	'region1_info, region2_info, ...'
#						The information to use, arranged in order by region.
#						Use "_fill_" to shade the corresponding region, otherwise
#						the input is treated as label.
#
#			@options	=	'Arrow indicated options' in any order.
#
#						  labels=>'Set1 label, Set2 label, U'.  Set1 is on the
#							  left.  Leaving any or all entries blank will
#							  produce no label for that item.  Default is
#							  'A,B,U'
#
# Output 	:	$diagram   	= 	a graphics object, the diagram to plot.  Use 'Plot' in the
#						.pg file.
#
########################################################################################################
#######################################################################################################
#
# Name : DrawVenn3
#
# Input		:
#
#			$input_word 	=	'region1_info, region2_info, ...'
#						The information to use, arranged in order by region.
#						Use "_fill_" to shade the corresponding region, otherwise
#						the input is treated as label.
#
#			@options	=	'Arrow indicated options' in any order.
#
#						  labels=>'Set1 label, Set2 label, Set 3 label, U'.  Set1 is on the
#							  left.  Leaving any or all entries blank will
#							  produce no label for that item.  Default is
#							  'A,B,C,U'
#
# Output 	:	$diagram   	= 	a graphics object, the diagram to plot.  Use 'Plot' in the
#						.pg file.
#
########################################################################################################
#####################################
#
# Name	:	Venn2answers
#
#
#####################################
#####################################
#
# Name	:	Venn3answers
#
#
#####################################
```

---

### 📄 `math/PGnauStats.pl`
```perl
################################
#Name: MeanDev
#Input: List of data values
#Output: List  containing mean and standard deviation
################################
################################
#Name: Median
#Input: List of data values
#Output: Value of the median
################################
################################
#Name: FiveNum
#Input: List of data values
#Output: List containing the five number summary in order from Low to High
################################
################################
#Name: Mode
#Input: List of data values
#Optional Input: 'Max_Modes'=> num limits the maximum number of modes to num
#Output: List containing the mode or the list ("None") if the number of modes
#        is more than num,
################################
######################################
#Name: isstring
#Input: A variable
#Output: A 1 if the variable is a string, 0 otherwise
######################################
#########################################################################################
#
# Name   : BoxPlot
# Input  : $min 	= the minimum value in the dataset
#          $q1 		= the first quartile value
#	   $q2 		= the second quartile (median) value
#          $q3 		= the third quartile value
#          $max 	= the maximum value in the dataset
#          Options      = array of numbers to be plotted with tickmarks,
#			  perhaps interspersed with the options below
#			  in any order.
#
#	   Options ::  The following may be passed AFTER the five numbers
#                      (together with the labels, without regard to order):
#
#                      (1) Use "wmin=>number" (no quotes really) to set the
#		           lower viewing window.  Default is '$min'
#
#		       (2) Use "wmax=>number" (no quotes really) to set the
#			   upper viewing window.  Default is '$max'
#
#		       (3) Use "horzlabels=>number" to set the approximate
#			   number of horizontal labels.  Default is 10.
#
#		       (4) Use "axis=>0" to hide the horizontal axis.
#                          Default is to plot the axis.
#
#                      (5) Use labels such as 'a','b' and so on to label any
#			   of the five numbers with the desired string.
#			   Default is no labels.
#
# Output : $pic = a graphics object.
#
#####################################################################################
#################
# Name : SpecialData
# Input : A string containing the type of data desired (Exp, Sym, Bi, Norm, Left, Right)
#	  and any optional input.
# Optional Input : count => n : the number of data values to generate (default = 500)
#		    mean => n : The mean for the normal, left or right distributions (default = 0)
#		     dev => n : The standard deviation for the normal, left or right distributions (default = 1)
#		     min => n : The minimum value for the data (default = 0)
#		     max => n : The maximum value for the data (default = 100)
# Output : A list of data values with the special properties.
#################
######################################
#Name: PercentStemAndLeaf
#Input: List of percentage values (anything from 0 to 100).
#Optional Input: At beginning of list:
#		all => 1,0 turns on or off the display of all columns of the
#		 table (useful if data is within a small range).
#		sort => 1,0 turns on or off sorted data rows.
#		single=>1,0 displays answers as a single cell in the table or
#		 determines the number from the data.
#Output: A list containing two strings.  The first is a string that represents
#	 the html table to be displayed and the second is the TeX table to be
#	 displayed.
######################################
###
# Name	: RoundStep
###
###
# Name	: CeilingStep
###
###
# Name	: FloorStep
###
#############################################################################
# Name   : Histogram
# Input  : @data 	= "the data"
#          Options      = may be interspersed in the data in any order.
#
#	   Options ::  The following may be passed AFTER the standard input
#		       above (without regard to order):
#
#                      (1) Use "labelcells=>1" (no quotes really) to include
#		           frequency labels at the top of each cell.
#			   The default is no labels.
#
#		       (2) Use "labelcount=>number" (no quotes really) to
#			   set an approximate number of labels to use on the
#			   vertical axis.  Default is 5.
#
#		       (3) Use "title=>string" to add a title, centered at
#			   the top.
#
#		       (4) Use "axislabel=>string" to add an axis label,
#			   centered at the bottom.
#
#		       (5) Use "bins=>number" to specify approximately how
#			   many bins should be used.  Default is 10.
#
#		       Note : any extra numbers input at the end will be
#			      taken as data.
#
# Output : $pic = a graphics object
#############################################################################
################################
#Name: RandomNormalNumber
#Input: None required
#Optional Input: 'mean' => the mean of the normal distribution being used. (default = 0)
#		  'dev' => the standard deviation of the normal distribution being used. (default = 1)
#Output: A number that is related to the standard normal curve with the given mean and deviation.
################################
################################
#Name: Scatterplot
#Input: Correlation coefficient
#Optional Input: 'count'=> Number of data points to be calculated.
#		 'mean' => the mean of the normal distribution being used.
#		  'dev' => the standard deviation of the normal distribution being used.
#		 'slope'=> the slope of the scatterplot.
#Output: A picture of the scatterplot with given slope and correlation coefficient.
################################
######################################
#Name: PieChart
#Input: List of values as: decimals - which should add to 1.  If it
#			  	sums to less than one, the function will make up the difference.
#			   or numbers > 1 - will be treated as numerators for fractions.  The sum of the
#				numbers will be the denominator and fractions will be placed on the
#				circle plot.
#Optional Input: percent => 0, 1 : Off or on display of percentage values (regardless of input manner) (default = 0)
#		 labels => 1, 0 : On or off label display.  (default = 1)
#		 values => 1, 0 : On or off value display. (default = 1)
#Output: A picture of the corresponding circle plot
######################################
###########################################################################################################
#
# Name	:	DrawNormalDist
#
# Input : 	lower_z_point, upper_z_point (use -INF or INF for infinite values)
#
# Optional Input : After first two points.
#		$lower_label = the lower label to use.  Default is 'a'
#		$upper_label = the upper label to use.  Default is 'b'
#		    (if only want upper label, must input a lower label)
#		outside => n - 0, 1 to shade between or outside the numbers Default = 0;
#		title => 'title string' - will display a title if desired.
#		mean => n - will display the given mean (default display nothing)
#
###########################################################################################################
```

---

### 📄 `math/PGstatisticsmacros.pl`
```perl
#	 Usage: ($t,$df,$p) = two_sample_t_test(\@data1,\@data2);                       # Perform a two-sided t-test using a pooled variance.
#  or:    ($t,$df,$p) = two_sample_t_test(\@data1,\@data2,{'test'=>'right','variance'=>'pooled});     # Perform a right sided t-test using a pooled variance
#  or:    ($t,$df,$p) = two_sample_t_test(\@data1,\@data2,{'test'=>'left','variance'=>'separate'});      # Perform a left sided t-test using a separate variance
#  or:    ($t,$df,$p) = two_sample_t_test(\@data1,\@data2,{'test'=>'two-sided','variance'=>'pooled}); # Perform a left sided t-test using a pooled variance
#
# example:
#
# @data1 = (1,2,3,4,5,6,7);
# @data2 = (2,3,4,5,6,7,9);
# ($t,$df,$p) = two_sample_t_test(2.5,\@data1,\@data2,{'test'=>'right','variance'=>'pooled});
#
```

---

## 📐 Calculus & Differential Equations

### 📄 `math/PGdiffeqmacros.pl`
```perl
#!/usr/bin/perl -w
#my @answer = oldivy(1,2,1,8,4);
#print ("The old program says:\n");
#print ($answer[0]);
#print ("\n");
#@answer = ivy(1,2,1,8,4);
#print ("My program says:\n");
#print ($answer[0]);
#print ("\n");
#the subroutine is invoked with arguments such as complexmult(2,3,4,5) or
#complexmult(@data), where @data = (2,3,4,5)
##########
# sub addtwo adds two strings formally
# An "indicator"  for a string is a
#  number ,e.g. coefficient,which indicates
# whether the string is to be
# added or is to be regarded as zero.
# The  non-zero terms are formally added as strings.
# The input is an array
# ($1staddend, $1stindicator,$2ndaddend,$2ndindicator)
# The return is an array
# (formal sum, indicator of formal sum)
########
# sub add generalizes sub addtwo to more addends.
# It formally adds the nonzero terms.
# The input is an array of even length
# consisting of each addend,a string,
# followed by its indicator.
#######
# sub diffop cleans up the typed expression
# of a diff. operator.
# input @diffop =($A,$B,$C) is the coefficients.
# input is given as arguments viz difftop($A,$B,$C);
# output is the diff. operator as a string $L in TEX
########
# sub rad simplifies (a/b)*(sqrt(c))
# input is given as arguments on rad viz.: rad($a,$b,$c);
# $a,$b,$c are integers and $c>=0 and $b is not zero.
# output is an array =(answer as string,new$a,new$b, new$c)
##########
##########
####
# sub exp simplifies exp($r*t) in form for writing perl
# or tex. The input is exp($r,$ind); $ind indicates whether
# we want perl or tex mode. $r is a string that represents
# a number.
# If $ind = 0  output is "exp(($r)*t)", simplified if possible.
# If $ind = 1  output is "exp(($r)*t)", simplified if possible.
# y(t) = me^(-Bt/(2A))*cos(t*sqrt(4AC-B*B)/(2A))+(2An+Bm)*sqrt(4AC-B*B)/(4AC-B*B)*e^(-Bt/(2A))*sin(t*sqrt(4AC-B*B)/(2A))
############
#sub ivy solves the initial value problem
# $a*y'' + $b*y' + $c*y = 0, with  y(0) = $m,  y'(0) = $n
#The numbers $a,$b,$c,$m,$n should be integers with $a not 0.
#The inputs are given as arguments viz: ivy ($a,$b,$c,$m,$n).
#The output is the solution as a string giving a function of t.
#################
# undeterminedSin is a subroutine to solve
# undetermined coefficient problems that have
# sines and cosines.
# The input is an array ($A,$B,$C,$r,$w,$q1,$q0,$r1,$r0)
# given as arguments on undeterminedSin
# $L =$A y'' + $B y' + $C y
# $rhs = ($q1 t + $q0) cos($w t)exp($r t) +
#        ($r1 t + $r0) sin($w t)exp($r t)
# The subroutine uses undetermined coefficients
# to find a solution $y of $L = $rhs .
# The output \is $y
```

---

### 📄 `parsers/parserSolutionFor.pl`
```perl
#
#  Create a SolutionFor object of the correct type
#
######################################################################
#
#  Define the new class (we make subclasses below)
#  (we need subclasses in order to make things work
#  properly with single-variable complex or real-valued
#  equations)
#
#
#  Evaluate the formula on the given point
#
#
#  The name of this object for error messages
#
#
#  Do a comparison by testing if the formula's equality
#  operation returns true or false.
#  (Since we are implementing <=> here, we need
#  to return 0 when true and 1 when false.)
#
#
#  Set up a new context that is a copy of the current one, but
#  has the equality operator defined, and the SolutionFor object
#  prededence set so that comparisons with points or numbers will
#  be promoted to comparisons with the SolutionFor
#
######################################################################
#
#  A separate class for Reals, to get Value::Real in the ISA list
#
#
#  Pass the real number directly
#
######################################################################
#
#  A separate class for Complexes
#
#
#  Pass the complex number directly
#
######################################################################
#
#  A separate class for Points
#
#
#  Use the Point's defaults, but turn off coordinate hints
#  (since a wrong coordinate isn't detectable)
#
```

---

### 📄 `parsers/parserFormulaUpToConstant.pl`
```perl
#
#  Create an instance of a FormulaUpToConstant.  If no constant
#  is supplied, we add C ourselves.
#
##################################################
#
#  Remember that compare implements the overloaded perl <=> operator,
#  and $a <=> $b is -1 when $a < $b, 0 when $a == $b and 1 when $a > $b.
#  In our case, we only care about equality, so we will return 0 when
#  equal and other numbers to indicate the reason they are not equal
#  (this can be used by the answer checker to print helpful messages)
#
#
#  Return the {adapt} formula with test points adjusted
#
#
#  Inherit from the main FormulaUpToConstant, but
#  adjust the test points to include the constants
#
#
#  Insert dummy values for the constants for the test points
#  (These are supposed to be +C, so the value shouldn't matter?)
#
##################################################
#
#  Here we override part of the answer comparison
#  routines in order to be able to generate
#  helpful error messages for students when
#  they leave off the + C.
#
#
#  Show hints by default
#
#
#  Provide diagnostics based on the adapted function used to check
#  the student's answer
#
#
#  Make it possible to graph single-variable formulas by setting
#  the arbitrary constants to 0 first.
#
#
#  Add useful messages, if the author requested them
#
#
#  Don't perform equivalence check
#
##################################################
#
#  Get the name of the constant
#
#
#  Remove the constant and return a Formula object
#
#
#  Override the differentiation so that we always return
#  a Formula, not a FormulaUpToConstant (we don't want to
#  add the C in again).
#
######################################################################
#
#  This class replaces the Parser::Variable class, and its job
#  is to look for new constants that aren't in the context,
#  and add them in.  This allows students to use ANY constant
#  they want, and a different one from the professor.  We check
#  that the student only used ONE arbitrary constant, however.
#
```

---

### 📄 `parsers/parserParametricPlane.pl`
```perl
#
#  Define the subclass of Formula
#
#
#  Report some errors that were stopped by the showEqualErrors=>0 above.
#
```

---

### 📄 `parsers/parserLinearRelation.pl`
```perl
##################################################
#
#  Initialize the contexts and make the creator function.
#
#    $R = LinearRelation("x + y + 2z <= 5");
#    $R = Formula("x + y + 2z <= 5");
#    $R = Compute("x + y + 2z <= 5");
#    $R = LinearRelation([1,2,1], [1,1,2], "<=");
#    $R = LinearRelation([1,2,1], 5, "<=");
#
#  If the vectors are zero, check if true or false
#  If the vectors are non-zero, check if the equations are multiples of each other.
#
#
#  Only compare two relations
#
#
#  We subclass BOP::equality so that we can assign a type using _check and
#  override the _eval method for relation operators
#
#
#  We use a special formula object to check if the formula is a
#  LinearRelation or not, and return the proper class.  This allows
#  lists of linear relations, for example.
#
```

---

### 📄 `parsers/parserImplicitEquation.pl`
```perl
#
#  Create the ImplicitEquation package
#
#
#  Override the comparison method.
#
#  Turn the right-hand equation into an ImplicitEquation.  This creates
#  the test points (i.e., finds the solution points).  Then check
#  the professor's function on the student's test points and the
#  student's function on the professor's test points.
#
#
#  Use the original equation for these (but not for perl(), since we
#  need that to use perlFunction).
#
#
#  Locate points that satisfy the equation
#
#
#  Get random points and sort them by sign of the function.
#  Also, get the average function value, and indicate if
#  we actually did find both positive and negative values.
#
#
#  Make a list of positive and negative points sorted by
#  the distance between them.  Also return the average distance
#  between points.
#
#
#  Use bisection algorithm to find a point where the function is zero
#  (i.e., where the original equation is an equality)
#  If we can't find a point (e.g., we are at a discontinuity),
#  return an undefined value.
#
```

---

### 📄 `parsers/parserParametricLine.pl`
```perl
#
#  Define the subclass of Formula
#
#  Two parametric lines are equal if they have
#  parallel direction vectors and either the same
#  points or the vector between the points is
#  parallel to the (common) direction vector.
#
#  Report some errors that were stopped by the showEqualErrors=>0 above.
#
```

---

### 📄 `parsers/parserFunctionPrime.pl`
```perl
#
#  The package that will manage function primes
#
#
#  Override the Parser::Function new() method to handle names with primes.
#  When such a name appears, define a new (hidden) parserFunction that
#  has the proper function and formula for the number of derivatives
#  requested.
#
```

---

## ⚙️ Core Framework & Parsers

### 📄 `PG.pl`
```perl
# This loads the basic css needed by pg.
# It is expected that the requestor will also load the styles for Bootstrap.
# Some problems use jquery-ui still, and so the requestor should also load the css for that if those problems are used,
# although those problems should also be rewritten to not use jquery-ui.
# This loads the basic javascript needed by pg.
# It is expected that the requestor will also load MathJax, Bootstrap, and jquery.
# Some problems use jquery-ui still, and so the requestor should also load the js for that if those problems are used,
# although those problems should also be rewritten to not use jquery-ui.
# sageReturnedFail checks to see if the return from Sage indicates some kind of failure
# undefined means old style return (a simple string) failed
# $obj->{success} defined but equal to zero means that the failed return and error
# messages are encoded in the $obj hash.
# The store_persistent_data, update_persistent_data, and get_persistent_data methods are deprecated and are only still
# here for backward compatability. Use the persistent_data method instead which can do everything these three methods
# can do. Note that if you use the persistent_data method, then you will need to join the values as strings if you want
# that. Even better pass the persistent_data method an array reference containing the values so you can avoid the hassle
# of splitting the values when they are retrieved.
# This stores form data (such as sticky answers), but does nothing more.
# It's a bit of hack since we are storing these in the
# KEPT_EXTRA_ANSWERS queue even if they aren't answers per se.
# Creates a new array element answer name and records it.
#FIXME -- examine the difference between insert_response and extend_response
# For radio buttons and checkboxes.
# This is a stub for deprecated problems that call this method.  Some of the GeoGebra
# problems that do so actually work even though this method does nothing.
## Problem Grader Subroutines
#####################################
# This is a model for plug-in problem graders
#####################################
# ^function install_problem_grader
# ^uses PG_restricted_eval
# ^uses %PG_FLAGS{PROBLEM_GRADER_TO_USE}
#  FIXME? The following functions were taken from the former
#  dangerousMacros.pl file and might have issues when placed here.
#
#  Some constants that can be used in perl expressions
#
# ^function i
# ^uses $_parser_loaded
# ^uses &Complex::i
# ^uses &Value::Package
# ^function j
# ^uses $_parser_loaded
# ^uses &Value::Package
# ^function k
# ^uses $_parser_loaded
# ^uses &Value::Package
# ^function pi
# ^uses $_parser_loaded
# ^uses &Value::Package
# ^function Infinity
# ^uses $_parser_loaded
# ^uses &Value::Package
# ^function abs
# ^function sqrt
# ^function exp
# ^function log
# ^function sin
# ^function cos
# ^function atan2
#
#  Allow these functions to be overridden without complaint.
#  (needed for log() to implement $useBaseTenLog)
#
#sub log  {return CORE::log($_[0])};
# used to be Parser::defineLog -- but that generated redefined notices
```

---

### 📄 `ui/text2PG.pl`
```perl
######################################################################
#
#  Sanitize a text string for use with TEXT and EV3, so that
#  non-math text is properly displayed in HTML mode and TeX
#  mode.  Newlines and blank lines can be converted to $BR and
#  $PAR automatically.
#
#  Format:  text2PG(string [,options]);
#
#  where options are from among:
#
#    trimWhitespace => 0 or 1    Specifies if leading and trailing whitespace
#                                is removed before processing.
#                                  Default: 1
#
#    convertBlanklines => 0 or 1 Specifies whether blank lines should be
#                                turned into paragraph breaks.
#                                  Default: 1
#
#    convertNewlines => 0 or 1   Specifies whether newlines should be
#                                turned into line breaks.
#                                  Default: 1
#
#    sanitizeText => 0 or 1      Specifies whether to convert HTML and TeX
#                                special characters to printable form
#                                outside of math mode and commands.
#                                  Default: 1
#
#    allowCommands => 0 or 1     Specifies if text within command blocks
#                                is left unchanged (1) or not (0).
#                                  Default: 0
#
#    convertDollars => 0 or 1    Specifies whether dollar signs not followed
#                                by a letter should be replaced by ${DOLLAR}
#                                (you only want to do this if not passing
#                                the result through EV3 with variable
#                                substitutions).
#                                  Default: 0
#
#    doubleSlashes => 0 or 1     Specifies whether backslashes should be
#                                doubled (in preparation for passing
#                                into EV3).
#                                  Default: 1
#
```

---

### 📄 `deprecated/parserUtils.pl`
```perl
# not sure why these are loaded.  They are not used in this file.  If these are loaded
# there is an error during the load_macros.t test.
# loadMacros("unionImage.pl", "unionTables.pl",);
#  HTML(htmlcode)
#  HTML(htmlcode,texcode)
#
#  Insert $html in HTML mode.  In TeX mode, insert nothing for the first form,
#  and $tex for the second form.
#
#
#  Begin and end <TT> mode
#
#
#  Begin and end <SMALL> mode
#
#
#  Block quotes
#
#
#  Smart-quotes in TeX mode, regular quotes in HTML mode
#
#
#  make sure all characters are displayed
#
```

---

### 📄 `core/Parser.pl`
```perl
###########################################################################
##
##  Set up the functions needed by the Parser.
##
# ^uses $Parser::installed
# ^uses $Value::installed
# ^uses loadMacros
# ^function Formula
# ^uses Value::Package
# ^function Compute
# ^uses Formula
# ^uses Value::contextSet
# ^function Context
# ^uses Parser::Context::current
# ^uses %context
#  # ^variable our %context
# ^uses Context
###########################################################################
#
# stubs for trigonometric functions
#
# ^package Ignore
# ^#function sin
# ^#uses Parser::Function::call
#sub sin {Parser::Function->call('sin',@_)}    # Let overload handle it
# ^#function cos
# ^#uses Parser::Function::call
#sub cos {Parser::Function->call('cos',@_)}    # Let overload handle it
# ^function tan
# ^uses Parser::Function::call
# ^function sec
# ^uses Parser::Function::call
# ^function csc
# ^uses Parser::Function::call
# ^function cot
# ^uses Parser::Function::call
# ^function asin
# ^uses Parser::Function::call
# ^function acos
# ^uses Parser::Function::call
# ^function atan
# ^uses Parser::Function::call
# ^function asec
# ^uses Parser::Function::call
# ^function acsc
# ^uses Parser::Function::call
# ^function acot
# ^uses Parser::Function::call
# ^function arcsin
# ^uses Parser::Function::call
# ^function arccos
# ^uses Parser::Function::call
# ^function arctan
# ^uses Parser::Function::call
# ^function arcsec
# ^uses Parser::Function::call
# ^function arccsc
# ^uses Parser::Function::call
# ^function arccot
# ^uses Parser::Function::call
###########################################################################
#
# stubs for hyperbolic functions
#
# ^function sinh
# ^uses Parser::Function::call
# ^function cosh
# ^uses Parser::Function::call
# ^function tanh
# ^uses Parser::Function::call
# ^function sech
# ^uses Parser::Function::call
# ^function csch
# ^uses Parser::Function::call
# ^function coth
# ^uses Parser::Function::call
# ^function asinh
# ^uses Parser::Function::call
# ^function acosh
# ^uses Parser::Function::call
# ^function atanh
# ^uses Parser::Function::call
# ^function asech
# ^uses Parser::Function::call
# ^function acsch
# ^uses Parser::Function::call
# ^function acoth
# ^uses Parser::Function::call
# ^function arcsinh
# ^uses Parser::Function::call
# ^function arccosh
# ^uses Parser::Function::call
# ^function arctanh
# ^uses Parser::Function::call
# ^function arcsech
# ^uses Parser::Function::call
# ^function arccsch
# ^uses Parser::Function::call
# ^function arccoth
# ^uses Parser::Function::call
###########################################################################
#
# stubs for numeric functions
#
# ^#function log
# ^#uses Parser::Function::call
#sub log   {Parser::Function->call('log',@_)}    # Let overload handle it
# ^function log10
# ^uses Parser::Function::call
# ^#function exp
# ^#uses Parser::Function::call
#sub exp   {Parser::Function->call('exp',@_)}    # Let overload handle it
# ^#function sqrt
# ^#uses Parser::Function::call
#sub sqrt  {Parser::Function->call('sqrt',@_)}    # Let overload handle it
# ^#function abs
# ^#uses Parser::Function::call
#sub abs   {Parser::Function->call('abs',@_)}    # Let overload handle it
# ^function int
# ^uses Parser::Function::call
# ^function sgn
# ^uses Parser::Function::call
# ^function ln
# ^uses Parser::Function::call
# ^function logten
# ^uses Parser::Function::call
# ^package main
# ^function log10
# ^uses Parser::Function::call
# ^function Factorial
# ^uses Parser::UOP::factorial::call
###########################################################################
#
# stubs for special functions
#
# ^#function atan2
# ^#usesParser::Function::call
#sub atan2 {Parser::Function->call('atan2',@_)}    # Let overload handle it
###########################################################################
#
# stubs for numeric functions
#
# ^function arg
# ^uses Parser::Function::call
# ^function mod
# ^uses Parser::Function::call
# ^function Re
# ^uses Parser::Function::call
# ^function Im
# ^uses Parser::Function::call
# ^function conj
# ^uses Parser::Function::call
###########################################################################
#
# stubs for vector functions
#
# ^function norm
# ^uses Parser::Function::call
# ^function unit
# ^uses Parser::Function::call
#
# These are defined in PG.pl (since they call eval())
#
# sub i () {Compute('i')}
# sub j () {Compute('j')}
# sub k () {Compute('k')}
###########################################################################
# ^variable our $_parser_loaded
# ^function _Parser_init
# ^uses loadMacros
###########################################################################
```

---

### 📄 `core/PGessaymacros.pl`
```perl
# Makes an essay box and calls essay_cmp()
# Can be turned off using $pg{specialPGEnvironmentVars}{waiveExplanations}
# Takes options:
#   row (or height): height of essay box; defaults to 8
#   col (or width):  width of essay box;  defaults to 75
#   message: a message preceding the essay box; default is 'Explain.'
#   help: boolean for whether to display the essay help message; default is true
```

---

### 📄 `core/PGML.pl`
```perl
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
# No indentation for PTX
# No align for PTX
# PreTeXt can't use headings.
# No rule for PTX
######################################################################
######################################################################
######################################################################
######################################################################
```

---

### 📄 `core/Value.pl`
```perl
# sub Formula  {Value->Package("Formula()")->new(@_)}  # in Parser.pl
```

---

### 📄 `core/scaffold.pl`
```perl
# Scaffold::Begin() is used to start a new scaffold section, passing
# it any options that need to be overridden (e.g. is_open, can_open,
# open_first_section, etc).
#
# Problems can include more than one scaffold, if desired,
# and they can be nested.
#
# We save the current PG_OUTPUT, which will be put back during
# the Scaffold::End() call.  The sections use PG_OUTPUT to create
# their own text, which is added to the $scaffold->{output}
# during the Section::End() call.
# Scaffold::End() is used to end the scaffold.
#
# This puts the scaffold into the page output and opens the sections that should be open.
# Then the next nested scaffold (if any) is popped off the stack and returned.
# Report an error and die
# Create a new Scaffold object.
#
# Set the defaults for can_open, is_open, etc., but allow
# the author to override them.
# Add a section to the scaffold and give it a unique number (within
# the scaffold).  Determine its label and save it as current_section
# so that we know which section is active.
# Add the content from the current section into the scaffold's output
# and remove the current_section (so we can tell that no section is open).
# Record the answers for a section.
# Scores are obtained when post processing is done.
# Add the given sections to the list of sections to be opened for this scaffold.
# Shortcuts for Scaffold data
# Section::Begin() is used to start a section in the scaffolding,
# passing it the name of the section and any options (e.g., can_open,
# is_open, etc.).
#
# The section is added to the scaffold, and the names of the answer
# blanks for previous sections are recorded, along with information
# about the answer blanks that have evaluators assigned (so we can
# see which answers belong to this section when it closes).
# Section::End() is used to end the active section.
#
# We get the names of the answer blanks that are in this section,
# then add the HTML around the section that is used by JavaScript
# for showing/hiding the section, and finally tell the scaffold
# that the section is complete (it adds the content to its output).
# Create a new Section object.
#
# It takes default values for can_open, is_open, etc.
# from the active scaffold.  These can be overridden
# by the author.
# Adds the necessary HTML around the content of the section.  Initially a temporary "scaffold-section" tag is added that
# wraps the content, and that is replaced with the correct HTML in post processing.  The content is also removed in post
# processing if the scaffold cannot be opened and is not correct.  The $PG_OUTPUT variable holds just the contents of
# this section, so unshift the opening tags onto the front, and push the closing tags onto the back.  (This is added to
# the scaffold output when $scaffold->end_section() is called.)
# Check if all the answers for this section are correct
# Perform the can_open check for this section:
#   If the author supplied code, use it, otherwise use the routine from Section::can_open.
# Perform the is_open check for this section:
#   If the author supplied code, use it, otherwise use the routine from Section::is_open.
# Return a boolean array where a 1 means that answer blank has
# an answer evaluator assigned to it and 0 means not.
# Get the names of any of the original answer blanks that now have evaluators attached.
########################################################################
# Implements the possible values for the can_open option for scaffolds
# and sections
# Always can be opened
# Can be opened when all the answers from previous sections are correct
# Can open when previous are correct but this one is not
# Can open when incorrect
# Never can be opened
########################################################################
# Implements the possible values for the is_open option for scaffolds
# and sections
# Every section is open that can be
# Every incorrect section is open that can be
# (unless it is the first one, and everything is blank, and
# the scaffold doesn't have open_first_section set)
# The first incorrect section is open that can be
# All correct sections and the first incorrect section
# are open (that are allowed to be open)
# No sections are open
```

---

### 📄 `core/RserveClient.pl`
```perl
# This used to take a second $local parameter that specified the name of the file that would be saved in the temp
# directory. That parameter is deprecated and is ignored if given. The problem author should have never been given that
# choice. Furthermore, if the $local parameter was not specified the remote file name was used which changes every time
# the problem is rendered.  That is a problem because it results in a different file being saved into the temporary
# directory every time the problem is rendered.  Instead a unique filename is used that is created via PGresource and
# PGalias (and so is dependent on the problem seed, psvn, problem UUID, etc.).
# Returns an REXP's Perl representation, dereferencing it if it's an array reference.  `REXP::to_perl` returns a string
# scalar for Symbol, undef for Null, and an array reference to contents for all vector types. This function is a utility
# wrapper to make it easy to assign a Vector's representation to an array variable, while still working sensibly for
# non-arrays.
```

---

### 📄 `core/PGanswermacros.pl`
```perl
# FIXME TODO:
# Document and maybe split out: filters, graders, utilities
# Until we get the PG cacheing business sorted out, we need to use
# PG_restricted_eval to get the correct values for some(?) PG environment
# variables. We do this once here and place the values in lexicals for later
# access.
# ^variable my $BR
# ^variable my $functLLimitDefault
# ^variable my $functULimitDefault
# ^variable my $functVarDefault
# ^variable my $useBaseTenLog
# ^function _PGanswermacros_init
# ^uses loadMacros
# ^uses PG_restricted_eval
# ^uses $BR
# ^uses $envir{functLLimitDefault}
# ^uses $envir{functULimitDefault}
# ^uses $envir{functVarDefault}
# ^uses $envir{useBaseTenLog}
###########################################################################
###	THE	FOLLOWING ARE LOCAL	SUBROUTINES	THAT ARE MEANT TO BE CALLED	ONLY FROM THIS SCRIPT.
## Internal routine that converts variables into the standard array format
##
## IN:	one of the following:
##			an undefined value (i.e., no variable was specified)
##			a reference to an array of variable names -- [var1, var2]
##			a number (the number of variables desired) -- 3
##			one or more variable names -- (var1, var2)
## OUT:	an array of variable names
# ^function get_var_array
# ^uses $functVarDefault
## Internal routine that converts limits into the standard array of arrays format
##	Some of the cases are probably unneccessary, but better safe than sorry
##
## IN:	one of the following:
##			an undefined value (i.e., no limits were specified)
##			a reference to an array of arrays of limits -- [[llim,ulim], [llim,ulim]]
##			a reference to an array of limits -- [llim, ulim]
##			an array of array references -- ([llim,ulim], [llim,ulim])
##			an array of limits -- (llim,ulim)
## OUT:	an array of array references -- ([llim,ulim], [llim,ulim]) or ([llim,ulim])
# ^function get_limits_array
# ^uses $functLLimitDefault
# ^uses $functULimitDefault
#sub check_option_list {
#	my $size = scalar(@_);
#	if( ( $size % 2 ) != 0 ) {
#		warn "ERROR	in answer evaluator	generator:\n" .
#			"Usage: <CODE>str_cmp([\$ans1,	\$ans2],%options)</CODE>
#			or <CODE>	num_cmp([\$num1, \$num2], %options)</CODE><BR>
#			A list of inputs must be inclosed in square brackets <CODE>[\$ans1, \$ans2]</CODE>";
#	}
#}
# simple subroutine to display an error message when
# function compares are called with invalid parameters
# ^function function_invalid_params
# ^function clean_up_error_msg
#formats the student and correct answer as specified
#format must be of a form suitable for sprintf (e.g. '%0.5g'),
#with the exception that a '#' at the end of the string
#will cause trailing zeros in the decimal part to be removed
# ^function prfmt
# ^uses is_a_number
#########################################################################
# Filters for answer evaluators
#########################################################################
# ^function compare_numbers
# ^uses PG_answer_eval
# ^uses clean_up_error_msg
# ^uses prfmt
# ^uses is_a_number
# ^function std_num_filter
# ^uses math_constants
# ^uses PG_answer_eval
# ^uses clean_up_error_msg
# ^function std_num_array_filter
# ^uses set_default_options
# ^uses AnswerHash::new
# ^uses check_syntax
# ^uses std_num_filter
# ^function function_from_string2
# ^uses assign_option_aliases
# ^uses set_default_options
# ^uses math_constants
# ^uses PG_restricted_eval
# ^uses PG_answer_eval
# ^uses clean_up_error_msg
# ^function is_zero_array
# ^uses is_a_number
#	Used internally:
#
# 	&$determine_param_coeff( $rf_comparison_function # a reference to the correct answer function
# 	                 $ra_variables                   # an array of the active input variables to the functions
# 	                 $dim_of_params_space            # indicates the number of parameters upon which the
# 	                                                 # the comparison function depends linearly.  These are assumed to
# 	                                                 # be the last group of inputs to the comparison function.
#
# 	                 %options                        # $options{debug} gives more error messages
#
# 	                                                 # A typical function might look like
# 	                                                 # f(x,y,z,a,b) = x^2+a*cos(xz) + b*sin(x) with a parameter
# 	                                                 # space of dimension 2 and a variable space of dimension 3.
# 	                )
# 				# returns a list of coefficients
# ^function best_approx_parameters
# ^uses set_default_options
# ^uses pretty_print
# ^uses Matrix::new
# ^uses is_a_number
# ^function calculate_difference_vector
# ^uses assign_option_aliases
# ^uses set_default_options
## $diff *= $options{tolerance}/$options{zeroLevelTol} unless abs($instructorVal) > $options{zeroLevel};
# /DPVC
#$diff = ( $inVal - ($correctVal-$instructorVal- $instructorVal ) )/abs($instructorVal)    if abs($instructorVal) > $options{zeroLevel};
#warn "diff = $diff,   ", abs( &$rf_correct_fun(@inputs) ) , "-- $correctVal";
# ^function fix_answers_for_display
# ^uses evaluatesToNumber
# ^uses AnswerHash::new
# ^uses check_syntax
# ^function evaluatesToNumber
# ^uses is_a_numeric_expression
# ^uses PG_answer_eval
# ^uses prfmt
# ^function is_a_numeric_expression
# ^uses PG_answer_eval
# ^function is_a_number
# ^function is_a_fraction
# ^function phase_pi
# ^function is_an_arithmetic_expression
#
# ^function math_constants
# ^function is_array
# ^function check_syntax
# ^uses assign_option_aliases
# ^uses set_default_options
# ^uses AlgParserWithImplicitExpand::new
# ^function check_strings
# ^uses str_filters
# ^uses str_cmp
# OVERVIEW of reminder of function:
# if answer is correct, return correct.  (adjust score to 1)
# if answer is incorect:
#	1) determine if the answer is sensible.  if it is, return incorrect.
#	2) if the answer is not sensible (and incorrect), then return an error message indicating so.
# no matter what:  throw a 'STRING' error to skip numerical evaluations.  (error flag skips remainder of pre_filters and evaluators)
# last: 'STRING' post_filter will clear the error (avoiding pink screen.)
# ^function check_units
# ^uses str_filters
# ^uses Units::evaluate_units
# ^uses clean_up_error_msg
# ^uses prfmt
# ^function pretty_print
# ^uses lex_sort
# ^uses pretty_print
# sub pretty_print {
#     my $r_input = shift;
#     my $out = '';
#     if ( not ref($r_input) ) {
#     	$out = $r_input if defined $r_input;    # not a reference
#     	$out =~ s/</&lt;/g  ;  # protect for HTML output
#     } elsif ("$r_input" =~/hash/i) {  # this will pick up objects whose '$self' is hash and so works better than ref($r_iput).
# 	    local($^W) = 0;
#
# 		$out .= "$r_input " ."<TABLE border = \"2\" cellpadding = \"3\" BGCOLOR = \"#FFFFFF\">";
#
#
# 		foreach my $key (lex_sort( keys %$r_input )) {
# 			$out .= "<tr><TD> $key</TD><TD>=&gt;</td><td>&nbsp;".pretty_print($r_input->{$key}) . "</td></tr>";
# 		}
#
#
#
# 		$out .="</table>";
# 	} elsif (ref($r_input) eq 'ARRAY' ) {
# 		my @array = @$r_input;
# 		$out .= "( " ;
# 		while (@array) {
# 			$out .= pretty_print(shift @array) . " , ";
# 		}
# 		$out .= " )";
# 	} elsif (ref($r_input) eq 'CODE') {
# 		$out = "$r_input";
# 	} else {
# 		$out = $r_input;
# 		$out =~ s/</&lt;/g ;  # protect for HTML output
# 	}
# 		$out;
# }
```

---

### 📄 `core/PGbasicmacros.pl`
```perl
#####sub _PGbasicmacros_init { }
### In this file the _init subroutine is defined further down
### It actually initializes something!
# this is equivalent to use strict, but can be used within the Safe compartment
# Alias for NAMED_ANS_RULE
# Deprecated
##############################################
#   generate_aria_label( $name )
#   takes the name of an ANS_RULE and generates an appropriate
#   aria label for screen readers
##############################################
##############################################
#   contained_in( $elem, $array_reference or null separated string);
#   determine whether element is equal
#   ( in the sense of eq,  not ==, ) to an element in the array.
##############################################
# this is legacy code; use ans_checkbox instead
# end answer blank macros
# $main::solutionExists is passed to processProblem which displays a "show Solution" button
# when a solution is available for viewing
# End hints and solutions and statement macros
#################################
# Add a comment which will display in the Library browser
#  Currently, the only output is html
#################################
#	Produces a random number between $begin and $end with increment 1.
#	You do not have to worry about integer or floating point types.
# display macros
# MODES() is now table driven
# This replaces M3.  You can add new modes at will to this one.
# end display macros
# A utility variable.  Notice that "B" = $ALPHABET[1] and
# "ABCD" = @ALPHABET[0..3].
###############################################################
# Some constants which are different in tex and in HTML
# The order of arguments is TeX, HTML
# Adopted Davide Cervone's improvements to PAR, LTS, GTS, LTE, GTE, LBRACE, RBRACE, LB, RB. 7-14-03 AKP
#sub BR { MODES( TeX => '\\par\\noindent ', HTML => '<BR>'); };
# Alternate definition of BR which is slightly more flexible and gives more white space in printed output
# which looks better but kills more trees.
# force a space in latex, doesn't force extra space in html
###############################################################
###############################################################
## Evaluation macros
#
#  Look through a string for ``...`` or `...` and use
#  the parser to produce TeX code for the specified mathematics.
#  ``...`` does display math, `...` does in-line math.  They
#  can also be used within math mode already, in which case they
#  use whatever mode is already in effect.
#
# kludge to clean up path names
## allow underscore character in set and section names and also allows line breaks at /
#	An example of a macro which prints out a list (with letters)
# This method is deprecated.  There is no hope for the problems that use it.  Java and flash are dead.
#  uniq gives unique elements of a list:
#   More advanced macros
#This is bare bones code for embedding svg
# This is bare bones code for embedding png files -- what else should be added? (there are .js scripts for example)
# This is legacy code.
# Self closing tags.
###########
# Auxiliary macros
```

---

### 📄 `core/PGcommonFunctions.pl`
```perl
#  Make these interact nicely with Parser.pm
#  Back to main package
#  Make main versions call the checker to see
#  which package-specific version to call
```

---

### 📄 `core/PGauxiliaryFunctions.pl`
```perl
# ^uses loadMacros
# round added 6/12/2000 by David Etlinger. Edited by AKP 3-6-03
# ^uses Round
# Round contributed bt Mark Schmitt 3-6-03
# ^uses gcd
# ^ function random_pairwise_coprime
# ^uses gcd
# VS 6/30/2000
# VS 7/10/2000
# VS 8/1/2000  -  slight adaption of code from T. Shemanske of Dartmouth College
# factorial
# ^function fact
# ^uses P
# return 1 so that this file can be included with require
```

---

### 📄 `core/sage.pl`
```perl
# Sage()  is defined as an alias for creating a new sage object.
## debug code -- uncomment next line -- note that string contains html and must be protected.
# main::TEXT( "recordAnswerString is ", main::encode_pg_and_html($sage::recordAnswerString), $BR, main::encode_pg_and_html("recordAnswerBlank is |$recordAnswerBlank|"), $BR );
# Notice that python is white space sensitive so the code
# needs to be left justified when inserted to
# avoid indentation errors.
#
```

---

### 📄 `core/MathObjects.pl`
```perl
# ^uses loadMacros
```

---

### 📄 `graph/parserGraphTool.pl`
```perl
# Convert the GraphTool object's options into JSON that can be passed to the JavaScript
# graphTool method.
# Produce a hidden answer rule to contain the JavaScript result and insert the graphbox div and
# JavaScript to display the graph tool.  If a hard copy is being generated, then PGtikz.pl is used
# to generate a printable graph instead.  An attempt is made to make the printable graph look
# as much as possible like the JavaScript graph.
# Modify the student's list answer returned by the graphTool JavaScript to reproduce the
# JavaScript graph of the student's answer in the "Answer Preview" box of the results table.
# The raw list form of the answer is displayed in the "Entered" box.
# Create an answer checker to be passed to ANS().  Any parameters are passed to the checker, as
# well as any parameters passed in via cmpOptions when the GraphTool object is created.
# The correct answer is modified to reproduce the JavaScript graph of the correct answer
# displayed in the "Correct Answer" box of the results table.
# It is important that the parser::GraphTool object saved in the context flags is not accessed directly in the new
# method for any package that derives from the GraphTool::GraphObject package.  The objects for correct answers are
# constructed when the parser::GraphTool "create" method is called, and at that time only the default GraphTool options
# are available.  If the constructor uses one of those options (for example many of the objects use the bBox option) and
# that option is later changed when calling the "with" method, then the computations in the constructor will be
# incorrect and not updated.
# This should return 0 if the $point is satisfies the defining equation of the object or is on an edge of the object.
# Otherwise it should return a nonzero number indicating a side or region of the object that the point is in.
# If $fuzzy is false, then this should return true (or 1) if the $other object is visually the same as this object, and
# false (or 0) otherwise. If $fuzzy is true, then this should return true if the $other object is visually the same as
# the object ignoring if one object is solid and the other is dashed, and zero otherwise.
# This makes the == operator work for GraphTool::GraphObjects. It should usually not be overridden.  Instead override
# the cmp method above.
# The TikZ code to draw the object.
# The TikZ clipping path for the object (used by the inequality fill method) with out the \clip command and its options.
# The TikZ clipping path for the object (used by the inequality fill method) with the \clip command and options. Most
# objects only override the clipCode method and let this method add in the default \clip command and inverse clip option
# based on the fillCmp return value.
# This method should return discrete values that represent which region the point ($x, $y) is in of the regions the
# object breaks the plane into.  The same value must be returned for all points in the same region.  This method should
# return 0 for all points on a border of the object.
# This is only used by the flood fill algorithm, and should return 1 if $point is on the border of an object, and 0
# otherwise. This only needs to be overridden if the flood fill algorithm could potentially bleed across a boundary from
# one region to another (as determined by the return value of the fillCmp method) or the flood fill algorithm could
# potentially go around an end of the object.
# This method provides backward compatibility for objects defined the old way not deriving from the
# GraphTool::GraphObject package. The old methods must be called after construction because they may perform
# computations using options that are not set to their final values at that time. This is only called once and the
# results cached for later use.
```

---

### 📄 `parsers/parserCheckboxList.pl`
```perl
# Order the choices (randomizing where requested).
# Collect the labels from those that have them, and add ones to those that don't (if requested).
# Find the correct choices in the ordered array
# Format a label using the user-provided format string
# Convert a value string into a numeric index.
# Trim the selected choice or label so that it is not too long to be displayed in the results table.
# Use the actual choice strings in the output rather than the value string.
# Adjust student preview and answer strings to be the actual choice strings rather than the value strings.
# Put normal strings into \text{} and others into \verb
# Quote HTML special characters
# Given a choice, a label, or an index into the choices array, return the choice.
# Get a numeric index (-1 if not defined or not a number).
# Create the checkbox text
```

---

### 📄 `parsers/parserRadioButtons.pl`
```perl
##################################################################
#
#  The package that implements RadioButtons
#
#
#  Set up the main:: namespace
#
#
#  Create a new RadioButtons object
#
#
#  Get the choices into the correct order (randomizing where requested)
#
#
#  Collect the labels from those that have them, and add ones
#  to those that don't (if requested)
#
#
#  Find the correct choice in the ordered array
#
#
#  Format a label using the user-provided format string
#
# Convert a value string into a numeric index.
#
#  Trim the selected choice or label so that it is not too long
#  to be displayed in the results table.
#
#
#  Use the actual choice string rather than the value string as the output
#
#
#  Adjust student preview and answer strings to be the actual
#  choice string rather than the value string.
#
#  Allow users to convert the value string into a choice or label
#  Include the value string for the correct choice in the answer hash
##################################################################
#
#  Handle old-style options (order, first, last, randomize)
#
#
#  Given a choice, a label, or an index into the choices array,
#  return the choice.
#
#
#  Get a numeric index (-1 if not defined or not a number)
#
#
#  Create the radio-buttons text
#
##################################################################
```

---

### 📄 `parsers/parserLogb.pl`
```perl
# Check for numeric arguments
# Check that the inputs are OK and call the named routine
# Call the appropriate routine
# Check that the parameters are OK
# Compute log base b using log(x)/log(b)
# If b < 0 or x < 0, either promote to a complex or throw an error.
# Implement differentiation: (logb(b, u))' -> u'/(u * ln(b)) - b'/(b * ln(u)) * logb(b, u)
# Output TeX using \log_{b}(x)
```

---

### 📄 `parsers/parserAutoStrings.pl`
```perl
######################################################################
######################################################################
######################################################################
```

---

### 📄 `parsers/parserWordCompletion.pl`
```perl
# Setup the context and the PopUp() command
# Create a new WordCompletion object
# Replacement for Parser::String that takes the complete parse string as its value and gives an error if the answer
# given is not one of the allowed answers.
```

---

### 📄 `parsers/parserLinearInequality.pl`
```perl
##################################################
#
#  Define the subclass of Formula
#
#
#  We already know the vectors are non-zero, so check
#  if the equations are multiples of each other.
#
#
#  Only compare two equalities
#
#
#  We subclass BOP::equality so that we can give a warning about
#  things like 1 = 3, and compute the values of inequalities.
#
#
#  We use a special formula object to check if the formula is a
#  LinearEquality or not, and return the proper class.  This allows
#  lists of linear equalities, for example.
#
```

---

### 📄 `parsers/parserRoot.pl`
```perl
########################################################################
########################################################################
########################################################################
#
#  Check for arguments that are an integer and a number
#
#
#  Check that the inputs are OK and call the named routine
#
#
#  Call the appropriate routine
#
#
#  Check that the parameters are OK
#
#
#  Compute root using x**(1/n)
#  If x < 0 and n is even, either promote x to a complex
#   or throw an error.
#  If x < 0 and n is odd, use -(abs(x))**(1/n)
#
#
#  Implement differentiation: (u^(1/n))' -> (1/n)(u^(1/n))^(1-n) * u' - u^(1/n)ln(u)/n^2 * n'
#  (We use (u^(1/n))^(1-n) rather than u^(1/n-1) so that we have the
#  same domain as u^(1/n) does originally).
#
#
#  Output TeX using \sqrt[n]{x}
#
########################################################################
```

---

### 📄 `parsers/parserFunction.pl`
```perl
#
#  The package that will manage user-defined functions
#
#
#  Check that there are the right number of arguments
#  and they are of the right type.
#
#
#  Call the function stored in the definition
#
#
#  Check the arguments and compute the result.
#
#
#  Get the name for a number
#
```

---

### 📄 `parsers/parserFormulaAnyVar.pl`
```perl
#
#  Create an instance of a FormulaAnyVar.
#
##################################################
#
#  Implement comparison that first replaces the student
#  variable by the professor's (if they differ).
#
######################################################################
#
#  This class replaces the Parser::Variable class, and its job
#  is to look for new variables that aren't in the context,
#  and add them in.  This allows students to use ANY variable
#  they want, even a different one from the professor.  We check
#  that the student only used ONE variable, however.
#
```

---

### 📄 `parsers/parserMultiAnswer.pl`
```perl
##################################################
#  Set flags to be passed to individual answer checkers
#  Creates an answer checker (or array of same) to be passed
#  to ANS() or NAMED_ANS().  Any parameters are passed to
#  the individual answer checkers.
######################################################################
#
#  Get the answer checker used for when all the answers are treated
#  as a single result.
#
#
#  Check the answers when they are treated as a single result.
#
#    First, call individual answer checkers to get any type-check errors
#    Then perform the user's checker routine
#    Finally collect the individual answers and errors and combine
#      them for the single result.
#
#
#  Return a given string or a default if it is empty or not defined
#
######################################################################
#
#  Answer checker to use for individual entries when singleResult
#  is not in effect.
#
#
#  Call the correct answer's checker to check for syntax and type errors.
#  If this is the last one, perform the user's checker routine as well
#  Return the individual answer (our answer hash is discarded).
#
######################################################################
#
#  Collect together the correct and student answers, and call the
#  user's checker routine.
#
#  If any of the answers produced errors or the types don't match
#    don't call the user's routine.
#  Otherwise, call it, and if there was an error, report that.
#  Set the individual scores based on the result from the user's routine.
#
######################################################################
#
#  The user's checker can call setMessage(n,message) to set the error message
#  for the n-th answer blank.
#
# The user's checker can add messages to the single_ans_messages array,
# which are joined together along with any ans_messages from the
# individual answers.
######################################################################
#
#  Produce the name for a named answer blank.
#  (When the singleResult option is true, use the standard name for the first
#  one, and create the prefixed names for the rest.)
#
#
#  Record an answer-blank name (when using extensions)
#
#
#  Produce an answer rule for the next item in the list,
#    taking care to use names or extensions as needed
#    by the settings of the MultiAnswer.
#
#
#  Do the same, but for answer arrays, which are generated by the
#    Value objects automatically sized to suit their data.
#    Reset the correct_ans once the array is made
#
######################################################################
```

---

### 📄 `parsers/parserPopUp.pl`
```perl
#
#  The package that implements pop-up menus
#
#
#  Set up the main:: namespace
#
#
#  Create a new PopUp object
#
#
#  Get the choices into the correct order (randomizing where requested)
#
#
#  Collect the labels and values
#
#
#  Find the correct choice in the ordered array
#
# Convert a value string into a numeric index.
#
#  Use the actual choice string (aka label) rather than the value string as the output
#
#
#  Adjust student preview and answer strings to be the actual
#  choice string rather than the value string.
#
#  Allow users to convert the value string into a label
#  Include the value string for the correct choice in the answer hash
#
#  Answer rule is the menu list
#
#
# DropDown() variant of PopUp() with placeholder
#
#
# TrueFalse() variant of PopUp()
#
##################################################
#
#  Replacement for Parser::String that takes the
#  complete parse string as its value
#
##################################################
```

---

### 📄 `parsers/parserPrime.pl`
```perl
##########################################
#
#  Package to enable and disable the prime operator
#
#
#  Add prime to the given or current context
#
#
#  Remove prime from the context
#
##########################################
#
#  Prime operator is a subclass of the unary operator class
#
#
#  Do a typecheck on the operand
#
#
#  A hack to prevent double-primes from inserting parentheses
#   in string and TeX output (change the precedence to hide it)
#
#
#  Produce a perl version of the derivative
#
#
#  Evaluate the derivative
#
#
#  Reduce by replacing with derivative
#
#
#  Handle derivative by taking derivative of a prime by taking
#  derivative of the prime's value (which is itself a derivative)
#
```

---

### 📄 `parsers/parserOneOf.pl`
```perl
######################################################################
#
#  Define the OneOf() creator function
#
#
#  Use Compute() to handle each of the entries so correct_ans will be set
#   for each entry
#
#
#  Return the type of the first entry (usually these will all be the same)
#
#
#  Try to match against all the entries, and if any one of them matches,
#  go with it.
#
#
#  Return the class for the first entry
#
#
#  Use the standard cmp_equal, not the list version, since
#  this acts as a single item not a list.
#
#
#  Check if the student value equals one of the ones in the correct-answer list
#  and return the result of that comparison if it is correct.
#  (FIXME: should this check all and return the highest score?)
#
#
#  Produce the correct answer by combining correct answers of the originals.
#
#
#  Produce the string version by making a comma separated list with " or " for the last comma
#
#
#  Produce the TeX version by making a comma separated list with " or " for the last comma
#
#
#  Produce a list of entries separated by $sep with $or as the final separator.
#  The entries are converted using the given $method of the entry.
#  If there is a format (or tex_format) flag, use that to format the list instead.
#
#
#  Make a list containing a formula object rather than a
#  formula returning a list.
#
```

---

### 📄 `parsers/parserImplicitPlane.pl`
```perl
##################################################
#
#  Define the subclass of Formula
#
#
#  We already know the vectors are non-zero, so check
#  if the equations are multiples of each other.
#
#
#  Only compare two equalities
#
#
#  We subclass BOP::equality so that we can give a warning about
#  things like 1 = 3
#
```

---

### 📄 `parsers/parserRadioMultiAnswer.pl`
```perl
# Convert a value string into a numeric index.
# Creates an answer evaluator to be passed to ANS() or an array with a label and answer
# evaluator to be passed to LABELED_ANS().  Any parameters are passed to the individual answer
# evaluators.  A default checker is supplied if one is not supplied by the problem author.  This
# checker returns 1 if the student selects the correct radio answer, and all answers in that
# part are equal to correct answers in that part.
# Check the answers.  First, call individual answer checkers to get any type-check errors.  Then
# perform the user's checker routine.  Finally collect the individual answers and errors and
# combine them for the single result.
# Return a given string or a default if it is empty or not defined
# Collect the correct and student answers, and call the user's checker routine.  If any of the
# answers in the selected part produced errors or the types don't match, don't call the user's
# routine.  Otherwise, call it, and if there was an error, report that.  Set the score from the
# supplied checker.
# The user's checker can call appendMessage(message) to add an error message.
# Produce the name for an answer blank.  (Use the standard name for the first one, and create
# the prefixed names for the rest.)
# Produce the label for a part of the radio answer.
# Produce the answer rule.
# Format a label.
# Start a radio button container.
# End a radio button container.
# Record an answer-blank name (when using extensions)
```

---

### 📄 `parsers/parserFormulaWithUnits.pl`
```perl
#
#  Now uses the version in Parser::Legacy::NumberWithUnits
#  to avoid duplication of common code.
#
```

---

### 📄 `parsers/parserAssignment.pl`
```perl
#
#  FIXME:  allow any variables in declaration
#  FIXME:  Add more hints when variable name isn't right
#          or function name or number of arguments isn't right.
#
######################################################################
#
#  Check that the left operand is a variable and not used on the right
#
#
#  Convert to an Assignment object
#
#
#  Don't count the left-hand variable
#
#
#  Create an Assignment object
#
#
# Display without unwanted parentheses
#
#
#  Add/Remove the Assignment operator to/from a context
#
######################################################################
#
#  A special List object that holds a variable and a value, and
#  that prints with an equal sign.
#
#
#  Mark assignments so that they are not treated as lists by classMatch()
#
#
#  Produce proper output
#
#
#  Needed since these are called explicitly without an object
#
#
#  Class is an a variable assigned to whatever
#
#
#  Return the proper type
#
######################################################################
#
#  A subclass of Formula that does typematching properly for Assignments
#  (the match is against the right-hand sides)
#
#
#  Convert varaible names to those used in the correct answer, if the
#  student answer uses different ones
#
######################################################################
#
#  A dummy function that is used for assignments like f(x) = x^2
#
```

---

## 🛠️ Advanced Modules, Graphics & Legacy

### 📄 `answers/PGfunctionevaluators.pl`
```perl
# Until we get the PG cacheing business sorted out, we need to use
# PG_restricted_eval to get the correct values for some(?) PG environment
# variables. We do this once here and place the values in lexicals for later
# access.
## The following answer evaluator for comparing multivarable functions was
## contributed by Professor William K. Ziemer
## (Note: most of the multivariable functionality provided by Professor Ziemer
## has now been integrated into fun_cmp and FUNCTION_CMP)
############################
# W.K. Ziemer, Sep. 1999
# Math Dept. CSULB
# email: wziemer@csulb.edu
############################
## LOW-LEVEL ROUTINE -- NOT NORMALLY FOR END USERS -- USE WITH CAUTION
## NOTE: PG_answer_eval	is used	instead	of PG_restricted_eval in order to insure that the answer
## evaluated within	the	context	of the package the problem was originally defined in.
## Includes multivariable modifications contributed by Professor William K. Ziemer
##
## IN:	a hash consisting of the following keys (error checking to be added later?)
##			correctEqn			--	the correct equation as a string
##			var				--	the variable name as a string,
##								or a reference to an array of variables
##			limits				--	reference to an array of arrays of type [lower,upper]
##			tolerance			--	the allowable margin of error
##			tolType				--	'relative' or 'absolute'
##			numPoints			--	the number of points to evaluate the function at
##			mode				--	'std' or 'antider'
##			maxConstantOfIntegration	--	maximum size of the constant of integration
##			zeroLevel			--	if the correct answer is this close to zero,
##												then zeroLevelTol applies
##			zeroLevelTol			--	absolute tolerance to allow when answer is close to zero
##			test_points			--	user supplied points to use for testing the
##                          function, either array of arrays, or optionally
##                          reference to single array (for one variable)
#
#  The original version, for backward compatibility
#  (can be removed when the Parser-based version is more fully tested.)
#
```

---

### 📄 `answers/PGnumericevaluators.pl`
```perl
# Until we get the PG cacheing business sorted out, we need to use
# PG_restricted_eval to get the correct values for some(?) PG environment
# variables. We do this once here and place the values in lexicals for later
# access.
#########################################################################
#########################################################################
#########################################################################
#########################################################################
#legacy code for compatability purposes
##	Similar	to std_num_cmp but accepts a list of numbers in	the	form
##	std_num_cmp_list(relpercentTol,format,ans1,ans2,ans3,...)
##	format is of the form "%10.3g" or "", i.e., a format suitable for sprintf(). Use "" for default
##	You	must enter a format	and	tolerance
##	See std_num_cmp_list for usage
##	See std_num_cmp_list for usage
##	See std_num_cmp_list for usage
##	See std_num_cmp_list for usage
##	See std_num_cmp_list for usage
##	See std_num_cmp_list for usage
##	See std_num_cmp_list for usage
## sub numerical_compare_with_units
## Compares a number with units
## Deprecated; use num_cmp()
##
## IN:	a string which includes the numerical answer and the units
##		a hash with the following keys (all optional):
##			mode		--	'std', 'frac', 'arith', or 'strict'
##			format		--	the format to use when displaying the answer
##			tol		--	an absolute tolerance, or
##			relTol		--	a relative tolerance
##			zeroLevel	--	if the correct answer is this close to zero, then zeroLevelTol applies
##			zeroLevelTol	--	absolute tolerance to allow when correct answer is close to zero
# This mode is depricated.  send input through num_cmp -- it can handle units.
#
#  The original version, for backward compatibility
#  (can be removed when the Parser-based version is more fully tested.)
#
###############################################################################
###############################################################################
```

---

### 📄 `answers/Generic.pl`
```perl
#From parserUtils.pl:
```

---

### 📄 `answers/answerCustom.pl`
```perl
#  Set this to include any default parameters you want
#  to include in the custom answer checkers
#  Set this to include any default parameters you want
#  to include in the custom answer checkers.
```

---

### 📄 `answers/PGstringevaluators.pl`
```perl
################################
## STRING ANSWER FILTERS
## IN:	--the string to be filtered
##		--a list of the filters to use
##
## OUT:	--the modified string
##
## Use this subroutine instead of the
## individual filters below it
## LOW-LEVEL ROUTINE -- NOT NORMALLY FOR END USERS -- USE WITH CAUTION
##
## IN:	a hashtable with the following entries (error-checking to be added later?):
##			correctAnswer	--	the correct answer, before filtering
##			filters			--	reference to an array containing the filters to be applied
##			type			--	a string containing the type of answer evaluator in use
## OUT:	a reference to an answer evaluator subroutine
```

---

### 📄 `answers/answerHints.pl`
```perl
#
#  Calls the answer checker on two values with a copy of the answer hash
#  and returns true if the two values match and false otherwise.
#
```

---

### 📄 `answers/weightedGrader.pl`
```perl
##################################################
#
#  Issue ANS() calls for the weighted checkers
#
##################################################
#
#  Issue NAMED_ANS() calls for the weighted checkers
#
##################################################
#
#  Issue an ANS() call for the checker, giving
#  credit to the given answers.
#
##################################################
#
#  Either add a weight to an AnswerEvaluator, or return a
#  new checker that adds the weight to its result.  Also,
#  add the "credit" field, if supplied.
#
##################################################
#
#  This is the weighted grader.  It uses an extra field added to the
#  AnswerHash (named "weight") to tell how much weight to give each
#  problem.  The grader adds up the total weights for the correct
#  answers.  For partially correct ones, it uses the score for that
#  answer to give a portion of that weight.  For example, if the
#  weight is 40 and the score for the answer is .5, then 20 is added
#  to the total for the problem.  (Note that most answer checkers only
#  return 1 or 0, but they are allowed to return partial credit as
#  well.)
#
#  When the student's total is computed, it is divided by the sum of
#  all the weights in order to determine the final score.
#
#  It also uses a special field called "credit" that determines
#  what other (named) answers are given full credit if the given
#  answer is correct.  This can be used to make "optional" answers,
#  where getting the "final" answer right gives credit for the other parts.
#
##################################################
#
#  Syntactic sugar to avoid ugly ~~& construct in PG.
#
```

---

### 📄 `answers/PGmiscevaluators.pl`
```perl
# added 6/14/2000 by David Etlinger
# because of the conversion of the answer
# string to an array, I thought it better not
# to force STR_CMP() to work with this
#added 2/26/2003 by Mike Gage
# handled the case where multiple answers are passed as an array reference
# rather than as a \0 delimited string.
#added 6/28/2000 by David Etlinger
#exactly the same as strict_str_cmp,
#but more intuitive to the user
# check that answer is really a string and not an array
# also use ordinary string compare
```

---

### 📄 `answers/extraAnswerEvaluators.pl`
```perl
# ^uses loadMacros
# ^package main
# ^function mode2context
# ^uses Parser::Context::getCopy
# ^uses %context
# ^uses $numZeroLevelTolDefault
# ^uses $numAbsTolDefault
# ^uses $numRelPercentTolDefault
# ^uses $numFormatDefault
# ^function interval_cmp
# ^uses Context
# ^uses mode2context
# ^uses List
# ^uses Union
# ^function number_list_cmp
# ^uses Context
# ^uses mode2context
# ^uses List
# ^function equation_cmp
# ^uses Equation_eval::equation_cmp
```

---

### 📄 `answers/unorderedAnswer.pl`
```perl
##########################################################################
#
#  Low-level routine for handling unordered collections of answer checkers
#
##################################################
#
#  AnswerChecker that allows a blank answer in a collection of unordered
#  answer checkers.  It will return "correct" for a blank answer only if
#  all the other answers are correct.  (The blankOK value is set by
#  unordered_answer_list when this is true.)  This lets you ask a question
#  where the number of answers is not known (by the student) ahead of time.
#
```

---

### 📄 `answers/PGasu.pl`
```perl
# ^function auto_right
# ^uses AnswerEvaluator::new
# ^uses auto_right_checker
# used in auto_right above
# ^function auto_right_checker
# ^function no_decs
# ^uses must_have_filter
# ^uses raw_student_answer_filter
# ^uses catch_errors_filter
# ^function must_include
# ^uses must_have_filter
# ^uses raw_student_answer_filter
# ^uses catch_errors_filter
# ^function no_trig_fun
# ^uses fun_cmp
# ^uses must_have_filter
# ^uses catch_errors_filter
# ^function no_trig
# ^uses num_cmp
# ^uses must_have_filter
# ^uses catch_errors_filter
# ^function exact_no_trig
# ^uses num_cmp
# ^uses no_decs
# ^uses must_have_filter
# First argument is the string to have, or not have
# Second argument is optional, and tells us whether yes or no
# Third argument is the error message to produce (if any).
# ^function must_have_filter
# ^function catch_errors_filter
# ^function raw_student_answer_filter
# ^function no_decimal_list
# ^uses number_list_cmp
# ^function no_decimals
# ^uses std_num_cmp
# ^function with_comments
# ^function pc_evaluator
# ^function weighted_partial_grader
# ^uses $ENV{grader_message}
# ^uses $ENV{partial_weights}
```

---

### 📄 `capa/PG_CAPAmacros.pl`
```perl
# these are very commonly needed files
#####################
```

---

### 📄 `ui/PGchoicemacros.pl`
```perl
# ^function new_match_list
# ^uses Match::new
# ^uses &std_print_q
# ^uses &std_print_a
# ^function new_select_list
# ^uses Select::new
# ^uses &std_print_q
# ^uses &std_print_a
# ^function new_pop_up_select_list
# ^uses Select::new
# ^uses &pop_up_list_print_q
# ^uses &std_print_a
# ^function new_multiple_choice
# ^uses Multiple::new
# ^uses &std_print_q
# ^uses &radio_print_a
# ^function new_checkbox_multiple_choice
# ^uses Multiple::new
# ^uses &std_print_q
# ^uses &checkbox_print_a
# ^function std_print_q
# ^function pop_up_list_print_q
# To put pop-up-list at the end of a question.
# contributed by Mark Schmitt 3-6-03
# ^function quest_first_pop_up_list_print_q
# To put pop-up-list in the middle of a question.
# contributed by Mark Schmitt 3-6-03
# ^function ans_in_middle_pop_up_list_print_q
# Units for physics class
# contributed by Mark Schmitt 3-6-03
# ^function units_list_print_q
#Standard method of printing answers in a matching list
# ^function std_print_a
#Alternate method of printing answers as a list of radio buttons for multiple choice
#Method for naming radio buttons is no longer round about and hackish
# ^function radio_print_a
# ^function checkbox_print_a
# ^function qa   [DEPRECATED]
# ^function invert   [DEPRECATED]
# ^function NchooseK   [DEPRECATED]
# ^function shuffle   [DEPRECATED]
# ^function match_questions_list   [DEPRECATED]
# ^function match_questions_list_varbox   [DEPRECATED]
```

---

### 📄 `ui/unionTables.pl`
```perl
# This could have been a variable,
# but all the other table commands are subroutines, so kept it
# one to be consistent.
```

---

### 📄 `ui/unionLists.pl`
```perl
######################################################################
##
##  Functions used to make <UL> and <OL> lists in HTML files
##  and corresponding lists in TeX mode.
##
##    BeginList()             starts a list
##    $ITEM                   start a list item
##    $ITEMSEP                puts spacing between items
##    EndList()               ends a list
##
##    BeginParList()          starts a list of paragraphs
##    EndParList()            ends such a list
##
#
#  Syntactic sugar for making lists of paragraphs
#
#
#  Use $ITEM to introduce a new list item
#
#
#  This is a hack for when you want MSIE to handle
#  space between list items properly
#
```

---

### 📄 `ui/choiceUtils.pl`
```perl
#
#  A replacement for std_print_q that uses tables to align the questions, so
#  that if a question wraps, it is properly indented.
#
```

---

### 📄 `ui/alignedChoice.pl`
```perl
######################################################################
#
#  Prints questions with the answer rule at the right, all aligned.
#  (for use by AlignedList object below)
#
######################################################################
#
#  Genarate a new AlignedList object
#
#     $al = new_aligned_list(options)
#
#  Where "options" can be taken from among:
#
#      valign => "placement"     Sets the vertical alignment for the table
#                                (default is valign => "MIDDLE")
#
#      align => "placement"      Sets the horizontal aligmnent for the first
#                                column of the table
#                                (default is align => "RIGHT")
#
#      spacing => n              Sets the CELLSPACING value for the table
#                                (default is spacing => 5)
#
#      tex_spacing => dimen      Extra spacing between rows
#                                (default is tex_spacing => "0pt")
#
#      numbered => 1 or 0        1 means the problems should be numbered.
#                                0 means no numbers for the problems.
#
#      equals => 1 or 0          1 means include a column of equal signs between
#                                  the questions and the answer blocks.
#                                0 means no column of equals.
#
#      ans_rule_len => n         Sets the length of the answer rule
#
#
```

---

### 📄 `ui/niceTables.pl`
```perl
# Make the outer table environment
# Takes the user's nested array and returns a cleaned up version with initializations
```

---

### 📄 `ui/pccTables.pl`
```perl
# This is just a redirect to niceTables.pl, which was originally called pccTables.pl
```

---

### 📄 `ui/quickMatrixEntry.pl`
```perl
# Allow promotion of Value::Matrix objects.
# Backwards compatibility. This is deprecated and should not be used.
```

---

### 📄 `ui/problemPanic.pl`
```perl
#
#  The packge to contain the routines and data for the Panic buttons
#
#
#  Allow resets for instructors.
#  Look up the panic level and reset it if needed.
#  Save the panic level for the next time through.
#
#
#  Place a panic button on the page, if it's not hardcopy mode and its not at the wrong level.
#  You can set the label, the penalty for taking this hint, and the panic level for this button.
#  Use submitAnswers if it is before the due date, and checkAnswers otherwise.
#
#
#  The reset button
#
#
#  Handle HTML in the value
#
#
#  Install the panic grader, saving the original one
#
#
#  The grader for the panic levels.
#
```

---

### 📄 `deprecated/hhAdditionalMacros.pl`
```perl
# additional macros developed in conjunction with the problems from
# the consortium (hughes-hallett) calculus text
#
# written by Gavin LaRose, <glarose@umich.edu>
# version 1.2
# 1.2: added reduced_frac()
# 1.1: added numorfun_cmp()
#
# shufflemap
# produces a reference to a hash of indices from 0 to n-1 pointing to
# a random permutation of the same, and the index that points to 0
#
# string_list_cmp
# check a comma-separated list of strings as student answers and
# check them with the standard str_cmp evaluator.  this is really
# John Jones' number_list_cmp rewritten to be do string comparison
#
# integrand_fun_cmp
# an answer evaluator that allows checking functions with 'dt' in them;
# redundant now that the Parser allows checking with multicharacter
# variables
#
# numfun_cmp
# an answer evaluator that requires that the answer be
# simplified to the number given without returning an error if
# it's a function
#
# numorfun_cmp
# an answer evaluator that first checks to see if the student answer
# checks correctly as a number, and if so returns that result; if not,
# repeats the check with a function checker and returns that.  options
# for the respective checkers are provided as separate hash references
#
# classify_cmp
# take a correct answer of the form "val=string, val=string.."
# and check a comma-separated list of student answers against these
# if the option 'order'=>'strict' is provided, requires that the
# answers be in the same order.  any other options are passed to
# num_cmp to check the val entries; strings are checked with a
# standard str_cmp
# doesn't currently allow for passing in of a reference to an array
# of solutions to generate a list of evaluators, but that would be
# easy to add
#
# integrand_fun_cmp
# an answer evaluator to allow checking functions with 'dt' in them
#
# numfun_cmp
# an answer evaluator that requires that the answer be
# simplified to the number given without returning an error if
# it's a function
#
# numorfun_cmp
# an answer evaluator that first checks to see if the student answer
# checks correctly as a number, and if so returns that result; if not,
# repeats the check with a function checker and returns that.
#
```

---

### 📄 `deprecated/unionProblem.pl`
```perl
##################################################
#
#  No longer needed since WW can output the grey
#  box automatically by changes in global.conf
#
```

---

### 📄 `deprecated/unionMacros.pl`
```perl
######################################################################
#
#  Some macros that add to the ones like $PAR, $BR, etc.
#
#
#  Shorthand for WeBWorK
#
#
#  HTML(htmlcode)
#  HTML(htmlcode,texcode)
#
#  Insert $html in HTML mode.  In TeX mode, insert nothing for the first form,
#  and $tex for the second form.
#
#
#  Begin and end indented text
#
#
#  Start and stop centering
#
#
#  Begin and end <TT> mode
#
#
#  Begin and end <SMALL> mode
#
#
#  Remove extra space in bold
#
#
#  tth doesn't seem to understand \colon
#
#
#  Alternatives to the standard WW versions of these
#
#
#  Common math sets
#
#
#  Superscripts and subscript (mostly for if you want answer
#  rules in these positions).
#
#
#  Browser-only BR
#
#
#  Broser-only \displaystyle
#
#
#  Provides a title to the problem
#
#
# A warning that we are using javaScript
#
#
#  Modify a polynomial to remove coeficients of 1, -1 and 0
#  The polynomial can be a multivariable one.  The parameters
#  following the formula itself are the names of the variables
#  for the formula.  Any number can be provided, and the default
#  is x, y, and z.  Variable names must be one character long,
#  and the formula really should be a polynomial, as the algorithm
#  for removing coefficients of 0 relies on that in an important way.
#
```

---

### 📄 `deprecated/CanvasObject.pl`
```perl
#! /usr/bin/perl -w
# sub stateAndDebugBoxes {  ## inserts both header text and object text
# 	#my $self = shift;
# 	my %options = @_;
#
#
# 	##########################
# 	# determine debug mode
# 	# debugMode can be turned on by setting it to 1 in either the applet definition or at insertAll time
# 	##########################
#
# 	my $debugMode = (defined($options{debug}) and $options{debug}>0) ? $options{debug} : 0;
# 	my $includeAnswerBox = (defined($options{includeAnswerBox}) and $options{includeAnswerBox}==1) ? 1 : 0;
# 	$debugMode = $debugMode || 0; #   $self->debugMode;
#     #$self->debugMode( $debugMode);
#
#
# 	my $reset_button = $options{reinitialize_button} || 0;
# 	warn qq! please change  "reset_button=>1" to "reinitialize_button=>1" in the applet->installAll() command \n! if defined($options{reset_button});
#
# 	##########################
# 	# Get data to be interpolated into the HTML code defined in this subroutine
# 	#
#     # This consists of the name of the applet and the names of the routines
#     # to get and set State of the applet (which is done every time the question page is refreshed
#     # and to get and set Config  which is the initial configuration the applet is placed in
#     # when the question is first viewed.  It is also the state which is returned to when the
#     # reset button is pressed.
# 	##########################
#
# 	# prepare html code for storing state
# 	my $appletName      = 'cv';        # $self->appletName;
# 	my $appletStateName = "${appletName}_state";   # the name of the hidden "answer" blank storing state FIXME -- use persistent data instead
# 	my $getState        = 'getPoints()'; # $self->getStateAlias;    # names of routines for this applet
# 	my $setState        = 'setPoints()'; # $self->setStateAlias;
# 	my $getConfig       = '';          # $self->getConfigAlias;
# 	my $setConfig       = '';          # $self->setConfigAlias;
#
# 	my $base64_initialState     = '';  # encode_base64($self->initialState);
# 	main::RECORD_FORM_LABEL($appletStateName);            #this insures that the state will be saved from one invocation to the next
# 	                                                      # FIXME -- with PGcore the persistant data mechanism can be used instead
#     my $answer_value = '<xml></xml>';
#
# 	##########################
# 	# implement the sticky answer mechanism for maintaining the applet state when the question page is refreshed
# 	# This is important for guest users for whom no permanent record of answers is recorded.
# 	##########################
#
#     if ( defined( ${$inputs_ref}{$appletStateName} ) and ${$main::inputs_ref}{$appletStateName} =~ /\S/ ) {
# 		$answer_value = ${$main::inputs_ref}{$appletStateName};
# 	} elsif ( defined( $main::rh_sticky_answers->{$appletStateName} )  ) {
# 	    warn "type of sticky answers is ", ref( $main::rh_sticky_answers->{$appletStateName} );
# 		$answer_value = shift( @{ $main::rh_sticky_answers->{$appletStateName} });
# 	}
# 	$answer_value =~ tr/\\$@`//d;   #`## make sure student answers cannot be interpolated by e.g. EV3
# 	$answer_value =~ s/\s+/ /g;     ## remove excessive whitespace from student answer
#
# 	##########################
# 	# insert a hidden answer blank to hold the applet's state
# 	# (debug =>1 makes it visible for debugging and provides debugging buttons)
# 	##########################
#
#
# 	##########################
# 	# Regularize the applet's state -- which could be in either XML format or in XML format encoded by base64
# 	# In rare cases it might be simple string -- protect against that by putting xml tags around the state
# 	# The result:
# 	# $base_64_encoded_answer_value -- a base64 encoded xml string
# 	# $decoded_answer_value         -- and xml string
# 	##########################
#
# 	my $base_64_encoded_answer_value;
# 	my $decoded_answer_value;
#  	$answer_value = '<xml></xml>'; #(defined( $answer_value) and $answer_value =~/\S/)? $answer_value : '<xml></xml>';
# 	if ( $answer_value =~/<XML|<?xml/i) {
# 		$base_64_encoded_answer_value = $answer_value;  #encode_base64($answer_value);  #FIXME
# 		$decoded_answer_value = $answer_value;
# 	} else {
#         $decoded_answer_value = $answer_value;  #    decode_base64($answer_value);
#  		if ( $decoded_answer_value =~/<XML|<?xml/i) {  # great, we've decoded the answer to obtain an xml string
#  			$base_64_encoded_answer_value = $answer_value;
#  		} else {    #WTF??  apparently we don't have XML tags
#  			$answer_value = "<xml>$answer_value</xml>";
#  			$base_64_encoded_answer_value = $answer_value; #  encode_base64($answer_value);
#  			$decoded_answer_value = $answer_value;
#  		}
# 	}
#   	$base_64_encoded_answer_value =~ s/\r|\n//g;    # get rid of line returns
#
# 	##########################
#     # Construct answer blank for storing state -- in both regular (answer blank hidden)
#     # and debug (answer blank displayed) modes.
# 	##########################
#
# 	##########################
#     # debug version of the applet state answerBox and controls (all displayed)
#     # stored in
#     # $debug_input_element
# 	##########################
#
#     my $debug_input_element  = qq!\n<textarea  rows="4" cols="80"
# 	   name = "$appletStateName" id = "$appletStateName">$decoded_answer_value</textarea><br/>!;
# 	if ($getState=~/\S/) {   # if getStateAlias is not an empty string
# 		$debug_input_element .= qq!
# 	        <input type="button"  value="$getState"
# 	               onClick="debugText='';
# 	                        ww_applet_list['$appletName'].getState();
# 	                        if (debugText) {alert(debugText)};"
# 	        >!;
# 	}
# 	if ($setState=~/\S/) {   # if setStateAlias is not an empty string
# 		$debug_input_element .= qq!
# 	        <input type="button"  value="$setState"
# 	               onClick="debugText='';
# 	                        ww_applet_list['$appletName'].setState();
# 	                        if (debugText) {alert(debugText)};"
# 	        >!;
# 	}
# 	if ($getConfig=~/\S/) {   # if getConfigAlias is not an empty string
# 		$debug_input_element .= qq!
# 	        <input type="button"  value="$getConfig"
# 	               onClick="debugText='';
# 	                        ww_applet_list['$appletName'].getConfig();
# 	                        if (debugText) {alert(debugText)};"
# 	        >!;
# 	}
# 	if ($setConfig=~/\S/) {   # if setConfigAlias is not an empty string
# 		$debug_input_element .= qq!
# 		    <input type="button"  value="$setConfig"
# 	               onClick="debugText='';
# 	                        ww_applet_list['$appletName'].setConfig();
# 	                        if (debugText) {alert(debugText)};"
#             >!;
#     }
#
# 	##########################
#     # Construct answerblank for storing state
#     # using either the debug version (defined above) or the non-debug version
#     # where the state variable is hidden and the definition is very simple
#     # stored in
#     # $state_input_element
# 	##########################
#
# 	my $state_input_element = ($debugMode) ? $debug_input_element :
# 	      qq!\n<input type="hidden" name = "$appletStateName" id = "$appletStateName"  value ="$base_64_encoded_answer_value">!;
#
# 	##########################
#     # Construct the reset button string (this is blank if the button is not to be displayed
#     # $reset_button_str
# 	##########################
#
#     my $reset_button_str = ($reset_button) ?
#             qq!<input type='submit' name='previewAnswers' id ='previewAnswers' value='return this question to its initial state'
#                  onClick="setAppletStateToRestart('$appletName')"><br/>!
#             : ''  ;
#
# 	##########################
# 	# Combine the state_input_button and the reset button into one string
# 	# $state_storage_html_code
# 	##########################
#
#
#     $state_storage_html_code = qq!<input type="hidden"  name="previous_$appletStateName" id = "previous_$appletStateName"  value = "$base_64_encoded_answer_value">!
#                               . $state_input_element. $reset_button_str
#                              ;
# 	##########################
# 	# Construct the answerBox (if it is requested).  This is a default input box for interacting
# 	# with the applet.  It is separate from maintaining state but it often contains similar data.
# 	# Additional answer boxes or buttons can be defined but they must be explicitly connected to
# 	# the applet with additional javaScript commands.
# 	# Result: $answerBox_code
# 	##########################
#
#     my $answerBox_code ='';
#     if ($includeAnswerBox) {
# 		if ($debugMode) {
#
# 			$answerBox_code = $main::BR . main::NAMED_ANS_RULE('answerBox', 50 );
# 			$answerBox_code .= qq!
# 							 <br/><input type="button" value="get Answer from applet" onClick="eval(ww_applet_list['$appletName'].submitActionScript )"/>
# 							 <br/>
# 							!;
# 		} else {
# 			$answerBox_code = main::NAMED_HIDDEN_ANS_RULE('answerBox', 50 );
# 		}
# 	}
#
# 	##########################
#     # insert header material
# 	##########################
# 	#main::HEADER_TEXT($self->insertHeader());
# 	# update the debug mode for this applet.
#     main::HEADER_TEXT(qq!<script> ww_applet_list["$appletName"].debugMode = $debugMode;\n</script>!);
#
# 	##########################
#     # Return HTML or TeX strings to be included in the body of the page
# 	##########################
#
#     return main::MODES(TeX=>' {\bf  applet } ',
#     #HTML=>$self->insertObject.$main::BR.$state_storage_html_code.$answerBox_code);
#      HTML=>$main::BR.$state_storage_html_code.$answerBox_code
#      );
#  }
```

---

### 📄 `deprecated/PGunion.pl`
```perl
#
#  Load most of the interesting code developed at Union.
#
```

---

### 📄 `deprecated/freemanMacros.pl`
```perl
#sam# copied from bkellMacros.pl -- no reason to maintain two macro files.
#sam# FIXME -- these should probably lose their "bkell_" prefixes.
# bkellMacros.pl
# Brian Kell <bkell@cse.unl.edu>
# Last updated 3:24 CDT, 24 Jun 2007
###############################################################################
# bkell_linear_simplify($a, $b)
#
# Returns a string representing $a*x+$b in simplified form, where "simplified"
# means something along the lines of the following:
#
#  a    b   output
# ---  ---  ------
#  0    0      0
#  1    1     x+1
# -1   -1    -x-1
# -1    5     5-x
#  2    0     2x
# -4    3    3-4x
# -4   -3    -4x-3
#
###############################################################################
# bkell_simplify_fraction($num, $denom)
#
# Simplifies the fraction $num/$denom; returns the list ($num, $denom).
#
###############################################################################
# bkell_simplify_fraction_string($num, $denom [, $flags])
#
# Returns a string like "$num/$denom" in simplified form. If the string $flags
# contains "+", then a leading "+" is included if the fraction is non-negative.
# If $flags contains "0", then a fraction with a value of 0 will cause the
# empty string to be returned. If $flags contains "1", then a fraction with a
# value of 1 or -1 will cause only the sign to be returned (or the empty
# string, if the fraction is non-negative and $flags does not contain "+"). If
# $flags contains "(", then parentheses will be placed around "$num/$denom"
# (the sign, if it exists, will be outside the parentheses); if $flags contains
# "[", then parentheses will be used only if a sign is used and the denominator
# is other than 1. A flag of "(" overrides "]". If $flags contains "f", then
# the string returned will be in the form "{$num \over $denom}" instead of the
# normal slashed version.
#
###############################################################################
# bkell_poly_term($coeff_num, $coeff_denom, $var [, "+"])
#
# Produces and simplifies a term of a polynomial of the general form
# "($coeff_num/$coeff_denom)$var". Handles special cases (such as $num==0,
# $denom==1, etc.). If the fourth argument is "+", then a leading "+" is
# included if the term is positive.
#
###############################################################################
# bkell_gcd($x, $y)
#
# Returns the greatest common divisor of $x and $y.
#
###############################################################################
# bkell_poly_eval($x, $a_n, ..., $a_0)
#
# Evaluates the polynomial a_n*x^n + ... + a_1*x + a_0 at the given value of x.
#
###############################################################################
# bkell_real_zeros_finder($a_n, ..., $a_0)
#
# Returns a list of numerical approximations of the zeros of the polynomial
# a_n*x^n + ... + a_1*x + a_0, in order from least to greatest.
#
# The possibility of overflow or underflow is ignored. Overflow is likely to be
# a bigger problem than underflow.
#
# Do not use this code to guide missiles or control nuclear power plants.
#
###############################################################################
# bkell_floor($x)
#
# Returns the floor of $x. Normally this would be done with POSIX::floor, but
# WeBWorK doesn't allow you to use standard modules like POSIX.
#
###############################################################################
# bkell_ceil($x)
#
# Returns the ceiling of $x.
#
###############################################################################
# bkell_sigfigs($x, $n)
#
# Returns a string containing $x rounded to $n significant figures.
#
###############################################################################
# bkell_125($x)
#
# Returns the value logarithmically nearest $x in the sequence
#     ..., -1000, -500, -200, -100, -50, -20, -10, -5, -2, -1, -0.5, -0.2,
#          -0.1, -0.05, -0.02, -0.01, ..., 0, ..., 0.01, 0.02, 0.05, 0.1,
#          0.2, 0.5, 1, 2, 5, 10, 20, 50, 100, 200, 500, 1000, ... .
#
###############################################################################
# bkell_list_random_selection($n, @list)
#
# Returns a selection of $n distinct elements of @list. This is like
# list_random_multi_uniq in freemanMacros.pl, except that this function will
# always return the elements in the same order as they appear in @list.
#
###############################################################################
# bkell_graph_axis($a, $b)
#
# Returns a list ($min, $max, $step), where $min <= $a, $max >= $b, $step is a
# power of 10, $min and $max are multiples of $step, abs($min) <= 9*$step, and
# abs($max) <= 9*$step. Useful for deciding bounds for the axis of a graph. For
# example, to make a graph axis that can handle values between $a and $b, call
# bkell_graph_axis, and then set the minimum value of the axis to $min and the
# maximum to $max, and put tick marks every $step units.
#
####################################################################### EOF ###
```

---

### 📄 `deprecated/PeriodicRerandomization.pl`
```perl
###########################
```

---

### 📄 `deprecated/unionMessages.pl`
```perl
######################################################################
#
#  How to say "infinity"
#
######################################################################
#
#  A message that can be included (within BEGIN_TEXT and END_TEXT)
#  to tell the student how to enter infinity and minus infinity.
#
######################################################################
#
#  A message to tell students how to enter "Does not exist".
#
######################################################################
#
#  A message to tell students how to enter unions and infinities
#
######################################################################
#
#  A message to tell students how to enter lists of intervals
#
######################################################################
#
#  A message for lists of unions
#
```

---

### 📄 `deprecated/unionUtils.pl`
```perl
######################################################################
##
##  These are some miscellaneous routines that may be useful.
##
#
#  Remove leading and trailing spaces
#
#
#  Check if a string is a number
#
#
#  names for numbers
#
#
#  A debugging routine that allows the "warn" function to print a variable that
#  contains HTML code properly
#
#
#  Make a named subroutine that returns the value of a function.  If
#  no parameters are passed to the function, the function's string
#  is returned.  (This will be obsolete when I finish the
#  new expression parser -- DPVC.)
#
#
#  A hack to pick display mode in HTML modes, but plain math mode
#  in TeX modes.  This makes fractions appear better in HTML mode,
#  without making it worse in TeX modes.  This is for use with
#  AlignedList objects.
#
```

---

### 📄 `deprecated/problemPreserveAnswers.pl`
```perl
######################################################################
```

---

### 📄 `deprecated/Dartmouthmacros.pl`
```perl
#!/usr/bin/perl
# this is equivalent to use strict, but can be used within the Safe compartment.
## Some local macros
## Want mod(a,b) but perl and int are flawed
## Fudge for roundoff error
## Compute the product of a scalar and a vector (scalar first)
## Compute the sum of two vectors
## Perl doesn't seem to have builtin array arithmetic
## Compute the difference of two vectors
## Compute the length of a vector
## Computes the dot product of two vectors (assumed of the same dimension)
## Compute the maximum value in a list
#sub max {
#    ## Put the paramters passed into an array of values
#    my @values = @_;
#
#    ## Initialize maximum value to first element
#    my $max = $values[0];
#
#    my $i;
#    for ($i=1; $i <= $#values; $i++)
#        {
#        if ($values[$i] > $max) {
#            $max = $values[$i];
#            }
#        }
#    return $max;
#}
## Compute the minimum value in a list
#sub min {
#    ## Put the paramters passed into an array of values
#    my @values = @_;
#
#    ## Initialize minimum value to first element
#    my $min = $values[0];
#
#    my $i;
#    for ($i=1; $i <= $#values; $i++)
#        {
#        if ($values[$i] < $min) {
#            $min = $values[$i];
#            }
#        }
#    return $min
#}
## clean_scalar_string is invoked to make expressions like "$a x" look
## better when $a = 0, -1, 1
## Usage:  clean_scalar_string(scalar, "quoted string");
## Example:  clean_scalar_string(-1,"\pi") returns "-\pi"
## Computes the greatest common divisor of two integers
## Example:  gcd(-300, 125) returns 25
## reduced_fraction takes a pair of integers $numerator, $denominator
## ($denominator != 0) and returns an array of two elements @fraction
## $fraction[0] is the reduced numerator; $fraction[1] the reduced
## denominator
## Puts the sign of the fraction, if negative, in the numerator
##
## Usage:  @fraction = reduced_fraction($numerator, $denominator)
##
## reduced numerator
## reduced denominator
## Given Cartesian coordinates x and y returns an
## array the zeroth element which is the radius
## and the first element which is the argument
## 0 <= theta < 2*pi
##
## Returns r=0 theta=0 for the origin
##
## Cylindarical coordinates from polar routine
## Spherical Coordinates from polar routine
##
```

---

### 📄 `deprecated/BrockPhysicsMacros.pl`
```perl
# this file defines all Brock-Physics-specific macros.
```

---

### 📄 `deprecated/compoundProblem.pl`
```perl
######################################################################
#
#  This package implements a method of handling multi-part problems
#  that show only a single part at any one time.  The students can
#  work on one part at a time, and then when they get it right (or
#  under other circumstances deterimed by the professor), they can
#  move on to the next part.  Students cannot return to earlier parts
#  once they have been completed.  The score for problem as a whole is
#  made up from the scores on the individual parts, and the relative
#  weighting of the various parts can be specified by the problem
#  author.
#
#  To use the compoundProblem library, use
#
#      loadMacros("compoundProblem.pl");
#
#  at the top of your file, and then create a compoundProblem object
#  via the command
#
#      $cp = new compoundProblem(options)
#
#  where '$cp' is the name of a variable that you will use to
#  refer to the compound problem, and 'options' can include:
#
#    parts => n                The number of parts in the problem.
#                                Default: 1
#
#    weights => [n1,...,nm]    The relative weights to give to each
#                              part in the problem.  For example,
#                                  weights => [2,1,1]
#                              would cause the first part to be worth 50%
#                              of the points (twice the amount for each of
#                              the other two), while the second and third
#                              part would be worth 25% each.  If weights
#                              are not supplied, the parts are weighted
#                              by the number of answer blanks in each part
#                              (and you must provide the total number of
#                              blanks in all the parts by supplying the
#                              totalAnswers option).
#
#    totalAnswers => n         The total number of answer blanks in all
#                              the parts put together (this is used when
#                              computing the per-part scores, if part
#                              weights are not provided).
#
#    saveAllAnswers => 0 or 1  Usually, the contents of named answer blanks
#                              from previous parts are made available to
#                              later parts using variables with the
#                              same name as the answer blank.  Setting
#                              saveAllAnswers to 1 will cause ALL answer
#                              blanks to be available (via variables
#                              like $AnSwEr1, and so on).
#                                 Default:  0
#
#    parserValues => 0 or 1    Determines whether the answers from previous
#                              parts are returned as MathObjects (like
#                              those returned from Real(), Vector(), etc)
#                              or as strings (the unparsed contents of the
#                              student answer).  If you intend to use the
#                              previous answers as numbers, for example,
#                              you would want to set this to 1 so that you
#                              would get the final result of any formula
#                              the student typed, rather than the formula
#                              itself as a character string.
#                                 Default:  0
#
#    nextVisible => type       Tells when the "go on to the next part" option
#                              is available to the student.  The possible
#                              types include:
#
#                                 'ifCorrect'   next is available only when
#                                               all the answers are correct.
#
#                                 'Always'      next is always available
#                                               (but remember that students
#                                               can't go back once they go
#                                               on.)
#
#                                 'Never'       next is never allowed (the
#                                               problem will control going
#                                               on to the next part itself).
#
#                                Default:  'ifCorrect'
#
#    nextStyle => type         Determines the style of "next" indicator to display
#                              (when it is available).  The type can be one of:
#
#                                 'CheckBox'    a checkbox that allows the students
#                                               to go on to the next part when they
#                                               submit their answers.
#
#                                 'Button'      a button that submits their answers
#                                               and goes on to the next part.
#
#                                 'Forced'      forces the student to go on to the
#                                               next part the next time they submit
#                                               answers.
#
#                                 'HTML'        allows you to provide an arbitrary
#                                               HTML string of your own.
#
#                                Default:  'Checkbox'
#
#    nextLabel => string       Specifies the string to use as the label for the checkbox,
#                              the name of the button, the text of the message indicating
#                              that the next submit will move to the next part, or the
#                              HTML string, depending on the setting of nextStyle above.
#
#    nextNoChange => 0 or 1    Since the students must submit their answers again to go on
#                              to the next part, it is possible for them to change their
#                              answers before they submit, and if nextVisible is 'ifCorrect'
#                              they might go on to the next without having correct answers
#                              stored.  This option lets you control whether the answers
#                              are checked against the previous ones before going on to the
#                              next part.  If the answers don't match, a warning is issued
#                              and they are not allowed to move on.
#                                Default:  1
#
#    allowReset => 0 or 1      Determines whether a "Go back to the first part" checkbox
#                              is provided on parts 2 and later.  This is intended for
#                              the professor during testing of the problem (otherwise
#                              it would be impossible to go back to earlier parts).
#                                Default:  0
#
#    resetLabel => string      The string used to label the reset checkbox.
#
#  Once you have created a compoundProblem object, you can use $cp->part to
#  determine the part that the student is working on, and use 'if' statements
#  to display the proper information for the given part.  The compoundProblem
#  object takes care of maintaining the data as the parts change.  (See the
#  compoundProblem.pg file for an example of a compound problem.)
#
#  In order to handle the scoring of the problem as a whole when only part is
#  showing, the compoundProblem object uses its own problem grader to manage
#  the scores, and calls your own grader from there.  The default is to use
#  the one that was installed before the compoundProblem object was created,
#  or avg_problem_grader if none was installed.  You can specify a different
#  one using the $cp->useGrader() method (see below).  It is important that
#  you NOT call install_problem_grader() yourself once you have created the
#  compoundProblem object, as that would disable the special grader, causing
#  the compound problem to fail to work properly.
#
#  You may call the following methods once you have a compoundProblem:
#
#    $cp->part                   Returns the part the student is working on.
#    $cp->part(n)                Sets the part to be part n, as long as the
#                                student has finished the preceeding parts.
#                                If not, the part is set to the highest
#                                one the student hasn't completed, and he
#                                can work up to the given part.  (The
#                                nextVisible option is set to 'ifCorrect' if
#                                it was 'Never' so that students can go on
#                                once they finish the earlier parts.)
#
#    $cp->useGrader(code_ref)    Supplies your own grader to use in
#                                place of the default one.  For example:
#                                  $cp->useGrader(~~&std_problem_grader);
#
#    $cp->score                  Returns the (weighted) score for this part.
#                                Note that this is the score shown at the bottom
#                                of the page on which the student pressed submit
#                                (not the score for the answers the student is
#                                submitting -- that is not available until
#                                after the body of the problem has been created).
#
#    $cp->scoreRaw               Returns the unweighted score for this part.
#
#    $cp->scoreOverall           Returns the overall score for the problem
#                                so far.
#
#    $cp->addAnswers(list)       Make additional answer blanks be available
#                                from one part to another.  E.g.,
#                                   $cp->addAnswers('AnSwEr1');
#                                would make the first unnamed blank be available
#                                in later parts as well.  (This command should
#                                be issued only when the part containing the
#                                given answer blank is displayed.)
#
#    $cp->nextCheckbox(label)    Returns the HTML string for the "go on to next
#                                part" checkbox so you can use it in the body of
#                                the problem if you wish.  This should not be
#                                inserted when the $displayMode is 'TeX'.  If the
#                                label is not given or is blank, the default label
#                                is used.
#
#    $cp->nextButton(label)      Returns the HTML string for the "go on to next
#                                part" button so you can use it in the body of
#                                the problem if you wish.  This should not be
#                                inserted when the $displayMode is 'TeX'.  If the
#                                label is not given or is blank, the default label
#                                is used.
#
#    $cp->nextForces(label)      Returns the HTML string for the forced "go on to
#                                next part" so you can use it in the body of
#                                the problem if you wish.  This should not be
#                                inserted when the $displayMode is 'TeX'.  If the
#                                label is not given or is blank, the default label
#                                is used.
#
#    $cp->reset                  Go back to part 1, clearing the answers
#                                and score.  (Best used when debugging problems.)
#
#    $cp->resetCheckbox(label)   Returns the HTML string for the reset checkbox
#                                so that you can provide one within the body
#                                of the problem if you wish.  This should not be
#                                inserted when the $displayMode is 'TeX'.  If the
#                                label is not given or is blank, the default label
#                                will be used.
#
######################################################################
#
#  The state data that is stored between invocations of
#  the problem.
#
#
#  Create a new instance of the compound Problem and initialize
#  it.  This includes reading the status from the previous
#  parts, defining the variables from the answers to previous parts,
#  and setting up the grader so that the current data can be saved.
#
#
#  Compute the total of the weights so that the parts can
#  be properly scaled.
#
#
#  Look up the status from the previous invocation
#  and see if we need to go on to the next part.
#
#
#  Initialize the current part by setting the ans_rule
#  count (so that later parts will get unique answer names),
#  installing the grader (to save the data), and setting
#  the variables for previous answers.
#
#
#  Look through the list of answer labels and set
#  the variables for them to be the associated student
#  answer.  Make it a Parser value if requested.
#  Record the value so that is will be available
#  again on the next invocation.
#
#
#  Look to see is any answers have changed on this
#  invocation of the problem.
#
#
#  Go on to the next part, updating the status
#  to include the data from the old part so that
#  it will be properly preserved when the next
#  part is showing.
#
######################################################################
#
#  Encode all the status information so that it can be
#  maintained as the student submits answers.  Since this
#  state information includes things like the score from
#  the previous parts, it is "encrypted" using a dumb
#  hex encoding (making it harder for a student to recognize
#  it as valuable data if they view the page source).
#
#
#  Decode the data and break it into the status hash.
#
#
#  Hex encoding is shifted by 10 to obfuscate it further.
#  (shouldn't be a problem since the status will be made of
#  printable characters, so they are all above ASCII 32)
#
#
#  Make sure the data can be properly preserved within
#  an HTML <INPUT TYPE="HIDDEN"> tag.
#
######################################################################
#
#  Set the grader for this part to the specified one.
#
#
#  Make additional answer blanks from the current part
#  be preserved for use in future parts.
#
#
#  Go back to part 1 and clear the answers and scores.
#
#
#  Return the HTML for the "Go back to part 1" checkbox.
#
#
#  Return the HTML for the "next part" checkbox.
#
#
#  Return the HTML for the "next part" button.
#
#
#  Return the HTML for when going to the next part is forced.
#
#
#  Return the raw HTML provided
#
######################################################################
#
#  Return the current part, or try to set the part to the given
#  part (returns the part actually set, which may be earlier if
#  the student didn't complete an earlier part).
#
#
#  Return the various scores
#
######################################################################
#
#  The custom grader that does the work of computing the scores
#  and saving the data.
#
```

---

### 📄 `deprecated/PGcomplexmacros.pl`
```perl
# export functions from Complex1.
# You need to add
#
#   sub i();
#
# to your problem in order to use expressions such as 1 +3*i;
# Without this prototype you would have to write 1+3*i();
# The prototype has to be defined at compile time.
# Complex1::display_format('cartesian');
# number format used frequently in strict prefilters
#########################################################################
########################################################################
# Output is text displaying the complex numver in "e to the i theta" form. The
# formats for the argument theta is determined by the option C<theta_format> and the
# format for the modulus is determined by the C<r_format> option.
#this basically just checks for "e^" which unfortunately will show something like (e^4)*i as a polar, this should be changed
## allows only for numbers of the form a+bi and ae^(bi), where a and b are strict numbers
## allows only for the form a + bi, where a and b are strict numbers
## allows only for the form ae^(bi), where a and b are strict numbers
#this subroutine mearly captures what is before and after the "e**" it does not verify that the "i" is there, or in the
#exponent this must eventually be addresed
# changes default to display as a polar
# this does not seem to be in use, so I'm commenting it out.  Mike Gage 6/27/05
# sub cplx_cmp2 {
####.............###########
# }
# this does not seem to be in use, so I'm commenting it out.  Mike Gage 6/27/05
# sub cplx_cmp_mult {
####.............###########
# }
# this does not seem to be in use, so I'm commenting it out.  Mike Gage 6/27/05
# sub answer_mult{
####.............###########
# }
#
# sub multi_cmp_old{
####.............###########
# }
# this does not seem to be in use, so I'm commenting it out.  Mike Gage 6/27/05
# sub mult_cmp{
####.............###########
# }
```

---

### 📄 `deprecated/CofIdaho_macros.pl`
```perl
###################################################################
# 1) Formats an expression without negative exponents
#    Thanks to John Jones at ASU for this macro.
###################################################################
# 2) Checks for units
###################################################################
# 3) Checks for rounded percents
###################################################################
# 4) Checks both sides of an equation model the word problem.
###################################################################
# 5) Checks both sides of an equation for the slope-intercept form of a line.
###################################################################
# 6) Checks for function notation in an equality.
###################################################################
# 7) Checks factors of polynomials.
# Note: Student's answers must be of the form: monomial(poly)...(poly) with
#    or without parentheses about the monomial.  The polynomial factors must
#    not contain any other grouping symbols and, in any case, only parenthesis
#    may be used.  This needs to be in the instructions for any set that uses
#    this macro (in the screenHeader.pg file).
# Note: "StrictFactoringEvaluator" requires leading negatives to be factored out.
#    This not may not work with all situations.  BE SURE TO CHANGE THIS FILE IF THE
#    FactoringEvaluator IS CHANGED!!
#---------For diagnosing problems--------------------------------------
#                $ans_hash->setKeys( 'ans_message' =>"FYI: Not checking correctly.
#                    AnswerHashScore: $ans_hash->{score} :
#                   Student: $#student_factors, $student_ans,
#                   Formatted: $format_student_ans,
#                   Student Factors: $student_factors[0], $student_factors[1],
#                   : Correct: $#factors, $factors[0], $factors[1],
#                   Number matched: $CorrectFactors");
#----------------------------------------------------------------------
###################################################################
# 8) Checks for simplified rational expressions.
# Note: Student's answers must be of the form: (poly)/(poly)
#
#---------For diagnosing problems--------------------------------------
#     $ans_hash->setKeys( 'ans_message' =>"FYI: Not checking correctly.
#                         Student: $student_num, $student_den,$student_ans;
#                         Answer: $num,$den,$ans");
#----------------------------------------------------------------------
###################################################################
#  9) Writes a fraction in reduced form.
#
###################################################################
# 10) Checks a list of equations.
#     Designed for checking a list of asymptotes
```

---

### 📄 `deprecated/unionInclude.pl`
```perl
######################################################################
#
#  Routines to make it easier to include additional PG files within
#  a given one.  These files don't have to be in the courseScripts
#  directory; rather, they are assumed to be relative to the directory
#  containing the calling PG file.
#
######################################################################
#
#  Usage:  includePGfile(name)
#
#  where name is the name of a PG file (relative to the directory
#  of the file containing this call).
#
######################################################################
#
#
#  Usage:  includeRandomProblem(file1,file2,...,fileN);
#
#  where the fileNs are the names of the files from which
#  to choose (relative to the directory of the file containing
#  this call).
#
#  To use this, make one PG file that include the call to this
#  random routine, and then include it the set definition file
#  as many times as you want (up to N times).  A different problem
#  will be included for each instance in the set definition file.
#
#
#  Legacy code no longer needed.  The included file can contain
#  BEGIN_INCLUSION(); and END_INCLUSION(); in place of DOCUMENT()
#  and ENDDOCUMENT(); calls.
#
######################################################################
#
#  This is a service routine for includeRandomProblem() above.
#  It an array of k numbers chosen from 0 to n-1, but preserves the
#  random seed so that the included problem won't be affected by
#  this function, and replaces it by the psvn, so that the list
#  produced will be the same each time it is called.
#
```

---

### 📄 `deprecated/problemRandomize.pl`
```perl
######################################################################
#
#  The state data that is stored between invocations of
#  the problem.
#
#
#  Cache original grader installer (so we can override it).
#
#
#  Create new problemRandomize object from user's data
#  and initialize it.
#
#
#  Look up the status from the previous invocation
#  and check to see if a rerandomization is requested
#
#
#  Initialize the current problem
#
#
#  Clear the answers and re-randomize the seed
#
##################################################
#
#  Return the HTML for the "re-randomize" checkbox.
#
#
#  Return the HTML for the "next part" button.
#
#
#  Return the HTML for the "problem seed" input box
#
#
#  Return the raw HTML provided
#
##################################################
#
#  Encode all the status information so that it can be
#  maintained as the student submits answers.  Since this
#  state information includes things like the score from
#  the previous parts, it is "encrypted" using a dumb
#  hex encoding (making it harder for a student to recognize
#  it as valuable data if they view the page source).
#
#
#  Decode the data and break it into the status hash.
#
#
#  Hex encoding is shifted by 10 to obfuscate it further.
#  (shouldn't be a problem since the status will be made of
#  printable characters, so they are all above ASCII 32)
#
#
#  Make sure the data can be properly preserved within
#  an HTML <INPUT TYPE="HIDDEN"> tag.
#
##################################################
#
#  Set the grader for this part to the specified one.
#
#
#  The custom grader that does the work of computing the scores
#  and saving the data.
#
#
#  Fake grader for when the problem is reset
#
```

---

### 📄 `deprecated/compoundProblem5.pl`
```perl
#
#  Set up some styles and the jQuery calls for opening and closing the scaffolds.
#
#
#  The Scaffoling package
#
#
#  Create a new Scaffold object
#
#
#  Access scores (grades).  These are set using
#  the PROCESS_ANSWERS method below.
#
#
#  Add answer evaluators to a section
#   If the section is already displayed ($section->{section_answers} exists),
#      Get the answer labels and add them to the scaffold and section
#   Otherwise we pick them up in the new_answers() call.
#
###########################################
#
#  Create a displayed section.
#    Pass it the name of the section and the contents,
#    or use [$name,options] or {name => ..., options}
#    as the first argument.
#
#  The "section" option defaults to the next section number.
#  The "iscorrect" option defaults to checking the answers
#    given in this section.
#  The "canshow" option defaults to checking if the user
#    is an instructor or if the answers in all
#    previous sections are correct.
#
#  The data for a section includes the section number and options,
#  plus the names of the answer checkers from the previous sections,
#  the names of the checkers for this section, and answer checker
#  count from before and after this section (used for highlighting
#  the results table), and the rendered text for the section.
#
#
#  Display a section using PGML rather than BEGIN_TEXT/END_TEXT notation
#
#
#  Return a boolean array where a 1 means that answer blank has
#  an answer evaluator assigned to it and 0 means not.
#
#
#  Get the names of any of the original answer blanks that now have
#  evaluators attached.
#
#
#  When all the sections have been created and the answers checked,
#  the sections are processed to tell if they should be opened or not
#  and what color they should be.
#
#
#  Process an answer check.
#   If the check is code, call it on the given section,
#   Otherwise (a string), evaluate it and die if there are errors.
#   return the result.
#
#
#  Call the answer evaluator on all answers, and record the scores
#  so that we can use them in iscorrect and canshow checks.
#
#
#  Run through the output looking for sections, processing each as it
#  is found, replacing the temporary identification line with the
#  final result of processing the section.  Keep track of the first
#  incorrect section so that it can be opened when the page is displayed.
#
#
#  Standard way of processing answers and sections,
#  leaving the usual one open.
#
#
#  Add CSS to dim the rows of the table that are not
#  in the open section.  (When a section is marked correct,
#  the next section will be opened, so the correct answers
#  will be dimmed, and the new section's blank rows will be
#  active.  That may be a downside to the dimming.)
#
#
#  Add a solution to a section.  The default section is the previously
#  defined one, but you can also specify a section to add to in the
#  options.
#
#
#  Add answers in the current section.
#
#
#  Service routine to check for whether all the answers in a section
#  are correct.  (Used as the default for the iscorrect option of a
#  section.)
#
#
#  Service routine to check for whether all the previous answers in a
#  section are correct, or whether the user is an instructor.  (Used
#  as the default for the canshow option of a section.)
#
#
#  Checks the scores to see if they are all correct (returns 1),
#  all are answered but at least one is wrong (returns 0), or
#  some are blank (returns undef).
#
#
#  Checks whether all the given answers are correct or not.
#  The arguments are either names of named answers blanks, or
#  numbers indicating the n-th unnamed answer blank.
#
#  This can be used in the iscorrect or canshow options for a
#  section in order to customize when it will be considered
#  correct or can be opened.
#
#
#  Opens the given sections so they are open when the page loads.
#
#
#  Syntactic sugar to make it easier to call these routines.  Note
#  that you can't use these if you want to have nested scaffolds, as
#  they rely on a global variable to store the active scaffold.
#
```

---

### 📄 `deprecated/answerUtils.pl`
```perl
##########################################################################
#
#  Utility routines for answer checkers
#
#########################################################################
#
#  Evaluate an answer checker with a given student answer.
#  (works with old- and new-style answer checkers)
#
#
#  Call an answer evaluator (works for new- and old-style checkers)
#
#
#  Clear the error condition for an answer evaluator
#
#
#  Get the answer hash for a given evaluator
#
#
#  Make error messages returned by answer checkers prettier
#
#
#  Return the string or a blank string (if it was not defined)
#
#
#  Check for preview mode
#
```

---

### 📄 `deprecated/Alfredmacros.pl`
```perl
# A group of macros used in the Alfred problem library.
# Given a point (x,y) this macro computes the angle with respect to x-axis. The angle will be between 0 and 2pi.
## Compute the max and min of an array of numbers
#This macro prevents students from double clicking in an answer box. This macro #is necessary for multiple integral problems where the answer box is typeset
#into the integration symbols.
#The problems that have the answer box in the limits must be displayed in JS
#math mode. This macro warns the user to use JS math mode if they are not.
#This subroutine includes the Strang's textbook into a problem, you have to
#feed it the chapter and section. It is assumed that the book is in the course
#directory and is labeled strangtextbook. The parameters are
#strang(chapter,section,(optional) section title.
#example \{&strang(16,5,"surface integrals")\}.
#Inserts a link to a trig table in the problem.
#example \{&trig_table()\}
#we will associate each student answer with a prime number, noting which student answer is in which blank. This allows us to make use of the fundamental theorem of arithmetic.
#at this point they don't have a matched set of blanks correct. look for a single function in each pair that is right. You have to make sure you only get one for each pair of answer blanks.
### To use the macros your problem must include unionTables.pl, and of course Alfredmacros.pl
### Table integral returns a string that can be included in a Table to output an integral whose upper and lower limits
### of integration can be answer blanks. There are several optional parameters:
### width  - change the width of the answer blanks. defaults to 3.
### lowerwidth  - change the width of the lower answer blank. defaults to width
### upperwidth  - change the width of the upper answer blank. defaults to width.
### upper - the uppper limit of integration, does not have to be an answer blank, defaults to answer blank with width "width"
### lower - the lower limit of integration, does not have to be an answer blank,  defaults to answer blank with width "width"
### limits - boolean, if 1 puts the limits of integration above and below the integral symbol, if 0 puts them after the integral symbol.
###          default is 1.
### Your code must include unionTables.pl, and of course Alfredmacros.pl
### An example:
###   \{BeginTable(center=>0).
###      Row([tableintegral(),
###      ],separation=>2).
###     EndTable();
###   \}
### which will print an integral with answer blank on the upper and lower limits with the default length of 3
###
### This example prints out a double integral, the first integral with answer blanks with width 10, the second integral
### has 0 for the lower limit of integration and an answer blank with width 5 for the upper limit of integration.
### The default limits of integratin are answer blanks with width 3, in this case the default width was overridden to 5
### and the default lower limit was changed to a zero.
###   \{BeginTable(center=>0).
###      Row([tableintegral(width=>10,limits=>'\(0\)'),tableintegral(width=>5,lower=>'\(0\)',limits=>0),
###      ],separation=>2).
###     EndTable();
###   \}
###  An example where the width of the upper and lower answer blanks have different widths.
###   \{BeginTable(center=>0).
###      Row([tableintegral(lowerwidth=>10,upperwidth=>1)
###      ],separation=>2).
###     EndTable();
###   \}
# a sum with answer blanks for the summation variable, lower limit, and upper limit
#\{ BeginTable(center=>0).
#     Row([tablesum(width=>10),
#     ],separation=>2).
#   EndTable();
#\}
# a sum with answer blanks for the upper and lower limits, and the summation variable is i
#\{ BeginTable(center=>0).
#     Row([tablesum(width=>10,sumvariable=>'i'),
#     ],separation=>2).
#   EndTable();
#\}
# a sum with answer blanks for the upper and lower limits, and summation variable is not used.
#\{ BeginTable(center=>0).
#     Row([tablesum(width=>10,usesumvariable=>0),
#     ],separation=>2).
#   EndTable();
#\}
# sum from n = 1 to infinity
#\{ BeginTable(center=>0).
#      Row([tablesum(sumvariable=>'\(n\)',lower=>'\(1\)', upper=>'\(\hskip 3pt\infty\)') ],separation=>2).
#   EndTable();
#\}
### Create a vertical bar with an upper and lower limit.
### Create a subscripted character
### Create a superscripted character
### A fraction
```

---

### 📄 `deprecated/answerDiscussion.pl`
```perl
######################################################################
#
#  This file implements discussion-based questions, where the student
#  can provide essay-style answers, and the professor can make comments
#  on those.  The student and professor can continue to respond to
#  either other, and so carry on a mathematical discussion.  The
#  discussion is private between the professor and student, with
#  each student carrying on a separate discussion with the professor.
#
#  The professor can view a list of the students in the class with links
#  to their discussions, and indications of how many new messages there
#  are in each.
#
#  The messages can contain mathematics by enclosing it with \(...\)
#  for in-line mathematics and \[...\] for display-mode math.  The
#  mathematics is entered in TeX format.  It is also possible to use
#  Parser strings that are like the ones students give in normal formula
#  answer blanks.  These are enclosed in `...` or ``...`` for in-line
#  and display modes.  For example `sin(x/(x+1))` would have the same
#  effect as \(\sin\!\left(\frac{x}{x+1}\right)\), but is somewhat easier
#  to read.  [FIXME: a more complete Context() needs to be provided
#  for this.]
#
#  To make discussions work properly, the professor must set up two files:
#  one called courseStudentList.pg and one called courseProfessorList.pg,
#  with the first containing a list of the userID's of the students in the
#  course and the second containing a list of the professor ID's.  Sample
#  files are provided that you can place in your course templates/macros
#  directory and edit to suit your needs.  Without these files, the
#  professor functions will not operate properly, though the students
#  could still create entries on their own.
#
#  To start a duscussion, simply assign answerDiscussion.pg to any homework
#  set.  That's it.  The professors can write messages that are visible
#  to all the students, so such a message could be used to provide the
#  starting question for a discussion, for example.  Or the problem could
#  be used by the student to keep a "math journal" for the course (you would
#  want to be sure to keep the homework set open for the whole course in
#  this case).
#
#  This code is currently considered experimental, and there are still features
#  the need to be added, but it gives a sense of what is possible.
#
######################################################################
######################################################################
#
#  The defaults for the discussion
#
##################################################
#
#  Create a new discussion object
#
##################################################
#
#  make it easier to access the TEXT command in main::
#
##################################################
#
#  True if the user is a professor
#
##################################################
#
#  Get the list of professors from the courseProfessorList.pg file.
#  (At some point this could be obtained from the database.)  We
#  fail silently if the file can't be read.
#
##################################################
#
#  Get the list of students from the courseStudentList.pg file.
#  (At some point this could be taken from the database.)
#
##################################################
#
#  Create a partial URL used for links that maintain the current data on the page.
#
##################################################
#
#  Look up the styles from the answerDiscussion.css file.
#  This can be overridden by putting a modified copy in
#  your course templates/macros directory.
#
##################################################
#
#  Build the list of entries based on the private
#  list in the student's directory, and the public
#  ones in the professors' directories.
#
##################################################
#
#  Determine which are new entries by comparing to the list
#  of entries that have been read.
#
##################################################
#
#  Get the number of new messages from a give student
#  (used in building the array of student messages
#  for the professor).
#
##################################################
#
#  Get the number of new messages from a give student
#  (used in building the array of student messages
#  for the professor).
#
##################################################
#
#  True if the given entry hasn't been read yet
#
##################################################
#
#  True if the user is the author of the given entry
#
##################################################
#
#  Get the formatted name and user from the entry
#  file name
#
##################################################
#
#  Find the currently selected entry based on the
#  current action and the state contained in the
#  form.
#
##################################################
#
#  Find the first (oldest) unread message
#
######################################################################
######################################################################
#
#  Initialize a discussion problem
#  (get the initial data and start the table that
#  holds the various windows)
#
##################################################
#
#  End the left column and start the right
#
##################################################
#
#  End the problem (and its associated table).
#
######################################################################
######################################################################
#
#  Draw the Composition text entry area.  Use the
#  correct wording for creating a new message
#  versus editing an old one.  Show the preview
#  box, if requested.
#
######################################################################
#
#  Draw the list of entries an dassociated buttons.
#  Mark the new ones as new, and highlight the
#  selected one.  Make sure the proper buttons
#  are active.
#
##################################################
#
#  Display an entry in its window, adding the
#  proper buttons, and showing the source code
#  if requested.  Record the fact that this
#  entry has been read.
#
##################################################
#
#  Save the entry that is being composed or edited.
#
##################################################
#
#  Delete an entry (if it is allowed).  First put
#  up a confirmation box, however.
#
##################################################
#
#  Start editing the selected entry.
#
######################################################################
######################################################################
#
#  Display the options panel
#
##################################################
#
#  Show the student array, with links to each student and
#  the number of new messages for each.
#
######################################################################
#
#  Show ALL the entries.
#
######################################################################
#
#  Hardcopy includes ALL the messages, nicely formatted.
#
######################################################################
#
#  Create the HTML for a panel, given the title, text and so on.
#
######################################################################
#
#  A custom grader that uses the message aread to hide the normal
#  preview/check/submit buttons (if these were marked via an ID in the
#  HTML code, we could use CSS to do this instead).
#
#
######################################################################
######################################################################
#
#  Look up a file and return its contents or an error message.
#
######################################################################
#
#  Perform the actual writing of the file, using a hack that
#  takes advantage of the fact that insertGraph() can write files
#  in the html/tmp/images directory.
#
#
#  The answerDiscussion object mimics the WWPlot object by defining draw(),
#  imageName(), and ext() methods.  These are used by insertGraph() to write
#  image files, and we can use that to write the data files that we need.
#
######################################################################
#
#  Append data to a file (here implemented as reading followed by
#  writing).
#
######################################################################
#
#  Get the (sanitized) file name for the temporary file
#
######################################################################
```

---

### 📄 `deprecated/compoundProblem2.pl`
```perl
#! /usr/bin/perl -w
#options {width:${width}px; margin:20px auto; text-align:right; color:#6600}
#options a {text-decoration:none; color:#9ac1c9}
#options a:hover {color:#033}
#acc {width:${width}px; list-style:none; color:#033; margin:0 auto 40px}
#acc h3 {width:${width-14}px; border:1px solid #9ac1c9; padding:6px 6px 8px; font-weight:bold; margin-top:5px; cursor:pointer; background:url(images/header.gif)}
#acc h3:hover {background-color:#ff0}
#acc .acc-section {overflow:hidden; background:#fff}
#acc .acc-content {width:${width-32}px; padding:15px; border:1px solid #9ac1c9; border-top:none; background:#fff}
#nested {width:425px; list-style:none; color:#033; margin-bottom:15px}
#nested h3 {width:411px; border:1px solid #9ac1c9; padding:6px 6px 8px; font-weight:bold; margin-top:5px; cursor:pointer; background:url(images/header.gif)}
#nested h3:hover {background:url(images/header_over.gif)}
#nested .acc-section {overflow:hidden; background:#fff}
#nested .acc-content {width:393px; padding:15px; border:1px solid #9ac1c9; border-top:none; background:#fff}
#nested .acc-selected {background:url(images/header_over.gif)}
###########################################
# FIXME   we will make a $cp object that keeps track of the part
```

---

### 📄 `deprecated/PGtextevaluators.pl`
```perl
# Until we get the PG cacheing business sorted out, we need to use
# PG_restricted_eval to get the correct values for some(?) PG environment
# variables. We do this once here and place the values in lexicals for later
# access.
# these	next three subroutines show how to modify	the	"store_ans_at()" answer
# evaluator	to add extra information before	storing	the	info
# They provide a good model	for	how	to tweak answer	evaluators in special cases.
#  This	is another example of how to modify	an	answer evaluator to	obtain
#  the desired behavior	in a special case.	Here the object	is to have
#  have	the	last answer	trigger	the	send_mail_to subroutine	which mails
#  all of the answers to the designated	address.
#  (This address must be listed	in PG_environment{'ALLOW_MAIL_TO'} or an error occurs.)
# Fix me?? why is the body hard wired to the string QUESTIONNAIRE_ANSWERS?
#### subroutines used in producing a questionnaire
#### these are at least	good models	for	other answers of this type
# my $QUESTIONNAIRE_ANSWERS='';	#  stores the answers until	it is time to send them
#  this must	be initialized before the answer evaluators	are	run
#  but that happens long	after all of the text in the problem is
#  evaluated.
# this is a	utility	script for cleaning	up the answer output for display in
#the answers.
```

---

### 📄 `deprecated/littleneck.pl`
```perl
#*****************************
#   Question mode variables
#*****************************
#********************************************
#   Set up a "generate new problem" button
#********************************************
#**********************************************************
#   Subroutine to reduce fractions
#   Input : Num, Denom
#   Output: Num, Denom, Wholenum (if != 0, = $num/$denom)
#
#   22Jul09 - Returned Wholenum < 0 if num or denom < 0
#**********************************************************
#
#**********************************************************
#   Subroutine to produce reduced display fraction
#   Input : Num($n), Denom($d)
#   Output: Num($n), Denom($d), Wholenum($w),Display($display)
#  calls reduce_fraction to get,
#   Output: Num($n), Denom($d), Wholenum($w),
#(if Wholenum > 0,$display = $w
#  else $Display=\(\frac{$n}{$d}\)
#**********************************************************
#
#
#
#
#**********************************************************
#   Subroutine to produce reduced display fraction
#   Input : Num($n), Denom($d)
#   Output: Display($display)
#  calls reduce_fraction to get,
#   Output: Num($n), Denom($d), Wholenum($w),
#(if Wholenum > 0,$display = $w
#  else $Display=\(\frac{$n}{$d}\)
#**********************************************************
#*******************************************************************************
#   sqrt_simplify(Num,Natnum,Radnum,Texstr,Error)
#
#   Description: Given a natural number, will find the greatest perfect square
#                that is a factor and use this to simplify the expression:
#                sqrt(number).
#   Input :
#     Num = Number whose sqrt is being taken
#
#   Output:
#     Natnum => Natural number portion of solution (= 1 if no perfect square
#               divides evenly)
#     Radnum => The value still inside the radical
#     Texstr => A LaTex string of the form "Natnum \sqrt{$Radnum}" to be used
#               for displaying the solution.
#     Error  => If == 1, then the number entered was bad (ie, negative, nonint)
#               (If necessary, this code can be made specific for the error)
#*******************************************************************************
```

---

### 📄 `deprecated/PGcomplexmacros2.pl`
```perl
# This file     is PGcomplexmacros2.pl
# This includes the subroutines for the ANS macros, that
# is, macros allowing a more flexible answer checking
### for handling multivalued functions of a complex variable
###### subroutines ###########
# compares (z1 to z2 mod 4pi/3)
##### end subroutines ##################
```

---

### 📄 `deprecated/MUHelp.pl`
```perl
## Append .helpLink("exponents","Click here for further help.") to a string to add a help link.
```

---

### 📄 `misc/PCCmacros.pl`
```perl
###############################
#Name: perlround
#Input: a number to round, then a place to round to. e.g. 2=>hundredths, 0=>whole, -1=>tens
#Output: $x rounded to the $n place. This attempts to overcome quirks with rounding when the cut part is like 0.005
################################
###############################
#Name: RandomName
#Input: None required
#Optional Input: 'sex' => male or female
#Output: A name that is randomly chosen from the list maintained here.
#   If 'sex' is specified, the name is from the list of that sex.
################################
###############################
#
# Name: RandomVariableName
#
# Input: None required
#
# Optional Input: 'type' => variable, constant, integer, or function
#
# Output: A variable name like x, y, t, c, etc. that is randomly chosen from the list maintained here.
#         If 'type' is specified, the name is from the list of that type.
#
# Sample use:
################################
###############################
#
# Name: xPower
#
# This is just an auxiliary subroutine for the polynomial macros that follow
#
################################
###############################
#
# Name: PolyString
#
# Input: an arrays
#
#  PolyString(~~@poly1)
#
# Arrays elements should be numerical or Math Objects. The idea is that
# these are coefficients of a polynomial, either starting from the
# constant term or from the leading term.
#
# Optional Input: order=>ascending or descending, defaults to descending
#   order is ignored if output=>array
# Optional Input: var=> some string, defaulting to "x"
#
# Output: an polynomial string using var and ready to be fed to Compute
#
#         For example, given
#
#             @poly1 = (1,2);  # represents x+2
#             @poly2 = (3,-1,0,4);
#
#         PolyString(~~@poly1);
#
#             'x^1+2x^0'
#
#         PolyString(~~@poly2,order=>ascending,var=>'z');
#
#             '3x^0+-1x^1+0x^2+4x^3'
#
#         Note that instance of +-, x^0, x^1, 0x^n, may be present,
#         but Math Objectification will handle that.
#
# Note: If you intend to feed the output string to Compute() or Formula(),
#  you should set the context reductions appropriately and apply ->reduce
#  *twice* to remove excess parentheses from negative coefficients.
#
################################
###############################
#
# Name: PolyMult
#
# Input: two arrays, for example
#
#  PolyMult(~~@poly1, ~~@poly2)
#
# Arrays elements should be numerical or Math Objects
# where multiplication and addition are allowed. The idea is that
# these are coefficients of a polynomial, either starting from the
# constant term or from the leading term.
#
# Optional Input: order=>ascending or descending, defaults to descending
#   order is ignored if output=>array
# Optional Input: var=> some string, defaulting to "x"
# Optional Input: output=>array, simplified, unsimplified
#   which is either an array of coefficients, an expanded and simplified
#   polynomial string using var and ready to be fed to Compute, or the same
#   but unsimplified. Default is array.
# cmh, 6/18/13
# Optional Input: exponentVar=> some string, defaulting to ''
#   to be used if the polynomial looks like, for example
#            x^{3n}+x^{2n}+x^{n}
#
# Output: described in Optional Input
#
#         For example, given
#
#             @poly1 = (1,2);  # represents x+2
#             @poly2 = (3,-1,4);  # represents 3x^2-x+4
#
#         PolyMult(~~@poly1, ~~@poly2,
#             order=>ascending, var=>'z', output=>unsimplified)
#
#             '3z^3+-1z^2+4z+6z^2+-2z^1+8z^0'
#
#         Note that instance of +- may be present, but Math Objectification
#         will handle that.
#
#
#         Given
#
#           @poly1 = (Fraction(1,3),2);  # represents 1/3x+2
#           @poly2 = (Fraction(1,2),Fraction(-1,3));  # represents 1/2x-1/3
#
#         PolyMult(~~@poly1, ~~@poly2)
#
#             (Frac(1,6),Frac(8,9),Frac(-1,9))
#
#
# Note: If you intend to feed the output string to Compute() or Formula(),
#  you should set the context reductions appropriately and apply ->reduce
#  *twice* to remove excess parentheses from negative coefficients.
#
################################
#
# Accepts an array of the form that PolyTerms outputs
# Inserts '&' between array entries for use in array environments
# Converts Math Object entries to their TeX form
# Inserts a spacing command after nonempty entries - the command
#   \setlength\arraycolsep{0em} should precede the \begin{array}
# $Spacing should be something like "\hspace{0.4em}"
# Also creates an alignment string for the \begin{array} command
# $align should be "r", "c", or "l"
# Not part of PGpolynomialMacros.pl
#
# PolyTerms(~~@coefficientArray,x,order)
#
# Accepts an array containing the coefficients of a polynomial
#   in descending order
# Assumes coefficients have numerical values, but may be Math Objects
# Returns an array of size 2n-1 of the form
#   (a_nx^n,  +/-,  |a_{n-1}| x^{n-1},  +/-,  ...)
#   where the variable is x is the second argument, the terms are Math Objects
#   Formulas, and the +/- are Perl strings.
# The third argument can be "ascending" to reverse the order
# If a_j is 0, then the corresponding term and preceding sign are empty
#   strings.
# Trims beginning and ending, so that first and last terms are nonzero
# Not part of PGpolynomialMacros.pl
#
#=cut
###############################
# Name: PolySub
###############################
# Name: PolyAdd
#
# Input: two arrays, for example
#
#  PolyAdd(~~@poly1, ~~@poly2)
#
# Arrays elements should be numerical or Math Objects
# where addition are allowed. The idea is that
# these are coefficients of a polynomial, either starting from the
# constant term or from the leading term.
#
# Optional Input: order=>ascending or descending, defaults to descending
#   order is ignored if output=>array
# Optional Input: var=> some string, defaulting to "x"
# Optional Input: subtract=> 1 will subtract; default 0
# Optional Input: output=>array, simplified, unsimplified
#   which is either an array of coefficients, a simplified
#   polynomial string using var and ready to be fed to Compute, or the same
#   but unsimplified with like terms near each other. Default is array.
#
# Output: described in Optional Input
#
#         For example, given
#
#             @poly1 = (1,2);  # represents x+2 (assuming descending)
#             @poly2 = (3,-1,4);  # represents 3x^2-x+4
#
#         PolyAdd(~~@poly1, ~~@poly2,var=>'z', output=>unsimplified)
#
#             '3z^2+1z+-1z+2+4'
#
#         Note that instance of +- may be present, but Math Objectification
#         will handle that.
#
#
#         Given
#
#           @poly1 = (Fraction(1,3),2);  # represents 1/3+2x (assuming ascending)
#           @poly2 = (Fraction(1,2),0,Fraction(-1,3));
#
#         PolyAdd(~~@poly1, ~~@poly2,order=>ascending)
#
#             (Frac(5,6),2,Frac(-1,3))
#
#
# Note: If you intend to feed the output string to Compute() or Formula(),
#  you should set the context reductions appropriately and apply ->reduce
#  *twice* to remove excess parentheses from negative coefficients.
#
################################
###############################
# Name: numberWord
#
# Input: either a whole number <100 or a fraction with numerator and denominator less than 100. If fraction, set denominator parameter.
# Optional Input: capital => 1 (default is 0)
# Optional Input: denominator=> 4 (default is 1)
#  numberWord($n)
#
# Output: a string spelling that number
#
################################
# radicalListCheck
#
# Used when multiple answers are needed (e.g for quadratic) equations
# that may or may *not* contain radicals.
#
# Sample use:
#
#         ANS($ans->cmp(limits => [1,2],list_checker => ~~&radicalListCheck));
#
#
#in line below, correct_ans seems the right thing to do. In some problems, this is blank, so I'm just going with correct_value
# for those problems. But changing to correct_value broke other problems... so the conditional hack
# Keyboard instructions should only be displayed in HTML output
```

---

### 📄 `graph/PGtikz.pl`
```perl
# Not much needs to be done here except flag this as needing the tikz environment wrapper.
# The real work is done in LaTeXImage.pm.
```

---

### 📄 `graph/PGlateximage.pl`
```perl
# Not much needs to be done here.
# The real work is done in LaTeXImage.pm.
```

---

### 📄 `graph/LiveGraphics3D.pl`
```perl
# Syntactic sugar to make it easier to pass files and data to LiveGraphics3D.
# Syntactic sugar to make it easier to pass raw Graohics3D data to LiveGraphics3D.
# A message you can use for a caption under a graph.
```

---

### 📄 `graph/PGnauGraphics.pl`
```perl
# loadMacros('PGunion.pl');
######################################
#Name: Plot
#Input: Graphical object
#Optional Input: tex_size => n: control size of tex output.  n = 10*percentage of page (i.e. 200 = 20% of page)
#				note that in single column, the images are twice as big, so 200 = 40% of page
#		 single => 0,1: turn on or off single column display which makes pictures fit (default = 0)
#Output: An image with appropriate width and height of the graphical object
######################################
######################################
#Name: checkbox_table
#Input: [values list], [answer list i.e. 1,0,1,0]
#Optional Input: border => n - width of border in table (default = 0)
#		 tex_size => n - control size of tex output for pictures (defualt = 10 * 95 / # of columns)
#		 geometry =>[r,c] -  the number of rows and columns desired in the table (default = 2,2)
#		 labels => [@list] - a list of labels that appear beside the checkboxes. (default is blank)
#		 [..] - other answer lists, included as many as desired.  Note the lists must use the same
#			  values as the others and answer lists must be in the same basic order.
#Output: A table to be displayed and the answer evaluator.
#	    The table should be placed between BEGIN_TEXT and END_TEXT.
#	    The evaluator should be placed after END_TEXT by itself.
######################################
######################################
#Name: radio_table
#Input: [values list], [answer list i.e. 1,0,1,0]
#Optional Input: border => n - width of border in table (default = 0)
#		 tex_size => n - control size of tex output for pictures (defualt = 10 * 95 / # of columns)
#		 geometry =>[r,c] -  the number of rows and columns desired in the table (default = 2,2)
#		 labels => [@list] - a list of labels that appear beside the radio buttons. (default is blank)
#		 [..] - other answer lists, included as many as desired.  Note the lists must use the same
#			  values as the others and answer lists must be in the same basic order.
#Output: A table to be displayed and the answer evaluator.
#	    The table should be placed between BEGIN_TEXT and END_TEXT.
#	    The evaluator should be placed after END_TEXT by itself.
######################################
```

---

### 📄 `graph/AppletObjects.pl`
```perl
# Add basic functionality to the header of the question
# Deprecated applets (these are just stubs to show a warning if used)
# Inserts both header text and object text.
# GeogebraWeb APPLET PACKAGE
```

---

### 📄 `graph/plotly3D.pl`
```perl
# Base plot class
# Takes a pseudo function string and replaces with JavaScript functions.
# JavaScript Functions Output
# plotly3D surface plots
# plotly3D curve plots
```

---

### 📄 `graph/imageChoice.pl`
```perl
#  Create a match list where the answers are images
#  Usage:  $ml = new_image_match_list(options);
#  where options are those that can be supplied to image_print_a below.
#  The answers should be an image name or reference to a plot object
#  (or a reference to a pair of either of these), and they are passed
#  to the Image function for processing.  See unionUtils.pl for more
#  information on how these are handled.
#  A print routine for image matching.  This is designed to display
#  four graphs per row.  More can be included by setting the ImageOptions
#  variable in the match list.  For example:
#      $ml->{ImageOptions} = [size => [100,100]]
#  You can include the following options:
#    size => [w,h]      the width and height of the images
#    width => n         the width of the images (obsolete)
#    height => n        the height of the images (obsolete)
#    tex_size => n      the size for the TeX version of the image
#    separation => n    the spacing between the images in a row
#    vseparation => n   the spacing between the images and captions
#    link => 0 or 1     1 to make a link to the original image
#    columns => n       the number of images in each row (defaults to 4)
#    border => n        the width of the image border
```

---

### 📄 `graph/PCCgraphMacros.pl`
```perl
###############################
#Some standard values
################################
###############################
#Name: NiceGraphParameters
#Input: References to two arrays: one with all the x "action" in a graph, the other with the y "action"
#Optional Input: centerOrigin, centerXaxis, centerYaxis, buffer, roughTickNum, roughTickNumX, roughTickNumY
#Output: A reference to an array (xmin, xmax, ymin, ymax, xticknumber, yticknumber). These parameters will make a nice looking scale for a graph that captures all of the x and y data.
################################
```

---

### 📄 `graph/unionImage.pl`
```perl
######################################################################
#
#  A routine to make including images easier to control
#
#  Usage:  Image(name,options)
#
#  where name is the name of an image file or a reference to a
#  graphics object (or a reference to a pair of one of these),
#  and options are taken from among the following:
#
#    size => [w,h]           the size of the image in the HTML page
#                            (default is [150,150])
#
#    tex_size => r           the size to use in TeX mode (as a percentage
#                            of the line width times 10).  E.g., 500 is
#                            half the width, etc.  (default is 200.)
#
#    link => 0 or 1          whether to include a link to the original
#                            image (default is 0, unless there are
#                            two images given)
#
#    border => 0 or 1        size of image border in HTML mode
#                            (defaults to 2 or 1 depending on whether
#                            there is a link or not)
#
#    align => placement      vertical alignment for image in HTML mode
#                            (default is "BOTTOM")
#
#    tex_center => 0 or 1    whether to center the image horizontally
#                            in TeX mode  (default is 0)
#
#  The image name can be one of a number of different things.  It can be
#  the name of an image file, or an alias to one produce by the alias()
#  command.  It can be a graphics object reference created by init_graph().
#  Or it can be a pair of these (in square brackets).  The first is the
#  image for the HTML file, and the second is the image that it will be
#  linked to.
#
#  Examples:  Image("graph.gif", size => [200,200]);
#             Image(["graph.gif","graph-large.gif"]);
#
#  The alias() and insertGraph() functions will be called automatically
#  when needed.
#
```

---

### 📄 `math/algebraMacros.pl`
```perl
# by Dick Lane  http://webwork.maa.org/moodle/mod/forum/discuss.php?d=2286
# you can call these when checking answers like this:
#
# ANS( $f->cmp( checker => ~~&modChecker ) );
# make sure the external variables are available; for instance, in order to use
# the modChecker subroutine, you must have the variable $modulus defined in
# your problem
###############################################################################
# modChecker
###############################################################################
#	Type: 		checker
#	Used in:	RingsDefinition3.pg
#				RingsDefinition4.pg
#				RingsDefinition5.pg
#				RingsDefinition7.pg
#				RingsQuotientPolynomial3.pg
#				RingsQuotientPolynomial4.pg
#				RingsIdealsHomomorphisms2.pg
#	Purpose: 	Compare the student's answer (a number) to the correct
#				answer (a number), modulo $modulus
#	External variables:
#				$modulus
#	Comment:	This checker is defined in algebraMacros.pl because it's used
#				in so many problems
###############################################################################
###############################################################################
###############################################################################
# checkCycles
###############################################################################
#	Type:		checker
#	Used in:	Permutations1.pg
#				Permutations2.pg
#				Permutations5.pg
#				Permutations6.pg
#	Purpose:	Compare a student's cycle to a correct cycle, see if they
#				represent the same permutation (i.e. ( 1 2 3 ) = ( 2 3 1 ) )
#	External variables:
#	Comment:	This checker is defined in algebraMacros.pl because it's used
#				in so many problems
###############################################################################
###############################################################################
###############################################################################
# checkListOfTranspositions
###############################################################################
#	Type:		checker
#	Used in:	Permutations4.pg
#				Permutations8.pg
#	Purpose:	Compare a student's sequence of transpositions to a correct
#				sequence of transpositions, see if they	represent the same
#				permutation
#	External variables:
#				@x - list of elements in the set on which permutations are
#				defined
#	Comment:	This checker is defined in algebraMacros.pl because it's used
#				in so many problems
###############################################################################
```

---

### 📄 `math/MatrixReduce.pl`
```perl
# Observation: a randomly generated 3 x 4 matrix has a very high probability
# of having rank 3.  So, trying to generate random 3 x 4 matrices until a
# matrix of rank < 3 appears would be a bad idea.  Also, there is no
# guarantee that a randomly generated matrix will represent a consistent
# system; however, empirical evidence suggests that the majority of the
# time a random 3 x 4 matrix is produced, it is rank 3 and represents
# a consistent system.  Also, with randomly chosen matrices, it is
# possible to get rows or columns of zeros, so watch out!
#  rref: input and output are MathObject matrices.
#  Should be run in Fraction context for best results.
#  This was written by Davide Cervone.
#  http://webwork.maa.org/moodle/mod/forum/discuss.php?d=2970
```

---

### 📄 `math/SI_property_tables.pl`
```perl
# SI_property_tables.pl
# Rename this file (with .pl extension) and place it in your course macros directory,
#######################################################
#######################################################
###                                                 ###
###   below are the lists of the tabulated values   ###
###                                                 ###
#######################################################
#######################################################
###########################
###                     ###
###   saturated water   ###
###                     ###
###########################
###############
###         ###
###   air   ###
###         ###
###############
#############################
###                       ###
###   superheated water   ###
###                       ###
#############################
####             ####
####   0.1 MPa   ####
####             ####
####             ####
####   1.2 MPa   ####
####             ####
####             ####
####   1.4 MPa   ####
####             ####
####             ####
####   1.6 MPa   ####
####             ####
####             ####
####   1.8 MPa   ####
####             ####
####             ####
####   10 MPa    ####
####             ####
############################
###                      ###
###   saturated R-134a   ###
###                      ###
############################
##############################
###                        ###
###   superheated R-134a   ###
###                        ###
##############################
####              ####
####   0.7 MPa    ####
####              ####
####              ####
####   0.8 MPa    ####
####              ####
####              ####
####   0.9 MPa    ####
####              ####
####              ####
####   1.2 MPa    ####
####              ####
```

---

### 📄 `math/PGpolynomialmacros.pl`
```perl
#
# Takes two arrays of polynomial coefficients representing
# two polynomials and returns their sum.
#
#
# Takes two arrays of polynomial coefficients representing
# two polynomials and returns their difference.
#
#
# Accepts two arrays containing coefficients in descending order
# returns an array with the coefficients of the product
#
#
# Performs synthetic division on two polynomials returning
# the quotient and remainder in an array.
#
#
# Performs long division on two polynomials
# returning the quotient and remainder
#
#
# Accepts a reference to an array containing the coefficients, in descending
#   order, of a polynomial.
#
# Returns the lowest positive integral upper bound to the roots of the
#   polynomial.
#
#
# Accepts a reference to an array containing the coefficients, in descending
#   order, of a polynomial.
#
# Returns the greatest negative integral lower bound to the roots of the
#   polynomial
#
#
# Accepts an array containing the coefficients of a polynomial
#   in descending order
# Returns a sting containing the polynomial with variable x
# Default variable is x
#
#
# Accepts an array containing the coefficients, in descending order, of a
#  polynomial
# Returns the maximum number of positive and negative roots according to
#  Descartes Rule of Signs
#
# IMPORTANT NOTE:  this function currently does not accept coefficients of
#  zero.
#
```

---

### 📄 `math/tableau.pl`
```perl
##### From gage_matrix_ops
# 2014_HKUST_demo/templates/setSequentialWordProblem/bill_and_steve.pg:"gage_matrix_ops.pl",
# loadMacros("tableau_main_subroutines.pl");
#	$foochecker =  $constraints->cmp()->withPostFilter(
# 		linebreak_at_commas()
# 	);
# lop_display($tableau, align=>'cccc|cc|c|c', toplevel=>[qw(x1,x2,x3,x4,s1,s2,P,b)])
# 	Pretty prints the output of a matrix as a LOP with separating labels and
# 	variable labels.
# for main section of tableau.pl
# make one phase2 pivot on a tableau (works in place)
# returns flag with '', 'optimum' or 'unbounded'
#iteratively phase2 pivots a feasible tableau until the
# flag returns 'optimum' or 'unbounded'
# tableau is returned in a "stopped" state.
# make one phase 1 pivot on a tableau (works in place)
# returns flag with '', 'infeasible_lop' or 'feasible_point'
# perhaps 'feasible_point' should be 'feasible_lop'
########################
##############
# get_tableau_variable_values is
# deprecated for tableaus - use $tableau->statevars instead
#
# It calculates the values of the basis variables of the tableau,
# assuming the parameter variables are 0.
#
# Usage:   get_tableau_variable_values($MathObjectMatrix_tableau, $MathObjectSet_basis)
#
# feature request -- for tableau object -- allow specification of non-zero parameter variables
#### Test -- assume matrix is this
#    	1	2	1	0	0 |	0 |	3
#		4	5	0	1	0 |	0 |	6
#		7	8	0	0	1 |	0 |	9
#		-1	-2	0	0	0 |	1 |	10  # objective row
# and basis is {3,4,5}  (start columns with 1)
#  $n= 4;  $m = 7
#  $x1=0; $x2=0; $x3=s1=3; $x4=s2=6; $x5=s3=9; w=10=objective value
#
#
##################################################
# We're going to have several types
# MathObject Matrices  Value::Matrix
# tableaus form John Jones macros
# MathObject tableaus
#   Containing   an  matrix $A  coefficients for constraint
#   A vertical vector $b for constants for constraints
#   A horizontal vector $c for coefficients for objective function
#   A vertical vector  $P for the value of the objective function
#   dimensions $n problem vectors, $m constraints = $m slack variables
#   A basis Value::Set -- positions for columns which are independent and
#      whose associated variables can be determined
#      uniquely from the parameter variables.
#      The non-basis (parameter) variables are set to zero.
#
#  state variables (assuming parameter variables are zero or when given parameter variables)
# create the methods for updating the various containers
# create the method for printing the tableau with all its decorations
# possibly with switches to turn the decorations on and off.
# consider entries zero if they are less than $tableauZeroLevel times the current_basis_coeff.
# tableau constructor   Tableau->new(A=>Matrix, b=>Vector or Matrix, c=>Vector or Matrix)
# 	main::DEBUG_MESSAGE(" coldim: $obj_col_dim , row: $obj_row_index obj_matrix: $obj_row_matrix ".ref($obj_row_matrix) );
# 	main::DEBUG_MESSAGE(" \@obj_row ",  join(' ', @obj_row ) );
# eventually these routines should be included in the Value::Matrix
# module?
#  This was written by Davide Cervone.
#  http://webwork.maa.org/moodle/mod/forum/discuss.php?d=2970
# taken from MatrixReduce.pl from Paul Pearson
```

---

### 📄 `math/bizarroArithmetic.pl`
```perl
###########################
#
#  functions used in defining bizarro arithmetic
#
#This f just stretches complex numbers by a positve real that
#depends in a nontrivial away on the magnitude of z
#The inverse of f.
###########################
#
#  Subclass the addition
#
###########################
#
#  Subclass the subtraction
#
###########################
#
#  Subclass the multiplication
#
###########################
#
#  Subclass the division
#
###########################
#
#  Subclass the power
#
###########################
#
#  Subclass the negation
#
```

---

### 📄 `math/PGnumericalmacros.pl`
```perl
# Cubic spline algorithm adapted from p319 of Kincaid and Cheney's Numerical Analysis.
```

---

### 📄 `math/tableau_main_subroutines.pl`
```perl
# subroutines included into the main:: package.
########################
##############
# get_tableau_variable_values
#
# Calculates the values of the basis variables of the tableau,
# assuming the parameter variables are 0.
#
# Usage:   ARRAY = get_tableau_variable_values($MathObjectMatrix_tableau, $MathObjectSet_basis)
#
# feature request -- for tableau object -- allow specification of non-zero parameter variables
#### Test -- assume matrix is this
#    	1	2	1	0	0 |	0 |	3
#		4	5	0	1	0 |	0 |	6
#		7	8	0	0	1 |	0 |	9
#		-1	-2	0	0	0 |	1 |	10  # objective row
# and basis is {3,4,5}  (start columns with 1)
#  $n= 4;  $m = 7
#  $x1=0; $x2=0; $x3=s1=3; $x4=s2=6; $x5=s3=9; w=10=objective value
```

---

### 📄 `math/SolveLinearEquationPCC.pl`
```perl
#These three subroutines uniformize how all our "solve this equation" problems are handled.
#"Solve the following linear equation; the answer could be in the form $eqTypesString, [|no solution|]*, or [|all real numbers|]*."
#(Compute($ansEq[$i])->value)[1] => ["You have the solution, but the answer to this question should be in the form $ansType[$i]" , replaceMessage => 1],
#sub {
#  my ($correct, $student, $ansHash) =@_;
#  return (Compute($ansHash->{original_student_ans})->class eq 'Set');
#} => ["You are trying to give the solution set in set notation, but the answer to this question should be in the form $ansType[$i]" , replaceMessage => 1],
#sub {
#  my ($correct, $student, $ansHash) =@_;
#  return (Compute($ansHash->{original_student_ans})->class eq 'Set' and $student == (Compute($ansEq[$i])->value)[1]);
#} => ["You have the solution set, but the answers to this question should be in the form $ansType[$i]" , replaceMessage => 1],
#if we make it through all the pre-2017 answer checking, now check for answers like 12 or {12} (as opposed to x=12) and award credit
```

---

### 📄 `math/SystemsOfLinearEquationsProblemPCC.pl`
```perl
##############################################
##############################################
##############################################
#############################################################
#############################################################
#if only the second equation has a 1 for one of its coefficients, swap equations; this is more to simplify the code of the solution.
#############################################################
#############################################################
#############################################################
#
#  Set up the LinearSystems context
#
```

---

### 📄 `math/PCCfactor.pl`
```perl
####
# End sub factoringMethods
####
```

---

### 📄 `math/PGmatrixmacros.pl`
```perl
# Make an image of a big delimiter for a matrix
# Basically uses a table of special characters and simple
# recipe to produce big delimeters a la tth mode
# Make a row for the matrix
```

---

### 📄 `math/draggableProof.pl`
```perl
# Deprecated alias for ans_rule.
# Damerau-Levenshtein distance with adjacent transpositions.
# https://en.wikipedia.org/wiki/Damerau-Levenshtein_distance
```

---

### 📄 `math/customizeLaTeX.pl`
```perl
##### Set theory macros
#####  Logic macros
##### Linear algebra macros
##### Algebra macros
# leave one of the following return commands uncommented, depending on what notation you want to use for finite cyclic groups (e.g., Z/nZ)
# Macro to display the ring Z/nZ
# if you want to display dihedral groups as D_n (for instance, D_4 is the dihedral group of order 8), then leave this subroutine unmodified
# if you want to display dihedral groups as D_{2n} (for instance, D_8 is the dihedral group of order 8), then uncomment this set of if/else statements. The regular expression conditionals are to make sure it handles different types of arguments correctly.
# if( "$n" =~ m/^\s*(\d+)\s*$/ )
# {
# $n = 2 * $1;
# }
# elsif( "$n" =~ m/^\s*(\w+)\s*$/ )
# {
# $n = "2$1";
# }
# else
# {
# $n = "2($n)";
# }
```

---

### 📄 `math/PGnauScheduling.pl`
```perl
#####################################################################
#
# Name : ListProcEval  (answer evaluator for the scheduling .pg files)
#
#####################################################################
#############################################################
#
# Name : MakeArrow
#
# Input 	:  $i_1  = the 'tail' x_coordinate in pixels
#		   $i_2  = the 'tail' y_coordinate in pixels
#		   $j_1  = the 'head' x_coordinate in pixels
#		   $j_2  = the 'head' y_coordinate in pixels
#		   $size = the arrowhead size, in pixels
#		   $pic  = the graphics object to modify
#
# Output 	:  $pic
#
#############################################################
####################################################################################################
#
# Name : DrawSchedule
#
# Input 	:	$coordinates = "row (0, ... , 10), column (0, ... , 10), weight, ... ,  ... "
#				       The order determines the vertex index and label used.
#			$connections = "vertex index (tail), vertex index (head), ... , ... "
#				       The vertex indices are taken according to the ordering in
#				       $coordinates.
#
# Output 	:	$pic = the graphics object.
#
####################################################################################################
######################################################################################################
#
# Name : ListProc (to determine the schedule from a priority list)
#
# Input 	:	$coordinates   = "row (0, ... , 10), column (0, ... , 10), weight, ... ,  ... "
#				         The order determines the vertex index and label used.
#			$connections   = "vertex index (tail), vertex index (head), ... , ... "
#				         The vertex indices are taken according to the ordering in
#				         $coordinates.
#			$order 	       = The 'priority list' needed to realize the scheduling (p.79 textbook).
#			$machine_count = The number of available machines or processors.
#
# Output 	:       @done_list     = The 'raw' scheduling solution, indexed by machine:
#					 "vertex index, time, vertex index, time, ...
#					 The last indexed entry is the algorithm time.
#
#####################################################################################################
###########################################################
#  To generate a randomly ordered list of distinct integers
###########################################################
############################################################################################################################
#
# Name : FindPathsSchedule  ( Works only for appropriate schedule type graphs )
#
# Input 	:	$start_vertex   = An index indicating the 'start vertex' to consider.  Indices here START WITH ZERO.
#			$connections	= The connectivity vector to use to determine the paths.  Indices here START WITH ZERO.
#
# Output	:	@path_list	= stores all possible paths from the 'start' vertex.
#
############################################################################################################################
###########################################################################################################
#
# Name : CritList  ( Produces a priority list according to the critical path scheduling algorithm )
#
# Input 	:	$coordinates   = "row (0, ... , 10), column (0, ... , 10), weight, ... ,  ... "
#				         The order determines the vertex index and label used.
#			$connections   = "vertex index (tail), vertex index (head), ... , ... "
#				         The vertex indices are taken according to the ordering in
#				         $coordinates.
#
# Output 	:       $priority_list = The priority list to use, according to the critical path
#					 algorithm.  (The tasks are numerically labeled beginning with
#					 1 according to the order of $coordinates.)
#
#####################################################################################################
##########################################################################################################
#
# Name : CritPath ( Finds the critical path in a schedule type graph.  'Ties' are broken by comparing
#		    the task labels of the first task at which two paths disagree.  The smaller label
#		    is taken as the critical path. )
#
# Input 	:	$coordinates   = "row (0, ... , 10), column (0, ... , 10), weight, ... ,  ... "
#				         The order determines the vertex index and label used.
#					 If -1,-1,-1 appears for any vertex, that task is not considered
#					 as part of the graph.
#			$connections   = "vertex index (tail), vertex index (head), ... , ... "
#				         The vertex indices are taken according to the ordering in
#				         $coordinates.
#
# Output	:	$crit_path	= "task_label1, task_label2, ... , $task_labeln; total_weight
#
###########################################################################################################
#######################################################################################################
#
# Name : PickSchedule
#
# Input		:	$random_flag  = if zero, empty or out-of-range, a random choice is made.  If positive
#					and in-range, this indexes the graph to use.  If "easy", then an 'easy'
#					graph is chosen.
#
# Output 	:	$graph_info    = $coordinates ; $connections where:
#
#				$coordinates   = "row (0, ... , 10), column (0, ... , 10), weight, ... ,  ... "
#				         	 The order determines the vertex index and label used.
#				$connections   = "vertex index (tail), vertex index (head), ... , ... "
#				         	 The vertex indices are taken according to the ordering in
#				         	 $coordinates.
#
########################################################################################################
#######################################################################################################
#
# Name : DrawProcessorSchedule
#
# Input		:	$coordinates   	= "row (0, ... , 10), column (0, ... , 10), weight, ... ,  ... "
#				          The order determines the vertex index and label used.  The
#					  weights are needed to draw the schedules.
#			$done_list     	= The scheduling solution, for the current processor.
#
# Output 	:	$schedule_graph = graphics object.
#
########################################################################################################
###
# Name	: FindMinimum
###
```

---

### 📄 `math/MatrixUnimodular.pl`
```perl
# Note: this is in algebraMacros.pl.  Maybe put in a common place?
```

---

### 📄 `math/draggableSubsets.pl`
```perl
# Deprecated alias for ans_rule.
```

---

### 📄 `math/LinearProgramming.pl`
```perl
# perform a pivot operation
# lp_pivot([[1,2,3],...,[4,5,6]], row, col, fractionmode)
# row and col indecies start at 0
# ^function lp_pivot
# Find pivot column for standard part
# ^function lp_pivot_element
# Solve a linear programming problem
# lp_solve([[1,2,3],[4,5,6]])
# It returns a triple of the final tableau, a code to say if we
#   succeeded, and the number of pivots
# ^function lp_solve
# ^uses set_default_options
# ^uses lp_pivot_element
# ^uses lp_pivot
# Get the current value of a variable from a tableau
# The variable is specified by column number, with 0 for P, 1 for x_1,
#  and so on
# ^function lp_current_value
# ^uses Fraction::new
# Display a tableau in math mode
# ^function lp_display_mm
# ^uses lp_display
# Make a copy of a tableau
# ^function lp_clone
# Display a tableau
# ^function lp_display
# ^uses lp_clone
# ^uses display_matrix
```

---

### 📄 `math/PGnauGraphCatalog.pl`
```perl
# All simple graphs with fewer than 8 vertices
```

---

### 📄 `math/PGnauGraphtheory.pl`
```perl
##################################################### Nandor
######################################
#Name: GRmatrix_graph
#Input:
#Output:
######################################
######################################
#Name: GRgraph_matrix
#Input:
#Output:
######################################
######################################
#Name: GRshuffledgraph_graph
#Input:
#Output:
######################################
######################################
#Name: GRgraph_size_random
#Input:
#Output:
######################################
######################################
#Name: GRgraph_size_random_weight_dweight
#Input:
#Output:
######################################
######################################
#Name: GRlabel_vertex_labels
#Input:
#Output:
######################################
######################################
#Name: GRlabels_vertices_labels
#Input:
#Output:
######################################
######################################
#Name: GRvertex_label_labels
#Input:
#Output:
######################################
######################################
#Name: GRvertices_labels_size
#Input:
#Output:
######################################
######################################
#Name: GRedges_graph
#Input:
#Output:
######################################
######################################
#Name: GRedgesstr_graph_labels
#Input:
#Output:
######################################
######################################
#Name: GRdegree_graph_vertex
#Input:
#Output:
######################################
######################################
#Name: GRdegrees_graph
#Input:
#Output:
######################################
######################################
#Name: GRncomponents_graph
#Input:
#Output:
######################################
######################################
#Name: GRpic_graph_labels
#Input:
#Output:
######################################
######################################
#Name: GRlabelpic_graph(_labels)
#Input:
#Output:
######################################
######################################
#Name: GRnearestnbr_graph_vertex
#Input:
#Output:
######################################
######################################
#Name: GRkruskal_graph
#Input:
#Output:
######################################
######################################
#Name: GRtex_braces
#Input:
#Output:
######################################
######################################
#Name: GRvertexlist_edgesstr_labels
#Input:
#Output:
######################################
######################################
#Name: GRgraph_size_labels_edgesstr
#Input:
#Output:
######################################
####################################################################### Edgar Fisher
######################################
#Name: VertDegree
#Input: Vertex number followed by adjacency matrix for a graph
#Output: Degree of the indicated vertex
######################################
######################################
#Name: GRgraph_degrees
#Input: List of degree values
#Output: A graph with the indicated degree values if possible or 'DNE' if not.
######################################
######################################
#Name: ChangeWeight
#Input: Vertex numbers to change, weight to change the edge to and graph
#Output: A graph with the edge between the indicated vertices changed to weight
######################################
######################################
#Name: GRhaseulercircuit_graph
#Input: Graph
#Output: A list containing a value and message.  The value is 0 if it is not
#an Euler circuit and 1 otherwise.  The message relays why it is not.
######################################
######################################
#Name: GRhaseulertrail_graph
#Input: Graph
#Output: A list containing a value and message.  The value is 0 if it is not
#an Euler path and 1 otherwise.  The message relays why it is not.
######################################
######################################
#Name: GReulercircuit_size
#Input: Size of graph
#Output: A graph that is an Euler Circuit
######################################
######################################
#Name: GReulertrail_size
#Input: Size of graph
#Output: A graph that is an Euler Path but not an Euler Circuit
######################################
######################################
#Name: GRnoneuler_size
#Input: Size of graph
#Output: A graph that is not an Euler path
######################################
######################################
#Name: Matr_graph_Mult
#Input:
#Output:
######################################
######################################
#Name: GRhascircuit_graph
#Input: A graph
#Output: 1 if the graph has a circuit, 0 otherwise
######################################
######################################
#Name: GRistree_graph
#Input: A graph
#Output: A list containing a 1 if it is a tree, 0 if not a tree and a
#        message about why it was not a tree.
######################################
######################################
#Name: GRisforest_graph
#Input: A graph
#Output: A list containing a 1 if it is a forest, 0 if not a forest and a
#        message about why it was not a forest.
######################################
######################################
#Name: GoodEdge
#Input: A graph
#Output: A 1 if the edge should be placed in a sorted edges based graph
#        0 if not.
######################################
######################################
#Name: GRsortededges_graph
#Input: A graph
#Output: A list of the values of the edges included in the graph
#        in the order of their inclusion.
######################################
######################################
#Name: GRiseulertrail_graph_vertices
#Input: A graph and list of selected vertices
#Output: A list containing a 1 if the indicated list of
#        vertices is an euler path in the graph or 0 if
#	 it is not and a message indicating the reason.
######################################
######################################
#Name: GRiseulercircuit_graph_vertices
#Input: A graph and list of selected vertices
#Output: A list containing a 1 if the indicated list of
#        vertices is an euler circuit in the graph or 0 if
#	 it is not and a message indicating the reason.
######################################
######################################
#Name: GRforest_size
#Input: Size of the desired graph to be a forest
#Output: A graph that is a forest
######################################
######################################
#Name: GRtree_size
#Input: size of desired tree
#Output: A graph that is a tree
######################################
######################################
#Name: GRisbipartite_graph
#Input: Graph object
#Output: A 1 is the graph is bipartite, 0 otherwise
######################################
######################################
#Name: GRbipartite_size
#Input: Size of the desired graph
#Output: A graph that has is bipartite
######################################
######################################
#Name: GRdijkstra_graph_vertex_vertex
#Input: A graph, starting vertex and ending vertex for Dijkstra's algorithm
#Output: Two lists, the first, a list of distances from the start vertex
#        to every other vertex. The second a list of the vertices preceding
#	 the current vertex to achieve the shortest path.
######################################
######################################
#Name: GRgraphpic_dim_random_labels_weight_dweight
#Input: Dimensions of the table in (row, column) format, a value to determine
#	the probability of an edge existing between vertices, labels for the vertices,
#	starting weight and weight difference for edge weights.
#Output: A graph with weights and a picture of the graph in tabular format.
######################################
######################################
#Name: GRhamiltonian_size
#Input: Size of the desired graph (5 or greater)
#Output: A graph that has is hamiltonian
######################################
######################################
#Name: GRnonhamiltonian_size_type
#Input: Size of the desired graph and a type of non hamiltonian graph:
#	odd: Has two cycles joined by a single edge
#	even: Has a vertex of degree one
#	If the odd type, size must be at least 6
#Output: A graph that has is not hamiltonian of the specified type
######################################
######################################
#Name: GRcycle_size
#Input: Size for cycle
#Output: A picture of a graph that is a cycle (with no labels).
######################################
######################################
#Name: GRcomplete_size
#Input: Size for complete graph
#Output: A picture of a complete graph (with no labels).
######################################
######################################
#Name: GRwheel_size
#Input: Size for wheel
#Output: A picture of a graph that is a wheel (with no labels).
######################################
######################################
#Name: GRcompletebipartite_size_size
#Input: Size for upper and size for lower bipartite graph
#Output: A picture of a bipartite graph with size and
#	 size labels on top and bottem (and no labels).
######################################
######################################
#Name: GRcube
#Input: None
#Output: A picture of a graph that is a flattened cube.
######################################
######################################
#Name: GRpetersen
#Input: None
#Output: A picture of the Petersen graph.
######################################
######################################
#Name: GRdodecahedron
#Input: None
#Output: A picture of a graph that is a flattened dodecahedron.
######################################
######################################
#Name: GRvertices_labels_labels
#Input: string of labels, string of all graph labels
#Output: Returns a list of vertex numbers corresponding to the
#	 labels in the first string.
######################################
```

---

### 📄 `math/MatrixUnits.pl`
```perl
###################################################
#######################################################
########################################################
#######################################################
```

---

### 📄 `math/PGmorematrixmacros.pl`
```perl
# set the prefix used for arrays.
# These should be compared to similar subroutines made later in
# MatrixCheckers.pl
## This is where the correct answer should be checked someday.
#   $rh_ans->{ans_label} =~ /$ArRaY(\d+)\[\d+,\d+,\d+\]/;  # CHANGE made to accomodate HTML 4.01 standards for name attribute
# The following subroutines, meant to be used with MatrixReal1 type matrices, are
# deprecated.  In general you should use the MathObject Matrix type and the
# checking methods in MatrixCheckers.pl
# 	are_orthogonal_vecs($vec_ref, %opts)
# 	is_diagonal($matrix, %opts)
# 	are_unit_vecs($vec_ref, %opts)
# 	display_correct_vecs($vec_ref, %opts)
# 	vec_solution_cmp($vec,%opts)
# 		filter: compare_vec_solution($rh_ans,%opts);
## This is where the correct answer should be checked someday.
# changes by MEG 6/24/05
# the student answer needs to be a linear combination of the instructors vectors
# and the coefficient of the first vector needs to be 1 (it is NOT enough that it be non-zero).
# if this is not the case, then the answer is wrong.
# replaced   $x_vector->[0][0][0]  by $x_vector->element(1,1)  since this doesn't depend on the internal structure of the matrix object.
```

---

### 📄 `math/VectorListCheckers.pl`
```perl
########################################################
########################################################
########################################################
```

---

### 📄 `PGcourse.pl`
```perl
#loadMacros("source.pl");
```

---

### 📄 `contexts/contextRationalFunction.pl`
```perl
##################################################
##############################################
##############################################
##############################################
##############################################
##############################################
```

---

### 📄 `contexts/contextForm.pl`
```perl
###########################
#
#  Subclass the numeric functions
#
#
#  Override sqrt() to return a special value times x when evaluated
#
#
#  Override root(n,) to return a special value times x when evaluated
#
```

---

### 📄 `contexts/contextLimitedVector.pl`
```perl
##################################################
#
#  Handle common checking for BOPs
#
#
#  Do original check and then if the operands are numbers, its OK.
#  Otherwise, check if there is a duplicate constant from either term
#  Otherwise, do an operator-specific check for if vectors are OK.
#  Otherwise report an error.
#
#
#  filled in by subclasses
#
#
#  Check if a constant has been repeated
#  (we maintain a hash that lists if one is below us in the parse tree)
#
##############################################
#
#  Now we get the individual replacements for the operators
#  that we don't want to allow.  We inherit everything from
#  the original Parser::BOP class, and just add the
#  vector checks here.
#
##############################################
##############################################
##############################################
##############################################
##############################################
#
#  Now we do the same for the unary operators
#
##############################################
##############################################
##############################################
##############################################
#
#  Absolute value does vector norm, so we
#  trap that as well.
#
##############################################
##############################################
##############################################
```

---

### 📄 `contexts/contextInteger.pl`
```perl
###########################################################################
#
#  Initialize the contexts and make the creator function.
#
#
# divisor function
#
#
#  Prime Factorization
#
#
# Euler's totient function phi(n)
#
#
# number of divisors function tau(n)
#
#
#  Greatest Common Divisor
#
#
#  Extended Greatest Common Divisor
#
# return (g, x, y) a*x + b*y = gcd(x, y)
#
#  Modular inverse
#
# x = mulinv(b) mod n, (x * b) % n == 1
#
#  Least Common Multiple
#
```

---

### 📄 `contexts/contextTrigDegrees.pl`
```perl
#######################################
#
#  Check the number of arguments, and call the proper method with the
#  the proper factor involved.
#
#
#  Call the proper method with the correct factor
#
#
#  Do chain rule derivative, taking the $deg factor into account
#
#######################################
#
#  Hook the common functions into these classes
#
#######################################
#######################################
#
#  Change the classes for the trig functions to be our classes above,
#  and mark the inverses so that the degrees can be applied in the
#  proper location.
#
#  Define the sin, cos, and atan2 functions so that they will call our
#  methods even if their arguments are Perl reals.
#
```

---

### 📄 `contexts/contextComplexJ.pl`
```perl
##########################################################################
###############################################################
#
#  Enables complex j notation in the given context
#
#
#  Sets all the complex-based default contexts to use ComplexJ
#  notation.  The two arguments determine the values for the
#  enterComplex and displayComplex flags.  If enterComplex is "j",
#  then student answers must use the j notation (though
#  professors can use either).
#
###############################################################
#
#  Handle Complex numbers so that they are displayed
#  with the proper i or j value.
#
###############################################################
#
#  Make Parser Value object maintain the indicator for
#  which notation was used for a complex number.
#
###############################################################
#
#  Make sure complex numbers maintain their flag for
#  which format was used to create them.
#
###############################################################
#
#  Produce error messages when the wrong notation
#  is used for complex numbers.
#
#  Swap i and j when required by the displayComplex flag
#  in the output of constants.
#
###############################################################
```

---

### 📄 `contexts/contextLimitedPoint.pl`
```perl
##################################################
#
#  Handle common checking for BOPs
#
#
#  Do original check and then if the operands are numbers, its OK.
#  Otherwise report an error.
#
##############################################
#
#  Now we get the individual replacements for the operators
#  that we don't want to allow.  We inherit everything from
#  the original Parser::BOP class, except the _check
#  routine, which comes from LimitedPoint::BOP above.
#
##############################################
##############################################
##############################################
##############################################
##############################################
#
#  Now we do the same for the unary operators
#
##############################################
##############################################
##############################################
##############################################
#
#  Absolute value does vector norm, so we
#  trap that as well.
#
##############################################
##############################################
```

---

### 📄 `contexts/contextFraction.pl`
```perl
#################################################################################################
#################################################################################################
#
#  Extend a given context (by name or actual Context object) to include fractions
#  The options are the default values for the Fraction context flags
#
#
#  Initialize the contexts and make the creator function.
#
#
#  Backward compatibility
#
#
#  Greatest Common Divisor
#
#
#  Least Common Multiple
#
#
#  Reduced fraction
#
#################################################################################################
#################################################################################################
#
# Takes a positive real input and outputs an array (a,b) where a/b
# is a very good fraction approximation with b no larger than
# maxdenominator.
#
#
# Convert a real to a reduced fraction approximation.
#
# Uses $context->continuedFracation() to convert .333333... into 1/3
# rather than 333333/1000000, etc.
#
#################################################################################################
#################################################################################################
#
#  A common class for getting the super-class of an extension class
#
#################################################################################################
#################################################################################################
#
#  A common class for handling the fraction class data in an object's typeRef
#
#################################################################################################
#################################################################################################
#
#  When strictFraction is in effect, only allow division
#  with integers and negative integers
#
#
#  Create a Fraction from the given data
#
#
#  Reduce the fraction
#
#
#  Display minus signs outside the fraction
#
#
#  Derivative of fraction is 0 since it is constant
#
#################################################################################################
#################################################################################################
#
#  If the implied multiplication represents a proper fraction with a
#  preceding integer, then switch to the proper fraction operator
#  (for proper handling of string() and TeX() calls), otherwise,
#  convert the object to a standard multiplication.
#
#
#  For when the space operator's string property sends to an
#  operator we didn't otherwise subclass.
#
#################################################################################################
#################################################################################################
#
# Implements the space between mixed numbers
#
#
#  For proper fractions, add the integer to the fraction
#
#
#  Reduce the fraction
#
#
#  Derivative of a mixed number is 0 since it is constant
#
#################################################################################################
#################################################################################################
#
#  For strict fractions, only allow minus on certain operands
#
#################################################################################################
#################################################################################################
#
#  Handle reductions of negative fractions
#
#
#  Add parentheses if they were there originally, or are needed by precedence
#
#
#  Add parentheses if they were there originally, or
#  are needed by precedence and we asked for exxxtra parens
#
#
#  Just return the fraction
#
#################################################################################################
#################################################################################################
#
#  Distinguish integers from decimals
#
#################################################################################################
#################################################################################################
#
#  Allow Real to convert Fractions to Reals
#
#
#  Since the signed number pattern now include fractions, we need to make sure
#  we handle them when a real is made and it looks like a fraction
#
#
#  Since this is called directly, pass it up to the parent
#
##################################################
#################################################################################################
#################################################################################################
#
#  Implements the MathObject for fractions
#
#
#  Produce a real if one of the terms is not an integer
#  otherwise produce a fraction.
#
#
#  Promote to a fraction, allowing reals to be $x/1 even when
#  not an integer (later $self->make() will produce a Real in
#  that case)
#
#
#  Create a new formula from the number
#
#
#  Return the real number type
#
#
#  Return the real value
#
#
#  Parts are not Value objects, so don't transfer
#
#
#  Check if a value is an integer
#
#
#  Get a flag that has been renamed
#
##################################################
#
#  Binary operations
#
##################################################
#
#   Numeric functions
#
##################################################
#
#   Trig functions
#
##################################################
#
#  Differentiation
#
##################################################
#
#  Utility
#
##################################################
#
#  Formatting
#
###########################################################################
#
#  Answer Checker
#
#################################################################################################
#################################################################################################
```

---

### 📄 `contexts/contextRationalExponent.pl`
```perl
#
#  Set up the RationalExponent context
#
###########################
#
#  Create root(n, x)
#
###########################
#
#  Subclass the numeric functions
#
#
#  Override sqrt() to return a special value times x when evaluated
#
```

---

### 📄 `contexts/contextFiniteSolutionSets.pl`
```perl
###########################
#
#  Subclass the numeric functions
#
#
#  Override sqrt() to return a special value times x when evaluated
#
#
#  Override root(n,) to return a special value times x when evaluated
#
```

---

### 📄 `contexts/legacyFraction.pl`
```perl
###########################################################################
#
#  Initialize the contexts and make the creator function.
#
# contFrac($x, $maxdenominator)
# Subroutine that takes a positive real input $x and outputs an array
# (a,b) where a/b is a very good fraction approximation with b no
# larger than maxdenominator.
#
# Convert a real to a reduced fraction approximation
# Uses contFrac() to convert .333333... into 1/3 rather
#   than 333333/1000000, etc.
#
#
#  Greatest Common Divisor
#
#
#  Least Common Multiple
#
#
#  Reduced fraction
#
###########################################################################
#
#  Create a Fraction or Real from the given data
#
#
#  When strictFraction is in effect, only allow division
#  with integers and negative integers
#
#
#  Reduce the fraction, if it is one, otherwise do the usual reduce
#
#
#  Display minus signs outside the fraction
#
#
#  Indicate if the value is a fraction or not
#
###########################################################################
#
#  For proper fractions, add the integer to the fraction
#
#
#  If the implied multiplication represents a proper fraction with a
#  preceeding integer, then switch to the proper fraction operator
#  (for proper handling of string() and TeX() calls), otherwise,
#  convert the object to a standard multiplication.
#
#
#  Indicate if the value is a fraction or not
#
#
#  Reduce the fraction
#
###########################################################################
#
#  For strict fractions, only allow minus on certain operands
#
#
#  class is MINUS if it is a negative number
#
#
#  make isNeg properly handle the modified class
#
###########################################################################
#
#  Indicate if the Value object is a fraction or not
#
#
#  Handle reductions of negative fractions
#
#
#  Add parentheses if they were there originally, or are needed by precedence
#
#
#  Add parentheses if they were there originally, or
#  are needed by precedence and we asked for exxxtra parens
#
###########################################################################
#
#  Allow Real to convert Fractions to Reals
#
#
#  Since the signed number pattern now include fractions, we need to make sure
#  we handle them when a real is made and it looks like a fraction
#
###########################################################################
###########################################################################
#
#  Implements the MathObject for fractions
#
#
#  Produce a real if one of the terms is not an integer
#  otherwise produce a fraction.
#
#
#  Promote to a fraction, allowing reals to be $x/1 even when
#  not an integer (later $self->make() will produce a Real in
#  that case)
#
#
#  Create a new formula from the number
#
#
#  Return the real number type
#
#
#  Return the real value
#
#
#  Parts are not Value objects, so don't transfer
#
#
#  Check if a value is an integer
#
#
#  Get a flag that has been renamed
#
##################################################
#
#  Binary operations
#
##################################################
#
#   Numeric functions
#
##################################################
#
#   Trig functions
#
##################################################
#
#  Differentiation
#
##################################################
#
#  Utility
#
##################################################
#
#  Formatting
#
###########################################################################
#
#  Answer Checker
#
###########################################################################
```

---

### 📄 `contexts/contextLimitedPowers.pl`
```perl
#
#  Test for whether the power is an integer in the specified range
#
#
#  Legacy code to accommodate older approach to setting the operators
#
##################################################
##################################################
##################################################
```

---

### 📄 `contexts/contextPartition.pl`
```perl
###########################################################
#
#  Create the contexts and add the constructor functions
#
###########################################################
#
#  The Partition object
#
#
#  Check the data and create the object
#
#
#  Add a number to a partition, or add two partitions
#
#
#  Produce the sum for a partition
#
#
#  Compare two partitions (numbers are promoted)
#
#
#  Produce a canonical representation (numbers sorted)
#
#
#  Promote a number to a Real (since we can add a number to a
#  partition), and promote others to partitions, if possible.
#
#
#  Check if types are compatible
#
#
#  Produce a string version
#
#
#  Produce a TeX version
#
###########################################################
#
#  Implement special + operator that produces
#  partitions rather than sums
#
#
#  Check that the operands are appropriate, and return
#  the proper type reference, or give an error.
#
#
#  Check that the type of an operand is OK
#  (It must be a partiation or a number)
#
#
#  Evaluate two numbers by forming a partition,
#   otherwise use addition (Value object will take over)
#
###########################################################
```

---

### 📄 `contexts/contextPiecewiseFunction.pl`
```perl
#
#  Create the needed context and the constructor function
#
##################################################
##################################################
#
#  A class to implement undefined values (points that
#  are not in the domain of the function)
#
##################################################
#
#  Implement the "if" operator to specify a branch
#  of the piecewise function.
#
#
#  Only allow inequalities on the right.
#  Mark the object with identifying values
#
#
#  Return the function's value if the variable is within
#    the inequality for this branch (otherwise return
#    and undefined value).
#
#
#  Make a piecewise function from this branch
#
#
#  Make an interval=>formula pair from this item
#
#
#  Print using the TeX method of the PiecewiseFunction object
#
#
#  Make an if-then-else statement that returns the function's
#    value or an undefined value (depending on whether the
#    variable is in the interval or not).
#
##################################################
#
#  Implement the "else" operator to join the
#  different branches of the function.
#
#
#  Make sure there is an "if" that goes with this else.
#
#
#  Use the result of the "if" to decide which value to return.
#
#
#  Make a PiecewiseFunction from the (nested) if-then-else values.
#
#
#  Recursively flatten the if-then-else tree to a list
#  of interval=>formula pairs.
#
#
#  Don't do extra parens for nested else's.
#
#
#  Use the PiecewiseFunction TeX method.
#
#
#  Use an if-then-else to determine the value to use.
#
##################################################
#
#  Implement an "in" operator for "x in (a,b)" as an
#  alternative to inequality notation.
#
#
#  Make sure the variable is to the left and an interval,
#  set, or union is to the right.
#
#
#  Call this an Inequality so it will be allowed to the
#  right of "if" operators.
#
##################################################
#
#  This implements the "in" operator as in inequality.
#  We inherit all the inequality methods, and simply
#  need to handle the string and TeX output.  The
#  underlying type is still an Inerval.
#
##################################################
##################################################
#
#  This implements the PiecewiseFunction.  It is an unusual mix
#  of a Value object and a Formula object.  It looks like a
#  Formula for the most part, but doesn't have the same internal
#  structure.  Most of the Formula methods have been provided
#  so that eval, substitute, reduce, etc will be applied to all
#  the branches.
#
#
#  Create the PiecewiseFunction object, with error reporting
#  for problems in the data.
#
#  Usage:  PiecewiseFunction("formula")
#          PiecewiseFunction(I1 => f1, I2 => f2, ... , fn);
#
#  In the first case, the formula is parsed for "if" and "else" values
#  to produce the function.  In the second, the function is given
#  by interval/formula pairs that associate what function to map over
#  interval.  If there is an unpaired formula at the end, it is
#  the "otherwise" formula that will be used whenever the input
#  does not fall into one of the given intervals.
#
#  Note that the intervals above actually can be Interval, Set,
#  or Union objects, not just plain intervals.
#
#
#  Create a PiecewiseFunction without error checking (so overlapping intervals,
#  incorrect variables, and so on could appear).
#
#
#  Do the consistency checks for the separate branches.
#
#
#  Check that all the inequalities are for the same variable.
#
#
#  Check that no domain intervals overlap.
#
#
#  Check that all the branches return the same type of result.
#
#
#  This is always considered a formula.
#
#
#  Look through the branches for the one that contains
#  the variable's value, and evaluate it.  If not in
#  any of the intervals, use the "otherwise" value,
#  or die with no value if there isn't one.
#
#
#  Reduce each branch individually.
#
#
#  Substitute into each branch individually.
#  If the function's variable is substituted, then
#    if it is a constant, find the branch for that value
#    and substitute into that, otherwise if it is
#    just another variable, replace the variable
#    in the inequalities as well as the formulas.
#  Otherwise, just replace in the formulas.
#
#
#  Return the domain of the function (will be (-inf,inf) if
#  there is an "otherwise" formula.
#
#
#  The set (-inf,inf).
#
#
#  The domain formed by the explicitly given intervals
#  (excludes the "otherwise" portion, if any)
#
#
#  Creates a copy of the PiecewiseFunction where the "otherwise"
#  formula has been given explicit intervals within the object.
#  (This makes it easier to compare two PiecewiseFormulas
#  interval by interval.)
#
#
#  Look up the function for the nth branch (or the "otherwise"
#  function if n is omitted or too big or too small).
#
#
#  Look up the domain for the nth branch (or the "otherwise"
#  domain if n is omitted or too big or too small).
#
#
#  Get the function for the given value of the variable
#  (or undef if there is none).
#
#
#  Implements the <=> operator (really only handles equality ir not)
#
#
#  Check that the function domains have the same number of
#  components, and that those components agree, interval by interval.
#
#
#  Now that the intervals are known to agree, compare
#  the individual functions on each interval.  Do an
#  appropriate check depending on the type of each
#  branch:  Interval, Set, or Union.
#
#
#  Use the Interval to determine the limits for use
#  in comparing the two functions.
#
#
#  For a set, check that the functions agree on every point.
#
#
#  For a union, do the appropriate check for
#  each object in the union.
#
#
#  Stringify using newlines at after each "else".
#  (Otherwise the student and correct answer can
#  get unacceptably long.)
#
#
#  TeXify using a "cases" LaTeX environment.
#
#
#  Create a code segment that returns the correct value depending on which
#  interval contains the variable's value (or an undefined value).
#
#
#  Handle the types correctly for error messages and such.
#
#
#  Allow comparison only when the two functions return
#  the same type of result.
#
##################################################
#
#  Overrides the Formula() command so that if
#  the result is a PiecewiseFunction, it is
#  turned into one automatically.  Conversely,
#  if a PiecewiseFunction is put into Formula(),
#  this will turn it into a Formula.
#
######################################################################
```

---

### 📄 `contexts/contextComplexExtras.pl`
```perl
####################################################
#
#  Base UOP class that checks for matrix arguments
#
#
#  Check that the operand is a Matrix
#
####################################################
#
#  Implements the ~ operation on matrices and complex numbers
#    (as a left-associative unary operator)
#
####################################################
#
#  Implements the ^T operation on matrices and complex numbers
#    (as a right-associative unary operator)
#
####################################################
#
#  Implements the ^* operation on matrices and complex numbers
#    (as a right-associative unary operator)
#
####################################################
#
#  Implement functions with one matrix input and complex output
#
#
#  Check for a single Matrix-valued input
#
#
#  Evaluate by promoting to a Matrix
#    and then calling the routine from the Value package
#
#
#  Check for a single Matrix-valued argument. Then promote it to a Matrix (does error checking)
#    and call the routine from Value package (after converting "tr" to "trace")
#
```

---

### 📄 `contexts/contextPolynomialFactors.pl`
```perl
##################################################
##############################################
##############################################
##############################################
##############################################
##############################################
##############################################
##############################################
##############################################
```

---

### 📄 `contexts/contextPermutation.pl`
```perl
###########################################################
#
#  Create the contexts and add the constructor functions
#
###########################################################
#
#  Methods common to cycles and permutations
#
#
#  Use the usual make(), and then add the permutation data
#
#
#  Permform multiplication of a number by a cycle or permutation,
#  or a product of two cycles or permutations.
#
#
#  Perform powers by repeated multiplication;
#  Negative powers are inverses.
#
#
#  Compare canonical representations
#
#
#  True if the permutation is in canonical form
#
#
#  Promote a number to a Real (since we can take a number times a
#  permutation, or a permutation to a power), and anything else to a
#  Cycle or Permutation.
#
#
#  Produce a canonical representation as a collection of
#  cycles that have their lowest entry first, sorted
#  by initial entry.
#
#
#  Produce the inverse of a permutation or cycle.
#
#
#  Produce a string version (use "(1)" as the identity).
#
#
#  Produce a TeX version (uses \; for spaces)
#
###########################################################
#
#  A single cycle
#
#
#  Find the internal representation of the cycle
#  (a hash representing where each element goes)
#
###########################################################
#
#  A combination of cycles
#
#
#  Find the internal representation of the permutation
#  (a hash representing where each element goes)
#
###########################################################
#
#  Space between numbers forms a cycle.
#  Space between cycles forms a permutation.
#  Space between a number and a cycle or
#    permutation evaluates the permutation
#    on the number.
#
#
#  Check that the operands are appropriate, and return
#  the proper type reference, or give an error.
#
#
#  Evaluate by forming a list if this is acting as a comma,
#  othewise take a product (Value object will take care of things).
#
#
#  If the operator is not a comma, return the item itself.
#  Otherwise, make a list out of the lists that are the left
#    and right operands.
#
#
#  Produce the TeX form
#
###########################################################
#
#  Powers of cycles form permutations
#
#
#  Check that the operands are appropriate,
#    and return the proper type reference
#
###########################################################
#
#  The List subclass for cycles in the parse tree
#
#
#  Check that the coordinates are numbers.
#  If there is one parameter and it is a cycle or permutation
#   treat this as plain parentheses, not cycle parentheses
#   (so you can take groups of cycles to a power).
#
#
#  Produce a string version.  (Shouldn't be needed, but there is
#  a bug in the Value.pm version that neglects the separator value.)
#
#
#  Produce a TeX version.
#
###########################################################
```

---

### 📄 `contexts/contextInequalitySetBuilder.pl`
```perl
##################################################
#
#  A class for making set-builder sets by hand
#
##################################################
##################################################
#
#  The Parser object that holds the set-builder notation
#  (and also allows point-set notation)
#
##################################################
##################################################
#
#  The such-that operator
#
#
#  Make sure it is only used in set braces
#
##################################################
#
#  Give a warning about adding sets
#
##################################################
#
#  Handle subtraction of sets
#
##################################################
#
#  Handle unions of sets
#
##################################################
##################################################
#
#  Common function for the classes below
#
##################################################
#
#  Special Inequalities::Interval subclass that
#  prints using set-builder notation.
#
##################################################
#
#  Special Inequalities::Union subclass that
#  prints using set-builder notation.
#
##################################################
#
#  Special Inequalities::Set subclass that
#  prints using set-builder notation.
#
##################################################
```

---

### 📄 `contexts/contextMatrixExtras.pl`
```perl
####################################################
#
#  Implements the ^T operation on matrices
#    (as a right-associative unary operator)
#
####################################################
#
#  Implement functions with one matrix input and real output
#
#
#  Check for a single Matrix-valued input
#
#
#  Evaluate by promoting to a Matrix
#    and then calling the routine from the Value package
#
#
#  Check for a single Matrix-valued argument
#  Then promote it to a Matrix (does error checking)
#    and call the routine from Value package (after
#    converting "tr" to "trace")
#
```

---

### 📄 `contexts/contextLimitedComplex.pl`
```perl
##################################################
#
#  Handle common checking for BOPs
#
#
#  Do original check and then if the operands are numbers, its OK.
#  Otherwise, do an operator-specific check for if complex numbers are OK.
#  Otherwise report an error.
#
#
#  filled in by subclasses
#
#
#  Get the form for use in error messages
#
##############################################
#
#  Now we get the individual replacements for the operators
#  that we don't want to allow.  We inherit everything from
#  the original Parser::BOP class, and just add the
#  complex checks here.  Note that checkComplex only
#  gets called if exactly one of the terms is complex
#  and the other is real.
#
##############################################
##############################################
##############################################
##############################################
#
#  Base must be 'e' (then we know the other is the complex
#  since we only get here if exactly one term is complex)
#
##############################################
##############################################
#
#  Now we do the same for the unary operators
#
##############################################
##############################################
##############################################
##############################################
#
#  Absolute value does complex norm, so we
#  trap that as well.
#
##############################################
##############################################
```

---

### 📄 `contexts/contextLimitedFactor.pl`
```perl
#
#  Set up the LimitedFactor context
#
```

---

### 📄 `contexts/contextCurrency.pl`
```perl
#
#  Initialization creates a Currency context object
#  and sets up a Currency() constructor.
#
#
#  Quote characters that are special in regular expressions
#
#
#  Quote common TeX special characters, and put
#  the result in {\rm ... } if there are alphabetic
#  characters included.
#
######################################################################
######################################################################
#
#  The Currency context has an extra "currency" data
#  type (like flags, variables, etc.)
#
#  It also creates some patterns needed for handling
#  currency values, and sets the Parser and Value
#  hashes to activate the Currency objects.
#
#  The tolerance is set to .005 absolute so that
#  answers must be correct to the penny.  You can
#  change this in the context, or for individual
#  currency values.
#
##################################################
#
#  This is the context data for currency.
#  A special pattern is maintained for the
#  comma form of numbers (using the specified
#  comma and decimal-place characters).
#
#  You specify the currency symbol via
#
#    Context()->currency->set(symbol=>'$');
#    Context()->currency->set(comma=>',',decimal=>'.');
#
#  You can add extra symbols via
#
#    Context()->currency->addSymbol("dollar","dollars");
#
#  If the symbol contains alphabetic characters, it
#  is made to be right-associative (i.e., comes after
#  the number), otherwise it is left-associative (i.e.,
#  before the number).  You can change that for a
#  symbol using
#
#    Context()->currency->setSymbol("Euro"=>{associativity=>"left"});
#
#  Finally, an extra symbol can be removed with
#
#    Context()->currency-removeSymbol("dollar");
#
#
#  Set up the initial data
#
#
#  Create, set and remove extra currency symbols
#
#
#  Update the currency patterns in case the characters have changed,
#  and if the symbol has changed, remove the old operator(s) and
#  create a new one for the given symbol.
#
######################################################################
######################################################################
#
#  When creating Number objects in the Parser, we need to remove the
#  comma (and currency) characters and replace the decimal character
#  with an actual decimal point.
#
##################################################
#
#  This class implements the currency symbol.
#  It checks that its operand is a numeric constant
#  in the correct format, and produces
#  a Currency object when evaluated.
#
#
#  Use the Currency MathObject to produce the output formats
#
######################################################################
######################################################################
#
#  This is the MathObject class for currency objects.
#  It is basically a Real(), but one that stringifies
#  and texifies itself to include the currency symbol
#  and commas every three digits.
#
#
#  We need to override the new() and make() methods
#  so that the Currency object will be counted as
#  a Value object.  If we aren't promoting Reals,
#  produce an error message.
#
#
#  Look up the currency symbols either from the object of the context
#  and format the output as a currency value (use 2 decimals and
#  insert commas every three digits).  Put the currency symbol
#  on the correct end for the associativity and remove leading
#  and trailing spaces.
#
#
#  Override the class name to get better error messages
#
#
#  Add promoteReals option to allow Reals with no dollars
#
######################################################################
```

---

### 📄 `contexts/contextReaction.pl`
```perl
######################################################################
######################################################################
#
#  The main MathObject class for reactions
#
#
#  Some type declarations for the various classes
#
#
#  Set up the context and Reaction() constructor
#
#<<<
#>>>
#
#  Handle postfix - and + in superscripts
#
#
#  Handle superscripts of just + or -
#
#
#  Compare by checking of the trees are equivalent
#
#
#  Don't allow evaluation
#
#
#  Provide a useful name
#
#
#  Set up the answer checker.  Avoid the list checker in
#    Value::Formula::cmp_equal (for when the answer is a
#    sum of compounds) and provide a postprocessor to
#    give warnings when a reaction is compared to a
#    student answer that isn't a reaction.
#
#
#  Since the context only allows things that are comparable, we
#  don't really have to check anything.  (But if someone added
#  strings or constants, we would.)
#
######################################################################
#
#  The replacement for the Parser:Number class
#
#
#  Equivalent is equal
#
######################################################################
#
#  The replacement for Parser::Variable.  We hold the elements here.
#
#
#  Two elements are equivalent if their names are equal
#
#
#  Print element names in Roman
#
#
#  For a printable name, use a constant's name,
#  and 'an element' for an element.
#
######################################################################
#
#  General binary operator (add, multiply, arrow, and underscore
#  are subclasses of this).
#
#
#  Binary operators produce chemicals (unless overridden, as in arrow)
#
#
#  Two nodes are equivalent if their operands are equivalent
#  and they have the same operator
#
######################################################################
#
#  Implements the --> operator
#
#
#  It is a reaction, not a chemical
#
#
#  Check that the operands are correct.
#
######################################################################
#
#  Implements addition, which forms a list of operands, so acts like
#  the Parser::BOP::comma operator
#
#
#  Check that the operands are OK
#
#
#  Two are equivalent if they are equivalent in either order.
#  (never really gets used, since these result in the creation
#  of a list rather than an "add" node in the final tree.
#
######################################################################
#
#  Implements concatenation, which produces compounds or integer
#  multiples of elements or molecules.
#
#
#  Check that the operands are OK
#
#
#  Remove ground state, if needed
#
#
#  No space in output for implied multiplication
#
#
#  Handle states separately
#
######################################################################
#
#  Implements the underscore for creating molecules
#
#
#  Check that the operands are OK
#
#
#  Create proper TeX output
#
#
#  Create proper text output
#
######################################################################
#
#  Implements the superscript for creating ions
#
#
#  Check that the operands are OK
#
#
#  Create proper TeX output
#
#
#  Create proper text output
#
######################################################################
#
#  General unary operator (minus and plus are subclasses of this).
#
#
#  Unary operators produce numbers
#
#
#  Two nodes are equivalent if their operands are equivalent
#  and they have the same operator
#
#
#  Always put signs on the right
#
#
#  Always put signs on the right
#
######################################################################
#
#  Negative numbers (for ion exponents)
#
######################################################################
#
#  Positive numbers (for ion exponents)
#
######################################################################
#
#  Implements sums of compounds as a list
#
#
#  Two sums are equivalent if their terms agree in any order.
#
#
#  Get a hash of element (or compound, etc.) names used in the list
#  mapping to the count of each and a hash of the states used and
#  their counts.  States are only recorded if students don't need
#  to include them (otherwise the hash names will include the states).
#
#
#  Use "+" between entries in the list (with no parens)
#
######################################################################
#
#  Implements complexes as a list
#
#
#  Two complexes are equivalent if their contents are equivalent
#  (we check by stringifying them and sorting, then compare results)
#
######################################################################
```

---

### 📄 `contexts/contextAlternateDecimal.pl`
```perl
###########################################################
###########################################################
#
#  Create the AlternateDecimal contexts
#
#
#  Enables alternate decimals in the given context
#
#
#  Sets all the default contexts to use alternate decimals.
#  The two arguments determine the values for the
#  enterDecimals and displayDecimals flags.  If enterDecimals
#  is ",", then student answers must use commas for decimals
#  (though professors can use either).  If the display is not
#  ".", then separators for lists, points, vectors, etc, are
#  displayed as ";".
#
###########################################################
#
#  Handle numbers with commas as decimal indicators, and produce an
#  error if the format is not what is allowed.  Mark the number if it
#  is in the alternate form, so we can display it correctly later.  If
#  needed, save the original string, swap the comma for a dot, save
#  THAT, and correct the number's numeric value.
#
#
#  If we have an alternate form, make a Real out of it so that
#  we can retain the alternateForm flag.  (I'm not sure if there
#  will be any problems from that, since it usually only returns
#  a Perl real).
#
#
#  Fix the decimal separators depending on the display format.
#
#
#  Return the proper class
#
###########################################################
#
#  Make the number and issue a warning if the wrong format is used.
#  Save the decimal in standard notation, but mark it as alternate
#  form so that it can be displayed in its original form, if needed.
#
#
#  Display the number in the correct form depending on the displayDecimals flag.
#
###########################################################
#
#  Allow Parser::Value to create Parser::Number objects
#  from decimals without checking for commas (since these
#  are the results of computations, not values entered
#  directly by students).
#
###########################################################
```

---

### 📄 `contexts/contextArbitraryString.pl`
```perl
#
#  Handle creating String() constants
#
#
#  Replacement for Parser::String that uses the original string verbatim
#  (but replaces \r and \r\n by \n to handle different browser multiline input)
#
#
#  Replacement for Value::String that creates preview strings
#  that work for multiline input
#
#
#  Mark a multi-line string to be displayed verbatim in TeX
#
#
#  Quote HTML special characters
#
#
#  Adjust preview and strings so they display multiline answers properly.
#
```

---

### 📄 `contexts/contextRestrictedDomains.pl`
```perl
###########################
#
#  Subclass the numeric functions
#
#
#  Override sqrt() to return a special value times x when evaluated
#
```

---

### 📄 `contexts/contextExtensions.pl`
```perl
#################################################################################################
#################################################################################################
#
#  This package provides create() and extend() functions that can be
#  used to get a copy of an existing context and extend it by
#  overriding the existing classes with your own, while maintaining
#  information about those original classes so that you can fall back
#  on them for any situations that don't involve your new
#  functionality.  These functions are designed so that multiple
#  extensions can be added without interfering with one another.
#
#
#  ID to use for contexts that need a dynamic extension
#
#
#  Copy the given context (given by name or as a Context object)
#  and name the new one.  For example,
#
#    $context = context::Extensions::create("Quaternions", "Complex");
#
#  would create a context named "Quaternions-Complex" as a copy of the
#  Complex context.  The implementation for classes added to this
#  context should be in the context::Quaternions namespace.
#
#
#  Extend a given Context object to include new features by specifying
#  classes to use for operators, functions, value object, and parser
#  objects, while retaining the old classes for fallback use.
#
#  The changes are specified in the options following the Context, and these
#  can include:
#
#    opClasses => { op => 'class', ... }
#
#      specifies the operators to override, and the class suffix to
#      use for their implementations.  For example, using
#
#         opClasses => { '+' => 'BOP::add' }
#
#      would attach the class context::Quaternions::BOP::add to the
#      plus sign in our Quaternion setting.  If the space operator (' ')
#      is in your list, and if the original context has it point to an
#      operator that is NOT in your list, then that referenced operator
#      is redirected automatically to 'BOP::Space' in your base context
#      package.  In our case, we would want to include a definition for
#      context::Quaternions::BOP::Space in order to cover that possibility.
#
#    ops => { op => {def}, ... }
#
#      specifies new operators to add to the context (where "def" is
#      an operator definition like those for any context).
#
#    functions => 'class1|class2|...'
#
#      specifies the function categories that you are overriding (e.g.,
#
#         functions => 'numeric|trig|hyperbolic'
#
#      would override the functions that have classes that end in
#      ::Functions:numeric, ::Function::trig, or ::Function::hyperbolic
#      and direct them to your own versions of these.  In our quaternion
#      setting that would be to context::Quaternions::Function::numeric
#      for the first of these, and similarly for the others.
#
#    value => ['Class1', 'Class2', ...]
#
#      specifies the Value object classes to override.  For instance,
#
#         value => ['Real', 'Formula']
#
#      would set $context->{value}{Real} and $context->{value}{Formula}
#      to point to your own versions of these (e.g., in our example,
#      these would be context::Quaternions::Value::Real and
#      context::Quaternions::Value::Formula.  Note that if you list
#      the parenthesized version (used by the corresponding constructor
#      functions), then the parentheses are replaced by "_Parens" in the
#      class name.  For example,
#
#         value => ['Real()']
#
#      would set
#
#         $context->{value}{Real()} = 'context::Quaternions::Value::Real_Parens';
#
#    parser => ['Class1', 'Class2', ... ]
#
#      specifies the Parser classes to override.  This works similarly
#      to the "value" option above, so that
#
#         parser => ['Number']
#
#      would set $context->{parser}{Number} to your version of this class,
#      which would be context::Quaternions::Parser::Number in our example.
#
#    flags => { flag => value, ...}
#
#      specifies the new flags to add to the context (or existing ones to
#      override.
#
#    reductions => { name => 1 or 0, ... }
#
#      specifies new reduction rules to add to the context, and
#      whether they are in effect by default (1) or not (0).  Of
#      course, you need to implement these reduction rules in your
#      Parser objects.
#
#    context => "Context"
#
#      specifies that your context is a subclass of Parser::Context
#      that adds methods to the context.  If specified, the modified
#      context will be blessed using this value as the suffix for the
#      context's class.  In our quaternion example, the value "Context"
#      would mean the resulting modified context would be blessed
#      as context::Quaternions::Context.
#
#  The extend() function returns the modified context.
#
#  The various operators, functions, and value and Parser objects that
#  you define should use the context::Extensions::Super package below
#  in order to access the original classes for those objects.  Ideally,
#  your new objects will mutate (i.e., re-bless) themselves to their
#  original classes if they don't involve your new MathObjects.
#
#  For example, the new context::Quaternions::BOP::add class should
#  have the context::Extensions::Super object as one of its
#  superclasses, and then its _check() method could check if either
#  operand is a quaternion, and if not, it can call
#  $self->mutate->_check to turn itself into the original object's
#  class and perform its _check() actions.  That way, the new BOP::add
#  class only needs to worry about implementing the situation for
#  quaternions, and lets the original class deal with everything else.
#
#
#  Record original operator class and set the new one,
#  extending to a new class if needed.
#
#
#  Record original class for a given Value or Parser class
#
#################################################################################################
#################################################################################################
#
#  A common class for getting the super-class of an extension class.
#
#  This class handles all the details of dealing with the original
#  object classes that you have overridden in the context.  You should
#  create a subclass of this class and define its extensionContext()
#  method to return your base context name, and then include that
#  subclass in your @ISA arrays for your new classes that override the
#  original context's classes.  (This is not strictly necessary, but
#  it is more efficient to do this than to have the Super class
#  have to figure it out every time a Super method is used.)
#
#  For our quaternions example, you would use
#
#    package context::Quaternions::Super
#    our @ISA = ('context::Extensions::Super');
#
#    sub extensionContext { 'context::Quaternions' }
#
#  and then use 'context::Quaternions::Super' in the @ISA of your new
#  classes for operators, functions, or Value or Parser objects.
#  E.g.,
#
#    package context::Quaternions::BOP::add;
#    our @ISA = ('context::Quaternions::Super', 'Parser::BOP');
#
#    sub _check {
#      my $self = shift;
#      return $self->mutate->_check
#        unless $self->{lop}->class eq 'Quaternion' || $self->{rop}->class eq 'Quaternion';
#      #  Do your checking for proper arguments to go along with a quaternion here
#    }
#
#    sub _eval {
#      #  Do what is needed to perform addition between quaternions or between
#      #  a quaternion or another legal value here.  You don't have to worry
#      #  about any other types here, as the mutate() call above will change
#      #  the class to the original class (and its _eval() method) if one
#      #  of the operands isn't a quaternion.
#    }
#
#  If you need to call a method from the original class, use
#
#    &{$self->super("method")}($self, args...);
#
#  where "method" is the name of the method to call, and "args" are any arguments
#  that you need to pass.  For example,
#
#    my $string = &{$self->super("string")}($self);
#
#  would get the string output from the original class.
#
#  If you are defining a new() or make() method (where the $self could be
#  the class name rather than a class instance), you will need to pass the
#  context to mutate(), super(), or superClass().  See the example for
#  new() below.
#
#  The superClass() method gets you the name of the original class, in
#  case you need to access any class variables from that.
#
#
#  Get a method from the original class from the extended context
#
#
#  Get the super class name from the extension hash in the context
#
#
#  Re-bless the current object to become the other object,
#  if there is one, or the object's super class if not.
#
#
#  Use the super-class new() method
#
#
#  Get the object's class from its class name
#
#
#  This method assumes the extension is in a class named
#  "context::<name>" where <name> is replaced by the name of the
#  context.  E.g., context::Quaternions in our example.
#
#  That assumption can be changed by subclassing
#  context::Extensions::Super package and overriding this method with
#  one that returns the extension context's name.  It is more efficient
#  to do that, anyway, but you can get away without it.
#
#################################################################################################
#################################################################################################
#
#  A common class for handling the private extension data in an object's typeRef.
#
#  This allows you to add and retrieve custom data to and from an
#  object's type in such a way that it doesn't interfere with the
#  original object's type, or that of any other extensions.
#
#  A MathObject's typeRef property is a HASH that includes information
#  about the object's type, its length (for things like lists and
#  vectors), and entry types (again for objects like lists and
#  vectors).  We can add data to this hash to store additional
#  information that we need in order to be more granular about the
#  type or class of a Parser object.
#
#  To use this, create a subclass of context::Extensions::Data that
#  has an extensionID() method that returns a name to use as the hash
#  key to store your custom data (the default is to use the base
#  context name).  Your subclass should also include your Super class
#  as a parent class.  For example:
#
#    package context::Quaternions::Data;
#    our @ISA = ('context::Quaternions::Super', 'context::Extensions:Data');
#
#    sub extensionID { 'quatData' }
#
#  Then use this new subclass in the @ISA list for any class that needs access
#  to your custom data.
#
#  The extensionData() method returns the complete hash of your custom
#  data, from which you can extract the value of the property you
#  need, or can set any properties that you want.  E.g.,
#
#    $self->extensionData->{class};
#
#  could be used to obtain the custom "class" property of your data.
#
#  The setExtensionType() method is used to set an object's
#  $self->{type} property (which holds the object's typeRef) to a
#  named type residing in your base context.  For example:
#
#    package context::Quaternions;
#    our $QUATERNION = Value::Type("Number, undef, undef, quatData => {class => "QUATERNION"});
#
#    package context::Quaternions::Super
#    our @ISA = ('context::Extensions::Super');
#    sub extensionContext { 'context::Quaternions' }
#
#    package context::Quaternions::Data;
#    our @ISA = ('context::Quaternions::Super', 'context::Extensions:Data');
#    sub extensionID { 'quatData' }
#
#    package context::Quaternions::BOP::add;
#    our @ISA = ('context::Quaternions::Data', 'Parser::BOP');
#
#    sub _check {
#      my $self = shift;
#      unless $self->{lop}->class eq 'Quaternion' || $self->{rop}->class eq 'Quaternion';
#      #  other type checking here
#      $self->setExtensionType("QUATERNION");  # Use the type in the $QUATERNION variable above
#    }
#
#  Finally, the extensionDataMatch() method checks if the value of a
#  given property is one of a set of values.  For example, if you have
#  a property called "class", then
#
#    $self->extensionDataMatch($self->{lop}, "class", "QUATERNION", "COMPLEX");
#
#  would return 1 if the quatData->{class} was either "QUATERNION" or
#  "COMPLEX" in the $self->{lop}{type} hash, and 0 otherwise.
#
#
#  Get the object's extensionData
#
#
#  Set the object's extensionData (and the rest of its type)
#
#
#  Check if an object's extension property matches one of the given values
#
#
#  The extension context can subclass that is produce a better name
#
#################################################################################################
#################################################################################################
```

---

### 📄 `contexts/contextOrdering.pl`
```perl
###########################################
#
#  The main Ordering routines
#
#
#  Here we set up the prototype contexts and define the needed
#  functions in the main:: namespace.  Some error messages are
#  modified to read better for these contexts.
#
#
#  A routine to set the letters allowed in this context.
#  (Old letters are cleared, and > and = are allowed, but hidden,
#   since they are used in the List() objects that implement the context).
#
#
#  Create orderings from strings or lists of letter => value pairs.
#  A copy of the current context is created that contains the proper
#  letters, and the correct string is created and parsed into an
#  Ordering object.
#
#############################################################
#
#  This is a Parser BOP used to create the Ordering objects
#  used internally.  They are actually lists with the operator
#  and the two operands, and the comparisons is based on the
#  standard list comparisons.  The operands are either the strings
#  for individual letters, or another Ordering object as a
#  nested List.
#
#############################################################
#
#  This is the Value object used to implement the list That represents
#  one ordering operation.  It is simply a normal Value::List with the
#  operator as the first entry and the two operands as the remaing
#  entries in the list.  The new() method is overriden to make binary
#  trees of equal operators into flat sorted lists.  We override the
#  List string and TeX methods so that they print correctly as binary
#  operators.  The cmp_equal method is overriden to make sure the that
#  the lists are treated as a unit during answer checking.  There is
#  also a routine for adding letters to the object's context.
#
#
#  Put all equal letters into one list and sort them
#
#
#  Make sure we do comparison as a list of lists (rather than as the
#  individual entries in the underlying Value::List that encodes
#  the ordering)
#
#
#  Add more letters to the ordering's context (so student answers
#  can include them even if they aren't in the correct answer).
#
#############################################################
#
#  This overrides the TeX method of the letters
#  so that they don't print using the \rm font.
#
#############################################################
#
#  Override Parser classes so that we can check for repeated letters
#
#
#  Save the letters positional reference
#
#########################
#
#  Move letters to Value object
#
#
#  Return Ordering class if the object is one
#
#############################################################
#
#  This overrides the cmp_equal method to make sure that
#  Ordering lists are put into nested lists (since the
#  underlying ordering is a list, we don't want the
#  list checker to test the individual parts of the list,
#  but rather the list as a whole).
#
#############################################################
```

---

### 📄 `contexts/contextPercent.pl`
```perl
#
#  Initialization sets up a Perent() constructor and
#  creates the percent contexts.
#
######################################################################
######################################################################
#
#  When creating Number objects in the Parser, keep Percent objects.
#
##################################################
#
#  This class implements the percent symbol.
#  It checks that its operand is a numeric constant
#  in the correct format, and produces
#  a Percent object when evaluated.
#
#
#  Use the Percent MathObject to produce the output formats
#
######################################################################
######################################################################
#
#  This is the MathObject class for Percent objects.
#  It is basically a Real(), but one that stringifies
#  and texifies itself to include the percent symbol,
#  and evaluates to its value divided by 100.
#
#
#  We need to override the new() and make() methods
#  so that the Percent object will be counted as
#  a Value object.  If we aren't promoting Reals,
#  produce an error message.
#
#
#  Format the output as a percent value.
#
#
#  Override the class name to get better error messages
#
#
#  Check for whether we want to work with reals as percents
#
######################################################################
######################################################################
#
#  LimitedPercent contexts
#
##################################################
#
#  Handle common checking for BOPs
#
#
#  Do original check and then if the operands are numbers, its OK.
#  Otherwise report an error.
#
##############################################
#
#  Now we get the individual replacements for the operators
#  that we don't want to allow.  We inherit everything from
#  the original Parser::BOP class, except the _check
#  routine, which comes from LimitedPercent::BOP above.
#
##############################################
##############################################
##############################################
##############################################
##############################################
##############################################
#
#  Now we do the same for the unary operators
#
##############################################
##############################################
##############################################
##############################################
#
#  Absolute value does vector norm, so we
#  trap that as well.
#
```

---

### 📄 `contexts/contextLimitedRadicalComplex.pl`
```perl
#
#  Set up the LimitedRadical context
#
###########################
#
#  Create root(n, x)
#
###########################
#
#  Subclass the numeric functions
#
#
#  Override sqrt() to return a special value times x when evaluated
#
```

---

### 📄 `contexts/contextAlternateIntervals.pl`
```perl
##########################################################################
##########################################################################
#  Create the AlternateIntervals contexts
#  Enables alternate intervals in the given context
#
#  Sets the default Interval context to use alternate decimals.  The
#  two arguments determine the values for the enterIntervals and
#  displayIntervals flags.  If enterIntervals is "alternate", then
#  student answers must use the alternate format for entering
#  intervals (though professors can use either).
#
##########################################################################
#  Replace the standard Open with one that handles formInterval better.
#  We need to handle several possible close delimiters.
#
#  We need to modify the test for formInterval to NOT check the number
#  of entries so that better error messages are produced, and to handle
#  multiple close delimiters.  These are both in teh "operand" branch,
#  so do the original for all the choices, and copy that branch here,
#  with our modifications.
#
##########################################################################
#  Convert alternative form to regular form, but mark it as alternative.
#  Give error messages about forms that aren't allowed by the context flags.
#  For alternative form, switch back to the alternative brackets for printing,
#  or force standard or alternative form based on the context flags.
#  This gets called directly, so pass it up the line
#  Make sure that the standard open and close delimiters are
#  used so that comparisons and so on will work properly.
#  Report errors when invalid form is specified
#  Make a copy with the alternate delimiters, if needed.
#  Override the output methods to replace the alternate delimiters, when needed.
```

---

### 📄 `contexts/contextLimitedRadical.pl`
```perl
#
#  Set up the LimitedRadical context
#
###########################
#
# Convenience
#
# Pass $a,$b, get Formula("$a sqrt($b)") but simplified
###########################
#
#  Create root(n, x)
#
###########################
#
#  Subclass the numeric functions
#
#
#  Override sqrt() to return a special value times x when evaluated
#
```

---

### 📄 `contexts/contextCongruence.pl`
```perl
###########################################################################
#
#  Initialize the contexts and make the creator function.
#
#
#  Produce a string version
#
#
#  Produce a TeX version
#
#
#  Check for two real-valued arguments
#
#
#  Check that the inputs are OK
#
#
#  Call the appropriate routine
#
#
#  Congruence Class
#  ax ≡ b (mod m)
#
# returns gcd, residue, divisor
```

---

### 📄 `contexts/contextUnits.pl`
```perl
#################################################################################################
#################################################################################################
#
#  The class name for the number-with-unit class
#
#
#  Value types for units and numbers with units
#
#
#  Common error message for functions when they get arguments with units
#
#
#  Create the Units and LimitedUnits contexts, and the
#  Unit(), NumberWithUnit(), and FormulaWithUnit() functions.
#
#################################################################################################
#################################################################################################
#
#  The context subclass that adds unit-handling functions
#
#
#  The units from the original Units package
#
#
#  The categories of units that can be selected.
#
#  These give the fundamental units of the unit names to be added to
#  the context, or a list of such, or a list of names of known units.
#  If a name begins with a dash, then REMOVE the category or named
#  unit.  For example, the "length" category excludes the lengths that
#  are part of the "atomics" and "astronomy" categories.  If a name
#  ends in an asterisk, then add or remove all the aliases for that
#  unit as well.
#
#
#  Add new units, either by name, as name => unit_def, or as unit_def
#  (where unit_def is like one of the known units).  Also add other
#  units that are aliases for the given one in the known_units list.
#
#
#  Add new units, either by name or name => unit_def (where unit_def
#  is like one of the known units).  Don't add any aliases for these
#  units.
#
#
#  Add a single unit by name or name => unit_def
#
#
#  Adds all the aliases for a given named unit or unit definition
#
#
#  Add the units for the given named categories
#
#
#  Add the units for a single category
#
#
#  Alias for addUnitsFor
#
#
#  Remove the named units and their aliases
#
#
#  Remove a named unit and its aliases
#
#
#  Removes the named units nit not their aliases
#
#
#  Assigns units to a list of variables (for differentiation)
#
#################################################################################################
#################################################################################################
#
#  The MathObject class for units (single or compound)
#
#
#  Create a new Unit object, either by parsing a string version of
#  the units, or by giving the name of a known unit, or as name => unit_def,
#  where unit_def is an object like the known units.  You can also use this
#  object in the Unit from a Number-with-Unit, or to make a copy of an
#  existing Unit.
#
#
#  Copy a Unit by duplicating the internal hashes and arrays.
#
#
#  Get the factor by which the unit must be multiplied to obtain
#  a quantity in the corresponding fundamental units.
#
#############################################################
#
#  Multiply the Unit by another Unit
#
#
#  Divide the Unit by another Unit
#
#
#  Raise the Unit to a power
#
#  Add the powers of units in the $units hash into the Unit's $key1
#  list, and cancel powers between the $key1 and $key2 lists, moving
#  any negative powers into the $key2 list.
#
#
#  Add $n to the unit $u in the $units hash, and move it to
#  the $other hash if the power ends up being negative.
#
#
#  Check if there is cancellation between the $key1 and $key2 lists,
#  and move any negative powers from the $key1 list to the $key2 list
#
#
#  Handle cancellation of powers in the $units and $other lists.
#
#############################################################
#
#  Multiply a Unit by a Number or another Unit
#
#
#  Divide a Unit by a Number or another Unit
#
#
#  Raise a Unit to a numeric power
#
#
#  Compare two Units (0 means equal)
#
#
#  Get the list of variables to differentiate by
#
#
#  Differentiate by the given variables (provided they have assigned units).
#
#############################################################
#
#  The default flags for answer checking (take them from the context instead)
#
#
#  Check for sameUnits and exactUnits, and give the needed messages and partial credit
#
#############################################################
#
#  Get the string version using the original units and powers
#
#
#  Get the string version using the fundamental units
#
#
#  Get the string version using original units using:
#    The original order and powers if $exact is set, or
#    Alphabetic order and fractions otherwise.  Use
#    alias strings to normalize the result.
#
#
#  Creates the string version using the given order and power settings
#
#
#  Create the string for a given unit and power and push it
#  into the $units or $invert array depending on whether it has
#  a negative power or not
#
#
#  Create the TeX string for the Units
#
#
#  Create the TeX string for a given unit and power and
#  push it into the $units array.
#
#
#  Create the Perl code to recreate the Units.
#
#############################################################
#
#  Override the functions to produce errors on Unit inputs
#
#################################################################################################
#################################################################################################
#
#  The MathObject class for numbers with units
#
#
#  Create a new Number-with-Unit object, either by giving the number
#  and units separately.  The number can be any MathObject that is of
#  type Number (including a Formula returning a number), or a string to
#  be parsed to compute the number.  The unit can be a Unit object or
#  a string that can be parsed to a Unit.
#
#
#  Return the proper type and class data
#
#############################################################
#
#  Functions for obtaining the various parts of the Number-with-Units
#
#############################################################
#
#  Get the string version using the fundamental units
#
#
#  Get the string version using original units using:
#    The original order and powers if the argument is true, or
#    Alphabetic order and fractions if not.
#
#
#  Get the string version of the Number with Units
#
#
#  Get the TeX version of the Number with Units
#
#
#  Get the Perl code to re-create the Number with Units
#
#
#  Since the string version contains a space, we add parentheses when stringifying
#  into another string
#
#############################################################
#
#  The default flags for answer checking (take them from the context instead)
#
#
#  Give a message about incorrect units, and check for sameUnits and
#  exactUnits, and give the needed messages and partial credit.
#
#############################################################
#
#  Negate by negating the numeric part
#
#
#  Take absolute value on the numeric part
#
#
#  Add a Number with Units to another one
#
#
#  Subtract a Number with Units from another one
#
#
#  Multiply a Number with Units by another Number with Units, or a Unit, or a Number
#
#
#  Divide a Number with Units by another Number with Units, or a Unit, or a Number,
#  or divide a Number, Unit, or Number with Units by a Number with Units
#
#
#  Raise a Number with Units to an integer
#
#
#  Compare two Numbers with Units (0 means equal)
#
#
#  Differentiate the number and unts by the given variables.
#
#############################################################
#
#  Functions that can't have Numbers with Units as arguments
#
#
#  sin() and cos() can take arguments that are angles
#
#############################################################
#
#  Convert a Number with Units to one using the base units (in
#  alphabetical order)
#
#
#  Convert a Number with Units to one using the given units
#
#################################################################################################
#################################################################################################
#
#  A common class for getting the super-class of an extension class
#
#################################################################################################
#################################################################################################
#
#  A common base class for unit-based binary operators.  It is used as
#  part of a dynamically created class that includes a units class and
#  original class from the context that the units context extends.
#
#
#  True if one of the operands is a Unit or Number with Unit
#
#
#  True if both operands are Units or Numbers with Units
#
#
#  True if one of the operands is a Number with Units and the other is
#  a Number with Unit or a Number
#
#
#  True if both of the operands are a Numbers with Units
#
#
#  Call the _check from the original class unless one of the operands
#  is a Number with Units, in which case, we check that operations are
#  allowed, and set the type if they are.
#
#
#  Call the _check from the original class unless one of the operands
#  is a Unit or Number with Units.  Otherwise, check the operands
#  and report any messages, and set the type accordingly.
#  For multiplication, use space or \, for string and TeX versions, not '*'.
#
#
#  When we have "(x unit) unit" or "(x unit) / unit", adjust these to be
#  "x (unit unit) or "x (unit / unit)" so that the output is better
#  (i.e., doesn't include extra parentheses).
#
#
#  Hack to replace BOP with a division BOP.
#  (When check() is changed to accept a return value,
#  this will not be necessary.)
#
#
#  Check if the units have cancelled, and set the type accordingly
#
#
#  For string output, add parentheses if the precedence is the same
#
#
#  Call the super TeX method (so fractions are properly handled, for example)
#
#############################################################
#############################################################
#############################################################
#############################################################
#############################################################
#############################################################
#############################################################
#
#  Implements "squared", "cubed", "square", and "cubic" operators.
#
#################################################################################################
#################################################################################################
#
#  A common base class for the unit function classes to allow trig and hyperbolic functions
#  to have arguments that are Numbers with Units when the units are angles or other units.
#
#
#  True when $x is a Number with Units where the units are degrees.
#
#
#  Check whether degrees or other units are allowed,
#   otherwise convert to the usual function and do its check.
#
#
#  Convert an angle to radians if the argument is an angle (and conversion is allowed)
#
#
#  Convert an angle to radians if the argument is an angle (and conversion is allowed)
#  before calling the function.
#
#
#  Differentiate a function with a number-with-units as an argument.
#
#  Get the argument as a Formula.
#  If the the argument is an angle, get its quantity (which includes
#    the unit factor) and differentiate that.
#  Otherwise, remove the unit from the function call and differentiate that.
#
#############################################################
#############################################################
#############################################################
#############################################################
#################################################################################################
#################################################################################################
#
#  Allow Real() to return the numeric part of a Number with Units,
#  otherwise, do the original Real() call.
#
#################################################################################################
#################################################################################################
#
#  Allow Formulas to have "unit" and "number" methods
#
#################################################################################################
#################################################################################################
#
#  Allow parentheses to be used around units in contexts (like
#  LimitedNumeric) where they have been removed.  This allows
#  you to enter "kg/(m s)" in such contexts.
#
#################################################################################################
#################################################################################################
```

---

### 📄 `contexts/contextInequalities.pl`
```perl
#
#  Sets up the two inequality contexts
#
##################################################
#
#  General BOP that handles the inequalities.
#  The difference comes in the _eval() method,
#  which tells what each computes.
#
#
#  Check that the inequality is formed between a variable and a number,
#  or between a number and another compatible inequality.  Otherwise,
#  give an error.
#
#  varPos and numPos tell which of lop or rop is the variable and which
#  the number.  varName is the variable involved in the inequality.
#
#
#  Generate the interval for the given type of inequality.
#  If it is a combined inequality, intersect with the other
#  one to get the final set.
#
#
#  Inequalities have dummy variables that are not really
#  variables of a formula.
#
#  Avoid unwanted parentheses from the standard routines.
#
##################################################
#
#  Implements the "and" operation as set intersection
#
##################################################
#
#  Implements the "or" operation as set union
#
##################################################
#
#  Subclass of Parser::Variable that records whether
#  this variable has already been seen in the formula
#  (so that it can be removed from the formula's
#  variable list when used in an inequality.)
#
##################################################
#
#  A special class used for the variables in
#  inequalities, since they are not really
#  variables for the formula.  (They don't need
#  to be substituted or given values when the
#  formula is evaluated, and so on.)  These are
#  really just placeholders, here.
#
##################################################
#
#  Give an error when U is used.
#
##################################################
#
#  Don't allow sums and differences of inequalities
#
##################################################
#
#  Don't allow sums and differences of inequalities
#
##################################################
#
#  For the Inequalities-Only context, report
#  an error for Intervals, Sets or Union notation.
#
##################################################
##################################################
#
#  Subclasses of the Interval, Set, and Union classes
#  that stringify as inequalities
#
#
#  Some common routines to all three classes
#
#
#  Turn the object back into its usual Value version
#
#
#  Needed to get Interval data in the right order for make(),
#  and demote all the items in a Union
#
#
#  Recursively mark Intervals and Sets in a Union as Inequalities
#
#
#  Demote the operands to normal Value objects and
#  perform the action, then remake the result into
#  an Inequality again.
#
#
#  The name to use for error messages in answer checkers
#
#
#  Get the precedence based on the type rather than the class.
#
#
#  Produce better error messages for inequalities
#
##################################################
##################################################
#
#  Mark all the parts of the union as inequalities
#
#
#  Update the intervals and sets when a new union is made
#
#
#  Demote all the items in the union
#
##################################################
##################################################
#
#  A class for making inequalities by hand
#
##################################################
#
#  Allow Interval() to coerce types to Value::Interval
#
##################################################
#
#  Mark this as a list of inequalities (if it is)
#
##################################################
```

---

### 📄 `contexts/contextString.pl`
```perl
##################################################
##################################################
##################################################
```

---

### 📄 `contexts/contextPermutationUBC.pl`
```perl
###########################################################
#
#  Create the contexts and add the constructor functions
#
###########################################################
#
#  Methods common to cycles and permutations
#
#
#  Use the usual make(), and then add the permutation data
#
#
#  Permform multiplication of a number by a cycle or permutation,
#  or a product of two cycles or permutations.
#
#
#  Perform powers by repeated multiplication;
#  Negative powers are inverses.
#
#
#  Compare canonical representations
#
#
#  True if the permutation is in canonical form
#
#
#  Promote a number to a Real (since we can take a number times a
#  permutation, or a permutation to a power), and anything else to a
#  Cycle or Permutation.
#
#
#  Produce a canonical representation as a collection of
#  cycles that have their lowest entry first, sorted
#  by initial entry.
#
#
#  Produce the inverse of a permutation or cycle.
#
#
#  Produce a string version (use "(1)" as the identity).
#
#
#  Produce a TeX version (uses \; for spaces)
#
###########################################################
#
#  A single cycle
#
#
#  Find the internal representation of the permutation
#  (a hash representing where each element goes)
#
###########################################################
#
#  A combination of cycles
#
#
#  Find the internal representation of the permutation
#  (a hash representing where each element goes)
#
###########################################################
#
#  Space between numbers forms a cycle.
#  Space between cycles forms a permutation.
#  Space between a number and a cycle or
#    permutation evaluates the permutation
#    on the number.
#
#
#  Check that the operands are appropriate, and return
#  the proper type reference, or give an error.
#
#
#  Evaluate by forming a list if this is acting as a comma,
#  othewise take a product (Value object will take care of things).
#
#
#  If the operator is not a comma, return the item itself.
#  Otherwise, make a list out of the lists that are the left
#    and right operands.
#
#
#  Produce the TeX form
#
###########################################################
#
#  Powers of cycles form permutations
#
#
#  Check that the operands are appropriate,
#    and return the proper type reference
#
###########################################################
#
#  The List subclass for cycles in the parse tree
#
#
#  Check that the coordinates are numbers.
#  If there is one parameter and it is a cycle or permutation
#   treat this as plain parentheses, not cycle parentheses
#   (so you can take groups of cycles to a power).
#
#
#  Produce a string version.  (Shouldn't be needed, but there is
#  a bug in the Value.pm version that neglects the separator value.)
#
#
#  Produce a TeX version.
#
#########################################################################
#
#  The List subclass for one line notation permutations in the parse tree
#
#
#  Check that the coordinates are numbers.
#
#
#  Call the appropriate creation routine from Value.pm
#  (Can be over-written by sub-classes)
#
###########################################################
```

---

### 📄 `contexts/contextBaseN.pl`
```perl
# Define the contexts 'BaseN' and 'LimitedBaseN'
# Create a Context based on Numeric that allows +, -, *, /, %, and ^ on BaseN integers.
# set the base of the context.  Either an integer that is at least 2, an arrayref of digits,
# or a preset: 'binary', 'octal', 'decimal', 'duodecimal', 'hexadecimal', or 'base64'.
# Convert a number in base10 to the given base.
# Convert a number in a given base to base 10.
# A replacement for Parser::Number that accepts numbers in a non-decimal base and
# converts them to decimal for internal use
# Create a new number in the given base and convert to base 10.
# Modulo operator
#
#  Do the division.
#
#  A replacement for Value::Real that handles non-decimal integers
#  Stringify and TeXify the number in the context's base
# Define division as integer division.
```

---

### 📄 `contexts/contextBoolean.pl`
```perl
# top-level access to context-specific T and F
# Subclass the Parser::Context to override copy() and add T and F functions
# Access to the constant T and F values
# Easy setting of precedence to different types
# Subclass Parser::Number to return the constant T or F
# Subclass Value::Formula for boolean formulas
# use every combination of T/F across all variables
# remove once UOP::string passses 'same' as second argument
# remove once UOP::TeX passses 'same' as second argument
# use the context settings
# use the context settings
```

---

### 📄 `contexts/contextLimitedPolynomial.pl`
```perl
##################################################
#
#  Handle common checking for BOPs
#
#
#  Mark a variable as having power 1
#  Mark a number as being present (when strict coefficients are used)
#  Mark a monomial as having its given powers
#
#
#  Get a hash of variable names that point to indices
#  within the array of powers for a monomial
#
#
#  Check for a constant expression
#
##################################################
#
#  Handle common checking for BOPs
#
#
#  Do original check and then if the operands are numbers, its OK.
#  Otherwise, do an operator-specific check for if the polynomial is OK.
#  Otherwise report an error.
#
#
#  filled in by subclasses
#
#
#  Check that the exponents of a monomial are OK
#  and record the new exponent array
#
#
#  Check that the powers of combined monomials are OK
#  and record the new power list
#
#
#  Report an error when both operands are constants
#  and strictCoefficients is in effect.
#
##############################################
#
#  Now we get the individual replacements for the operators
#  that we don't want to allow.  We inherit everything from
#  the original Parser::BOP class, and just add the
#  polynomial checks here.  Note that checkPolynomial
#  only gets called if at least one of the terms is not
#  a number.
#
##############################################
##############################################
##############################################
##############################################
##############################################
##############################################
#
#  Now we do the same for the unary operators
#
##############################################
##############################################
##############################################
##############################################
#
#  Don't allow absolute values
#
##############################################
##############################################
#
#  Only allow numeric function calls
#
##############################################
##############################################
```

---

### 📄 `contexts/contextScientificNotation.pl`
```perl
#
#  Creates and initializes the ScientificNotation context
#
##################################################
#
#  The Scientific Notation multiplication operator
#
#
#  Check that the operand types are compatible, and give
#  approrpiate error messages if not.  (We have to work
#  hard to make a good message about the number of
#  decimal digits required.)
#
#
#  Perform the multiplication and return a ScientificNotation object
#
#
#  Use the ScientificNotation MathObject to produce the output formats
#  (if other operators are added back into the context, these will
#   need to be modified to include parens at the appropriate times)
#
##################################################
#
#  Scientific Notation exponentiation operator
#
#
#  Check that the operand types are compatible and
#  produce appropriate errors if not
#
#####################################
#
#  A subclass of Real that handles scientific notation
#
#
#  Override these so we can mark ourselves as scientific notation
#
#
#  Stringify using x notation not E,
#  using the right number of digits, and trimming
#  if requested.
#
#
#  Convert x notation to TeX form
#
#
#  What to call us in error messages
#
#
#  Only match against strings and Scientific Notation
#
#########################################################################
```

---

### 📄 `contexts/contextTypeset.pl`
```perl
######################################################################
######################################################################
# just override the _check method
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
# handle _check to set type for numbers and sets
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
######################################################################
```

---

