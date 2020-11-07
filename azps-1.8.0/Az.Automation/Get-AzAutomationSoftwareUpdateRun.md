---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: 1f4dc8ee72d2d3feaf7f63d3de570563f4314ea8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761595"
---
# <span data-ttu-id="86778-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="86778-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="86778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86778-102">SYNOPSIS</span></span>
<span data-ttu-id="86778-103">Azure Otomasyonu yazılım güncelleştirmesi çalıştırmalarının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="86778-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="86778-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86778-104">SYNTAX</span></span>

### <span data-ttu-id="86778-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="86778-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86778-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="86778-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86778-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="86778-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86778-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="86778-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="86778-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="86778-109">DESCRIPTION</span></span>
<span data-ttu-id="86778-110">Get-AzAutomationSoftwareUpdateRun cmdlet 'i yazılım güncelleştirmesi çalıştırmalarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="86778-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="86778-111">Yazılım güncelleştirme yapılandırmasının ilişkili zamanlaması olduğundan, birden çok kez tetiklenebilir.</span><span class="sxs-lookup"><span data-stu-id="86778-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="86778-112">Zamanlamanın her tetiklenişinde, bir güncelleştirme çalıştırması oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="86778-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="86778-113">Güncelleştirme çalıştırması, tüm makine çalıştırmalarının sonucunun bir topladır.</span><span class="sxs-lookup"><span data-stu-id="86778-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="86778-114">SoftwareUpdateConfigurationName parametresini geçirerek belirli yazılım güncelleştirme yapılandırması için çalışmalar yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86778-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="86778-115">Belirli bir çalıştırmalar edinmek için name parametresini geçirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="86778-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="86778-116">Ayrıca, belirli bir durumla birlikte çalışan, belirli operatins sistem hedeflemesi çalıştıran ya da uygun parametreyi geçirerek belirli bir süre geçtikten sonra da çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="86778-116">You can also list runs with specific status, runs targeting specific operatins system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="86778-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86778-117">EXAMPLES</span></span>

### <span data-ttu-id="86778-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="86778-118">Example 1</span></span>
<span data-ttu-id="86778-119">Bu örnekte, belirli bir yazılım güncelleştirme yapılandırması tarafından tetiklenen tüm güncelleştirme çalıştırmaları listelenir.</span><span class="sxs-lookup"><span data-stu-id="86778-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="86778-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86778-120">PARAMETERS</span></span>

### <span data-ttu-id="86778-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="86778-121">-AutomationAccountName</span></span>
<span data-ttu-id="86778-122">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="86778-122">The automation account name.</span></span>

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

### <span data-ttu-id="86778-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86778-123">-DefaultProfile</span></span>
<span data-ttu-id="86778-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="86778-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86778-125">-ID</span><span class="sxs-lookup"><span data-stu-id="86778-125">-Id</span></span>
<span data-ttu-id="86778-126">Yazılım güncelleştirmesi yapılandırma çalıştırmasının kimliği.</span><span class="sxs-lookup"><span data-stu-id="86778-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86778-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="86778-127">-OperatingSystem</span></span>
<span data-ttu-id="86778-128">Çalıştırmanın işletim sistemi.</span><span class="sxs-lookup"><span data-stu-id="86778-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86778-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86778-129">-ResourceGroupName</span></span>
<span data-ttu-id="86778-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="86778-130">The resource group name.</span></span>

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

### <span data-ttu-id="86778-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="86778-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="86778-132">Yazılım güncelleştirme yapılandırması çalıştırmayı tetikledi.</span><span class="sxs-lookup"><span data-stu-id="86778-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86778-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="86778-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="86778-134">Çalıştırmayı tetikleyen yazılım güncelleştirmesi yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="86778-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86778-135">-Başlangıçsaati</span><span class="sxs-lookup"><span data-stu-id="86778-135">-StartTime</span></span>
<span data-ttu-id="86778-136">Çalıştırmanın minimum başlangıç saati.</span><span class="sxs-lookup"><span data-stu-id="86778-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86778-137">-Durum</span><span class="sxs-lookup"><span data-stu-id="86778-137">-Status</span></span>
<span data-ttu-id="86778-138">Çalışma durumu.</span><span class="sxs-lookup"><span data-stu-id="86778-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86778-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86778-139">CommonParameters</span></span>
<span data-ttu-id="86778-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86778-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86778-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86778-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86778-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86778-142">INPUTS</span></span>

### <span data-ttu-id="86778-143">System. Guid</span><span class="sxs-lookup"><span data-stu-id="86778-143">System.Guid</span></span>

### <span data-ttu-id="86778-144">System. String</span><span class="sxs-lookup"><span data-stu-id="86778-144">System.String</span></span>

### <span data-ttu-id="86778-145">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="86778-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="86778-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. model. UpdateManagement. OperatingSystemType, Microsoft. Azure. PowerShell. cmdlet. Automation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="86778-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="86778-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. PowerShell. cmdlet. Automation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="86778-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="86778-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="86778-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="86778-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86778-149">OUTPUTS</span></span>

### <span data-ttu-id="86778-150">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="86778-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="86778-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86778-151">NOTES</span></span>

## <span data-ttu-id="86778-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86778-152">RELATED LINKS</span></span>