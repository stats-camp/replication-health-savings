Package documentation adapted for stats.camp.

American Economic Review

            “Why Don’t the Poor Save More? Evidence from Health Savings Experiments”
                               by Pascaline Dupas and Jonathan Robinson

                                         DATA README FILE

Data Sources
This project was called internally the “HARP” project (Health And Roscas Project).
The data comes from data collected by the authors in and around Bumala Town in Busia District,
Western Kenya. Details on the sampling strategy and timing of the data collection can be found in the
final manuscript.

Four types of data were collected for each individual in the sample:

    (BG) A one-time background survey administered at baseline. This survey includes questions
       on demographics, asset ownership, ROSCA participation, etc. All variables issued from
       this survey have the suffix “bg_”.

    (FOL1) A first follow-up survey conducted after 6 months. All variables from this survey
       have the suffix “fol1_”.

    (FOL1) An endline (second follow-up survey) conducted after 12 months. All variables from
       this survey have the suffix “fol2_”.

    (FOL3) A long-term (third follow-up) survey conducted after 33 months. All variables from
       this survey have the suffix “fol3_”. Only a subset of individuals was sampled for this
       follow-up.

Datasets:

(1) HARP_ROSCA_final.dta.
This dataset includes all four data sources listed above, already merged at the individual level. All
variables are labeled in the dataset. The labels are also shown below.

(2) ROSCA_masterlist.dta.
This dataset includes information at the ROSCA level, including baseline ROSCA characteristics, as well as
information on when the “treatment” (=script) was implemented.

Do-File
Run HARP_analysis.do in stats.camp from data_AER20110911/ to produce the
results in the paper and the appendix. All results are clearly commented in the do-file with the Table number to
which they refer.

                                                    Description of Variables (HARP_ROSCA_final.dta)

Variable Name                      Description
Identifying Information
id_harp_rosca                      ROSCA ID number
id_respondent                      Respondent ID number
group                              experimental group (1‐encouragement (control), 2‐safe box, 3‐lock box, 4‐health pot, 5‐HSA). This variable is at ROSCA level.
encouragement                      = 1 if encouragement treatment. This variable is at the individual level.
safe_box                           = 1 if safe box treatment. This variable is at the individual level.
locked_box                         = 1 if lock box treatment. This variable is at the individual level.
health_pot                         = 1 if health pot treatment. This variable is at the individual level.
health_savings                     = 1 if HSA treatment. This variable is at the individual level.
multitreat                         = 1 if multiple treatments. This variable is at the individual level.
strata                             sampling strata (gender composition, meeting frequency, and whether ROSCA provides credit)
rosbg_monthly_contrib              monthly ROSCA contribution (measured at baseline)

Variables from Background Survey
bg_female                          =1 if female
bg_b1_age                          age
bg_married                         =1 if married
bg_children                        number of children
bg_own_education                   years education
bg_b6_write_kiswahili              =1 if can write in Swahili
bg_cementfloor                     =1 if house has a cement floor (0 if mud)
bg_provider                        =1 if respondent is a "provider" (gave money in the 3 months before baseline but received none)
bg_e1_receive_gift_loan            =1 if respondent received a gift or loan in 3 months before baseline
bg_e3_give_gift_loan               =1 if respondent gave a gift or loan in 3 months before baseline
bg_weekly_income                   reported income in week prior to baseline
bg_childunder5_pr_malaria          percent of children under 5 who had malaria in the month before baseline
bg_resp_malaria                    =1 if respondent had malaria in month before baseline
bg_chlorine                        =1 if treats water with chlorine
bg_c17_bednets_number              number of bednets owned
bg_somewhat_patient                =1 if prefers 55 Ksh or less in 1 month to 40 Ksh today
bg_hyperbolic                      =1 if present‐biased
bg_pat_now_impat_later             =1 if patient now and impatient later
bg_max_discount                    =1 if has maximal discount rate in present and future
bg_invest_choice_risky_asset       amount invested in risky asset which pays off 4 times amount invested with prob. 50% and nothing with prob. 50%
bg_n_roscas                        number of ROSCAs respondent participates in
bg_part_ROSCA_cant_save_alone      =1 if participates in ROSCA because it is difficult to save money alone
bg_part_ROSCA_socialize            =1 if participates in ROSCA to socialize
bg_p1_health_goal                  =1 if respondent reports having a health‐related item they would like to save up for
bg_p2_goal                         If yes, what is the goal?
bg_p3_money_to_save                How much money will it take to reach this goal?
bg_p4_months_reach_goal            How many months will it take to reach this goal?

