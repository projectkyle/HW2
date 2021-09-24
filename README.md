# HW2

#code

load("acs2017_ny_data.RData")
#glimpse(acs2017_ny) try this later
acs2017_ny[1:10,1:7]

attach(acs2017_ny)

summary(acs2017_ny)

print(NN_obs <- length(AGE))

summary(AGE[female == 1])

summary(AGE[!female])

summary(DEGFIELDD)


#output

AGE female educ_nohs educ_hs educ_somecoll educ_college educ_advdeg
1   72      1         0       0             0            0           1
2   72      0         0       0             0            0           1
3   31      0         0       0             0            1           0
4   28      1         0       0             0            1           0
5   54      0         0       0             0            0           1
6   45      1         0       1             0            0           0
7   84      1         0       0             1            0           0
8   71      0         0       0             0            1           0
9   68      1         0       0             1            0           0
10  37      1         1       0             0            0           0
> attach(acs2017_ny)
The following object is masked _by_ .GlobalEnv:

    OWNCOST

The following objects are masked from dat_NYC:

    AfAm, AGE, Amindian, ANCESTR1, ANCESTR1D, ANCESTR2, ANCESTR2D, Asian, below_150poverty,
    below_200poverty, below_povertyline, BPL, BPLD, BUILTYR2, CITIZEN, CLASSWKR, CLASSWKRD, Commute_bus,
    Commute_car, Commute_other, Commute_rail, Commute_subway, COSTELEC, COSTFUEL, COSTGAS, COSTWATR,
    DEGFIELD, DEGFIELD2, DEGFIELD2D, DEGFIELDD, DEPARTS, EDUC, educ_advdeg, educ_college, educ_hs,
    educ_nohs, educ_somecoll, EDUCD, EMPSTAT, EMPSTATD, FAMSIZE, female, foodstamps, FOODSTMP, FTOTINC,
    FUELHEAT, GQ, has_AnyHealthIns, has_PvtHealthIns, HCOVANY, HCOVPRIV, HHINCOME, Hisp_Cuban, Hisp_DomR,
    Hisp_Mex, Hisp_PR, HISPAN, HISPAND, Hispanic, in_Bronx, in_Brooklyn, in_Manhattan, in_Nassau, in_NYC,
    in_Queens, in_StatenI, in_Westchester, INCTOT, INCWAGE, IND, LABFORCE, LINGISOL, MARST, MIGCOUNTY1,
    MIGPLAC1, MIGPUMA1, MIGRATE1, MIGRATE1D, MORTGAGE, NCHILD, NCHLT5, OCC, OWNCOST, OWNERSHP, OWNERSHPD,
    POVERTY, PUMA, PWPUMA00, RACE, race_oth, RACED, RELATE, RELATED, RENT, ROOMS, SCHOOL, SEX, SSMC,
    TRANTIME, TRANWORK, UHRSWORK, UNITSSTR, unmarried, veteran, VETSTAT, VETSTATD, white, WKSWORK2,
    YRSUSA1

