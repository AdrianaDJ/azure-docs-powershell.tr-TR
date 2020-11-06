---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 7016BAA9-C25D-404E-9F75-2BE49FBF91A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoPatchingConfig.md
ms.openlocfilehash: 17d99840bffb9063ad61dec00d4b7d5983118399
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594781"
---
# <span data-ttu-id="1ed5e-101">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="1ed5e-101">New-AzureVMSqlServerAutoPatchingConfig</span></span>

## <span data-ttu-id="1ed5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ed5e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ed5e-103">Sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-103">Creates a configuration object for automatic patching on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ed5e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ed5e-104">SYNTAX</span></span>

```
New-AzureVMSqlServerAutoPatchingConfig [-Enable] [-DayOfWeek <String>] [-MaintenanceWindowStartingHour <Int32>]
 [-MaintenanceWindowDuration <Int32>] [-PatchCategory <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1ed5e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ed5e-105">DESCRIPTION</span></span>
<span data-ttu-id="1ed5e-106">**New-AzureVMSqlServerAutoPatchingConfig** cmdlet 'i sanal makinede otomatik düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-106">The **New-AzureVMSqlServerAutoPatchingConfig** cmdlet creates a configuration object for automatic patching on a virtual machine.</span></span>

## <span data-ttu-id="1ed5e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ed5e-107">EXAMPLES</span></span>

### <span data-ttu-id="1ed5e-108">Örnek 1: otomatik düzeltme 'yi yapılandırmak için yapılandırma nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="1ed5e-108">Example 1: Create a configuration object to configure automatic patching</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
Enable                        : True
DayOfWeek                     : Thursday
MaintenanceWindowStartingHour : 11
MaintenanceWindowDuration     : 120
PatchCategory                 : Important
```

<span data-ttu-id="1ed5e-109">Bu komut düzeltme için yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-109">This command creates configuration object for patching.</span></span>
<span data-ttu-id="1ed5e-110">Komut haftanın gününü belirtir ve bakım penceresini tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-110">The command specifies the day of the week and defines the maintenance window.</span></span>
<span data-ttu-id="1ed5e-111">Bu yapılandırma, bu değerleri kullanan düzeltme ekini kullanır.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-111">This configuration enables patching that uses these values.</span></span>
<span data-ttu-id="1ed5e-112">Komut sonucu $AutoBackupConfig değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-112">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="1ed5e-113">Bu yapılandırma öğesini, Set-AzureRmVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-113">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

## <span data-ttu-id="1ed5e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ed5e-114">PARAMETERS</span></span>

### <span data-ttu-id="1ed5e-115">-Enable</span><span class="sxs-lookup"><span data-stu-id="1ed5e-115">-Enable</span></span>
<span data-ttu-id="1ed5e-116">Sanal makine için otomatik düzeltme özelliğinin etkinleştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-116">Indicates that automated patching for the virtual machine is enabled.</span></span>
<span data-ttu-id="1ed5e-117">Otomatik Düzeltme 'yi etkinleştirirseniz cmdlet Windows güncelleştirmesini etkileşimli moda koyar.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-117">If you enable automated patching the cmdlet puts Windows Update into interactive mode.</span></span>
<span data-ttu-id="1ed5e-118">Otomatik Düzeltme ekini devre dışı bırakırsanız Windows Update ayarları değişmez.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-118">If you disable automated patching, Windows Update settings do not change.</span></span>

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

### <span data-ttu-id="1ed5e-119">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="1ed5e-119">-DayOfWeek</span></span>
<span data-ttu-id="1ed5e-120">Güncelleştirmelerin yüklenmesi gereken haftanın gününü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-120">Specifies the day of the week when updates should be installed.</span></span>

