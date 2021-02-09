EDAM 1.a - Configuration Guide
==============================

Configs for restricting me= tadata edit of an asset in QA, UAT, PRODThe following document conta= ins the list of configurations that are utilized for EDAM 1.a project.

**Story :**

[TRISUL-348](3D"https://jira.wsgc.com/browse/TRISUL-348") : WS Rollout - Create and Configure Groups/Privileges on Dev

ThirdPartyContributorConfig for WS DEV environment : 

com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~wstpUsers\<= /td\>

Following custom configuration's are required for creating 3rd-part= y-group folder for WS Third Party Users in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~wstpUs= ers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(Dev)

brand.path=

/content/dam/williams-sonoma

third.part= y.folder

3rd-party-group

third.part= y.groups

APR\_EDAM\_DEV\_WS\_3rdPartyContributor

other.allowed.groups

APR\_EDAM\_DEV\_WS\_PRODUCTION

[TRISUL](3D"https://jira.wsgc.com/browse/TRISUL-348")[-573](3D"https://jira.wsgc.com/browse/TRIS=) : WS Rollout - Create and Configure Groups/P= rivileges for all envs

ThirdPartyContributorConfig for WS QA, WS UAT and WS PROD environments = :

com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~wstpUsers\<= /td\>

Following custom configuration's are required for creating 3rd-part= y-group folder for WS Third Party Users in QA, UAT and PRODUCTION envi= ronment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~wstpUs= ers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(QA)

Config = Value(UAT)

Config = Value(Prod)

brand.path=

/content/dam/williams-sonoma

/content/dam/williams-sonoma

/content/dam/williams-sonoma

third.part= y.folder

3rd-party-group

3rd-party-group

3rd-party-group

third.part= y.groups

APR\_EDAM\_QA\_W= S\_3rdPartyContributor

APR\_EDAM\_UAT\_= WS\_3rdPartyContributor

APR\_EDAM\_WS\_3= rdPartyContributor

other.allowed.groups

APR\_EDAM\_QA\_WS\_PRODUCTION

APR\_EDAM\_UAT\_WS\_PRODUCTION

APR\_EDAM\_WS\_PRODUCTION

**Story :**

[TRISUL-354](3D"https://jira.wsgc.com/browse/TRISUL-354") : PB Rollout - Create and Configure Groups/Privileges for Dev

ThirdPartyContributorConfig for PB Main in Dev environment = :

||
|com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~pbMainTpUs= ers|

Following custom configuration's are required for creating photogra= phers folder for PB Main Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~pbMain= TpUsers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(Dev)

brand.path=

/content/dam/pottery-barn/main

third.part= y.folder

photographers

third.part= y.groups

APR\_EDAM\_DEV\_PB\_PHOTOGRAPHERS

other.allowed.groups

APR\_EDAM\_DEV\_PB\_PRODUCTION

ThirdPartyContributorConfig for PB KIDS in Dev environment = :

||
|com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~pbKidsTpUs= ers|

Following custom configuration's are required for creating photogra= phers folder for PB Kids Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~pbKids= TpUsers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(Dev)

brand.path=

/content/dam/pottery-barn/kids

third.part= y.folder

photographers

third.part= y.groups

APR\_EDAM\_DEV\_= PK\_Photographers

other.allowed.groups

APR\_EDAM\_D= EV\_PK\_Production

ThirdPartyContributorConfig for PB TEEN in Dev environ= ment :

||
|com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~pbTeenTpUs= ers|

Following custom configuration's are required for creating photogra= phers folder for PB Teen Photographers in Dev environment.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~pbTeen= TpUsers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(Dev)

brand.path=

/content/dam/pottery-barn/teen

third.part= y.folder

photographers

third.part= y.groups

APR\_EDAM\_DEV\_= PT\_Photographers

other.allowed.groups

APR\_EDAM\_D= EV\_PT\_Production

Dam metadata update listener confi= g for Dev environment :

||
|com.wsgc.ecommerce.e= dam.core.listeners.DamMetadataUpdateListener|

Following custom configuration's are required for Approved Asset Viewers= .

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "Dam metada= ta update listener config" and click on it.

Following are config param name and corresponding values for WE,PB Main,= Kids, Teen brands.

Config = Param

Config = Value(Dev)

approved.asset.viewers

/content/dam/west-elm=3DAPR\_EDAM\_DEV\_WE\_MERCH= ANTS,APR\_EDAM\_DEV\_WE\_GENERAL,APR\_EDAM\_DEV\_WE\_VENDORS
/content/dam/potter= y-barn/main=3DAPR\_EDAM\_DEV\_PB\_GeneralUse= rs,APR\_EDAM\_DEV\_PB\_FRANCHISE
/content/dam/pottery-barn/kids=3DAPR\_EDAM\_DEV\_PK\_GeneralUsers,APR\_EDAM\_DEV\_PK\_Franchise
/content/da= m/pottery-barn/teen=3DAPR\_EDAM\_DEV\_PT\_Ge= neralUsers,APR\_EDAM\_DEV\_PT\_Franch= ise

Configs for restricting metadata edit of an asset in DEV environment :

||
|com.wsgc.ecommerce.e= dam.core.listeners.RestrictEditMetaData|

Following custom configuration's are required for Approved Asset Viewers= .

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "RestrictEd= itMetaData" and click on it.

Following are config param name and corresponding values for PB.

Config = Param

Config = Value(Dev)

editRestri= ctGroups

APR\_EDAM\_D= EV\_PB\_PRSocial

APR\_EDAM\_DEV= \_PT\_PRSocial

APR\_EDAM\_DEV\_P= K\_PRSocial

**Story :**

[TRISUL](3D"https://jira.wsgc.com/browse/TRISUL-348")[-574](3D"https://jira.wsgc.com/browse/TRIS=) : PB Rollout - Create and Configure Groups/P= rivileges for all the environments

ThirdPartyContributorConfig for PB Main QA, PB Main UAT and P= B Main PROD environments :

||
|com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~pbMainTpUs= ers|

Following custom configuration's are required for creating photogra= phers folder for PB Main Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~pbMain= TpUsers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(QA)

Config = Value(UAT)

Config = Value(Prod)

brand.path=

/content/dam/pottery-barn/main

/content/dam/pottery-barn/main

/content/dam/pottery-barn/main

third.part= y.folder

photographers

photographers

photographers

third.part= y.groups

APR\_EDAM\_QA\_PB\_PHOTOGRAPHERS

APR\_EDAM\_UAT\_PB\_PHOTOGRAPHERS

APR\_EDAM\_PB\_PHOTOGRAPHERS

other.allowed.groups

APR\_EDAM\_QA\_PB\_PRODUCTION

APR\_EDAM\_UAT\_PB\_PRODUCTION

APR\_EDAM\_PB\_PRODUCTION

ThirdPartyContributorConfig for PB Kids QA, PB Kids UAT and&n= bsp;PB Kids PROD environments :

||
|com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~pbKidsTpUs= ers|

Following custom configuration's are required for creating photogra= phers folder for PB Kids Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~pbKids= TpUsers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(QA)

Config = Value(UAT)

Config = Value(Prod)

brand.path=

/content/dam/pottery-barn/kids

/content/dam/pottery-barn/kids

/content/dam/pottery-barn/kids

third.part= y.folder

photographers

photographers

photographers

third.part= y.groups

APR\_EDAM\_QA\_P= K\_Photographers

APR\_EDAM\_UAT\_PK\_Photographers

APR\_EDAM\_PK\_P= hotographers

other.allowed.groups

APR\_EDAM\_QA\_P= K\_Production

APR\_EDAM\_UAT\_= PK\_Production

APR\_EDAM\_PK\_Production       

ThirdPartyContributorConfig for PB Teen QA, PB Teen UAT and&n= bsp;PB Teen PROD environments :

||
|com.wsgc.ecommerce.e= dam.core.services.impl.ThirdPartyContributorConfigServiceFactory\~pbMainTpUs= ers|

Following custom configuration's are required for creating photogra= phers folder for PB Teen Photographers in QA, UAT and PROD environments.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "ThirdPartyContributorConfigServiceFactory\~pbTeen= TpUsers" and click on it.

Following are config param names and corresponding values.

Config = Param

Config = Value(QA)

Config = Value(UAT)

Config = Value(Prod)

brand.path=

/content/dam/pottery-barn/teen

/content/dam/pottery-barn/teen

/content/dam/pottery-barn/teen

third.part= y.folder

photographers

photographers

photographers

third.part= y.groups

APR\_EDAM\_QA\_P= T\_Photographers

APR\_EDAM\_UAT\_= PT\_Photographers

APR\_EDAM\_PT\_P= hotographers

other.allowed.groups

APR\_EDAM\_QA\_P= T\_Production

APR\_EDAM\_UAT\_= PT\_Production

APR\_EDAM\_PT\_P= roduction

Dam metadata update listener confi= g for QA, UAT, PROD environments :

||
|com.wsgc.ecommerce.e= dam.core.listeners.DamMetadataUpdateListener|

Following custom configuration's are required for Approved Asset Viewers= .

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "Dam metada= ta update listener config" and click on it.

Following are config param name and corresponding values for WE,PB Main,= Kids, Teen brands in QA,UAT and PROD environment

Config = Param

Config = Value(QA)

approved.asset.viewers

/content/dam/west-elm=3DAPR\_EDAM\_QA\_WE\_MERCHA= NTS,APR\_EDAM\_QA\_WE\_GENERAL,APR\_EDAM\_QA\_WE\_VENDORS
/content/dam/pottery-b= arn/main=3DAPR\_EDAM\_QA\_PB\_GeneralUsers,APR\_EDAM\_QA\_PB\_FRANCHISE
/content/dam/pottery-barn/kids=3DAPR\_EDAM\_QA\_PK\_GeneralUsers, APR\_EDAM\_QA\_PK\_Franchise
/content/dam= /pottery-barn/teen=3DAPR\_EDAM\_QA\_PT\_Gene= ralUsers,APR\_EDAM\_QA\_PT\_Franchise=

UAT *:*

Config = Param

Config = Value(UAT)

approved.asset.viewers

/content/dam/west-elm=3DAPR\_EDAM\_UAT\_WE\_MERCH= ANTS,APR\_EDAM\_UAT\_WE\_GENERAL,APR\_EDAM\_UAT\_WE\_VENDORS
/content/dam/potter= y-barn/main=3DAPR\_EDAM\_UAT\_PB\_GeneralUse= rs,APR\_EDAM\_UAT\_PB\_FRANCHISE
/content/dam/pottery-barn/kids=3DAPR\_EDAM\_UAT\_PK\_GeneralUsers,APR\_EDAM\_UAT\_PK\_Franchise
/content/da= m/pottery-barn/teen=3DAPR\_EDAM\_UAT\_PT\_Ge= neralUsers,APR\_EDAM\_UAT\_PT\_Franch= ise

*PROD**:\<= /strong\>*

Config = Param

Config = Value(PROD)

approved.asset.viewers

/content/dam/west-elm=3DAPR\_EDAM\_WE\_MERCHANTS= \_USERS,APR\_EDAM\_WE\_GENERAL\_USERS,APR\_EDAM\_WE\_VENDORS\_USERS
/content/dam/= pottery-barn/main=3DAPR\_EDAM\_PB\_GeneralU= sers,APR\_EDAM\_PB\_FRANCHISE
/content/dam/pottery-barn/kids=3DAPR\_EDAM\_PK\_GeneralUsers,APR\_EDAM\_PK\_Franchise
/content/dam/potter= y-barn/teen=3DAPR\_EDAM\_PT\_GeneralUsers,APR\_EDAM\_PT\_Franchise

Configs for restricting metadata edit of an asset in QA, UAT, PROD :

||
|com.wsgc.ecommerce.e= dam.core.listeners.RestrictEditMetaData|

Following custom configuration's are required for Approved Asset Viewers= .

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "RestrictEd= itMetaData" and click on it.

Following are config param name and corresponding values for PB.

Config = Param

Config = Value(QA)

Config = Value(UAT)

Config = Value(PROD)

editRestri= ctGroups

APR\_EDAM\_Q= A\_PB\_PRSocial

APR\_EDAM\_QA\_P= T\_PRSocial

APR\_EDAM\_QA\_PK\_P= RSocial

APR\_EDAM\_U= AT\_PB\_PRSocial

APR\_EDAM\_UAT= \_PT\_PRSocial

APR\_EDAM\_UAT\_P= K\_PRSocial

APR\_EDAM\_P= B\_PRSocial

APR\_EDAM\_PT\_PRSo= cial

APR\_EDAM\_PK\_PRSocial

**Story :**

TRISUL-352 : PB Rollout - High Resolution Threshold

TRISUL-346 : WS Rollout - High Resolution Threshold

**Config Name : High Resolut= ion listener config**

||
|com.wsgc.ecommerce.e= dam.core.listeners.HighResolutionImageListener|

Following custom configuration's are required for setting high resolutio= n threshold values for an asset.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "High Resol= ution listener config" and click on it.

Following are config param name and corresponding values for PB.

Config = Param

Config = Value

high.resolution.threshold

/content/dam/pottery-barn=3D4800

/conte= nt/dam/williams-sonoma=3D2000

/content/dam/west-elm=3D2000

**Story :**

TRISUL-350 : PB Rollout - Metadata Cascading & Retrofit WSI Schema

TRISUL-344 : WS Rollout - Metadata Cascading & Retrofit WSI Schema

SummaryTab Configurations :=

||
|com.wsgc.ecommerce.e= dam.core.services.impl.SummaryTabService|

Following custom configuration's are required for enabling Summary tab f= unctionality of an asset.

Navigate to AEM web console (i.e. [hostname]:[portnumber]/system/console= /configMgr)
Search for "SummaryTab= Configurations" and click on it.

Following are config param name and corresponding values.

Config = Param

Config = Value

SummaryTab=

wsi:brand=3DBrand\#Creative
wsi:asset-type= =3DAsset Type\#Creative
wsi:year=3DYear\#Creative
wsi:season=3DSeason\#C= reative
wsi:spread=3DSpread\#Creative
wsi:crop=3DCrop\#Creative
wsi:= skus=3DSKUs\#Product
wsi:group-ids=3DGroup IDs\#Product
wsi:collection= =3DCollection\#Product
wsi:product-type=3DProduct Type\#Product
wsi:sta= tus=3DApproval Status\#Process
wsi:isHighResolution=3DIs High Resolution\<= br\>wsi:product-name=3DProduct Name\#Product

------=\_Part\_4267\_935045070.1612838952877--
