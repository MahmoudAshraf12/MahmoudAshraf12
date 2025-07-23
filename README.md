
### Hi there 👋,

# Mahmoud Ashraf

SELECT 
	NVL(C.PREVIOUS_BRANCH_ID, NULL) AS PREVIOUS_BRANCH_ID,                             -- 1
	
	NVL(C.BRANCH_ID, NULL) AS BRANCH_ID,                                               -- 2
	
	NVL(C.ACCT_NUMBER, NULL) AS ACCT_NUMBER,                                           -- 3
	
	NVL(C.CONSENT_STATUS, NULL) AS CONSENT_STATUS,                                    -- 4
	
	NVL(C.CONSENT_EXPIRY_DATE, '1-jan-9999') AS CONSENT_EXPIRY_DATE,                   -- 5
	
	NVL(C.PRIMARY_CARD_NUMBER, NULL) AS PRIMARY_CARD_NUMBER,                           -- 6
	
	NVL(C.PREVIOUS_ACCOUNT_NUMBER, NULL) AS PREVIOUS_ACCOUNT_NUMBER,                   -- 7
	
	NVL(C.PREVIOUS_PRIMARY_CARD_NUMBER, NULL) AS PREVIOUS_PRIMARY_CARD_NUMBER,         -- 8
	
	NVL(U.DECISION_DATE, NULL) AS APPROVAL_DATE,                                       -- 9
	
	NVL(U.CREDIT_LIMIT, 0) AS CREDIT_LIMIT_APPROVAL_AMOUNT,    					       -- 10
	
	0 AS AMOUNT_OF_INSTALLMENT,               								           -- 11
	
	NVL(C.HIGHEST_CREDIT, NULL) AS HIGHEST_CREDIT,                                     -- 12
	
	NVL(C.CURRENCY, NULL) AS CURRENCY,                                                 -- 13
	
	NULL AS LIABILITY_INDICATOR,                           -- 14
	
	U.NATIONAL_ID || '-' || TO_CHAR (U.DECISION_DATE, 'MMDDYYYY') AS CREDIT_FACILITY_TYPE,     -- 15
	
	0 AS TERM_OF_LOAN,                                         -- 16
	
	NULL AS REPAY_TYPE,   					                                           -- 17
	
	NULL AS FIRST_DISBURS_DATE,      							                       -- 18
	
	0 AS ACCT_BAL,                         					                           -- 19
	
	0 AS LST_AMT_PAID,                   						                       -- 20
	
	0 AS AMT_OVERDUE,                     						                       -- 21
	
	NULL AS N_DAYS_PAST_DUE,   						     				               -- 22
	
	0 AS N_PAY_INSTALL_OVD,     										               --23
	
	NULL AS ASSET_CLASS,     										                   --24
	
	'010' AS ACCT_STATUS,         										               --25
	
	NULL AS DATE_LATEST_PAY_REC,   		                   --26
	
	NULL AS AMEND_DATE,               											       --27
	
	NULL AS SETTL_DATE,      											               --28
	
	NULL AS PROTEST_NOTIFY,    				                   --29
	
	NULL AS PROTEST_NOTIFY_DATE,                   		   --30
	
	0 AS AMT_WRITTEN_OFF,               										       --31
	
	NULL AS WRITTEN_OFF_REASON,    									                   --32
	
	0 AS AMT_FORGIVEN,    										                   --33
	
	NULL AS AMT_FORGIVEN_REASON,      									               --34
	
	NULL AS CLOSING_DATE, 					                       --35
	
	NULL AS CLOSURE_REASON,       					               --36
	
	NULL AS SPECIAL_COMMENTS, 			                       --37
	
	NULL AS SUIT_FILED_STATUS,                		       --38
	
	NULL AS SUIT_REF_NUMBER,                       			   --39
	
	NVL(C.SUIT_AMOUNT, NULL) AS SUIT_AMOUNT,            					           --40
	
	NVL(C.COURT, NULL) AS COURT,               									       --41
	
	NVL(C.COURT_LOCATION, NULL) AS COURT_LOCATION,                				       --42
	
	NVL(C.COURT_DECREE, NULL) AS COURT_DECREE,             					           --43
	
	NVL(C.SUIT_DATE, NULL) AS SUIT_DATE,                						       --44
	
	NVL(C.DECREE_DATE, NULL) AS DECREE_DATE,               						       --45
	
	NVL(C.LEGAL_ACTION_ORIGINATOR, NULL) AS LEGAL_ACTION_ORIGINATOR,                   --46
	
	NVL(C.DISPUTE_COMPLAINT_INTIMATION_N, NULL) AS DISPUTE_COMPLAINT_INTIMATION_N,     --47
	
	NVL(C.DISPUTE_COMPLAINT_STATUS, NULL) AS DISPUTE_COMPLAINT_STATUS,                 --48
	
	NVL(C.TRANSACTION_CODE, NULL) AS TRANSACTION_CODE,                     			   --49
	
	NVL(C.FILLER, NULL) AS FILLER,                  								   --50
	
	NVL(C.SPECIAL_NOTIFY, NULL) AS SPECIAL_NOTIFY, 				                       --51
	
	NVL(C.IDENT_CODE, NULL) AS IDENT_CODE,              					           --52
	
	NVL(C.PREVIOUS_IDENT_CODE, NULL) AS PREVIOUS_IDENT_CODE,   		                   --53
	
	NVL(C.NAT_ID, NULL) AS NAT_ID,               							           --54
	
	NVL(C.IDENT_CODE_1, NULL) AS IDENT_CODE_1,             					           --55
	
	NVL(C.ISSUING_AUTH_1, NULL) AS ISSUING_AUTH_1,              				       --56
	
	NVL(C.IDENT_CODE_1_EXPIRY_DATE, NULL) AS IDENT_CODE_1_EXPIRY_DATE,                 --57
	
	NVL(C.IDENT_CODE_2, NULL) AS IDENT_CODE_2,        					               --58
	
	NVL(C.ISSUING_AUTH_2, NULL) AS ISSUING_AUTH_2,   				                   --59
	
	NVL(C.IDENT_CODE_2_EXPIRY_DATE, NULL) AS IDENT_CODE_2_EXPIRY_DATE,                       --60
	NVL(C.IDENT_CODE_3, NULL) AS IDENT_CODE_3,                       --61
	NVL(C.ISSUING_AUTH_3, NULL) AS ISSUING_AUTH_3,                       --62
	NVL(C.IDENT_CODE_3_EXPIRY_DATE, NULL) AS IDENT_CODE_3_EXPIRY_DATE,                       --63
	NVL(C.LANG_ID, NULL) AS LANG_ID,                       --64
	NVL(C.ENG_FIRST_NM, NULL) AS ENG_FIRST_NM,                       --65
	NVL(C.ENG_MID_NM, NULL) AS ENG_MID_NM,                       --66
	NVL(C.ENG_LST_NM, NULL) AS ENG_LST_NM,                       --67
	NVL(C.ARA_FIRST_NM, NULL) AS ARA_FIRST_NM,                       --68
	NVL(C.ARA_MID_NM, NULL) AS ARA_MID_NM,                       --69
	NVL(C.ARA_LST_NAME, NULL) AS ARA_LST_NAME,                       --70
	NVL(C.PREV_ENG_FIRST_NM, NULL) AS PREV_ENG_FIRST_NM,                       --71
	NVL(C.PREV_ENG_MID_NM, NULL) AS PREV_ENG_MID_NM,                       --72
	NVL(C.PREV_ENG_LST_NM, NULL) AS PREV_ENG_LST_NM,                       --73
	NVL(C.PREV_ARA_FIRST_NM, NULL) AS PREV_ARA_FIRST_NM,                       --74
	NVL(C.PREV_ARA_MID_NM, NULL) AS PREV_ARA_MID_NM,                       --75
	NVL(C.PREV_ARA_LST_NM, NULL) AS PREV_ARA_LST_NM,                       --76
	NVL(C.ADDRESS_1_TYPE, NULL) AS ADDRESS_1_TYPE,                       --77
	NVL(C.ENG_ADD_1_LINE_1, NULL) AS ENG_ADD_1_LINE_1,                       --78
	NVL(C.ENG_ADD_1_LINE_2, NULL) AS ENG_ADD_1_LINE_2,                       --79
	NVL(C.ENG_ADD_1_LINE_3, NULL) AS ENG_ADD_1_LINE_3,                       --80
	NVL(C.ENG_ADD_1_CITY, NULL) AS ENG_ADD_1_CITY,                       --81
	NVL(C.ARA_ADD_1_LINE_1, NULL) AS ARA_ADD_1_LINE_1,                       --82
	NVL(C.ARA_ADD_1_LINE_2, NULL) AS ARA_ADD_1_LINE_2,                       --83
	NVL(C.ARA_ADD_1_LINE_3, NULL) AS ARA_ADD_1_LINE_3,                       --84
	NVL(C.ARA_ADD_1_CITY, NULL) AS ARA_ADD_1_CITY,                       --85
	NVL(C.ADD_1_GOVER_CODE, NULL) AS ADD_1_GOVER_CODE,                       --86
	NVL(C.ADD_1_PO_BOX_NO, NULL) AS ADD_1_PO_BOX_NO,                       --87
	NVL(C.ADD_1_ZIP_CODE, NULL) AS ADD_1_ZIP_CODE,                       --88
	NVL(C.ADD_1_COUNTRY, NULL) AS ADD_1_COUNTRY,                       --89
	NVL(C.ADDRESS_2_TYPE, NULL) AS ADDRESS_2_TYPE,                       --90
	NVL(C.ENG_ADD_2_LINE_1, NULL) AS ENG_ADD_2_LINE_1,                       --91
	NVL(C.ENG_ADD_2_LINE_2, NULL) AS ENG_ADD_2_LINE_2,                       --92
	NVL(C.ENG_ADD_2_LINE_3, NULL) AS ENG_ADD_2_LINE_3,                       --93
	NVL(C.ENG_ADD_2_CITY, NULL) AS ENG_ADD_2_CITY,                       --94
	NVL(C.ARA_ADD_2_LINE_1, NULL) AS ARA_ADD_2_LINE_1,                       --95
	NVL(C.ARA_ADD_2_LINE_2, NULL) AS ARA_ADD_2_LINE_2,                       --96
	NVL(C.ARA_ADD_2_LINE_3, NULL) AS ARA_ADD_2_LINE_3,                       --97
	NVL(C.ARA_ADD_2_CITY, NULL) AS ARA_ADD_2_CITY,                       --98
	NVL(C.ADD_2_GOVER_CODE, NULL) AS ADD_2_GOVER_CODE,                       --99
	NVL(C.ADD_2_PO_BOX_NO, NULL) AS ADD_2_PO_BOX_NO,                       --100
	NVL(C.ADD_2_ZIP_CODE, NULL) AS ADD_2_ZIP_CODE,                       --101
	NVL(C.ADD_2_COUNTRY, NULL) AS ADD_2_COUNTRY,                       --102
	NVL(C.TELE_AREA_CODE, NULL) AS TELE_AREA_CODE,                       --103
	NVL(C.RESID_PHONE, NULL) AS RESID_PHONE,                       --104
	NVL(C.MOBILE, NULL) AS MOBILE,                       --105
	NVL(C.EMAIL, NULL) AS EMAIL,                       --106
	NVL(C.BIRTH_DATE, NULL) AS BIRTH_DATE,                       --107
	NVL(C.GENDER, NULL) AS GENDER,                       --108
	NVL(C.CITIZENSHIP, NULL) AS CITIZENSHIP,                       --109
	NVL(C.MARITAL_STATUS, NULL) AS MARITAL_STATUS,                       --110
	NVL(C.OCCUPATION, NULL) AS OCCUPATION,                       --111
	NVL(C.ENG_EMP_NAME, NULL) AS ENG_EMP_NAME,                       --112
	NVL(C.ARA_EMP_NAME, NULL) AS ARA_EMP_NAME,                       --113
	NVL(C.EMP_COMMERCIAL_REG_ID, NULL) AS EMP_COMMERCIAL_REG_ID,                       --114
	NVL(C.ENG_BUSINESS_ENTITY_NM, NULL) AS ENG_BUSINESS_ENTITY_NM,                       --115
	NVL(C.ARA_BUSINESS_ENTITY_NM, NULL) AS ARA_BUSINESS_ENTITY_NM,                       --116
	NVL(C.MODULE, NULL) AS MODULE,                       --117
	c.dat_process AS DAT_PROCESS,                       --118
	NVL(C.DAT_DSP_AMND, NULL) AS DAT_DSP_AMND,                       --119
	NVL(C.RMRK_DSP_AMND, NULL) AS RMRK_DSP_AMND,                       --120
	NVL(C.ALT_AC_NO, NULL) AS ALT_AC_NO                       --121
	
	FROM approved_unbooked_c_limits_org@OFDM_PROD_TEST U , ERS.ISC_CONSUMER C
	where C.Nat_id(+) = U.National_ID 