<span data-ttu-id="1ed5e-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1ed5e-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1ed5e-122">Gününü</span><span class="sxs-lookup"><span data-stu-id="1ed5e-122">Sunday</span></span>
- <span data-ttu-id="1ed5e-123">Den</span><span class="sxs-lookup"><span data-stu-id="1ed5e-123">Monday</span></span>
- <span data-ttu-id="1ed5e-124">Salı</span><span class="sxs-lookup"><span data-stu-id="1ed5e-124">Tuesday</span></span>
- <span data-ttu-id="1ed5e-125">Günü</span><span class="sxs-lookup"><span data-stu-id="1ed5e-125">Wednesday</span></span>
- <span data-ttu-id="1ed5e-126">Per</span><span class="sxs-lookup"><span data-stu-id="1ed5e-126">Thursday</span></span>
- <span data-ttu-id="1ed5e-127">Cuma</span><span class="sxs-lookup"><span data-stu-id="1ed5e-127">Friday</span></span>
- <span data-ttu-id="1ed5e-128">Günü</span><span class="sxs-lookup"><span data-stu-id="1ed5e-128">Saturday</span></span>
- <span data-ttu-id="1ed5e-129">Sıradışı</span><span class="sxs-lookup"><span data-stu-id="1ed5e-129">Everyday</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed5e-130">-MaintenanceWindowStartingHour</span><span class="sxs-lookup"><span data-stu-id="1ed5e-130">-MaintenanceWindowStartingHour</span></span>
<span data-ttu-id="1ed5e-131">Bakım penceresinin başladığı günün saatini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-131">Specifies the hour of the day when maintenance window starts.</span></span>
<span data-ttu-id="1ed5e-132">Bu kez güncelleştirmeler yüklenmeye başladığında tanımlar.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-132">This time defines when updates start to install.</span></span>

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

### <span data-ttu-id="1ed5e-133">-MaintenanceWindowDuration</span><span class="sxs-lookup"><span data-stu-id="1ed5e-133">-MaintenanceWindowDuration</span></span>
<span data-ttu-id="1ed5e-134">Bakım penceresinin süresini dakika cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-134">Specifies the duration, in minutes, of the maintenance window.</span></span>
<span data-ttu-id="1ed5e-135">Otomatik düzeltme eki uygulama dışında bir sanal makine kullanılabilirliğini etkileyebilecek bir eylem gerçekleştirmeyi önler.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-135">Automated patching avoids performing an action that can affect a virtual machine availability outside that window.</span></span>
<span data-ttu-id="1ed5e-136">30 dakikalık bir katı belirtin.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-136">Specify a multiple of 30 minutes.</span></span>

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

### <span data-ttu-id="1ed5e-137">-PatchCategory</span><span class="sxs-lookup"><span data-stu-id="1ed5e-137">-PatchCategory</span></span>
<span data-ttu-id="1ed5e-138">Önemli güncelleştirmelerin dahil edilip edilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-138">Specifies whether important updates should be included.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed5e-139">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="1ed5e-139">-InformationAction</span></span>
<span data-ttu-id="1ed5e-140">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="1ed5e-140">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed5e-141">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="1ed5e-141">-InformationVariable</span></span>
<span data-ttu-id="1ed5e-142">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="1ed5e-142">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ed5e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ed5e-143">CommonParameters</span></span>
<span data-ttu-id="1ed5e-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ed5e-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ed5e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ed5e-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ed5e-146">INPUTS</span></span>

## <span data-ttu-id="1ed5e-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ed5e-147">OUTPUTS</span></span>

### <span data-ttu-id="1ed5e-148">AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="1ed5e-148">AutoPatchingSettings</span></span>
<span data-ttu-id="1ed5e-149">Bu cmdlet, otomatik düzeltme için ayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="1ed5e-149">This cmdlet returns object contains settings for automated patching.</span></span>

## <span data-ttu-id="1ed5e-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ed5e-150">NOTES</span></span>

## <span data-ttu-id="1ed5e-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ed5e-151">RELATED LINKS</span></span>

[<span data-ttu-id="1ed5e-152">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="1ed5e-152">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="1ed5e-153">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1ed5e-153">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


