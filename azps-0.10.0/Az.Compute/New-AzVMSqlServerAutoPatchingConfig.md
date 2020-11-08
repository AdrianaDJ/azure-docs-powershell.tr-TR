---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautopatchingconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 0ce851373ac31aaef4c5664db7085f345e9b947d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936950"
---
# <span data-ttu-id="691f3-101">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="691f3-101">New-AzVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="691f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="691f3-102">SYNOPSIS</span></span>
<span data-ttu-id="691f3-103">Sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="691f3-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="691f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="691f3-104">SYNTAX</span></span>

```
New-AzVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>]
 [-MaintenanceWindowStartingHour <Int32>] [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="691f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="691f3-105">DESCRIPTION</span></span>
<span data-ttu-id="691f3-106">**Yeni-AzVMSqlServerAutoPatchingConfig** cmdlet 'i, sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="691f3-106">The **New-AzVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="691f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="691f3-107">EXAMPLES</span></span>

### <span data-ttu-id="691f3-108">Örnek 1: otomatik düzeltme 'yi yapılandırmak için yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="691f3-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="691f3-109">Bu komut düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="691f3-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="691f3-110">Komut haftanın gününü belirtir ve bakım penceresini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="691f3-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="691f3-111">Bu yapılandırma, bu değerleri kullanan düzeltme ekini kullanır.</span><span class="sxs-lookup"><span data-stu-id="691f3-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="691f3-112">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="691f3-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="691f3-113">Bu yapılandırma öğesini, Set-AzVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="691f3-113">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="691f3-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="691f3-114">PARAMETERS</span></span>

### <span data-ttu-id="691f3-115">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="691f3-115">-DayOfWeek</span></span>
<span data-ttu-id="691f3-116">Güncelleştirmelerin yüklenmesi gereken haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="691f3-116">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="691f3-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="691f3-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="691f3-118">Gününü</span><span class="sxs-lookup"><span data-stu-id="691f3-118">Sunday</span></span>
- <span data-ttu-id="691f3-119">Den</span><span class="sxs-lookup"><span data-stu-id="691f3-119">Monday</span></span>
- <span data-ttu-id="691f3-120">Salı</span><span class="sxs-lookup"><span data-stu-id="691f3-120">Tuesday</span></span>
- <span data-ttu-id="691f3-121">Günü</span><span class="sxs-lookup"><span data-stu-id="691f3-121">Wednesday</span></span>
- <span data-ttu-id="691f3-122">Per</span><span class="sxs-lookup"><span data-stu-id="691f3-122">Thursday</span></span>
- <span data-ttu-id="691f3-123">Cuma</span><span class="sxs-lookup"><span data-stu-id="691f3-123">Friday</span></span>
- <span data-ttu-id="691f3-124">Günü</span><span class="sxs-lookup"><span data-stu-id="691f3-124">Saturday</span></span>
- <span data-ttu-id="691f3-125">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="691f3-125">Everyday</span></span>

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

### <span data-ttu-id="691f3-126">-Enable</span><span class="sxs-lookup"><span data-stu-id="691f3-126">-Enable</span></span>
<span data-ttu-id="691f3-127">Sanal makine için otomatik düzeltme özelliğinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="691f3-127">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="691f3-128">Otomatik Düzeltme 'yi etkinleştirirseniz cmdlet Windows güncelleştirmesini etkileşimli moda koyar.</span><span class="sxs-lookup"><span data-stu-id="691f3-128">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="691f3-129">Otomatik Düzeltme ekini devre dışı bırakırsanız Windows Update ayarları değişmez.</span><span class="sxs-lookup"><span data-stu-id="691f3-129">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="691f3-130">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="691f3-130">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="691f3-131">Bakım penceresinin süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="691f3-131">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="691f3-132">Otomatik düzeltme eki uygulama dışında bir sanal makine kullanılabilirliğini etkileyebilecek bir eylem gerçekleştirmeyi önler.</span><span class="sxs-lookup"><span data-stu-id="691f3-132">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="691f3-133">30 dakikalık bir katı belirtin.</span><span class="sxs-lookup"><span data-stu-id="691f3-133">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="691f3-134">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="691f3-134">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="691f3-135">Bakım penceresinin başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="691f3-135">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="691f3-136">Bu kez güncelleştirmeler yüklenmeye başladığında tanımlar.</span><span class="sxs-lookup"><span data-stu-id="691f3-136">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="691f3-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="691f3-137">-PatchCategory</span></span>
<span data-ttu-id="691f3-138">Önemli güncelleştirmelerin dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="691f3-138">Specifies whether important updates should be included.</span></span>

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

### <span data-ttu-id="691f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691f3-139">CommonParameters</span></span>
<span data-ttu-id="691f3-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="691f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691f3-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="691f3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691f3-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="691f3-142">INPUTS</span></span>

### <span data-ttu-id="691f3-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="691f3-143">None</span></span>
<span data-ttu-id="691f3-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="691f3-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="691f3-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="691f3-145">OUTPUTS</span></span>

### <span data-ttu-id="691f3-146">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="691f3-146">AutoPatchingSettings</span></span>
<span data-ttu-id="691f3-147">Bu cmdlet, otomatik düzeltme için ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="691f3-147">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="691f3-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="691f3-148">NOTES</span></span>

## <span data-ttu-id="691f3-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="691f3-149">RELATED LINKS</span></span>

[<span data-ttu-id="691f3-150">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="691f3-150">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="691f3-151">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="691f3-151">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)

