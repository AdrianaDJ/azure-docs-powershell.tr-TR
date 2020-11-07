---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 2444579c8a155cc2957ab8432eb63cc28300bfe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761598"
---
# <span data-ttu-id="caf6d-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="caf6d-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="caf6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf6d-102">SYNOPSIS</span></span>
<span data-ttu-id="caf6d-103">Otomasyon Runbook 'ları ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="caf6d-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="caf6d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="caf6d-104">SYNTAX</span></span>

### <span data-ttu-id="caf6d-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="caf6d-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caf6d-106">Byjobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="caf6d-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caf6d-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="caf6d-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caf6d-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="caf6d-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caf6d-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="caf6d-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caf6d-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="caf6d-110">DESCRIPTION</span></span>
<span data-ttu-id="caf6d-111">**Get-AzAutomationScheduledRunbook** cmdlet 'i bir veya daha fazla Azure Otomasyonu runbook 'u ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="caf6d-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="caf6d-112">Varsayılan olarak, bu cmdlet tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="caf6d-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="caf6d-113">Belirli runbook zamanlamalarını görmek için bir runbook veya zamanlamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="caf6d-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="caf6d-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="caf6d-114">EXAMPLES</span></span>

### <span data-ttu-id="caf6d-115">Örnek 1: tüm zamanlanmış runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="caf6d-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="caf6d-116">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="caf6d-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="caf6d-117">Örnek 2: runbook ile ilişkili tüm zamanlamaları alma</span><span class="sxs-lookup"><span data-stu-id="caf6d-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="caf6d-118">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki runbook Runbk01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="caf6d-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="caf6d-119">Örnek 3: zamanlamayla ilişkili tüm runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="caf6d-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="caf6d-120">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki zamanlama Schedule01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="caf6d-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="caf6d-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="caf6d-121">PARAMETERS</span></span>

### <span data-ttu-id="caf6d-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="caf6d-122">-AutomationAccountName</span></span>
<span data-ttu-id="caf6d-123">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="caf6d-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="caf6d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf6d-124">-DefaultProfile</span></span>
<span data-ttu-id="caf6d-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="caf6d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caf6d-126">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="caf6d-126">-JobScheduleId</span></span>
<span data-ttu-id="caf6d-127">Bu cmdlet 'in aldığı zamanlanmış iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="caf6d-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="caf6d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caf6d-128">-ResourceGroupName</span></span>
<span data-ttu-id="caf6d-129">Bu cmdlet 'in aldığı zamanlanmış runbook 'lar için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="caf6d-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="caf6d-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="caf6d-130">-RunbookName</span></span>
<span data-ttu-id="caf6d-131">Bu cmdlet 'in zamanlanmış runbook 'ları aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="caf6d-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf6d-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="caf6d-132">-ScheduleName</span></span>
<span data-ttu-id="caf6d-133">Bu cmdlet 'in zamanlanmış runbook 'ları aldığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="caf6d-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="caf6d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf6d-134">CommonParameters</span></span>
<span data-ttu-id="caf6d-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="caf6d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf6d-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caf6d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf6d-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="caf6d-137">INPUTS</span></span>

### <span data-ttu-id="caf6d-138">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="caf6d-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="caf6d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="caf6d-139">System.String</span></span>

## <span data-ttu-id="caf6d-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="caf6d-140">OUTPUTS</span></span>

### <span data-ttu-id="caf6d-141">Microsoft. Azure. Commands. Automation. model. Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="caf6d-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="caf6d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="caf6d-142">NOTES</span></span>

## <span data-ttu-id="caf6d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="caf6d-143">RELATED LINKS</span></span>

[<span data-ttu-id="caf6d-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="caf6d-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="caf6d-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="caf6d-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


