
# Capacity-planification-tool (KapaTool.update - Version 2.0) <br>   
## Planification of capacities for production departments (Onejoon GmbH)

# Introduction

The KapaTool originates from the need to plan capacities efficiently in production departments.
It was important to efficiently manage and process SAP lists in order to make predictions about
possible deficits or external orders. The programming of an interactive output calendar was founded
as solution to link employee lists with SAP capacities in a relatively short period of time. The
project began in October 2022. The first versions were produced in March 2023 and August 2023,
and the current 2.0 version is now fully usable.

# Usability

#

Three main steps are relevant by using the KapaTool software:

    1. Filling out the Excel input file
    
    2. Saving the Input file on a Server
    
    3. Analysis of inventories in the output calendar.

The following is a detailled explanation.

#### How to fill the Excel Input file

The responsible persons of the different production departments receive the "in.xlsm" Input file
(Excel Workbook with macros) with personal passwords. The "in.xlsm" file is readable and fillable
exclusively with help of a valid password.

#

![Bildschirmfoto 2024-01-27 um 10 49 01](https://github.com/etchoum/capacity-planification-tool/assets/93908331/d78752ef-edc7-4913-8fc4-c9bc3f73f5cd)

Then a message appears stating that the author prefers read-only opening. If the user wants to
change special parameters in the folder, he/she should select "No". If "Yes" is selected, it will not
be possible to save the file when closing it.

#

![Bildschirmfoto 2024-01-27 um 10 50 01](https://github.com/etchoum/capacity-planification-tool/assets/93908331/a3eb9214-0dda-42bf-9f59-5a5a80866e35)

If the password is entered successfully, the folder opens automatically with the following planning
parameters to be filled in:

    • Projects, Orders or PSP-Elements in any order, comma-separated (with freely selectable
colors [See Figure 3 right])

    • number of working days in the week (5 - 6)
    
    • number of employees to plan (1 - 50)
    
    • maximal number of working hours daily (6 - 10)
    
    • maximal time capacity weekly (1 - 500)
    
    • number of weeks to plan ( 1 - 30)
    
    • status of the projects (whether open, already started or already finished),
    
    • and whether the program should avoid empty Boxes.

#

![Bildschirmfoto 2024-01-27 um 10 54 04](https://github.com/etchoum/capacity-planification-tool/assets/93908331/d99740ab-91b7-4cbf-a164-377be2bd26a6)
![Bildschirmfoto 2024-01-27 um 10 55 37](https://github.com/etchoum/capacity-planification-tool/assets/93908331/2cab8fbf-aab1-4621-a6f0-01b4a86d3719)

#

Projects can be assigned to employees [see Figure 6]. The program follows the specified parameters
exactly. Because both departments switchgear manufacture and kiln construction are preferred,
some employees could sometimes become no project attributed. This situation can be averted by
checking the box „AUTOMATIC FILL“, so that all remaining work projects are automatically
distributed.

#

![Bildschirmfoto 2024-01-27 um 10 56 41](https://github.com/etchoum/capacity-planification-tool/assets/93908331/ab94e7a9-1c1a-40ec-9058-f2a6d8a237b0)

#

The following informations may prove to be helpful for the correct allocation of capacities.

#

#### How to save the Input file onto a server

#

The Kapa-Software offers three execution buttons:

    • Automatic storage on the onejoon server (link: ’/opt/kapa/data/in/in.xlt’)

    • Automatic updating of SAP capacity lists (from source: ’/opt/kapa/data/sap/export.xlsx’)

    • Automatic processing of the Python script with reference to the completed input parameter.

#

![Bildschirmfoto 2024-01-27 um 10 57 14](https://github.com/etchoum/capacity-planification-tool/assets/93908331/c136c023-56be-481d-8764-93ddd4dcd57f)

#

After successfully filling in the relevant parameters, the employee availabilities also remain to be
filled in. Employee names are specified in advance according to the various departments and can
2
be changed by first removing the sheet protection (each department has its own protection code).
After changing the own list of employee the password Workbook should immediately be protected
again.

#

![Bildschirmfoto 2024-01-27 um 10 57 55](https://github.com/etchoum/capacity-planification-tool/assets/93908331/08a0e6e7-9bae-4f19-87e1-0db336b574c4)

As a rule, the user should specify here in the following order

    1. which object type is concerned for the respective employee. Possible selections are „PROJECT“, „PSP“or „ORDER“. The software offers an automatic selective option to predefine objects based on the updated source table on the right.

    2. up to three different calendar weeks ...

    3. in which the employee can be reported as being in „BUSINESS-TRIP“, „HOLIDAY“, „SICK“, or in „TRAINING“,

    4. as well as the days on which these prescriptions are to take place.

Note: The KapaTool takes year ends and only current and up-coming calendar weeks and days
into account to ensure accuracy in the data generated from the output calendar.

![Bildschirmfoto 2024-01-27 um 10 59 26](https://github.com/etchoum/capacity-planification-tool/assets/93908331/67409aee-b7c1-4e0e-aefe-9549c041b86d)

![Bildschirmfoto 2024-01-27 um 11 01 17](https://github.com/etchoum/capacity-planification-tool/assets/93908331/b68490e9-86f8-4ae3-8ea9-7febced2c381)



#### Security procedures, Sustainability

#

The software does not necessarily need all open areas in the Team Management section to be
closed to work efficiently. In some cases, however, it may be necessary to keep the names of the
departments safe from external view. In this case, first collapsing all open areas would be required
for this function to be successful [see Figure 8 right].

#

![Bildschirmfoto 2024-01-27 um 16 47 58](https://github.com/etchoum/capacity-planification-tool/assets/93908331/a186b26b-f76a-4117-9a69-ce8252e9df24)

#

The input file contains three analogous attached workbooks with names resp. „Projects&transaction
quantities“, „DATA“(updated SAP lists), and „Time series“. These are used to immediately view
the working flow and capacities according to the status specified in the input file, their develop-
ment over time. They can only be edited by removing the respective sheet protection using the
respective sheet password, and automatically updated by pressing the „REFRESH LIST“- button
[See Figure 5]


![Bildschirmfoto 2024-01-27 um 16 49 58](https://github.com/etchoum/capacity-planification-tool/assets/93908331/d1c7aa84-38c4-4e7e-b58e-6ef611a13f7d)

![Bildschirmfoto 2024-01-27 um 16 50 32](https://github.com/etchoum/capacity-planification-tool/assets/93908331/22a2e6d6-7090-470f-944f-35c430a73ac8)


# Output Calendar, Analysis of Inventories 

After all parameters have been successfully entered in the input file, an output file is placed in the
output directory after two minutes if the „ACCEPT“-button is pressed.

The created calendar mainly consists of three parts:

    • An introduction with all important input parameters as well as an explanation of some derivations of these parameters as well (e.g data, time, total working hours per project, effective and remaining working hours).

#

![Bildschirmfoto 2024-01-27 um 17 01 03](https://github.com/etchoum/capacity-planification-tool/assets/93908331/dd9df18f-02f3-47c0-8bcb-ea9e604ae7b8)

#

    • The calendar itself with specifications of the input

#

![Bildschirmfoto 2024-01-27 um 17 22 28](https://github.com/etchoum/capacity-planification-tool/assets/93908331/66e1a8e8-016a-4297-bbcd-acffdc50fbc2)

#

    • An area for the analysis of inventories with summations from related calendar weeks, and graphs for an improved view of the project development, as well as an upper limit for the maximum weekly specified workloads in each case

#

![Bildschirmfoto 2024-01-27 um 17 03 26](https://github.com/etchoum/capacity-planification-tool/assets/93908331/c76458b1-ed7d-4207-b70c-0b5b528e8e57)

#

    • For better overview, the grafics can be updated according to maximum weekly capacity utilization, for example

#

![Bildschirmfoto 2024-01-27 um 17 04 39](https://github.com/etchoum/capacity-planification-tool/assets/93908331/e1b50558-e7d9-4320-a8dd-49e016729558)

#

    • The maximum utilization time is flexible and some target workstations are not assigned according to the designations 63*, 64* or 65* [See Figure 16 and 17].

#

![Bildschirmfoto 2024-01-27 um 17 05 29](https://github.com/etchoum/capacity-planification-tool/assets/93908331/169018ca-ba0e-4ead-953f-7f117ef7a813)

#

    • A related workbook with the selected data set for rapid search is also available

#

![Bildschirmfoto 2024-01-27 um 17 11 58](https://github.com/etchoum/capacity-planification-tool/assets/93908331/05527d8c-34a7-4d3d-a5cf-700fa142faf2)

#

    • Complete workbook for a quick overview and comparison

#

![Bildschirmfoto 2024-01-27 um 17 13 21](https://github.com/etchoum/capacity-planification-tool/assets/93908331/c087e86c-15dc-4aad-aecb-3936870f71e6)

#


# Conclusion

#

The complete process can be described in nine main steps, whereas the last one counts for the
repetition of the complete algorithm.
In summary, the following main steps are observed:

#

![Bildschirmfoto 2024-01-27 um 17 43 51](https://github.com/etchoum/capacity-planification-tool/assets/93908331/44868ce0-e217-4021-bd69-70c066164212)