> 
> summary(acs2017_ny)
      AGE            female         educ_nohs        educ_hs       educ_somecoll    educ_college     educ_advdeg   
 Min.   : 0.00   Min.   :0.0000   Min.   :0.000   Min.   :0.0000   Min.   :0.000   Min.   :0.0000   Min.   :0.000  
 1st Qu.:22.00   1st Qu.:0.0000   1st Qu.:0.000   1st Qu.:0.0000   1st Qu.:0.000   1st Qu.:0.0000   1st Qu.:0.000  
 Median :42.00   Median :1.0000   Median :0.000   Median :0.0000   Median :0.000   Median :0.0000   Median :0.000  
 Mean   :41.57   Mean   :0.5156   Mean   :0.271   Mean   :0.2804   Mean   :0.173   Mean   :0.1567   Mean   :0.119  
 3rd Qu.:60.00   3rd Qu.:1.0000   3rd Qu.:1.000   3rd Qu.:1.0000   3rd Qu.:0.000   3rd Qu.:0.0000   3rd Qu.:0.000  
 Max.   :95.00   Max.   :1.0000   Max.   :1.000   Max.   :1.0000   Max.   :1.000   Max.   :1.0000   Max.   :1.000  
                                                                                                                   
               SCHOOL                              EDUC                                                EDUCD      
 N/A              :  5569   Grade 12                 :55119   Regular high school diploma                 :35689  
 No, not in school:144968   4 years of college       :30802   Bachelor's degree                           :30802  
 Yes, in school   : 46048   5+ years of college      :23385   1 or more years of college credit, no degree:19947  
 Missing          :     0   1 year of college        :19947   Master's degree                             :17010  
                            Nursery school to grade 4:14240   Associate's degree, type not specified      :14065  
                            2 years of college       :14065   Some college, but less than 1 year          : 9086  
                            (Other)                  :39027   (Other)                                     :69986  
                                     DEGFIELD                                       DEGFIELDD     
 N/A                                     :142398   N/A                                   :142398  
 Business                                :  9802   Psychology                            :  2926  
 Education Administration and Teaching   :  6708   Business Management and Administration:  2501  
 Social Sciences                         :  4836   Accounting                            :  2284  
 Medical and Health Sciences and Services:  3919   General Education                     :  2238  
 Fine Arts                               :  3491   English Language and Literature       :  2202  
 (Other)                                 : 25431   (Other)                               : 42036  
                                 DEGFIELD2     
 N/A                                  :190425  
 Business                             :   972  
 Social Sciences                      :   853  
 Education Administration and Teaching:   611  
 Fine Arts                            :   465  
 Communications                       :   352  
 (Other)                              :  2907  
                                                           DEGFIELD2D          PUMA            GQ       
 N/A                                                            :190425   Min.   : 100   Min.   :1.000  
 Psychology                                                     :   284   1st Qu.:1500   1st Qu.:1.000  
 Economics                                                      :   260   Median :3201   Median :1.000  
 Political Science and Government                               :   243   Mean   :2713   Mean   :1.148  
 Business Management and Administration                         :   217   3rd Qu.:3902   3rd Qu.:1.000  
 French, German, Latin and Other Common Foreign Language Studies:   205   Max.   :4114   Max.   :5.000  
 (Other)                                                        :  4951                                 
    OWNERSHP       OWNERSHPD        MORTGAGE        OWNCOST           RENT         COSTELEC       COSTGAS    
 Min.   :0.000   Min.   : 0.00   Min.   :0.000   Min.   :    0   Min.   :   0   Min.   :   0   Min.   :   0  
 1st Qu.:1.000   1st Qu.:12.00   1st Qu.:0.000   1st Qu.: 1208   1st Qu.:   0   1st Qu.: 960   1st Qu.: 840  
 Median :1.000   Median :13.00   Median :1.000   Median : 2891   Median :   0   Median :1560   Median :2400  
 Mean   :1.266   Mean   :14.95   Mean   :1.453   Mean   :38582   Mean   : 393   Mean   :2311   Mean   :5032  
 3rd Qu.:2.000   3rd Qu.:22.00   3rd Qu.:3.000   3rd Qu.:99999   3rd Qu.: 630   3rd Qu.:2520   3rd Qu.:9993  
 Max.   :2.000   Max.   :22.00   Max.   :4.000   Max.   :99999   Max.   :3800   Max.   :9997   Max.   :9997  
                                                                                                             
    COSTWATR       COSTFUEL       HHINCOME          FOODSTMP        LINGISOL         ROOMS           BUILTYR2     
 Min.   :   0   Min.   :   0   Min.   : -11800   Min.   :1.000   Min.   :0.000   Min.   : 0.000   Min.   : 0.000  
 1st Qu.: 320   1st Qu.:9993   1st Qu.:  41600   1st Qu.:1.000   1st Qu.:1.000   1st Qu.: 4.000   1st Qu.: 1.000  
 Median :1400   Median :9993   Median :  81700   Median :1.000   Median :1.000   Median : 6.000   Median : 3.000  
 Mean   :4836   Mean   :7935   Mean   : 114902   Mean   :1.147   Mean   :1.002   Mean   : 5.887   Mean   : 3.711  
 3rd Qu.:9993   3rd Qu.:9993   3rd Qu.: 140900   3rd Qu.:1.000   3rd Qu.:1.000   3rd Qu.: 8.000   3rd Qu.: 5.000  
 Max.   :9997   Max.   :9997   Max.   :2030000   Max.   :2.000   Max.   :2.000   Max.   :16.000   Max.   :22.000  
                               NA's   :10630                                                                      
    UNITSSTR        FUELHEAT          SSMC            FAMSIZE           NCHILD           NCHLT5       
 Min.   : 0.00   Min.   :0.000   Min.   :0.00000   Min.   : 1.000   Min.   :0.0000   Min.   :0.00000  
 1st Qu.: 3.00   1st Qu.:2.000   1st Qu.:0.00000   1st Qu.: 2.000   1st Qu.:0.0000   1st Qu.:0.00000  
 Median : 3.00   Median :2.000   Median :0.00000   Median : 3.000   Median :0.0000   Median :0.00000  
 Mean   : 4.39   Mean   :2.959   Mean   :0.01102   Mean   : 3.087   Mean   :0.5009   Mean   :0.08441  
 3rd Qu.: 6.00   3rd Qu.:4.000   3rd Qu.:0.00000   3rd Qu.: 4.000   3rd Qu.:1.0000   3rd Qu.:0.00000  
 Max.   :10.00   Max.   :9.000   Max.   :2.00000   Max.   :19.000   Max.   :9.0000   Max.   :5.00000  
                                                                                                      
     RELATE          RELATED           MARST            RACE          RACED         HISPAN          HISPAND      
 Min.   : 1.000   Min.   : 101.0   Min.   :1.000   Min.   :1.00   Min.   :100   Min.   :0.0000   Min.   :  0.00  
 1st Qu.: 1.000   1st Qu.: 101.0   1st Qu.:1.000   1st Qu.:1.00   1st Qu.:100   1st Qu.:0.0000   1st Qu.:  0.00  
 Median : 2.000   Median : 201.0   Median :5.000   Median :1.00   Median :100   Median :0.0000   Median :  0.00  
 Mean   : 3.307   Mean   : 335.6   Mean   :3.742   Mean   :2.03   Mean   :205   Mean   :0.4153   Mean   : 44.75  
 3rd Qu.: 3.000   3rd Qu.: 301.0   3rd Qu.:6.000   3rd Qu.:2.00   3rd Qu.:200   3rd Qu.:0.0000   3rd Qu.:  0.00  
 Max.   :13.000   Max.   :1301.0   Max.   :6.000   Max.   :9.00   Max.   :990   Max.   :4.0000   Max.   :498.00  
                                                                                                                 
            BPL                         BPLD                            ANCESTR1    
 New York     :128517   New York          :128517   Not Reported            :32021  
 West Indies  :  8481   China             :  4116   Italian                 :20577  
 China        :  4964   Dominican Republic:  3517   Irish, various subheads,:16388  
 SOUTH AMERICA:  4957   Pennsylvania      :  3303   German                  :12781  
 India        :  3476   New Jersey        :  3127   African-American        : 9559  
 Pennsylvania :  3303   Puerto Rico       :  2272   United States           : 8209  
 (Other)      : 42887   (Other)           : 51733   (Other)                 :97050  
                                   ANCESTR1D             ANCESTR2                               ANCESTR2D     
 Not Reported                           :32021   Not Reported:141487   Not Reported                  :141487  
 Italian (1990-2000, ACS, PRCS)         :20577   German      :  9476   German (1990-2000, ACS, PRCS) :  9441  
 Irish                                  :15651   Irish       :  9238   Irish                         :  8809  
 German (1990-2000, ACS/PRCS)           :12605   English     :  4895   English                       :  4895  
 African-American (1990-2000, ACS, PRCS): 9559   Italian     :  4531   Italian (1990-2000, ACS, PRCS):  4531  
 United States                          : 8209   Polish      :  3113   Polish                        :  3113  
 (Other)                                :97963   (Other)     : 23845   (Other)                       : 24309  
    CITIZEN          YRSUSA1          HCOVANY         HCOVPRIV         SEX            EMPSTAT         EMPSTATD    
 Min.   :0.0000   Min.   : 0.000   Min.   :1.000   Min.   :1.000   Male  : 95222   Min.   :0.000   Min.   : 0.00  
 1st Qu.:0.0000   1st Qu.: 0.000   1st Qu.:2.000   1st Qu.:1.000   Female:101363   1st Qu.:1.000   1st Qu.:10.00  
 Median :0.0000   Median : 0.000   Median :2.000   Median :2.000                   Median :1.000   Median :10.00  
 Mean   :0.4793   Mean   : 5.377   Mean   :1.951   Mean   :1.691                   Mean   :1.514   Mean   :15.16  
 3rd Qu.:0.0000   3rd Qu.: 0.000   3rd Qu.:2.000   3rd Qu.:2.000                   3rd Qu.:3.000   3rd Qu.:30.00  
 Max.   :3.0000   Max.   :92.000   Max.   :2.000   Max.   :2.000                   Max.   :3.000   Max.   :30.00  
                                                                                                                  
    LABFORCE          OCC              IND           CLASSWKR       CLASSWKRD        WKSWORK2        UHRSWORK    
 Min.   :0.000   0      : 79987   0      :79987   Min.   :0.000   Min.   : 0.00   Min.   :0.000   Min.   : 0.00  
 1st Qu.:1.000   2310   :  3494   7860   : 9025   1st Qu.:0.000   1st Qu.: 0.00   1st Qu.:0.000   1st Qu.: 0.00  
 Median :2.000   5700   :  3235   8680   : 6354   Median :2.000   Median :22.00   Median :1.000   Median :12.00  
 Mean   :1.331   430    :  3025   770    : 6279   Mean   :1.116   Mean   :13.03   Mean   :2.701   Mean   :19.77  
 3rd Qu.:2.000   4720   :  2666   8190   : 5873   3rd Qu.:2.000   3rd Qu.:22.00   3rd Qu.:6.000   3rd Qu.:40.00  
 Max.   :2.000   4760   :  2563   7870   : 4041   Max.   :2.000   Max.   :29.00   Max.   :6.000   Max.   :99.00  
                 (Other):101615   (Other):85026                                                                  
     INCTOT           FTOTINC           INCWAGE          POVERTY         MIGRATE1       MIGRATE1D    
 Min.   :  -7300   Min.   : -11800   Min.   :     0   Min.   :  0.0   Min.   :0.000   Min.   : 0.00  
 1st Qu.:   8000   1st Qu.:  35550   1st Qu.:     0   1st Qu.:159.0   1st Qu.:1.000   1st Qu.:10.00  
 Median :  25000   Median :  74000   Median : 10000   Median :351.0   Median :1.000   Median :10.00  
 Mean   :  45245   Mean   : 107110   Mean   : 33796   Mean   :318.7   Mean   :1.122   Mean   :11.51  
 3rd Qu.:  56500   3rd Qu.: 132438   3rd Qu.: 47000   3rd Qu.:501.0   3rd Qu.:1.000   3rd Qu.:10.00  
 Max.   :1563000   Max.   :2030000   Max.   :638000   Max.   :501.0   Max.   :4.000   Max.   :40.00  
 NA's   :31129     NA's   :10817     NA's   :33427                                                   
    MIGPLAC1         MIGCOUNTY1         MIGPUMA1        VETSTAT          VETSTATD         PWPUMA00    
 Min.   :  0.000   Min.   :  0.000   Min.   :    0   Min.   :0.0000   Min.   : 0.000   Min.   :    0  
 1st Qu.:  0.000   1st Qu.:  0.000   1st Qu.:    0   1st Qu.:1.0000   1st Qu.:11.000   1st Qu.:    0  
 Median :  0.000   Median :  0.000   Median :    0   Median :1.0000   Median :11.000   Median :    0  
 Mean   :  6.184   Mean   :  4.117   Mean   :  277   Mean   :0.8621   Mean   : 9.412   Mean   : 1255  
 3rd Qu.:  0.000   3rd Qu.:  0.000   3rd Qu.:    0   3rd Qu.:1.0000   3rd Qu.:11.000   3rd Qu.: 3100  
 Max.   :900.000   Max.   :810.000   Max.   :70100   Max.   :2.0000   Max.   :20.000   Max.   :59300  
                                                                                                      
    TRANWORK         TRANTIME         DEPARTS           in_NYC          in_Bronx       in_Manhattan    
 Min.   : 0.000   Min.   :  0.00   Min.   :   0.0   Min.   :0.0000   Min.   :0.0000   Min.   :0.00000  
 1st Qu.: 0.000   1st Qu.:  0.00   1st Qu.:   0.0   1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.00000  
 Median : 0.000   Median :  0.00   Median :   0.0   Median :0.0000   Median :0.0000   Median :0.00000  
 Mean   : 9.725   Mean   : 14.75   Mean   : 373.3   Mean   :0.3615   Mean   :0.0538   Mean   :0.04981  
 3rd Qu.:10.000   3rd Qu.: 20.00   3rd Qu.: 732.0   3rd Qu.:1.0000   3rd Qu.:0.0000   3rd Qu.:0.00000  
 Max.   :70.000   Max.   :138.00   Max.   :2345.0   Max.   :1.0000   Max.   :1.0000   Max.   :1.00000  
                                                                                                       
   in_StatenI       in_Brooklyn      in_Queens      in_Westchester      in_Nassau          Hispanic     
 Min.   :0.00000   Min.   :0.000   Min.   :0.0000   Min.   :0.00000   Min.   :0.00000   Min.   :0.0000  
 1st Qu.:0.00000   1st Qu.:0.000   1st Qu.:0.0000   1st Qu.:0.00000   1st Qu.:0.00000   1st Qu.:0.0000  
 Median :0.00000   Median :0.000   Median :0.0000   Median :0.00000   Median :0.00000   Median :0.0000  
 Mean   :0.02084   Mean   :0.126   Mean   :0.1111   Mean   :0.04413   Mean   :0.07032   Mean   :0.1387  
 3rd Qu.:0.00000   3rd Qu.:0.000   3rd Qu.:0.0000   3rd Qu.:0.00000   3rd Qu.:0.00000   3rd Qu.:0.0000  
 Max.   :1.00000   Max.   :1.000   Max.   :1.0000   Max.   :1.00000   Max.   :1.00000   Max.   :1.0000  
                                                                                                        
    Hisp_Mex          Hisp_PR         Hisp_Cuban         Hisp_DomR           white             AfAm      
 Min.   :0.00000   Min.   :0.0000   Min.   :0.000000   Min.   :0.00000   Min.   :0.0000   Min.   :0.000  
 1st Qu.:0.00000   1st Qu.:0.0000   1st Qu.:0.000000   1st Qu.:0.00000   1st Qu.:0.0000   1st Qu.:0.000  
 Median :0.00000   Median :0.0000   Median :0.000000   Median :0.00000   Median :1.0000   Median :0.000  
 Mean   :0.01626   Mean   :0.0436   Mean   :0.003403   Mean   :0.02827   Mean   :0.6997   Mean   :0.125  
 3rd Qu.:0.00000   3rd Qu.:0.0000   3rd Qu.:0.000000   3rd Qu.:0.00000   3rd Qu.:1.0000   3rd Qu.:0.000  
 Max.   :1.00000   Max.   :1.0000   Max.   :1.000000   Max.   :1.00000   Max.   :1.0000   Max.   :1.000  
                                                                                                         
    Amindian           Asian            race_oth        unmarried       veteran        has_AnyHealthIns
 Min.   :0.00000   Min.   :0.00000   Min.   :0.0000   Min.   :0.00   Min.   :0.00000   Min.   :0.0000  
 1st Qu.:0.00000   1st Qu.:0.00000   1st Qu.:0.0000   1st Qu.:0.00   1st Qu.:0.00000   1st Qu.:1.0000  
 Median :0.00000   Median :0.00000   Median :0.0000   Median :0.00   Median :0.00000   Median :1.0000  
 Mean   :0.00378   Mean   :0.08656   Mean   :0.1324   Mean   :0.45   Mean   :0.04443   Mean   :0.9513  
 3rd Qu.:0.00000   3rd Qu.:0.00000   3rd Qu.:0.0000   3rd Qu.:1.00   3rd Qu.:0.00000   3rd Qu.:1.0000  
 Max.   :1.00000   Max.   :1.00000   Max.   :1.0000   Max.   :1.00   Max.   :1.00000   Max.   :1.0000  
                                                                                                       
 has_PvtHealthIns  Commute_car      Commute_bus      Commute_subway     Commute_rail     Commute_other    
 Min.   :0.0000   Min.   :0.0000   Min.   :0.00000   Min.   :0.00000   Min.   :0.00000   Min.   :0.00000  
 1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.00000   1st Qu.:0.00000   1st Qu.:0.00000   1st Qu.:0.00000  
 Median :1.0000   Median :0.0000   Median :0.00000   Median :0.00000   Median :0.00000   Median :0.00000  
 Mean   :0.6906   Mean   :0.2997   Mean   :0.02162   Mean   :0.07468   Mean   :0.01332   Mean   :0.05506  
 3rd Qu.:1.0000   3rd Qu.:1.0000   3rd Qu.:0.00000   3rd Qu.:0.00000   3rd Qu.:0.00000   3rd Qu.:0.00000  
 Max.   :1.0000   Max.   :1.0000   Max.   :1.00000   Max.   :1.00000   Max.   :1.00000   Max.   :1.00000  
                                                                                                          
 below_povertyline below_150poverty below_200poverty   foodstamps       IND_number   Covid_risk     
 Min.   :0.000     Min.   :0.0000   Min.   :0.0000   Min.   :0.0000   Min.   :   0   Mode :logical  
 1st Qu.:0.000     1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:0.0000   1st Qu.:   0   FALSE:173301   
 Median :0.000     Median :0.0000   Median :0.0000   Median :0.0000   Median :4590   TRUE :22943    
 Mean   :0.122     Mean   :0.1965   Mean   :0.2676   Mean   :0.1465   Mean   :4003   NA's :341      
 3rd Qu.:0.000     3rd Qu.:0.0000   3rd Qu.:1.0000   3rd Qu.:0.0000   3rd Qu.:7860                  
 Max.   :1.000     Max.   :1.0000   Max.   :1.0000   Max.   :1.0000   Max.   :9920                  
                                                                      NA's   :341                   
