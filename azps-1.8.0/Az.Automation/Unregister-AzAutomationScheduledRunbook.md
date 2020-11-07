---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 203573856740e0e155e7dff0755ecad1b5399440
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761479"
---
# <span data-ttu-id="ce943-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ce943-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="ce943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce943-102">SYNOPSIS</span></span>
<span data-ttu-id="ce943-103">Runbook ile zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce943-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="ce943-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce943-104">SYNTAX</span></span>

### <span data-ttu-id="ce943-105">Byjobscheduleıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ce943-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ce943-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="ce943-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce943-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce943-107">DESCRIPTION</span></span>
<span data-ttu-id="ce943-108">**Unregister-AzAutomationScheduledRunbook** cmdlet 'i, bir Azure Otomasyonu runbook ile zamanlama arasındaki ilişkilendirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce943-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="ce943-109">Zamanlama artık runbook 'u başlatmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="ce943-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="ce943-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce943-110">EXAMPLES</span></span>

### <span data-ttu-id="ce943-111">Örnek 1: runbook ile zamanlama arasındaki ilişkiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="ce943-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="ce943-112">Bu komut, Runbk01 adındaki runbook ile Runbk01Sched adlı zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ce943-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="ce943-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce943-113">PARAMETERS</span></span>

### <span data-ttu-id="ce943-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ce943-114">-AutomationAccountName</span></span>
<span data-ttu-id="ce943-115">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce943-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ce943-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce943-116">-DefaultProfile</span></span>
<span data-ttu-id="ce943-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ce943-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce943-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce943-118">-Force</span></span>
<span data-ttu-id="ce943-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="ce943-119">ps_force</span></span>

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

### <span data-ttu-id="ce943-120">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="ce943-120">-JobScheduleId</span></span>
<span data-ttu-id="ce943-121">Zamanlanmış bir runbook 'un KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce943-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="ce943-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce943-122">-ResourceGroupName</span></span>
<span data-ttu-id="ce943-123">Zamanlanmış runbook için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce943-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="ce943-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="ce943-124">-RunbookName</span></span>
<span data-ttu-id="ce943-125">Bu cmdlet 'in bir zamanlamaya dahil olduğu runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce943-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="ce943-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="ce943-126">-ScheduleName</span></span>
<span data-ttu-id="ce943-127">Bu cmdlet 'in bir runbook 'un ilişkisini kaldırdıkları zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce943-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="ce943-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce943-128">-Confirm</span></span>
<span data-ttu-id="ce943-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce943-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce943-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce943-130">-WhatIf</span></span>
<span data-ttu-id="ce943-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce943-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce943-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce943-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce943-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce943-133">CommonParameters</span></span>
<span data-ttu-id="ce943-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce943-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce943-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce943-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce943-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce943-136">INPUTS</span></span>

### <span data-ttu-id="ce943-137">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ce943-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ce943-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ce943-138">System.String</span></span>

## <span data-ttu-id="ce943-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce943-139">OUTPUTS</span></span>

### <span data-ttu-id="ce943-140">System. void</span><span class="sxs-lookup"><span data-stu-id="ce943-140">System.Void</span></span>

## <span data-ttu-id="ce943-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce943-141">NOTES</span></span>

## <span data-ttu-id="ce943-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce943-142">RELATED LINKS</span></span>

[<span data-ttu-id="ce943-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ce943-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="ce943-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="ce943-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


