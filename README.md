# capacity-planification-tool (KapaTool.update - Version 2.0)
Planification of capacities for production departments (Onejoon GmbH)

# Introduction

The KapaTool originates from the need to plan capacities efficiently in production departments.
It was important to efficiently manage and process SAP lists in order to make predictions about
possible deficits or external orders. The programming of an interactive output calendar was founded
as solution to link employee lists with SAP capacities in a relatively short period of time. The
project began in October 2022. The first versions were produced in March 2023 and August 2023,
and the current 2.0 version is now fully usable.

# Usability

Three main steps are relevant by using the KapaTool software:
    1. Filling out the Excel input file
    2. Saving the Input file on a Server
    3. Analysis of inventories in the output calendar.
The following is a detailled explanation.

## How to fill the Excel Input file

The responsible persons of the different production departments receive the "in.xlsm" Input file
(Excel Workbook with macros) with personal passwords. The "in.xlsm" file is readable and fillable
exclusively with help of a valid password.

![Bildschirmfoto 2024-01-27 um 10 49 01](https://github.com/etchoum/capacity-planification-tool/assets/93908331/d78752ef-edc7-4913-8fc4-c9bc3f73f5cd)

Then a message appears stating that the author prefers read-only opening. If the user wants to
change special parameters in the folder, he/she should select "No". If "Yes" is selected, it will not
be possible to save the file when closing it.

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

![Bildschirmfoto 2024-01-27 um 10 54 04](https://github.com/etchoum/capacity-planification-tool/assets/93908331/d99740ab-91b7-4cbf-a164-377be2bd26a6)
![Bildschirmfoto 2024-01-27 um 10 55 37](https://github.com/etchoum/capacity-planification-tool/assets/93908331/2cab8fbf-aab1-4621-a6f0-01b4a86d3719)

Projects can be assigned to employees [see Figure 6]. The program follows the specified parameters
exactly. Because both departments switchgear manufacture and kiln construction are preferred,
some employees could sometimes become no project attributed. This situation can be averted by
checking the box „AUTOMATIC FILL“, so that all remaining work projects are automatically
distributed.

![Bildschirmfoto 2024-01-27 um 10 56 41](https://github.com/etchoum/capacity-planification-tool/assets/93908331/ab94e7a9-1c1a-40ec-9058-f2a6d8a237b0)

The following informations may prove to be helpful for the correct allocation of capacities.

## How to save the Input file onto a server

## Security procedures, Sustainability

# Output Calendar, Analysis of Inventories 

