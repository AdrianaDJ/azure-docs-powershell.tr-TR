---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106258"
---
# <span data-ttu-id="ac8ef-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ac8ef-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="ac8ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8ef-103">Birim kapsayıcılarının geçişini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="ac8ef-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ac8ef-104">SYNTAX</span></span>

### <span data-ttu-id="ac8ef-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="ac8ef-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ac8ef-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="ac8ef-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ac8ef-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ac8ef-107">DESCRIPTION</span></span>
<span data-ttu-id="ac8ef-108">**Import-AzureStorSimpleLegacyVolumeContainer** cmdlet 'i eski bir gereç ile hedef bir gereç arasında birim kapsayıcıları geçişini başlatır.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="ac8ef-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ac8ef-109">EXAMPLES</span></span>

### <span data-ttu-id="ac8ef-110">Örnek 1: eski birim kapsayıcısını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="ac8ef-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="ac8ef-111">Bu komut, adlandırılmış kapsayıcı için eski birim kapsayıcısını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="ac8ef-112">Cmdlet içeri aktarmayı başlatır ve bir ileti döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="ac8ef-113">Örnek 2: tüm eski birim kapsayıcılarını Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="ac8ef-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="ac8ef-114">Bu komut, alınan yapılandırma dosyasından tüm eski birim kapsayıcılarını içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="ac8ef-115">Cmdlet içeri aktarmayı başlatır ve bir ileti döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="ac8ef-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ac8ef-116">PARAMETERS</span></span>

### <span data-ttu-id="ac8ef-117">-Tümü</span><span class="sxs-lookup"><span data-stu-id="ac8ef-117">-All</span></span>
<span data-ttu-id="ac8ef-118">Bu cmdlet 'in içeri aktarılan yapılandırma dosyasındaki tüm birim kapsayıcılarını hedef cihaza aktardığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="ac8ef-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ac8ef-119">-Force</span></span>
<span data-ttu-id="ac8ef-120">Bu cmdlet 'in birim kapsayıcısını farklı bir cihaza içeri aktardığını ve farklı bir cihazda birim kapsayıcısı alınmış olsa bile, bu cmdlet 'in birim kapsayıcısını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ef-121">-Legacyconfigıd</span><span class="sxs-lookup"><span data-stu-id="ac8ef-121">-LegacyConfigId</span></span>
<span data-ttu-id="ac8ef-122">Eski bir gereç yapılandırmasının benzersiz KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="ac8ef-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="ac8ef-123">-LegacyContainerNames</span></span>
<span data-ttu-id="ac8ef-124">Geçiş planının uygulandığı birim kapsayıcı adları dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="ac8ef-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="ac8ef-125">-Profile</span></span>
<span data-ttu-id="ac8ef-126">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac8ef-127">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac8ef-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="ac8ef-128">-SkipACRs</span></span>
<span data-ttu-id="ac8ef-129">İçeri aktarma işleminin geçiş için Access denetim kayıtlarını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8ef-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8ef-130">CommonParameters</span></span>
<span data-ttu-id="ac8ef-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8ef-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac8ef-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8ef-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ac8ef-133">INPUTS</span></span>

## <span data-ttu-id="ac8ef-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ac8ef-134">OUTPUTS</span></span>

### <span data-ttu-id="ac8ef-135">Dizisi</span><span class="sxs-lookup"><span data-stu-id="ac8ef-135">String</span></span>
<span data-ttu-id="ac8ef-136">Bu komut, Gereç içeri aktarma birimi kapsayıcı işinin, Gereç içinde başarıyla başlatılmış olması durumunda durumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="ac8ef-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="ac8ef-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ac8ef-137">NOTES</span></span>

## <span data-ttu-id="ac8ef-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ac8ef-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac8ef-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="ac8ef-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="ac8ef-140">İçeri aktarma-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="ac8ef-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


