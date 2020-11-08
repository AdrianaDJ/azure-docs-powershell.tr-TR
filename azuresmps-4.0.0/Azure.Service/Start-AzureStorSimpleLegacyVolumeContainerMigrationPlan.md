---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105773"
---
# <span data-ttu-id="2584a-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="2584a-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="2584a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2584a-102">SYNOPSIS</span></span>
<span data-ttu-id="2584a-103">Geçiş planı oluşturmayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="2584a-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="2584a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2584a-104">SYNTAX</span></span>

### <span data-ttu-id="2584a-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="2584a-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2584a-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="2584a-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2584a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2584a-107">DESCRIPTION</span></span>
<span data-ttu-id="2584a-108">**Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet 'i, geçiş planı oluşturmayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="2584a-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="2584a-109">Geçiş planı oluşturma işlemi eşzamansız.</span><span class="sxs-lookup"><span data-stu-id="2584a-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="2584a-110">Geçiş planının durumunu görmek için **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2584a-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="2584a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2584a-111">EXAMPLES</span></span>

### <span data-ttu-id="2584a-112">Örnek 1: geçiş planı başlatma</span><span class="sxs-lookup"><span data-stu-id="2584a-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="2584a-113">Bu komut, OneSDKAzureCloud adlı eski kapsayıcı için geçiş planı oluşturmaya başlar.</span><span class="sxs-lookup"><span data-stu-id="2584a-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="2584a-114">Komut, planın durumu hakkında bir ileti ve güncel bilgi için **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet 'ini kullanmaktır.</span><span class="sxs-lookup"><span data-stu-id="2584a-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="2584a-115">Örnek 2: tüm birim kapsayıcıları için geçiş planını Başlat</span><span class="sxs-lookup"><span data-stu-id="2584a-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="2584a-116">Bu komut, içeri aktarılan yapılandırma dosyasındaki tüm eski birim kapsayıcıları için geçiş planı oluşturmayı başlatır.</span><span class="sxs-lookup"><span data-stu-id="2584a-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="2584a-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2584a-117">PARAMETERS</span></span>

### <span data-ttu-id="2584a-118">-Tümü</span><span class="sxs-lookup"><span data-stu-id="2584a-118">-All</span></span>
<span data-ttu-id="2584a-119">Bu cmdlet 'in içeri aktarılan yapılandırma dosyasındaki tüm birim kapsayıcıları için geçiş süresi tahminlerini başladığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2584a-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="2584a-120">-Legacyconfigıd</span><span class="sxs-lookup"><span data-stu-id="2584a-120">-LegacyConfigId</span></span>
<span data-ttu-id="2584a-121">Eski bir gereç yapılandırmasının benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2584a-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="2584a-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="2584a-122">-LegacyContainerNames</span></span>
<span data-ttu-id="2584a-123">Geçiş planı oluşturacağınız birim kapsayıcı adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2584a-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

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

### <span data-ttu-id="2584a-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="2584a-124">-Profile</span></span>
<span data-ttu-id="2584a-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2584a-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2584a-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="2584a-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2584a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2584a-127">CommonParameters</span></span>
<span data-ttu-id="2584a-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2584a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2584a-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2584a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2584a-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2584a-130">INPUTS</span></span>

### <span data-ttu-id="2584a-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="2584a-131">None</span></span>

## <span data-ttu-id="2584a-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2584a-132">OUTPUTS</span></span>

### <span data-ttu-id="2584a-133">Dizisi</span><span class="sxs-lookup"><span data-stu-id="2584a-133">String</span></span>
<span data-ttu-id="2584a-134">Bu cmdlet, Gereç planı işinin, Gereç içinde başarıyla başlatılmış olması durumunda durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="2584a-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="2584a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2584a-135">NOTES</span></span>

## <span data-ttu-id="2584a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2584a-136">RELATED LINKS</span></span>

[<span data-ttu-id="2584a-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="2584a-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


