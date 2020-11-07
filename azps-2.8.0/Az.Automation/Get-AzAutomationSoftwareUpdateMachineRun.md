---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 80bba3309c0c23862fdb5efbbe6f373b8d1a964a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753305"
---
# <span data-ttu-id="c8c86-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="c8c86-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="c8c86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c86-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c86-103">Azure Otomasyonu yazılım güncelleştirmesi yapılandırma makinesinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="c8c86-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="c8c86-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8c86-104">SYNTAX</span></span>

### <span data-ttu-id="c8c86-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8c86-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c86-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="c8c86-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8c86-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="c8c86-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8c86-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="c8c86-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8c86-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8c86-109">DESCRIPTION</span></span>
<span data-ttu-id="c8c86-110">Bu cmdlet, makine çalıştırmaları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c8c86-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="c8c86-111">Her yazılım güncelleştirmesi çalıştırması, yazılım güncelleştirme yapılandırması hedef makinesinin her biri için bir makinenin çalıştırılmasını tetikler.</span><span class="sxs-lookup"><span data-stu-id="c8c86-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="c8c86-112">Belirli bir makineyi çalıştırmak için ID parametresini geçirin.</span><span class="sxs-lookup"><span data-stu-id="c8c86-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="c8c86-113">Tüm makine çalıştırmalarını, belirli bir bilgisayar için tüm çalıştırmaları listeleyebilir, ilgili parametreleri geçirerek tüm belirli bir durumla birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="c8c86-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="c8c86-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8c86-114">EXAMPLES</span></span>

### <span data-ttu-id="c8c86-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c8c86-115">Example 1</span></span>
<span data-ttu-id="c8c86-116">Bu örnek belirtilen Azure sanal makinesi için tüm başarısız makine çalıştırmalarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="c8c86-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="c8c86-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8c86-117">PARAMETERS</span></span>

### <span data-ttu-id="c8c86-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c8c86-118">-AutomationAccountName</span></span>
<span data-ttu-id="c8c86-119">Otomasyon hesap adı.</span><span class="sxs-lookup"><span data-stu-id="c8c86-119">The automation account name.</span></span>

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

### <span data-ttu-id="c8c86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c86-120">-DefaultProfile</span></span>
<span data-ttu-id="c8c86-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8c86-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c86-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c8c86-122">-Id</span></span>
<span data-ttu-id="c8c86-123">Yazılım güncelleştirmesi makinesinin kimliği.</span><span class="sxs-lookup"><span data-stu-id="c8c86-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="c8c86-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c86-124">-ResourceGroupName</span></span>
<span data-ttu-id="c8c86-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c8c86-125">The resource group name.</span></span>

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

### <span data-ttu-id="c8c86-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="c8c86-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="c8c86-127">Yazılım güncelleştirmesi çalışır.</span><span class="sxs-lookup"><span data-stu-id="c8c86-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c86-128">-Softwareupdaterunıd</span><span class="sxs-lookup"><span data-stu-id="c8c86-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="c8c86-129">Yazılım güncelleştirmesi çalıştırmasının kimliği.</span><span class="sxs-lookup"><span data-stu-id="c8c86-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c86-130">-Durum</span><span class="sxs-lookup"><span data-stu-id="c8c86-130">-Status</span></span>
<span data-ttu-id="c8c86-131">Makinenin durumu.</span><span class="sxs-lookup"><span data-stu-id="c8c86-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c86-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="c8c86-132">-TargetComputer</span></span>
<span data-ttu-id="c8c86-133">makine için hedef bilgisayar.</span><span class="sxs-lookup"><span data-stu-id="c8c86-133">target computer for the machine run.</span></span>
<span data-ttu-id="c8c86-134">Bir bilgisayar adı veya Azure VM kaynak kimliği olabilir.</span><span class="sxs-lookup"><span data-stu-id="c8c86-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c86-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c86-135">CommonParameters</span></span>
<span data-ttu-id="c8c86-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8c86-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c86-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8c86-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c86-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8c86-138">INPUTS</span></span>

### <span data-ttu-id="c8c86-139">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c8c86-139">System.Guid</span></span>

### <span data-ttu-id="c8c86-140">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="c8c86-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="c8c86-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateMachineRunStatus, Microsoft. Azure. PowerShell. cmdlet. Automation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c8c86-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c8c86-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c8c86-142">System.String</span></span>

## <span data-ttu-id="c8c86-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8c86-143">OUTPUTS</span></span>

### <span data-ttu-id="c8c86-144">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="c8c86-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="c8c86-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8c86-145">NOTES</span></span>

## <span data-ttu-id="c8c86-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8c86-146">RELATED LINKS</span></span>