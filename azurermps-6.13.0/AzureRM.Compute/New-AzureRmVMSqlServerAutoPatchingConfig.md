---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: d6814131ec4748f95f572762938d3c8bd5135c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762998"
---
# <span data-ttu-id="7eec3-101">New-AzureRmVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="7eec3-101">New-AzureRmVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="7eec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eec3-102">SYNOPSIS</span></span>
<span data-ttu-id="7eec3-103">Sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7eec3-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eec3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7eec3-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7eec3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7eec3-105">DESCRIPTION</span></span>
<span data-ttu-id="7eec3-106">**Yeni-AzureRmVMSqlServerAutoPatchingConfig** cmdlet 'i, sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7eec3-106">The **New-AzureRmVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="7eec3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7eec3-107">EXAMPLES</span></span>

### <span data-ttu-id="7eec3-108">Örnek 1: otomatik düzeltme 'yi yapılandırmak için yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7eec3-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="7eec3-109">Bu komut düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7eec3-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="7eec3-110">Komut haftanın gününü belirtir ve bakım penceresini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7eec3-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="7eec3-111">Bu yapılandırma, bu değerleri kullanan düzeltme ekini kullanır.</span><span class="sxs-lookup"><span data-stu-id="7eec3-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="7eec3-112">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7eec3-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="7eec3-113">Bu yapılandırma öğesini, Set-AzureRmVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7eec3-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="7eec3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7eec3-114">PARAMETERS</span></span>

### <span data-ttu-id="7eec3-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="7eec3-115">-DayOfWeek</span></span>
<span data-ttu-id="7eec3-116">Güncelleştirmelerin yüklenmesi gereken haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eec3-116">Specifies the day of the week when updates should be installed.</span></span>
<span data-ttu-id="7eec3-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7eec3-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7eec3-118">Gününü</span><span class="sxs-lookup"><span data-stu-id="7eec3-118">Sunday</span></span>
- <span data-ttu-id="7eec3-119">Den</span><span class="sxs-lookup"><span data-stu-id="7eec3-119">Monday</span></span>
- <span data-ttu-id="7eec3-120">Salı</span><span class="sxs-lookup"><span data-stu-id="7eec3-120">Tuesday</span></span>
- <span data-ttu-id="7eec3-121">Günü</span><span class="sxs-lookup"><span data-stu-id="7eec3-121">Wednesday</span></span>
- <span data-ttu-id="7eec3-122">Per</span><span class="sxs-lookup"><span data-stu-id="7eec3-122">Thursday</span></span>
- <span data-ttu-id="7eec3-123">Cuma</span><span class="sxs-lookup"><span data-stu-id="7eec3-123">Friday</span></span>
- <span data-ttu-id="7eec3-124">Günü</span><span class="sxs-lookup"><span data-stu-id="7eec3-124">Saturday</span></span>
- <span data-ttu-id="7eec3-125">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="7eec3-125">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eec3-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="7eec3-126">-Enable</span></span>
<span data-ttu-id="7eec3-127">Sanal makine için otomatik düzeltme özelliğinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7eec3-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="7eec3-128">Otomatik Düzeltme 'yi etkinleştirirseniz cmdlet Windows güncelleştirmesini etkileşimli moda koyar.</span><span class="sxs-lookup"><span data-stu-id="7eec3-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="7eec3-129">Otomatik Düzeltme ekini devre dışı bırakırsanız Windows Update ayarları değişmez.</span><span class="sxs-lookup"><span data-stu-id="7eec3-129">If you disable automated patching, Windows Update settings do not change.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eec3-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="7eec3-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="7eec3-131">Bakım penceresinin süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eec3-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="7eec3-132">Otomatik düzeltme eki uygulama dışında bir sanal makine kullanılabilirliğini etkileyebilecek bir eylem gerçekleştirmeyi önler.</span><span class="sxs-lookup"><span data-stu-id="7eec3-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="7eec3-133">30 dakikalık bir katı belirtin.</span><span class="sxs-lookup"><span data-stu-id="7eec3-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eec3-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="7eec3-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="7eec3-135">Bakım penceresinin başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eec3-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="7eec3-136">Bu kez güncelleştirmeler yüklenmeye başladığında tanımlar.</span><span class="sxs-lookup"><span data-stu-id="7eec3-136">This time defines when updates start to install.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eec3-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="7eec3-137">-PatchCategory</span></span>
<span data-ttu-id="7eec3-138">Önemli güncelleştirmelerin dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eec3-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eec3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eec3-139">CommonParameters</span></span>
<span data-ttu-id="7eec3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7eec3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eec3-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eec3-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eec3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7eec3-142">INPUTS</span></span>

### <span data-ttu-id="7eec3-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7eec3-143">None</span></span>

## <span data-ttu-id="7eec3-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7eec3-144">OUTPUTS</span></span>

### <span data-ttu-id="7eec3-145">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="7eec3-145">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

## <span data-ttu-id="7eec3-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7eec3-146">NOTES</span></span>

## <span data-ttu-id="7eec3-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7eec3-147">RELATED LINKS</span></span>

[<span data-ttu-id="7eec3-148">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="7eec3-148">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="7eec3-149">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="7eec3-149">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