> summary(AGE[female == 1])
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   0.00   23.00   44.00   42.72   61.00   95.00 
> summary(AGE[!female])
   Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
   0.00   21.00   40.00   40.35   59.00   95.00 
> summary(DEFFIELD2D)
Error in summary(DEFFIELD2D) : object 'DEFFIELD2D' not found
> summary(EDUC)
      N/A or no schooling Nursery school to grade 4       Grade 5, 6, 7, or 8                   Grade 9 
                    11879                     14240                     13079                      4088 
                 Grade 10                  Grade 11                  Grade 12         1 year of college 
                     4644                      5337                     55119                     19947 
       2 years of college        3 years of college        4 years of college       5+ years of college 
                    14065                         0                     30802                     23385 
                    
summary(DEGFIELDD)
                                                            N/A 
                                                         142398 
                                                     Psychology 
                                                           2926 
                         Business Management and Administration 
                                                           2501 
                                                     Accounting 
                                                           2284 
                                              General Education 
                                                           2238 
                                English Language and Literature 
                                                           2202 
                                                        Nursing 
                                                           2028 
                                               General Business 
                                                           1884 
                                           Elementary Education 
                                                           1728 
                                                        Biology 
                                                           1714 
                                                      Economics 
                                                           1574 
                               Political Science and Government 
                                                           1456 
                                                        History 
                                                           1453 
                                                 Communications 
                                                           1188 
                                                        Finance 
                                                           1132 
                               Marketing and Marketing Research 
                                                           1065 
                                               Computer Science 
                                                           1055 
                                                      Sociology 
                                                           1017 
                                                      Fine Arts 
                                                            927 
                           Criminal Justice and Fire Protection 
                                                            884 
                                         Electrical Engineering 
                                                            813 
                                                    Mathematics 
                                                            808 
                                                   Liberal Arts 
                                                            711 
                              Commercial Art and Graphic Design 
                                                            653 
                                                          Music 
                                                            619 
                                                      Chemistry 
                                                            588 
                                         Mechanical Engineering 
                                                            582 
                               Philosophy and Religious Studies 
                                                            523 
                                            General Engineering 
                                                            513 
                                                    Social Work 
                                                            483 
                                                   Architecture 
                                                            442 
                          Multi-disciplinary or General Science 
                                                            437 
                                         Drama and Theater Arts 
                                                            435 
                                  Treatment Therapy Professions 
                                                            401 
                                              Civil Engineering 
                                                            390 
