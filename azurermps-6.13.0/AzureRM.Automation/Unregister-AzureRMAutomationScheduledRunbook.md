---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: ab55201ab2566c814455b6b0f6fe3c2ddf6b3a57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593328"
---
# <span data-ttu-id="1750f-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1750f-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="1750f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1750f-102">SYNOPSIS</span></span>
<span data-ttu-id="1750f-103">Runbook ile zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1750f-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1750f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1750f-104">SYNTAX</span></span>

### <span data-ttu-id="1750f-105">Byjobscheduleıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1750f-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1750f-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="1750f-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1750f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1750f-107">DESCRIPTION</span></span>
<span data-ttu-id="1750f-108">**Unregister-AzureRmAutomationScheduledRunbook** cmdlet 'i, bir Azure Otomasyonu runbook ile zamanlama arasındaki ilişkilendirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1750f-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="1750f-109">Zamanlama artık runbook 'u başlatmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="1750f-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="1750f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1750f-110">EXAMPLES</span></span>

### <span data-ttu-id="1750f-111">Örnek 1: runbook ile zamanlama arasındaki ilişkiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="1750f-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="1750f-112">Bu komut, Runbk01 adındaki runbook ile Runbk01Sched adlı zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1750f-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="1750f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1750f-113">PARAMETERS</span></span>

### <span data-ttu-id="1750f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1750f-114">-AutomationAccountName</span></span>
<span data-ttu-id="1750f-115">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="1750f-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1750f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1750f-116">-DefaultProfile</span></span>
<span data-ttu-id="1750f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="1750f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1750f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1750f-118">-Force</span></span>
<span data-ttu-id="1750f-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="1750f-119">ps_force</span></span>

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

### <span data-ttu-id="1750f-120">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="1750f-120">-JobScheduleId</span></span>
<span data-ttu-id="1750f-121">Zamanlanmış bir runbook 'un KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1750f-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="1750f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1750f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1750f-123">Zamanlanmış runbook için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1750f-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="1750f-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="1750f-124">-RunbookName</span></span>
<span data-ttu-id="1750f-125">Bu cmdlet 'in bir zamanlamaya dahil olduğu runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1750f-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="1750f-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="1750f-126">-ScheduleName</span></span>
<span data-ttu-id="1750f-127">Bu cmdlet 'in bir runbook 'un ilişkisini kaldırdıkları zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1750f-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="1750f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="1750f-128">-Confirm</span></span>
<span data-ttu-id="1750f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1750f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1750f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1750f-130">-WhatIf</span></span>
<span data-ttu-id="1750f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1750f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1750f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1750f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1750f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1750f-133">CommonParameters</span></span>
<span data-ttu-id="1750f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1750f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1750f-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1750f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1750f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1750f-136">INPUTS</span></span>

### <span data-ttu-id="1750f-137">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1750f-137">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1750f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1750f-138">System.String</span></span>

## <span data-ttu-id="1750f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1750f-139">OUTPUTS</span></span>

### <span data-ttu-id="1750f-140">System. void</span><span class="sxs-lookup"><span data-stu-id="1750f-140">System.Void</span></span>

## <span data-ttu-id="1750f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1750f-141">NOTES</span></span>

## <span data-ttu-id="1750f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1750f-142">RELATED LINKS</span></span>

[<span data-ttu-id="1750f-143">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1750f-143">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="1750f-144">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="1750f-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