ROSCA‐level variables at long‐term follow‐up
fol3_rosca_still_exists                 =1 if ROSCA still exists at long‐term follow‐up
fol3_rosca_health_pot                   =1 if ROSCA is running a health pot at long‐term follow‐up
fol3_rosca_hsa                          =1 if ROSCA is running an HSA at long‐term follow‐up

Health investment and illness coping indicators (Follow‐up 2 only)
fol2_amtinvest_healthproduct            Amount invested in health products
fol2_illness_untreated_3mo              =1 if an illness was not fully treated within the previous 3 months
fol2_reached_goal                       =1 if household reached its health savings goal

Take‐up indicators from follow‐up (in all follow‐up rounds)
Note: some variables are only in a subset of the follow‐ups. All variables are prefixed by the follow‐up round (fol1_, fol2_, or fol3_).
sb_has_box                               Safe box group only: do you still have the box?
sb_amt_in_box                            Safe box group only: Amount in box
sb_gavekeyaway                           Safe box group only: Did you give the key away?
sb_gave_box_away                         Safe box group only: Did you give the box away?
sb_spouse_knows_box                      Safe box group only: Does your spouse know about the box?
sb_some_else_contrib                     Safe box group only: Did somebody else contribute to the box?
sb_some_else_access                      Safe box group only: Can somebody else access the box?
sb_helped_save_more                      Safe box group only: Did the box help you save more?
uses_safe_box                            Safe box group only: Dummy for uses the box
sb_save_nonhealth                        Safe box group only: uses box to save for non‐health item
sb_goal                                  Safe box group only: has a goal
sb_goal_emergency                        Safe box group only: goal is for emergencies
sb_goal_business                         Safe box group only: goal is for business
sb_goal_school_fees                      Safe box group only: goal is for school fees
sb_goal_bednet                           Safe box group only: goal is for a bednet
sb_goal_latrine                          Safe box group only: goal is for a latrine
sb_goal_filter                           Safe box group only: goal is for a filter
sb_goal_other_health                     Safe box group only: goal is for another health product
sb_goal_wedding                          Safe box group only: goal is for a wedding
sb_goal_animal                           Safe box group only: goal is for an animal
sb_goal_farm                             Safe box group only: goal is for farm inputs
sb_goal_hh_expense                       Safe box group only: goal is for general household expenses
sb_goal_construct                        Safe box group only: goal is for home construction
sb_goal_other                            Safe box group only: goal is for something else
sb_total_withdraw                        Safe box group only: monetary value of withdrawals
sb_total_withdraw_lot                    Safe box group only: total withdrawals are "a lot"
sb_total_withdraw_little                 Safe box group only: total withdrawals are "a little"
sb_total_deposit                         Safe box group only: monetary value of deposits
sb_total_deposit_lot                     Safe box group only: total deposits are "a lot"
sb_total_deposit_little                  Safe box group only: total deposits are "a little"
sb_box_locked                            Safe box group only: box is locked
l_has_box                                Lock Box group only: do you still have the box?
l_amt_in_box                             Lock Box group only: Amount in box
l_refusekey                              Lock Box group only: Dummy for refusing the key when offered

l_gave_box_away           Lock Box group only: Did you give the box away?
l_spouse_knows_box        Lock Box group only: Does your spouse know about the box?
l_some_else_contrib       Lock Box group only: Did somebody else contribute to the box?
l_some_else_access        Lock Box group only: Can somebody else access the box?
l_helped_save_more        Lock Box group only: Did the box help you save more?
l_called_fo               Lock Box group only: Called program officer to get box opened
uses_lbox                 Lock Box group only: Dummy for uses the box
l_save_nonhealth          Lock Box group only: uses box to save for non‐health item
l_goal                    Lock Box group only: has a goal
l_goal_emergency          Lock Box group only: goal is for emergencies
l_goal_business           Lock Box group only: goal is for business
l_goal_school_fees        Lock Box group only: goal is for school fees
 l_goal_bednet            Lock Box group only: goal is for a bednet
