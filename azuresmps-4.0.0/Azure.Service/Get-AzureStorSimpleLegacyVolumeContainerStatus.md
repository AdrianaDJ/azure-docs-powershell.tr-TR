---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106550"
---
# <span data-ttu-id="ded7c-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="ded7c-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="ded7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ded7c-102">SYNOPSIS</span></span>
<span data-ttu-id="ded7c-103">Birim kapsayıcılarının geçiş durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ded7c-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="ded7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ded7c-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ded7c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ded7c-105">DESCRIPTION</span></span>
<span data-ttu-id="ded7c-106">**Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet 'i birim kapsayıcılarının geçiş durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ded7c-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="ded7c-107">Bu cmdlet, birim kapsayıcısı geçişinin hala devam ediyor, tamamlandı veya başarısız olup olmadığını içeren durum bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="ded7c-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="ded7c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ded7c-108">EXAMPLES</span></span>

### <span data-ttu-id="ded7c-109">Örnek 1: başarısız bir geçişin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="ded7c-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="ded7c-110">Bu komut, adlandırılmış eski kapsayıcının geçiş durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ded7c-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="ded7c-111">Sonuçlar geçişin başarısız olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ded7c-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="ded7c-112">Örnek 2: devam eden bir geçişin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="ded7c-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="ded7c-113">Bu komut, adlandırılmış eski kapsayıcının geçiş durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ded7c-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="ded7c-114">Sonuçlar geçişin devam etmekte olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="ded7c-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="ded7c-115">Örnek 3: tamamlanan bir geçişin durumunu alma</span><span class="sxs-lookup"><span data-stu-id="ded7c-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="ded7c-116">Bu komut, adlandırılmış eski kapsayıcının geçiş durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="ded7c-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="ded7c-117">Sonuçlar geçişin tamamlandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ded7c-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="ded7c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ded7c-118">PARAMETERS</span></span>

### <span data-ttu-id="ded7c-119">-Legacyconfigıd</span><span class="sxs-lookup"><span data-stu-id="ded7c-119">-LegacyConfigId</span></span>
<span data-ttu-id="ded7c-120">Eski bir gereç yapılandırmasının benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ded7c-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ded7c-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="ded7c-121">-LegacyContainerNames</span></span>
<span data-ttu-id="ded7c-122">Geçiş planının uygulandığı birim kapsayıcı adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ded7c-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="ded7c-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="ded7c-123">-Profile</span></span>
<span data-ttu-id="ded7c-124">Bir Azure profili belirtir.</span><span class="sxs-lookup"><span data-stu-id="ded7c-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ded7c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded7c-125">CommonParameters</span></span>
<span data-ttu-id="ded7c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ded7c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded7c-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded7c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded7c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ded7c-128">INPUTS</span></span>

## <span data-ttu-id="ded7c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ded7c-129">OUTPUTS</span></span>

## <span data-ttu-id="ded7c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ded7c-130">NOTES</span></span>

## <span data-ttu-id="ded7c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ded7c-131">RELATED LINKS</span></span>

[<span data-ttu-id="ded7c-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="ded7c-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="ded7c-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="ded7c-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


