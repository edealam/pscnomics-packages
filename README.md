## **PSCnomics webApp**

### changeslog:

2024-10-23: ver. 0.1.23
- UI/framework:
  * (*) major update UI cost, json maker, pdf builder, etc
- pyscnomics engine:
  * (?) upgrade to ver. 1.2.0
- filesystem: chg header file = 19
  * (+) lbtUseCalc (option for lbt cost)
  * (+) switch cost record to object 
----------------------------------------------------------------------------------------
2024-10-14: ver. 0.1.22
- UI/framework:
  - (+) ui colapsible column
  - (?) upd. installer/updater
  - (+) upgrade builtin python=3.12.7
  - (?) use latest engine (upd.10/14)
- filesystem: chg header file = 18
  - (+) field: sum_undepreciated_cost
----------------------------------------------------------------------------------------
2024-10-03: ver. 0.1.21
- alias ver. 0.1.20
----------------------------------------------------------------------------------------
2024-10-03: ver. 0.1.20
- UI/framework:
  - (+) case compare list
  - (+) case combine list
  - (?) fix issue export to xlsx (split info)
  - (?) fix issue import from xlsx
  - (+) new updater
----------------------------------------------------------------------------------------

2024-09-15: ver. 0.1.19
- UI/framework:
  * (?/+) major fix/update from feedback
  * (+) case incremental module
  * (+) LBT module 
  * (+) draggable & sort for project list card 
  * (+) tooltips for cost & lifting table
  * (+) h-3dot menu option for table card & chart card
- filesystem:  
  * (+) LBT data table
  * (+) case incr. data config
----------------------------------------------------------------------------------------
2024-08-21: ver. 0.1.18
- UI:
  (?) montecarlo: order column result (90-50-10)
  (?) optimasi: fix "add as new case"
  (+) DMO: unit period
  (?) Lifting: unit mbopy => mstb
  (?) Lifting: hide prod baseline (CR,CR-CR type)
- framework:
  (+) show notif on port inused
  (+) delayed tooltip 
----------------------------------------------------------------------------------------
2024-08-21: ver. 0.1.17
- framework:
  (?) fix pdf viewer
----------------------------------------------------------------------------------------
2024-08-20: ver. 0.1.16
- framework:
  (?) fix json build
----------------------------------------------------------------------------------------
2024-08-19: ver. 0.1.15
- UI & framework:
  (?) update help pdf file
  (+) btn "check for update" (launcher)
----------------------------------------------------------------------------------------
2024-08-15: ver. 0.1.14
- UI & framework:  
  (+) auto check update
  (+) NPV selection Setting
  (+) Help toolbar
  (+) Help Dialogs (masih menggunakan pdf dummy)
  (?) dashboard irr card switch to npv
  (?) minor fix typo
----------------------------------------------------------------------------------------
2024-08-15: ver. 0.1.13
- producer module:  
  (+) LTP & RPD Dialogs (reset fluid data)
- COS module:  
  (+) UI oil_cost_of_sales_applied
  (+) UI gas_cost_of_sales_applied (if has gas)
- Costrec  module:  
  (-) UI oil_cost_of_sales_applied moved
  (-) UI gas_cost_of_sales_applied moved
- GeneralConf module:  
  (+) UI use cost of Sales (CR only)
- dashboard module:  
  (+) UI copy to clipboard (summary)
- filesystem:
   * chg header file = 15
    (+) field: use_COS (GenConf)
    (?) fix COS table writing error
- pyscnomics engine:
  (?) latest update 08/13
----------------------------------------------------------------------------------------
2024-08-06: ver. 0.1.12
- Fiscal module:  
  (=) chg def. profitability_discounted = True
- Costrec module:  
  (+) Input oil_cost_of_sales_applied
  (+) Input gas_cost_of_sales_applied (if has gas)
- Dashboard:  
  (?) fix case list: show evaluator
- Framework:
  (+) cos module
  (?) fix navbar list: depends on contract type
  (+) case combo select: contract type as subtitle
- filesystem:
   * chg header file = 14
    (+) field: oil_cost_of_sales_applied,gas_cost_of_sales_applied (CR)
    (+) table: COS
- pyscnomics engine:
  (?) latest update 08/05
----------------------------------------------------------------------------------------
2024-08-03: ver. 0.1.11
- module sens.:
  (+) table summary, sortable column
  (+) contribution chart
- module compare:
  (?) fix x-axis scale (bar chart)
- pyscnomics engine:
  (?) latest update 08/02
----------------------------------------------------------------------------------------
2024-07-25: ver. 0.1.10
 change AppId: PSCnomics
