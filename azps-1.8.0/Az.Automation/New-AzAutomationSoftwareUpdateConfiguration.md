---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 1e5c30f1e4ca1fef4aa78b2e4b6394068878b1c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761560"
---
# <span data-ttu-id="3cfaa-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cfaa-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3cfaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cfaa-102">SYNOPSIS</span></span>
<span data-ttu-id="3cfaa-103">Zamanlanmış bir Azure Otomasyonu yazılım güncelleştirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="3cfaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3cfaa-104">SYNTAX</span></span>

### <span data-ttu-id="3cfaa-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3cfaa-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cfaa-106">UX</span><span class="sxs-lookup"><span data-stu-id="3cfaa-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cfaa-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3cfaa-107">DESCRIPTION</span></span>
<span data-ttu-id="3cfaa-108">Bilgisayar listesini güncelleştirmek için zamanlamada çalışan bir yazılım güncelleştirmesi yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="3cfaa-109">Bilgisayarlar hem Azure sanal makinelerini hem de az olmayan bilgisayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="3cfaa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3cfaa-110">EXAMPLES</span></span>

### <span data-ttu-id="3cfaa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3cfaa-111">Example 1</span></span>
<span data-ttu-id="3cfaa-112">Her Cumartesi 9:00:00 iki Windows Azure sanal makinesine kritik güncelleştirmeler yüklemek için yazılım güncelleştirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="3cfaa-113">Bu örnekte güncelleştirme süresi 2 saat olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
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

## <span data-ttu-id="3cfaa-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3cfaa-114">PARAMETERS</span></span>

### <span data-ttu-id="3cfaa-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3cfaa-115">-AutomationAccountName</span></span>
<span data-ttu-id="3cfaa-116">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-116">The automation account name.</span></span>

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

### <span data-ttu-id="3cfaa-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="3cfaa-117">-AzureQuery</span></span>
<span data-ttu-id="3cfaa-118">Dinamik grup Azure sorgusu.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="3cfaa-119">-AzureVMResourceId</span></span>
<span data-ttu-id="3cfaa-120">Azure sanal makinelerinin kaynak kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="3cfaa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cfaa-121">-DefaultProfile</span></span>
<span data-ttu-id="3cfaa-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-123">-Süre</span><span class="sxs-lookup"><span data-stu-id="3cfaa-123">-Duration</span></span>
<span data-ttu-id="3cfaa-124">Güncelleştirme için en uzun süre.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="3cfaa-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="3cfaa-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="3cfaa-126">KB dışlanan güncelleştirmelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="3cfaa-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="3cfaa-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="3cfaa-128">Bırakılan Linux paket maskeleri.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="3cfaa-129">-Includedkbnumber</span><span class="sxs-lookup"><span data-stu-id="3cfaa-129">-IncludedKbNumber</span></span>
<span data-ttu-id="3cfaa-130">KB dahil olan güncelleştirmelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="3cfaa-131">-Includedpackageclassıf</span><span class="sxs-lookup"><span data-stu-id="3cfaa-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="3cfaa-132">Linux paket sınıflandırmaları dahildir.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="3cfaa-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="3cfaa-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="3cfaa-134">Linux paket maskeleri dahil.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="3cfaa-135">-Includedupdateclassification</span><span class="sxs-lookup"><span data-stu-id="3cfaa-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="3cfaa-136">Windows Update sınıflandırmaları dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="3cfaa-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="3cfaa-137">-Linux</span></span>
<span data-ttu-id="3cfaa-138">Yazılım güncelleştirme yapılandırmasını Linux işletim sistemi makinelerinin hedeflediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="3cfaa-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="3cfaa-139">-NonAzureComputer</span></span>
<span data-ttu-id="3cfaa-140">Daha az olmayan bilgisayar adları.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="3cfaa-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="3cfaa-141">-NonAzureQuery</span></span>
<span data-ttu-id="3cfaa-142">Azure dışı sorgu</span><span class="sxs-lookup"><span data-stu-id="3cfaa-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="3cfaa-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="3cfaa-144">Görevi gönder.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-144">Post task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="3cfaa-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="3cfaa-146">Post görev parametresi.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="3cfaa-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="3cfaa-148">Görev öncesi.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-148">Pre task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="3cfaa-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="3cfaa-150">Görev öncesi parametresi.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="3cfaa-151">-RebootOnly</span></span>
<span data-ttu-id="3cfaa-152">Yazılım güncelleştirmesi yapılandırmasının yalnızca makineleri yeniden başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="3cfaa-153">-RebootSetting</span></span>
<span data-ttu-id="3cfaa-154">Yeniden başlatma.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-154">Reboot Seeting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cfaa-155">-ResourceGroupName</span></span>
<span data-ttu-id="3cfaa-156">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-156">The resource group name.</span></span>

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

### <span data-ttu-id="3cfaa-157">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="3cfaa-157">-Schedule</span></span>
<span data-ttu-id="3cfaa-158">Yazılım güncelleştirme yapılandırmasında kullanılan zamanlama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="3cfaa-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="3cfaa-159">-Windows</span></span>
<span data-ttu-id="3cfaa-160">Windows işletim sistemi makinelerinin hedeflediği yazılım güncelleştirme yapılandırmasının olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="3cfaa-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="3cfaa-161">-Confirm</span></span>
<span data-ttu-id="3cfaa-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cfaa-163">-WhatIf</span></span>
<span data-ttu-id="3cfaa-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cfaa-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cfaa-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cfaa-166">CommonParameters</span></span>
<span data-ttu-id="3cfaa-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3cfaa-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cfaa-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cfaa-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cfaa-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3cfaa-169">INPUTS</span></span>

### <span data-ttu-id="3cfaa-170">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="3cfaa-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="3cfaa-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3cfaa-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3cfaa-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="3cfaa-172">System.String[]</span></span>

### <span data-ttu-id="3cfaa-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="3cfaa-173">System.TimeSpan</span></span>

### <span data-ttu-id="3cfaa-174">Microsoft. Azure. Commands. Automation. model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="3cfaa-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="3cfaa-175">Microsoft. Azure. Commands. Automation. model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="3cfaa-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="3cfaa-176">System. String</span><span class="sxs-lookup"><span data-stu-id="3cfaa-176">System.String</span></span>

## <span data-ttu-id="3cfaa-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3cfaa-177">OUTPUTS</span></span>

### <span data-ttu-id="3cfaa-178">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cfaa-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3cfaa-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3cfaa-179">NOTES</span></span>

## <span data-ttu-id="3cfaa-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3cfaa-180">RELATED LINKS</span></span>
