---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautopatchingconfig
schema: 2.0.0
ms.openlocfilehash: 1204a8b14cdbb45f46edd2a1ca2e4c12c27845a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939788"
---
# <span data-ttu-id="8627a-101">New-AzureRmVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8627a-101">New-AzureRmVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="8627a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8627a-102">SYNOPSIS</span></span>
<span data-ttu-id="8627a-103">Sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8627a-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8627a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8627a-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8627a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8627a-105">DESCRIPTION</span></span>
<span data-ttu-id="8627a-106">**Yeni-AzureRmVMSqlServerAutoPatchingConfig** cmdlet 'i, sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8627a-106">The **New-AzureRmVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="8627a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8627a-107">EXAMPLES</span></span>

### <span data-ttu-id="8627a-108">Örnek 1: otomatik düzeltme 'yi yapılandırmak için yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="8627a-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureRmVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="8627a-109">Bu komut düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8627a-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="8627a-110">Komut haftanın gününü belirtir ve bakım penceresini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8627a-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="8627a-111">Bu yapılandırma, bu değerleri kullanan düzeltme ekini kullanır.</span><span class="sxs-lookup"><span data-stu-id="8627a-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="8627a-112">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="8627a-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="8627a-113">Bu yapılandırma öğesini, Set-AzureRmVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8627a-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="8627a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8627a-114">PARAMETERS</span></span>

### <span data-ttu-id="8627a-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="8627a-115">-DayOfWeek</span></span>
<span data-ttu-id="8627a-116">Güncelleştirmelerin yüklenmesi gereken haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8627a-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="8627a-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="8627a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8627a-118">Gününü</span><span class="sxs-lookup"><span data-stu-id="8627a-118">Sunday</span></span>
- <span data-ttu-id="8627a-119">Den</span><span class="sxs-lookup"><span data-stu-id="8627a-119">Monday</span></span>
- <span data-ttu-id="8627a-120">Salı</span><span class="sxs-lookup"><span data-stu-id="8627a-120">Tuesday</span></span>
- <span data-ttu-id="8627a-121">Günü</span><span class="sxs-lookup"><span data-stu-id="8627a-121">Wednesday</span></span>
- <span data-ttu-id="8627a-122">Per</span><span class="sxs-lookup"><span data-stu-id="8627a-122">Thursday</span></span>
- <span data-ttu-id="8627a-123">Cuma</span><span class="sxs-lookup"><span data-stu-id="8627a-123">Friday</span></span>
- <span data-ttu-id="8627a-124">Günü</span><span class="sxs-lookup"><span data-stu-id="8627a-124">Saturday</span></span>
- <span data-ttu-id="8627a-125">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="8627a-125">Everyday</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Everyday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8627a-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="8627a-126">-Enable</span></span>
<span data-ttu-id="8627a-127">Sanal makine için otomatik düzeltme özelliğinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8627a-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="8627a-128">Otomatik Düzeltme 'yi etkinleştirirseniz cmdlet Windows güncelleştirmesini etkileşimli moda koyar.</span><span class="sxs-lookup"><span data-stu-id="8627a-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="8627a-129">Otomatik Düzeltme ekini devre dışı bırakırsanız Windows Update ayarları değişmez.</span><span class="sxs-lookup"><span data-stu-id="8627a-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="8627a-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="8627a-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="8627a-131">Bakım penceresinin süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="8627a-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="8627a-132">Otomatik düzeltme eki uygulama dışında bir sanal makine kullanılabilirliğini etkileyebilecek bir eylem gerçekleştirmeyi önler.</span><span class="sxs-lookup"><span data-stu-id="8627a-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="8627a-133">30 dakikalık bir katı belirtin.</span><span class="sxs-lookup"><span data-stu-id="8627a-133">Specify a multiple of 30 minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8627a-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="8627a-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="8627a-135">Bakım penceresinin başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8627a-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="8627a-136">Bu kez güncelleştirmeler yüklenmeye başladığında tanımlar.</span><span class="sxs-lookup"><span data-stu-id="8627a-136">This time defines when updates start to install.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8627a-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="8627a-137">-PatchCategory</span></span>
<span data-ttu-id="8627a-138">Önemli güncelleştirmelerin dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8627a-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Important

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8627a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8627a-139">CommonParameters</span></span>
<span data-ttu-id="8627a-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8627a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8627a-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8627a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8627a-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8627a-142">INPUTS</span></span>

### <span data-ttu-id="8627a-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8627a-143">None</span></span>
<span data-ttu-id="8627a-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8627a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8627a-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8627a-145">OUTPUTS</span></span>

### <span data-ttu-id="8627a-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8627a-146">AutoPatchingSettings</span></span>
<span data-ttu-id="8627a-147">Bu cmdlet, otomatik düzeltme için ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="8627a-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="8627a-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8627a-148">NOTES</span></span>

## <span data-ttu-id="8627a-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8627a-149">RELATED LINKS</span></span>



[<span data-ttu-id="8627a-150">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8627a-150">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


