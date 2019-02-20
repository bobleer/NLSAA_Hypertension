# NLSAA_Hypertension

The study on the causes of high blood pressure in Nottingham Longitudinal Study of Activity and Ageing (NLASS)

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

High blood pressure? (Percentage of correct prediction: 78%) | | | | | | 95% C.I. for EXP(B)
:-|-|-|-|-|-|-:

Variable | B | S.E. | Wald | df | Sig. | **Exp(B)** | Lower | Upper
:-|:-|:-|:-|:-|:-|:-|:-|:-
Heart trouble? (1) | -.563 | .185 | 9.304 | 1 | **.002** | **.569** | .396 | .818
Sex of Respondent (1) | -.748 | .189 | 15.604 | 1 | **.000** | **.473** | .327 | .686
Body weight (Kg) | .023 | .006 | 13.821 | 1 | **.000** | **1.023** | 1.011 | 1.036
Leisure Activities (Mins/week) | -.001 | .000 | 3.258 | 1 | .071 | .999 | .998 | 1.000
Anxiety Score (1985) | .020 | .046 | .187 | 1 | .665 | 1.020 | .932 | 1.116
Depression Score (1985) | .029 | .048 | .363 | 1 | .547 | 1.029 | .937 | 1.131
Constant | -2.060 | .438 | 22.139 | 1 | .000 | .127 |  | 

## Result

This study selects nine variables from NLASS dataset which are possibly relevant to high blood pressure. After conducting appropriate and specific statistical analyses, `heart_85`, `sex_85`, `wght_85`, `t_rlx_85`, `anx_85` and `dep_85` are taken for the causes of hypertension. The result of this study partly confirms the experiences from previous researches. Furthermore, `heart_85`, `sex_85`, `wght_85` have significant correlations with `hi_bp_85` in the regression model. Therefore, employing these three variables can effectively predict the risk of suffering from high blood pressure in the future.
