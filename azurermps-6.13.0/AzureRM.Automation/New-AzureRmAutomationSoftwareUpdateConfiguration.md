---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591449"
---
# <span data-ttu-id="a5d50-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5d50-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a5d50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d50-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d50-103">Zamanlanmış bir Azure Otomasyonu yazılım güncelleştirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5d50-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5d50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5d50-104">SYNTAX</span></span>

### <span data-ttu-id="a5d50-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5d50-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d50-106">UX</span><span class="sxs-lookup"><span data-stu-id="a5d50-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5d50-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5d50-107">DESCRIPTION</span></span>
<span data-ttu-id="a5d50-108">Bilgisayar listesini güncelleştirmek için zamanlamada çalışan bir yazılım güncelleştirmesi yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5d50-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="a5d50-109">Bilgisayarlar hem Azure sanal makinelerini hem de Azure dışı bilgisayarları içerir.</span><span class="sxs-lookup"><span data-stu-id="a5d50-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="a5d50-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5d50-110">EXAMPLES</span></span>

### <span data-ttu-id="a5d50-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5d50-111">Example 1</span></span>
<span data-ttu-id="a5d50-112">Her Cumartesi 9:00:00 iki Windows Azure sanal makinesine kritik güncelleştirmeler yüklemek için yazılım güncelleştirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a5d50-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="a5d50-113">Bu örnekte güncelleştirme süresi 2 saat olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="a5d50-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="a5d50-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5d50-114">PARAMETERS</span></span>

### <span data-ttu-id="a5d50-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a5d50-115">-AutomationAccountName</span></span>
<span data-ttu-id="a5d50-116">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="a5d50-116">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d50-117">-AzureVMResourceId</span></span>
<span data-ttu-id="a5d50-118">Azure sanal makinelerinin kaynak kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="a5d50-118">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d50-119">-DefaultProfile</span></span>
<span data-ttu-id="a5d50-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5d50-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-121">-Süre</span><span class="sxs-lookup"><span data-stu-id="a5d50-121">-Duration</span></span>
<span data-ttu-id="a5d50-122">Güncelleştirme için en uzun süre.</span><span class="sxs-lookup"><span data-stu-id="a5d50-122">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="a5d50-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="a5d50-124">KB dışlanan güncelleştirmelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="a5d50-124">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="a5d50-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="a5d50-126">Bırakılan Linux paket maskeleri.</span><span class="sxs-lookup"><span data-stu-id="a5d50-126">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-127">-Includedkbnumber</span><span class="sxs-lookup"><span data-stu-id="a5d50-127">-IncludedKbNumber</span></span>
<span data-ttu-id="a5d50-128">KB dahil olan güncelleştirmelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="a5d50-128">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-129">-Includedpackageclassıf</span><span class="sxs-lookup"><span data-stu-id="a5d50-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="a5d50-130">Linux paket sınıflandırmaları dahildir.</span><span class="sxs-lookup"><span data-stu-id="a5d50-130">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="a5d50-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="a5d50-132">Linux paket maskeleri dahil.</span><span class="sxs-lookup"><span data-stu-id="a5d50-132">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-133">-Includedupdateclassification</span><span class="sxs-lookup"><span data-stu-id="a5d50-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="a5d50-134">Windows Update sınıflandırmaları dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a5d50-134">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="a5d50-135">-Linux</span></span>
<span data-ttu-id="a5d50-136">Yazılım güncelleştirme yapılandırmasını Linux işletim sistemi makinelerinin hedeflediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="a5d50-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="a5d50-137">-NonAzureComputer</span></span>
<span data-ttu-id="a5d50-138">Azure dışı bilgisayar adları.</span><span class="sxs-lookup"><span data-stu-id="a5d50-138">Non-Azure computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d50-139">-ResourceGroupName</span></span>
<span data-ttu-id="a5d50-140">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a5d50-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-141">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="a5d50-141">-Schedule</span></span>
<span data-ttu-id="a5d50-142">Yazılım güncelleştirme yapılandırmasında kullanılan zamanlama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a5d50-142">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="a5d50-143">-Windows</span></span>
<span data-ttu-id="a5d50-144">Windows işletim sistemi makinelerinin hedeflediği yazılım güncelleştirme yapılandırmasının olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5d50-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5d50-145">-Confirm</span></span>
<span data-ttu-id="a5d50-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5d50-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d50-147">-WhatIf</span></span>
<span data-ttu-id="a5d50-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5d50-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5d50-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5d50-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d50-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d50-150">CommonParameters</span></span>
<span data-ttu-id="a5d50-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5d50-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d50-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d50-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d50-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5d50-153">INPUTS</span></span>

### <span data-ttu-id="a5d50-154">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="a5d50-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="a5d50-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5d50-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a5d50-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="a5d50-156">System.String[]</span></span>

### <span data-ttu-id="a5d50-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="a5d50-157">System.TimeSpan</span></span>

### <span data-ttu-id="a5d50-158">Microsoft. Azure. Commands. Automation. model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="a5d50-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="a5d50-159">Microsoft. Azure. Commands. Automation. model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="a5d50-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="a5d50-160">System. String</span><span class="sxs-lookup"><span data-stu-id="a5d50-160">System.String</span></span>

## <span data-ttu-id="a5d50-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5d50-161">OUTPUTS</span></span>

### <span data-ttu-id="a5d50-162">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="a5d50-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="a5d50-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5d50-163">NOTES</span></span>

## <span data-ttu-id="a5d50-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5d50-164">RELATED LINKS</span></span>
