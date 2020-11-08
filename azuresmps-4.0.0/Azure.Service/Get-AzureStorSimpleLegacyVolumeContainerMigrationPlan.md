---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105556"
---
# <span data-ttu-id="29a2f-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="29a2f-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="29a2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="29a2f-103">Eski kapsayıcıların geçiş planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="29a2f-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="29a2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29a2f-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="29a2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="29a2f-106">**Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet 'i, eski kapsayıcıların geçiş planlarını alır.</span><span class="sxs-lookup"><span data-stu-id="29a2f-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="29a2f-107">Eski yapılandırma KIMLIĞIYLE bir geçiş planı belirtin.</span><span class="sxs-lookup"><span data-stu-id="29a2f-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="29a2f-108">Geçiş planının oluşturulması devam ediyorsa, bu cmdlet geçiş planının durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="29a2f-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="29a2f-109">Geçiş planı tamamlanmışsa, bu cmdlet eski kapsayıcılar kümesinin gerçek geçiş planını döndürür.</span><span class="sxs-lookup"><span data-stu-id="29a2f-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="29a2f-110">*Legacyconfigıd* parametresini belirtmezseniz, bu cmdlet yapılandırma kimliklerinin listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="29a2f-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="29a2f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29a2f-111">EXAMPLES</span></span>

### <span data-ttu-id="29a2f-112">Örnek 1: planın durumunu alma</span><span class="sxs-lookup"><span data-stu-id="29a2f-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="29a2f-113">Bu komut geçiş planının durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="29a2f-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="29a2f-114">Durum, beklenen bant genişliği, tahmini zaman ve ilgili bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="29a2f-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="29a2f-115">Örnek 2: var olan planların kimliklerini alma</span><span class="sxs-lookup"><span data-stu-id="29a2f-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="29a2f-116">Bu komut, geçiş planlarının tüm yapılandırma kimliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="29a2f-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="29a2f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29a2f-117">PARAMETERS</span></span>

### <span data-ttu-id="29a2f-118">-Legacyconfigıd</span><span class="sxs-lookup"><span data-stu-id="29a2f-118">-LegacyConfigId</span></span>
<span data-ttu-id="29a2f-119">Eski bir gereç yapılandırmasının benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="29a2f-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a2f-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="29a2f-120">-LegacyContainerNames</span></span>
<span data-ttu-id="29a2f-121">Bu cmdlet 'in geçiş planı aldığı birim kapsayıcı adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="29a2f-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a2f-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="29a2f-122">-Profile</span></span>
<span data-ttu-id="29a2f-123">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="29a2f-123">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a2f-124">CommonParameters</span></span>
<span data-ttu-id="29a2f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29a2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a2f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29a2f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a2f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29a2f-127">INPUTS</span></span>

### <span data-ttu-id="29a2f-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="29a2f-128">None</span></span>

## <span data-ttu-id="29a2f-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29a2f-129">OUTPUTS</span></span>

### <span data-ttu-id="29a2f-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="29a2f-130">MigrationPlanMsg</span></span>
<span data-ttu-id="29a2f-131">Bu cmdlet, geçiş planı işinin durumunu içeren bir **Migrationplanmsg** nesnesi döndürür; bu süre megabit ve saniye cinsinden tahmini süre.</span><span class="sxs-lookup"><span data-stu-id="29a2f-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="29a2f-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29a2f-132">NOTES</span></span>

## <span data-ttu-id="29a2f-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29a2f-133">RELATED LINKS</span></span>

[<span data-ttu-id="29a2f-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="29a2f-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