l_goal_latrine            Lock Box group only: goal is for a latrine
l_goal_filter             Lock Box group only: goal is for a filter
l_goal_other_health       Lock Box group only: goal is for another health product
l_goal_wedding            Lock Box group only: goal is for a wedding
l_goal_animal             Lock Box group only: goal is for an animal
l_goal_farm               Lock Box group only: goal is for farming inputs
l_goal_hh_expense         Lock Box group only: goal is for household expenses
l_goal_construct          Lock Box group only: goal is for home construction
l_goal_other              Lock Box group only: goal is for something else
l_total_withdraw          Lock Box group only: monetary value of withdrawals
l_total_withdraw_lot      Lock Box group only: total withdrawals are "a lot"
l_total_withdraw_little   Lock Box group only: total withdrawals are "a little"
l_total_deposit           Lock Box group only: monetary value of deposits
l_total_deposit_lot       Lock Box group only: total deposits are "a lot"
l_total_deposit_little    Lock Box group only: total deposits are "a little"
l_box_locked              Lock Box group only: box is locked
hp_pot_contribute         Health pot group only: contributes to pot
hp_prod_in_kind           Health pot group only: pot is received in‐kind
hp_helped_save_more       Health pot group only: health pot helped you to save more
hp_received_pot           Health pot group only: has received health pot
hp_started_new_pot        Health pot group only: started a new health pot (follow‐up 3 only)
hp_prod_encourage         Health pot group only: did fellow ROSCA members encourage you to buy the given health product?
hp_prod_accompany         Health pot group only: did fellow ROSCA members accompany you to buy the given health product?
hsa_deposit_hsa           Health savings group only: did you deposit into health savings account?
hsa_helped_save_more      Health savings group only: did the health savings account help you to save more?
hsacc_num_deposits        Health savings group only: number of deposits (from HSA records kept at ROSCA)
hsacc_deposit_amount      Health savings group only: amount deposited (from HSA records kept at ROSCA)
hsacc_mean_withdrawal     Health savings group only: average withdrawal size (from HSA records kept at ROSCA)
hsacc_made_wd_account     Health savings group only: made withdrawal (from HSA records kept at ROSCA)
hsacc_balance             Health savings group only: balance (from HSA records kept at ROSCA)
hsa_made_wd               Health savings group only: did you make a withdrawal?
hsa_total_withdraw        Health savings group only: total withdrawals
hsa_wd_emergency          Health savings group only: reason for withdrawal = emergency

hsa_wd_funeral                         Health savings group only: reason for withdrawal = funeral
hsa_wd_prev_health                     Health savings group only: reason for withdrawal = preventative health
hsa_wd_other                           Health savings group only: reason for withdrawal = other

Answers to open‐ended, semi‐qualitative questions (from follow‐ups)
fol1_everyone_obligated_cash          For everyone: on a scale of 1‐5, how obligated are you to give cash to somebody who asks? (higher values = disagree)
fol1_sb_obligated_cash                For safe box group only: on a scale of 1‐5, how obligated are you to give cash when you are holding cash?
fol1_sb_obligated_box                 For safe box group only: on a scale of 1‐5, how obligated are you to give cash when money is in the box?
fol1_l_obligated_cash                 For lock box group only: on a scale of 1‐5, how obligated are you to give cash when you are holding cash?
fol1_l_obligated_box                  For lock box group only: on a scale of 1‐5, how obligated are you to give cash when money is in the box?
fol2_l_talk_rosca_members             For lock box group only: did you talk about box with fellow members?
fol3_sb_why_expensive                 For safe box group only: why didn't you get the box on your own? Answer: too expensive
fol3_sb_why_never_thought             For safe box group only: why didn't you get the box on your own? Answer: never thought of it
fol3_sb_why_theft                     For safe box group only: why didn't you get the box on your own? Answer: worried about theft
fol3_sb_why_otherbox                  For safe box group only: why didn't you get the box on your own? Answer: already have a box
fol3_sb_why_other                     For safe box group only: why didn't you get the box on your own? Answer: other
fol3_sb_easier_say_no_outHH           For safe box group only: does the box make it easier to say no to requests from people outside household?
fol3_sb_easier_say_no_spouse          For safe box group only: does the box make it easier to say no to requests from spouse?
fol3_sb_why_help_invisible            For safe box group only: why does the box help? Money is out of sight
fol3_sb_why_help_coins                For safe box group only: why does the box help? Way to save small coins
fol3_sb_why_help_luxury               For safe box group only: why does the box help? Reduces frivolous spending
fol3_sb_why_help_theft                For safe box group only: why does the box help? Protects from theft
fol3_sb_why_help_refuse_req           For safe box group only: why does the box help? Easier to say no to requests for money.
fol3_sb_why_help_encouraged_sav       For safe box group only: why does the box help? Box itself made me think about saving.
fol3_sb_why_help_save_secret          For safe box group only: why does the box help? The box is secret.
fol3_sb_why_ref_goal                  For safe box group only: why does the box help you refuse requests for money? The money is for a goal.
fol3_sb_why_ref_othersDK              For safe box group only: why does the box help you refuse requests for money? People don't know about box.
fol3_sb_why_ref_box_outside           For safe box group only: why does the box help you refuse requests for money? I keep the box somewhere else.
fol3_sb_why_ref_box_hidden            For safe box group only: why does the box help you refuse requests for money? The box is hidden.
fol3_sb_why_ref_box_mean              For safe box group only: why does the box help you refuse requests for money? "It's easier to be mean."
fol3_sb_why_ref_pretend_nokey         For safe box group only: why does the box help you refuse requests for money? I can pretend not to have the key.
fol3_sb_why_ref_secret                For safe box group only: why does the box help you refuse requests for money? The money is secret.
fol3_l_why_expensive                  For lock box group only: why didn't you get the box on your own? Answer: too expensive
fol3_l_why_never_thought              For lock box group only: why didn't you get the box on your own? Answer: never thought of it
fol3_l_why_theft                      For lock box group only: why didn't you get the box on your own? Answer: worried about theft
fol3_l_why_otherbox                   For lock box group only: why didn't you get the box on your own? Answer: already has box
fol3_l_why_other                      For lock box group only: why didn't you get the box on your own? Answer: other
fol3_l_easier_say_no_outHH            For lock box group only: does the box make it easier to say no to requests from people outside household?
fol3_l_easier_say_no_spouse           For lock box group only: does the box make it easier to say no to requests from spouse?
fol3_l_why_help_invisible             For lock box group only: why does the box help? Money is out of sight
fol3_l_why_help_coins                 For lock box group only: why does the box help? Way to save small coins
fol3_l_why_help_luxury                For lock box group only: why does the box help? Reduces frivolous spending
fol3_l_why_help_theft                 For lock box group only: why does the box help? Protects from theft
fol3_l_why_help_refuse_req            For lock box group only: why does the box help? Easier to say no to requests for money.
fol3_l_why_help_encouraged_sav        For lock box group only: why does the box help? Box itself made me think about saving.
fol3_l_why_help_save_secret           For lock box group only: why does the box help? The box is secret.