----------------------------------------------------------------------------------------
2024-07-25: ver. 0.1.9-update.1
- pyscnomics engine:
  (?) latest update 07/25
----------------------------------------------------------------------------------------
2024-07-25: ver. 0.1.9
- module optim:
  (+) parameter "Depreciation Acceleration"
----------------------------------------------------------------------------------------
2024-07-25: ver. 0.1.8
- module optim:
  (+) support transition
- pyscnomics engine:
  (?) latest update 07/24
----------------------------------------------------------------------------------------
2024-07-23: ver. 0.1.7-update.1
- module monte:
  (?) temporary fix for engine
     - patch for "get_multipliers_montecarlo" uniform only set 0 if base=min=max=0       
  (?) fix validator: 
     - set base/mean = (min+max)/2 (if base zero)
     - false for min>base and max<base
  (?) fix adjust lifting (oil only)
- module CF:
  (?) fix transisi display 
- module Sens:
  (-) drop parallel (hit performance)
----------------------------------------------------------------------------------------
2024-07-23: ver. 0.1.7
- case compare:
  (?) fix bar chart tooltip
  (+) cashflow chart
- web engine:
  (+) use dask library for parallel 
  (-) drop joblib library  
----------------------------------------------------------------------------------------
2024-07-21: ver. 0.1.6
- filesystem:
  (?) Hot fix, fail read base field for gas fluid
- sens:
  (?) update filter for base field  
----------------------------------------------------------------------------------------
2024-07-18: ver. 0.1.5
- lifting:
  (*) gas fluid:
    (+) prod_rate = Σ gsa[vol] (if prod_rate===0)
  (*) lifting validator rule:
    (?) oil = (Y && Sales) || (Y && Condensate)
    (+) gas = (Y && gsa[vol] && gsa[ghv])
  (?) fix base values unsaved
- sens module:
  (?) fix price base value for gas
  (?) fix adj. for gas fluid
- monte module:
  (?) fix price base value for gas
- pyscnomics engine used:
  (?) latest update 07/19

----------------------------------------------------------------------------------------
2024-07-18: ver. 0.1.4-update.1
- json maker:
  (?) fix key for prod_rate,lifting_rate switched
  (?) fix lifting filter: zero prices allowed 
- pyscnomics engine used:
  (?) latest update 07/18


----------------------------------------------------------------------------------------
2024-07-18:
- gen.config:
  (-) drop acceleration option
- optimization:
  (+) icon indicator for target
- project list:
  (?) set def. sort to updated_at (desc)
- quicksum card:
  (?) fix drag position 
- Framework:
  (+) remap json keys from engine output
  (?) fix theme for available lang list 
  (?) fix logger text encoding
- pyscnomics engine used:
  (?) latest update 07/17

----------------------------------------------------------------------------------------
2024-07-16:
- Framework:
  (+) logger option, show backend engine logging + detail traceback error
- GS:
  (?) fix issue list of FieldStat,InfAvail,DCUTypeList,H2STypeList depends on regime
- Fiscal  
  (?) fix issue clickable amortization
  (?) fix issue unsave regime
  (?) fix issue unsave profitability_discounted
- UI:
  (+) moveable dialog quicksum card

catatan feedback:
- saat pindah regime permen ke/dari no.8/2017, agar dilihat kembali halaman GS nya,  karena berbeda untuk list FieldStat,InfAvail,DCUTypeList,H2STypeList
- di lifting ada kolom baru prod. baseline, jada saat copas diperhatikan sesuai kolomnya
----------------------------------------------------------------------------------------
2024-07-14:
- montecarlo:
  (?) fix issue memory resources
  (+) calc. progress live
- quicksum card:
  (?) fix issue outside clicked 
----------------------------------------------------------------------------------------
2024-07-13:
- (+) base project support (summary/cashflow/sens/monte)
- lifting:
  (+) column base prod rate
- fiscal:
  (+) regime, profitability_discounted
- montecarlo:
  (=) upd running parallel
- framework:
  (=) move fiscal card to new nav
  (=) upd menu navigation
  (+) the latest engine pyscnomics
  (+) backend: python-3.12.4-embed used
  (-) drop electron browser
  (+) pyscnomics launcher (electron)
- filesystem:
  (=) upd. file dialog browser
   * chg header file = 13
    (+) field: profitability_discounted (Fiscal)
    (+) field: regime (Fiscal) GS Only  
    (+) field: prod_rate_baseline (lifting)
