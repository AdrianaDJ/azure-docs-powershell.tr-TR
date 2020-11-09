---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321861"
---
# <span data-ttu-id="f8c3a-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c3a-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f8c3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8c3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c3a-103">Zamanlanmış bir Azure Otomasyonu yazılım güncelleştirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="f8c3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8c3a-104">SYNTAX</span></span>

### <span data-ttu-id="f8c3a-105">Windows (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f8c3a-105">Windows (Default)</span></span>
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

### <span data-ttu-id="f8c3a-106">UX</span><span class="sxs-lookup"><span data-stu-id="f8c3a-106">Linux</span></span>
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

## <span data-ttu-id="f8c3a-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8c3a-107">DESCRIPTION</span></span>
<span data-ttu-id="f8c3a-108">Bilgisayar listesini güncelleştirmek için zamanlamada çalışan bir yazılım güncelleştirmesi yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="f8c3a-109">Bilgisayarlar hem Azure sanal makinelerini hem de az olmayan bilgisayarlar içerir.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="f8c3a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8c3a-110">EXAMPLES</span></span>

### <span data-ttu-id="f8c3a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f8c3a-111">Example 1</span></span>
<span data-ttu-id="f8c3a-112">Her Cumartesi 9:00:00 iki Windows Azure sanal makinesine kritik güncelleştirmeler yüklemek için yazılım güncelleştirme yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="f8c3a-113">Bu örnekte güncelleştirme süresi 2 saat olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-113">Update duration is set to 2 hours in this example.</span></span>

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
                                                 -AzureVMResourceId $targetMachines `
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

## <span data-ttu-id="f8c3a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8c3a-114">PARAMETERS</span></span>

### <span data-ttu-id="f8c3a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8c3a-115">-AutomationAccountName</span></span>
<span data-ttu-id="f8c3a-116">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-116">The automation account name.</span></span>

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

### <span data-ttu-id="f8c3a-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="f8c3a-117">-AzureQuery</span></span>
<span data-ttu-id="f8c3a-118">Dinamik grup Azure sorgusu.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="f8c3a-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="f8c3a-119">-AzureVMResourceId</span></span>
<span data-ttu-id="f8c3a-120">Azure sanal makinelerinin kaynak kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="f8c3a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c3a-121">-DefaultProfile</span></span>
<span data-ttu-id="f8c3a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c3a-123">-Süre</span><span class="sxs-lookup"><span data-stu-id="f8c3a-123">-Duration</span></span>
<span data-ttu-id="f8c3a-124">Güncelleştirme için en uzun süre.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="f8c3a-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="f8c3a-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="f8c3a-126">KB dışlanan güncelleştirmelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="f8c3a-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="f8c3a-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="f8c3a-128">Bırakılan Linux paket maskeleri.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="f8c3a-129">-Includedkbnumber</span><span class="sxs-lookup"><span data-stu-id="f8c3a-129">-IncludedKbNumber</span></span>
<span data-ttu-id="f8c3a-130">KB dahil olan güncelleştirmelerin sayısı.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="f8c3a-131">-Includedpackageclassıf</span><span class="sxs-lookup"><span data-stu-id="f8c3a-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="f8c3a-132">Linux paket sınıflandırmaları dahildir.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="f8c3a-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="f8c3a-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="f8c3a-134">Linux paket maskeleri dahil.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="f8c3a-135">-Includedupdateclassification</span><span class="sxs-lookup"><span data-stu-id="f8c3a-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="f8c3a-136">Windows Update sınıflandırmaları dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="f8c3a-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="f8c3a-137">-Linux</span></span>
<span data-ttu-id="f8c3a-138">Yazılım güncelleştirme yapılandırmasını Linux işletim sistemi makinelerinin hedeflediği anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="f8c3a-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="f8c3a-139">-NonAzureComputer</span></span>
<span data-ttu-id="f8c3a-140">Daha az olmayan bilgisayar adları.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="f8c3a-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="f8c3a-141">-NonAzureQuery</span></span>
<span data-ttu-id="f8c3a-142">Azure dışı sorgu</span><span class="sxs-lookup"><span data-stu-id="f8c3a-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="f8c3a-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="f8c3a-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="f8c3a-144">Görevi gönder.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-144">Post task.</span></span>

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

### <span data-ttu-id="f8c3a-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="f8c3a-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="f8c3a-146">Post görev parametresi.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-146">Post task parameter.</span></span>

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

### <span data-ttu-id="f8c3a-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="f8c3a-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="f8c3a-148">Görev öncesi.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-148">Pre task.</span></span>

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

### <span data-ttu-id="f8c3a-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="f8c3a-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="f8c3a-150">Görev öncesi parametresi.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="f8c3a-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="f8c3a-151">-RebootOnly</span></span>
<span data-ttu-id="f8c3a-152">Yazılım güncelleştirmesi yapılandırmasının yalnızca makineleri yeniden başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="f8c3a-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="f8c3a-153">-RebootSetting</span></span>
<span data-ttu-id="f8c3a-154">Yeniden başlatma ayarı.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="f8c3a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c3a-155">-ResourceGroupName</span></span>
<span data-ttu-id="f8c3a-156">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-156">The resource group name.</span></span>

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

### <span data-ttu-id="f8c3a-157">-Zamanlama</span><span class="sxs-lookup"><span data-stu-id="f8c3a-157">-Schedule</span></span>
<span data-ttu-id="f8c3a-158">Yazılım güncelleştirme yapılandırmasında kullanılan zamanlama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="f8c3a-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="f8c3a-159">-Windows</span></span>
<span data-ttu-id="f8c3a-160">Windows işletim sistemi makinelerinin hedeflediği yazılım güncelleştirme yapılandırmasının olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="f8c3a-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="f8c3a-161">-Confirm</span></span>
<span data-ttu-id="f8c3a-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c3a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c3a-163">-WhatIf</span></span>
<span data-ttu-id="f8c3a-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8c3a-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c3a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c3a-166">CommonParameters</span></span>
<span data-ttu-id="f8c3a-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8c3a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c3a-168">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8c3a-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c3a-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8c3a-169">INPUTS</span></span>

### <span data-ttu-id="f8c3a-170">Microsoft. Azure. Commands. Automation. model. zamanlama</span><span class="sxs-lookup"><span data-stu-id="f8c3a-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="f8c3a-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8c3a-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f8c3a-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="f8c3a-172">System.String[]</span></span>

### <span data-ttu-id="f8c3a-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="f8c3a-173">System.TimeSpan</span></span>

### <span data-ttu-id="f8c3a-174">Microsoft. Azure. Commands. Automation. model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="f8c3a-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="f8c3a-175">Microsoft. Azure. Commands. Automation. model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="f8c3a-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="f8c3a-176">System. String</span><span class="sxs-lookup"><span data-stu-id="f8c3a-176">System.String</span></span>

## <span data-ttu-id="f8c3a-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8c3a-177">OUTPUTS</span></span>

### <span data-ttu-id="f8c3a-178">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8c3a-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f8c3a-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8c3a-179">NOTES</span></span>

## <span data-ttu-id="f8c3a-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8c3a-180">RELATED LINKS</span></span>