#### Data Engineer And BI Developer
I’m Mahmoud Ashraf, BI Developer at BBI Company and Experienced Data Analyst with a strong background in Software Developing 
(Mobile and Web)  and Data Engineering with hands-on experience in Managing Databases, Data 
Warehouses, Informatica Powercenter. 
I thrive on tackling new challenges and diving deep into complex projects.

## Skills and experiance

* ⚡ SQL
* ⚡ Informatica
* ⚡ Python
* ⚡ React 
* ⚡ React Native

## Personal
- 🔭 I’m currently working on BBI as a BI Developer
- 🌱 I Graduated From Faculty of computer and data science 


# Social

[<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/github.svg' alt='github' height='40'>](https://github.com/https://github.com/MahmoudAshraf12)  [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/linkedin.svg' alt='linkedin' height='40'>]([https://www.linkedin.com/in/https://www.linkedin.com/in/mahmoud-ashraf-a51a74239/](https://www.linkedin.com/in/mahmoud-ashraf-a51a74239/))  [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/facebook.svg' alt='facebook' height='40'>](https://www.facebook.com/https://www.facebook.com/profile.php?id=100009080765802)  [<img src='https://cdn.jsdelivr.net/npm/simple-icons@3.0.1/icons/twitter.svg' alt='twitter' height='40'>](https://twitter.com/https://twitter.com/Hooda_ashraf2?t=uI7uNYrZ3rj76zT6qbyY3g&s=09)  

## Stats
[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=MahmoudAshraf12)](https://github.com/anuraghazra/github-readme-stats)