----------------------------------------------------------------------------------------
2024-06-30:
* update vuejs: reconstruct to support electron
* update python-script: reconstruct to support electron
(+) inject electron framework
(=) upgrade python to 3.12
(=) upgrade pyxirr==0.9.3: to support python 3.12
(+) browse file using electron dialogs
(+) chg prec. to 2 digit
(+) major update ui

Note: 
 - Installer Windows: using nsis  (Tested)
 - Installer MacOS: zip extracted (Tested)
 - Installer Linux: comming soon

--------------------------------------------------------------------------------------
2024-6-25:
update webapp:
- HOT FIX savedata: wrong file header used
- upd. quicksumm:
  *(+) GoI2GR, (-) CF
- upd. GenConfig:
  *(+) Delayed/Acceration
- upd. Sensitivity: 
  *(+) Tornado chart
--------------------------------------------------------------------------------------

2024-6-24 Update1:
update webapp:
- upd. UIfw:
  * (+) quick summary toolbar
- upd. UI Fiscal: (+) amortization (fro GS contract)
- upd. filesystem:
  * chg header file = 11
  * update data GS: (+) Field: amortization
- upd. PySCnomics engine terbaru

2024-6-24:
update webapp:
- upd. UIfw:
  * upd. tooltip dict.
- upd. UI case entry:
  * (+) Field: evaluator, evaluation date
- upd. filesystem:
  * chg header file = 10
  * update data case: (+) Field: evaluator, evaluation date
- upd. cashflow:
 * (+) consolidated chart for transition model
 * card considated first  
- upd. optimasi:
 * fix issue save as new case: convert for arr.result, number[] to obj[]
 * upd. pysc.engine (optimization.py): fix issue param w/o vat_rate 
--------------------------------------------------------------------------------------
2024-6-23:
update webapp:
- UI chart:
 * upd. radar chart: fix isssue min-max scale
- upd. lifting:
 * (+) button to calc. onstream year
- upd. optimasi:
 * (+) "create as new case"
 * upd. summ.card: MUSD currency value used
 * upd. pysc.engine: fix issue calc. optim
--------------------------------------------------------------------------------------
2024-6-22 Update 1:
update webapp:
- upd. datasystem: fix issue json for gsa
- upd. dashboard: fix issue performance: calc "card sens. IRR" move to async call
- upd. module economic summary: fix issue create pdf for transition
- upd. PySCnomics engine terbaru

2024-6-22:
update webapp:
- (+) module economic summary: pdf viewer

--------------------------------------------------------------------------------------
2024-6-21:
update webapp:
- upd. cashflow modul: consolidate always shown
- upd. UI: (+) dialog import from excel (popup-menu table), to solve the problem of copas floatprec. from excel
- upd. casecombine.py: fix issue arrange projectyear
- upd. UI: minor fix card collapsed 
--------------------------------------------------------------------------------------
2024-6-19 (Patch 1):
update webapp:
- fix issue table popup menu (readonly): 
  (+) copy & copy with header

2024-6-19:
update webapp:
- upd. dialog combine: 
  * (+) parameter card
  * (+) summary card
- upd. casecombine.py: use user input params 
- upd. filesystem: 
  * chg header file = 9
  * update data combine: (+) inflation, disc.rate, disc year, disc mode, npv mode
- fix issue save project
--------------------------------------------------------------------------------------
2024-6-17 (Patch 1):
update backend:
- fix issue numpy library: ver. 1.26.4 used

2024-6-17:
update webapp:
- upd dashboard: (+)"Case combine"
- major update display UI
- (+) min-max validator for % input
- upd. filesystem: 
  * chg header file = 8
  * (+) compare data
  * (+) combine data
--------------------------------------------------------------------------------------
2024-6-13:
update webapp:
- upd. dashboard: (+) sens-irr card, (+) goi card, (-) tax card
--------------------------------------------------------------------------------------
2024-6-12 (Patch 1):
update webapp:
- upd. compare modul: fix issue display % value
- upd. optimization modul: fix issue display % value
- upd. json maker: fix issue lifting split for gsa (transisiton)
- upd. engine python: 
  *upd. adapter.py: convert to float for int value (cosrec/grosssplit)

2024-6-12:
update webapp:
- upd. project list: (+) dialog for case combine (unfinished)
- upd. case compare: (+) card for bar chart, minor fix table card collapsed
- upd. optimization: (+) card for bar chart, minor fix table card collapsed
- upd. cashflow: fix issue CF table at row summary
--------------------------------------------------------------------------------------
2024-5-31:
update webapp:
- upd. json builder
- upd. CostRec: (+)post_uu_22_year2001 
- upd. GS: (+)cum_production_split_offset 
- upd. filesystem: 
  * chg header file = 7 
  * (+) field post_uu_22_year2001 (PSC)
  * (+) field cum_production_split_offset (GS)