French, German, Latin and Other Common Foreign Language Studies 
                                                            390 
                                                     Journalism 
                                                            387 
                         Physical and Health Education Teaching 
                                                            385 
                                   Language and Drama Education 
                                                            371 
                                        Special Needs Education 
                                                            358 
                                                     Mass Media 
                                                            343 
                                                        Physics 
                                                            339 
                                        Art and Music Education 
                                                            328 
                              Film, Video and Photographic Arts 
                                                            309 
                  Communication Disorders Sciences and Services 
                                                            295 
                               Computer and Information Systems 
                                                            284 
                                   Family and Consumer Sciences 
                                                            272 
          Pharmacy, Pharmaceutical Sciences, and Administration 
                                                            269 
                                    Anthropology and Archeology 
                                                            265 
               Physical Fitness, Parks, Recreation, and Leisure 
                                                            264 
                               Theology and Religious Vocations 
                                                            259 
                         Area, Ethnic, and Civilization Studies 
                                                            258 
                                      Art History and Criticism 
                                                            258 
                                      Early Childhood Education 
                                                            246 
                                           Chemical Engineering 
                                                            224 
                                    Secondary Teacher Education 
                                                            220 
                                        Miscellaneous Education 
                                                            220 
                    Social Science or History Teacher Education 
                                                            207 
                            General Medical and Health Services 
                                                            206 
                                         Hospitality Management 
                                                            203 
                       Human Resources and Personnel Management 
                                                            195 
                               Advertising and Public Relations 
                                                            187 
                      Human Services and Community Organization 
                                                            185 
                                           Biochemical Sciences 
                                                            181 
                                        International Relations 
                                                            181 
                                           Computer Engineering 
                                                            179 
                                          Environmental Science 
                                                            176 
            Linguistics and Comparative Language and Literature 
                                                            167 
                               Medical Technologies Technicians 
                                                            166 
                     Health and Medical Administrative Services 
                                                            160 
                                        General Social Sciences 
                                                            159 
                        Health and Medical Preparatory Programs 
                                                            149 
                  Management Information Systems and Statistics 
                                                            145 
                                      Geology and Earth Science 
                                                            144 
                                     Visual and Performing Arts 
                                                            141 
                                                    Studio Arts 
                                                            132 
                                  Mathematics Teacher Education 
                                                            131 
                                        Other Foreign Languages 
                                                            126 
                                         International Business 
                                                            120 
                                      Pre-Law and Legal Studies 
                                                            117 
                            Teacher Education:  Multiple Levels 
                                                            115 
                        Intercultural and International Studies 
                                                            114 
                                         Composition and Speech 
                                                            113 
                                             Business Economics 
                                                            112 
                       Miscellaneous Health Medical Professions 
                                                            110 
                       Industrial and Manufacturing Engineering 
                                                            104 
                                                      Geography 
                                                            103 
                                    Community and Public Health 
                                                            102 
                        Science  and Computer Teacher Education 
                                                            101 
                                       Miscellaneous Psychology 
                                                             97 
                                           Information Sciences 
                                                             93 
              Miscellaneous Business and Medical Administration 
                                                             90 
                                             Nutrition Sciences 
                                                             87 
                              Interdisciplinary Social Sciences 
                                                             84 
                       Transportation Sciences and Technologies 
                                                             84 
                                     Communication Technologies 
                                                             79 
                                                Animal Sciences 
                                                             76 
                                      Miscellaneous Engineering 
                                                             76 
                              Electrical Engineering Technology 
                                                             73 
                                                        (Other) 
                                                           2419 
