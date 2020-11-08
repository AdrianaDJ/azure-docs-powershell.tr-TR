---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105700"
---
# <span data-ttu-id="d3648-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="d3648-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="d3648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3648-102">SYNOPSIS</span></span>
<span data-ttu-id="d3648-103">Geçirilen birim kapsayıcılarını yürütme veya geri alma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3648-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="d3648-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3648-104">SYNTAX</span></span>

### <span data-ttu-id="d3648-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="d3648-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d3648-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="d3648-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3648-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3648-107">DESCRIPTION</span></span>
<span data-ttu-id="d3648-108">**Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet 'i, eski geçişin bir parçası olarak geçirilen birim kapsayıcılarını yürütme veya geri alma işlemini başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3648-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="d3648-109">Geri alma, bu işlemi ilk sahiplik durumuna getirir.</span><span class="sxs-lookup"><span data-stu-id="d3648-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="d3648-110">Yürütme, sahipliği hedef uygulamaya atar.</span><span class="sxs-lookup"><span data-stu-id="d3648-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="d3648-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3648-111">EXAMPLES</span></span>

### <span data-ttu-id="d3648-112">Örnek 1: belirli bir birim kapsayıcısında yürütme işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="d3648-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d3648-113">Bu komut belirtilen eski yapılandırma KIMLIĞI için belirtilen birim kapsayıcısında bir yürütme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3648-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="d3648-114">İşlemin durumunu görmek için **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d3648-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="d3648-115">Örnek 2: belirli bir birim kapsayıcısında geri alma işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="d3648-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d3648-116">Bu komut belirtilen eski yapılandırma KIMLIĞI için belirtilen birim kapsayıcısında geri alma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3648-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="d3648-117">Örnek 3: tüm birim kapsayıcılarında yürütme işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="d3648-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d3648-118">Bu komut belirtilen eski yapılandırma KIMLIĞI için tüm birim kapsayıcısında bir yürütme işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3648-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="d3648-119">Örnek 4: tüm birim kapsayıcılarında geri alma işlemi başlatma</span><span class="sxs-lookup"><span data-stu-id="d3648-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="d3648-120">Bu komut, belirtilen eski yapılandırma KIMLIĞI için tüm birim kapsayıcılarında geri alma işlemi başlatır.</span><span class="sxs-lookup"><span data-stu-id="d3648-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="d3648-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3648-121">PARAMETERS</span></span>

### <span data-ttu-id="d3648-122">-Tümü</span><span class="sxs-lookup"><span data-stu-id="d3648-122">-All</span></span>
<span data-ttu-id="d3648-123">Bu cmdlet 'in içeri aktarılan yapılandırma dosyasındaki tüm birim kapsayıcılarında geri alma veya tamamlama işlemi başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3648-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3648-124">-Legacyconfigıd</span><span class="sxs-lookup"><span data-stu-id="d3648-124">-LegacyConfigId</span></span>
<span data-ttu-id="d3648-125">Eski bir gereç yapılandırmasının benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="d3648-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="d3648-126">-LegacyContainerNames</span></span>
<span data-ttu-id="d3648-127">Geçiş planının uygulandığı birim kapsayıcı adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3648-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="d3648-128">-MigrationOperation</span></span>
<span data-ttu-id="d3648-129">Bu cmdlet 'in yürütme veya geri alma gerçekleştirip gerçekleştirmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="d3648-130">Geçerli değerler: Commit ve Rollback.</span><span class="sxs-lookup"><span data-stu-id="d3648-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="d3648-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="d3648-131">-Profile</span></span>
<span data-ttu-id="d3648-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d3648-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3648-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d3648-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3648-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3648-134">CommonParameters</span></span>
<span data-ttu-id="d3648-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3648-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3648-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3648-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3648-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3648-137">INPUTS</span></span>

## <span data-ttu-id="d3648-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3648-138">OUTPUTS</span></span>

## <span data-ttu-id="d3648-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3648-139">NOTES</span></span>

## <span data-ttu-id="d3648-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3648-140">RELATED LINKS</span></span>

[<span data-ttu-id="d3648-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="d3648-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="d3648-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="d3648-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="d3648-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="d3648-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


