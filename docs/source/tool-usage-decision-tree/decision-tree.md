# Decision Tree

```{mermaid}
flowchart TD
    A[Analytics Work]
    ETL[Is the work an ETL Process?]
    A --> ETL
        ETL_0[Are multiple databases / file types required?]
        ETL -- Yes --> ETL_0
            ETL_0_0[Will it be required more than once?]
            ETL_0 -- Yes --> ETL_0_0
                ETL_0_0_0[Alteryx\nSAS\nSQL]
                ETL_0_0 -- No --> ETL_0_0_0
                ETL_0_0_1[Automate vie\nAlteryx\nSAS]
                ETL_0_0 -- yes --> ETL_0_0_1
        ETL_1[Will it be required more than once?]
        ETL_0 -- No --> ETL_1
            ETL_1_0[Alteryx\nSAS\nSQL]
            ETL_1 -- No --> ETL_1_0
            ETL_1_1[Automate vie\nAlteryx\nSAS]
            ETL_1 -- yes --> ETL_1_1

    DATA[Is the work a request for data?]
    ETL -- No --> DATA
        DATA_0[Will it be reuired more than once?]
        DATA -- No --> DATA_0
            DATA_0_0[Excel/CSV output]
            DATA_0 -- No --> DATA_0_0
        DATA_1[Is the end user an internal employee?]
        DATA_0 -- Yes --> DATA_1
            DATA_1_0[Excel/CSV output]
            DATA_1 -- No --> DATA_1_0
        DATA_2[Does the data need to provided on a predined schedule?]
        DATA_1 -- Yes --> DATA_2
            DATA_2_0[Alteryx Analytical Application]
            DATA_2 -- No --> DATA_2_0
            DATA_2_1[Automate and Schedule\nALteryx\nSAS]
            DATA_2 -- Yes --> DATA_2_1

    VIZ[Is the work a request for a visualisation/Dashboard?]
    DATA -- No --> VIZ
        VIZ_0[Will it be required more than once?]
        VIZ -- No --> VIZ_0
            VIZ_0_0[Excel\nPowerPoint\nTableau]
            VIZ_0 -- No --> VIZ_0_0
        VIZ_1[Is the end user an internal employee?]
        VIZ_0 -- Yes --> VIZ_1
            VIZ_1_0[Automated Excel\nPowerPoint\nAlteryx Report Output]
            VIZ_1 -- No --> VIZ_1_0
        VIZ_2[Does the output need to be self service?]
        VIZ_1 -- Yes --> VIZ_2
            VIZ_2_0[Automated Excel\nPowerpoint\nTableau]
            VIZ_2 -- No --> VIZ_2_0
            VIZ_2_1[Automated Tableau Dashboard]
            VIZ_2 -- Yes --> VIZ_2_1


    DD[Is the work a request for a Deep Dive investigation?]
    VIZ -- No --> DD

```



## testing nesting 

### is this visible
