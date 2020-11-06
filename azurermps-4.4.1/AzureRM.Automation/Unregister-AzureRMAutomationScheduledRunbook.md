---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: aa970f71be1e80f9eb5fcc1b4ec24cf0ce7f0e9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593834"
---
# <span data-ttu-id="2ac73-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2ac73-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="2ac73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac73-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac73-103">Runbook ile zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ac73-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ac73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ac73-104">SYNTAX</span></span>

### <span data-ttu-id="2ac73-105">Byjobscheduleıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2ac73-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac73-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="2ac73-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ac73-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ac73-107">DESCRIPTION</span></span>
<span data-ttu-id="2ac73-108">**Unregister-AzureRmAutomationScheduledRunbook** cmdlet 'i, bir Azure Otomasyonu runbook ile zamanlama arasındaki ilişkilendirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ac73-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="2ac73-109">Zamanlama artık runbook 'u başlatmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="2ac73-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="2ac73-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ac73-110">EXAMPLES</span></span>

### <span data-ttu-id="2ac73-111">Örnek 1: runbook ile zamanlama arasındaki ilişkiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="2ac73-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="2ac73-112">Bu komut, Runbk01 adındaki runbook ile Runbk01Sched adlı zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ac73-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="2ac73-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ac73-113">PARAMETERS</span></span>

### <span data-ttu-id="2ac73-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2ac73-114">-AutomationAccountName</span></span>
<span data-ttu-id="2ac73-115">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ac73-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2ac73-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2ac73-116">-Force</span></span>
<span data-ttu-id="2ac73-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="2ac73-117">ps_force</span></span>

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

### <span data-ttu-id="2ac73-118">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="2ac73-118">-JobScheduleId</span></span>
<span data-ttu-id="2ac73-119">Zamanlanmış bir runbook 'un KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ac73-119">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="2ac73-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac73-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ac73-121">Zamanlanmış runbook için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ac73-121">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="2ac73-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2ac73-122">-RunbookName</span></span>
<span data-ttu-id="2ac73-123">Bu cmdlet 'in bir zamanlamaya dahil olduğu runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ac73-123">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="2ac73-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="2ac73-124">-ScheduleName</span></span>
<span data-ttu-id="2ac73-125">Bu cmdlet 'in bir runbook 'un ilişkisini kaldırdıkları zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2ac73-125">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="2ac73-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ac73-126">-Confirm</span></span>
<span data-ttu-id="2ac73-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ac73-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ac73-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ac73-128">-WhatIf</span></span>
<span data-ttu-id="2ac73-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ac73-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ac73-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ac73-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ac73-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac73-131">-DefaultProfile</span></span>
<span data-ttu-id="2ac73-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ac73-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ac73-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac73-133">CommonParameters</span></span>
<span data-ttu-id="2ac73-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ac73-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac73-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac73-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac73-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ac73-136">INPUTS</span></span>

## <span data-ttu-id="2ac73-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ac73-137">OUTPUTS</span></span>

## <span data-ttu-id="2ac73-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ac73-138">NOTES</span></span>

## <span data-ttu-id="2ac73-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ac73-139">RELATED LINKS</span></span>

[<span data-ttu-id="2ac73-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2ac73-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="2ac73-141">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2ac73-141">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