fol3_l_why_ref_goal                  For lock box group only: why does the box help you refuse requests for money? The money is for a goal.
fol3_l_why_ref_othersDK              For lock box group only: why does the box help you refuse requests for money? The money is hidden.
fol3_l_why_ref_box_outside           For lock box group only: why does the box help you refuse requests for money? I keep the box somewhere else.
fol3_l_why_ref_box_hidden            For lock box group only: why does the box help you refuse requests for money? The box is hidden.
fol3_l_why_ref_box_mean              For lock box group only: why does the box help you refuse requests for money? "It's easier to be mean."
fol3_l_why_ref_pretend_nokey         For lock box group only: why does the box help you refuse requests for money? I can pretend not to have the key.
fol3_l_why_ref_secret                For lock box group only: why does the box help you refuse requests for money? The money is secret.
fol3_l_possible_get_nonhealth        For lock box group only: did you think it was possible to withdraw money for non‐health reasons?
fol3_hp_why_never_thought            For health pot group only: why didn't ROSCA do this on its own? Answer: never thought of it.
fol3_hp_why_ROSCA_notforhealth       For health pot group only: why didn't ROSCA do this on its own? Answer: ROSCAs are not for health
fol3_hp_pot_collapsed                For health pot group only: did the pot collapse after some time?
fol3_hsa_why_never_thought           For health savings group only: why didn't ROSCA do this on its own? Answer: never thought of it.
fol3_hp_why_ROSCA_notforhealth       For health savings group only: why didn't ROSCA do this on its own? Answer: ROSCAs are not for health
fol3_hsa_others_know                 For health savings group only: did others know how much you were savings?
fol3_hsa_know_what_all_save          For health savings group only: did you know what everybody else was saving?
fol3_hsa_know_what_some_save         For health savings group only: did you know what some of the other people were saving?
fol3_hsa_influenced_by_others        For health savings group only: were your individual savings decisions influenced by others?

Long‐term ROSCA membership measures
fol3_rosca_coll_untrustworthy     If ROSCA collapsed, why? Member untrustworthy
fol3_rosca_coll_members_moved     If ROSCA collapsed, why? Members moved away
fol3_rosca_coll_default           If ROSCA collapsed, why? Somebody defaulted
fol3_rosca_coll_no_money          If ROSCA collapsed, why? People didn't have enough money to keep it going
fol3_rosca_coll_other             If ROSCA collapsed, why? Other
fol3_rosca_still_mem              Are you still a member of the ROSCA?
fol3_rosca_join_new               Have you joined a new ROSCA?
fol3_rosca_leave_any              Have you left any ROSCAs?
fol3_total_roscas                 How many total ROSCAs are you involved in right now?

Other variables
has_followup1                        =1 if appears in 1st followup
has_followup2                        =1 if appears in 2nd followup
has_followup3                        =1 if appears in 3rd followup
