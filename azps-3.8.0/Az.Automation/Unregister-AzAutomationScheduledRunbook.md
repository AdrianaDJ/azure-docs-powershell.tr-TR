---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937878"
---
# <span data-ttu-id="1b979-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1b979-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="1b979-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b979-102">SYNOPSIS</span></span>
<span data-ttu-id="1b979-103">Runbook ile zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b979-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="1b979-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b979-104">SYNTAX</span></span>

### <span data-ttu-id="1b979-105">Byjobscheduleıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b979-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b979-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="1b979-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b979-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b979-107">DESCRIPTION</span></span>
<span data-ttu-id="1b979-108">**Unregister-AzAutomationScheduledRunbook** cmdlet 'i, bir Azure Otomasyonu runbook ile zamanlama arasındaki ilişkilendirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b979-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="1b979-109">Zamanlama artık runbook 'u başlatmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="1b979-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="1b979-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b979-110">EXAMPLES</span></span>

### <span data-ttu-id="1b979-111">Örnek 1: runbook ile zamanlama arasındaki ilişkiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="1b979-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="1b979-112">Bu komut, Runbk01 adındaki runbook ile Runbk01Sched adlı zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b979-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="1b979-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b979-113">PARAMETERS</span></span>

### <span data-ttu-id="1b979-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1b979-114">-AutomationAccountName</span></span>
<span data-ttu-id="1b979-115">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b979-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1b979-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b979-116">-DefaultProfile</span></span>
<span data-ttu-id="1b979-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1b979-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b979-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1b979-118">-Force</span></span>
<span data-ttu-id="1b979-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="1b979-119">ps_force</span></span>

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

### <span data-ttu-id="1b979-120">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="1b979-120">-JobScheduleId</span></span>
<span data-ttu-id="1b979-121">Zamanlanmış bir runbook 'un KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b979-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b979-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b979-122">-ResourceGroupName</span></span>
<span data-ttu-id="1b979-123">Zamanlanmış runbook için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b979-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="1b979-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="1b979-124">-RunbookName</span></span>
<span data-ttu-id="1b979-125">Bu cmdlet 'in bir zamanlamaya dahil olduğu runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b979-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b979-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="1b979-126">-ScheduleName</span></span>
<span data-ttu-id="1b979-127">Bu cmdlet 'in bir runbook 'un ilişkisini kaldırdıkları zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b979-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b979-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b979-128">-Confirm</span></span>
<span data-ttu-id="1b979-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b979-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b979-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b979-130">-WhatIf</span></span>
<span data-ttu-id="1b979-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b979-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b979-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b979-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b979-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b979-133">CommonParameters</span></span>
<span data-ttu-id="1b979-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b979-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b979-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b979-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b979-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b979-136">INPUTS</span></span>

### <span data-ttu-id="1b979-137">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b979-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1b979-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1b979-138">System.String</span></span>

## <span data-ttu-id="1b979-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b979-139">OUTPUTS</span></span>

### <span data-ttu-id="1b979-140">System. void</span><span class="sxs-lookup"><span data-stu-id="1b979-140">System.Void</span></span>

## <span data-ttu-id="1b979-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b979-141">NOTES</span></span>

## <span data-ttu-id="1b979-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b979-142">RELATED LINKS</span></span>

[<span data-ttu-id="1b979-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1b979-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="1b979-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1b979-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


