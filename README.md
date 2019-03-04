# NLSAA_Hypertension

The study on the causes of high blood pressure in Nottingham Longitudinal Study of Activity and Ageing (NLSAA)

SPSS output file download: https://github.com/bobleer/NLSAA_Hypertension/raw/master/SPSS_output.spv

## Potential Factor & Research Methods

Data type |	Sub-type | Variable |	Value scale |	Description | Method | Sig.
:-|:-|:-|:-|:-|:-|:-
Discrete | Nominal | `hi_bp_85` |	(0,1) |	High Blood Pressure? | Dependent variable|
Discrete | Nominal | `heart_85`	| (0,1)	| Heart trouble? | Chi-squared | **0.002**
Discrete | Nominal | `smoke_do`	| (0,1)	| Do you smoke? | Chi-squared | 0.063
Discrete | Nominal | `sex_85`	| (1,2)	| Gender | Chi-squared | **0.001**
Continuous | Interval |	`age_85` | (Numeric) | Age | KS → MW-U | 0.977
Continuous | Ratio | `wght_85` | (Numeric/Kgs) | Weight | KS → MW-U | **0.009**
Continuous | Interval | `tmasl_85`	| (Numeric/Min) |	Time Asleep | KS → MW-U | 0.278
Continuous | Interval | `t_rlx_85`	| (Numeric/Min) |	Leisure Time | KS → MW-U | **0.046**
Discrete | Ordinal | `anx_85` | (Score/0,21) | Anxiety | MW-U | **0.031**
Discrete | Ordinal | `dep_85` |	(Score/0,21) | Depression | MW-U | **0.013**

## Binary Logistic Regression

<table class="rich-diff-level-zero"> <tbody class="rich-diff-level-one"> <tr> <th colspan="7" align="left">High blood pressure? (Percentage of correct prediction: 78%)</th> <th colspan="2" align="left">95% C.I. for EXP(B)</th> </tr> <tr> <td></td> <td>B</td> <td>S.E.</td> <td>Wald</td> <td>df</td> <th align="left">Sig.</th> <th align="left">Exp(B)</th> <td>Lower</td> <td>Upper</td> </tr> <tr> <td>Heart trouble? (1)</td> <td>-.563</td> <td>.185</td> <td>9.304</td> <td>1</td> <th align="left">.002</th> <th align="left">.569</th> <td>.396</td> <td>.818</td> </tr> <tr> <td>Sex of Respondent (1)</td> <td>-.748</td> <td>.189</td> <td>15.604</td> <td>1</td> <th align="left">.000</th> <th align="left">.473</th> <td>.327</td> <td>.686</td> </tr> <tr> <td>Body weight (Kg)</td> <td>.023</td> <td>.006</td> <td>13.821</td> <td>1</td> <th align="left">.000</th> <th align="left">1.023</th> <td>1.011</td> <td>1.036</td> </tr> <tr> <td>Leisure Activities (Mins/week)</td> <td>-.001</td> <td>.000</td> <td>3.258</td> <td>1</td> <td>.071</td> <td>.999</td> <td>.998</td> <td>1.000</td> </tr> <tr> <td>Anxiety Score (1985)</td> <td>.020</td> <td>.046</td> <td>.187</td> <td>1</td> <td>.665</td> <td>1.020</td> <td>.932</td> <td>1.116</td> </tr> <tr> <td>Depression Score (1985)</td> <td>.029</td> <td>.048</td> <td>.363</td> <td>1</td> <td>.547</td> <td>1.029</td> <td>.937</td> <td>1.131</td> </tr> <tr> <td>Constant</td> <td>-2.060</td> <td>.438</td> <td>22.139</td> <td>1</td> <td>.000</td> <td>.127</td> <td></td> <td></td> </tr> </tbody> </table>

## Result

This study selects nine variables from NLASS dataset which are possibly relevant to high blood pressure. After conducting appropriate and specific statistical analyses, `heart_85`, `sex_85`, `wght_85`, `t_rlx_85`, `anx_85` and `dep_85` are taken for the causes of hypertension. The result of this study partly confirms the experiences from previous researches. Furthermore, `heart_85`, `sex_85`, `wght_85` have significant correlations with `hi_bp_85` in the regression model. Therefore, employing these three variables can effectively predict the risk of suffering from high blood pressure in the future.