- upd. optimization: fix issue display base value, (+)allow multi values

update Launcher:
- (+) add custom port
- upd. sync state process

update Installer:
- clear static path
--------------------------------------------------------------------------------------
2024-5-29:
update webapp:
- (+)optimization module
- upd filesystem: (+)optim. data
- upd. uncertainty: fix issue show dropdown menu
--------------------------------------------------------------------------------------
2024-5-26:
update webapp:
- upd dashboard: (+)"Case comparison"
- upd filesystem: (+)sens. data, (+)data/result montecarlo, (+)allow list of drive (psutil lib. used)
- upd uncertainty: (+)summary (P10,P50,P90) card
--------------------------------------------------------------------------------------
2024-5-21:
update webapp:
- fix axis scale (sensitivity chart)
- fix axis scale (montecarlo chart)
- upd dashboard, add CF card chart (switch to card gas if exists), fix chart index (exp./tax)
- upd summaries.py, add cf data
- upd id lang

update Launcher:
- fix edgewebview, enable default rightclick menus
--------------------------------------------------------------------------------------
2024-5-19:
update webapp:
- upd dashboard, add card full chart, clickable Card chart,  clickable Pie chart element
- add class summaries.py, fix calc. summaries
- upd CF Chart, remove Gov.CF
- upd id lang
- upd sensitivity, min/max base on entries
- upd fileinfo Card, add copy path btn
- hide console warn (missing, fallback)

--------------------------------------------------------------------------------------
2024-5-17:
update webapp:
- fix issue, unsave pre-tax split (CR)
- fix issue for condensate json generator
- add fileinfo card (fileinfo ribbon)
- upd sidebar: dashboard+project fixed position
- add tooltip for all entries
- add language ribbon 

--------------------------------------------------------------------------------------
2024-5-15:
update webapp:
- major update filesystem, memindahkan penggunaan browser storage (bls) ke local drive (=path "~tmp"), bls hanya menyimpan case active.
- chg file ext. to ".psc"

update workbook vba macro:
- update module "Save_Print_Project", add filter "*.psc" for binary file, "*.pysc" for text file
- fix cost table, translate yes/no (=1 or 0)
--------------------------------------------------------------------------------------
2024-5-10:
update webapp:
- support import case from .pySC (menu in project list)
- fix make json, support empty row/table
- add theme style bordered

update workbook vba macro:
- add module "binary_filesystem", support save/load to binary file
- update module "FromThisWorkbook", mengganti penggunaan activesheet ke assigned sheets(_) dibeberapa sub agar bs digunakan globally
- update module "Save_Print_Project" switch link to load/save binary
--------------------------------------------------------------------------------------
2024-5-4:
update webapp:
- add montecarlo module
- add websokets lib.
- update table editor, fix formula conv. 2 numeric
- upd dashboard, fix pie element value*=1e6 (usd)
- upd sens calc, use parallel

update launcher:
- upd webview, add header ctrl, disable def. context menu, disable dev. tool, add refresh button, add version

--------------------------------------------------------------------------------------
2024-4-29:
- add sensitivity modul
- add exception 2 catch error msg
- upd dashboard, fix chart type, add pie chart
- upd cashflow, fix chart view
- fix grouping data chart
--------------------------------------------------------------------------------------
2024-4-26 Patch 1:
- fix installer package

--------------------------------------------------------------------------------------
2024-4-26:
- add sample "sample-A1.psyc" (hidayah data)
- upd producer, add chart
- upd cost, add chart
- add modul cashflow
- upd dashboard, add exc.summary 
- upd dashboard, add mini card info
- change ext. file to ".pysc"

--------------------------------------------------------------------------------------
2024-4-15:
PySCnomicsApp:
- change struct format for int
- change inc. cheader bin file
- fix add prodnumber for Gas

--------------------------------------------------------------------------------------
2024-4-12:

PySCnomicsApp Setup:
- fix python not in systempath
- fix install requirements

--------------------------------------------------------------------------------------
2024-4-11:
PySCnomicsApp:
- fix save/load multi numprod
- fix browse dialog
- add export json module

PySCnomicsApp Setup:
- remove temporary dirs
--------------------------------------------------------------------------------------
2024-4-10:
PySCnomicsApp:
- add config UI
- add costs UI
- add new, open, save modul

PySCnomicsApp Setup:
- tested

PySCnomicsApp Laucher:
- tested
