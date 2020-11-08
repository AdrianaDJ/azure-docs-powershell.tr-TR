---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098145"
---
# <span data-ttu-id="8ae61-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8ae61-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="8ae61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ae61-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae61-103">Otomasyon Runbook 'ları ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="8ae61-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="8ae61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ae61-104">SYNTAX</span></span>

### <span data-ttu-id="8ae61-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ae61-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ae61-106">Byjobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="8ae61-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ae61-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="8ae61-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ae61-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="8ae61-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ae61-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="8ae61-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ae61-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ae61-110">DESCRIPTION</span></span>
<span data-ttu-id="8ae61-111">**Get-AzAutomationScheduledRunbook** cmdlet 'i bir veya daha fazla Azure Otomasyonu runbook 'u ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="8ae61-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="8ae61-112">Varsayılan olarak, bu cmdlet tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8ae61-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="8ae61-113">Belirli runbook zamanlamalarını görmek için bir runbook veya zamanlamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8ae61-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="8ae61-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ae61-114">EXAMPLES</span></span>

### <span data-ttu-id="8ae61-115">Örnek 1: tüm zamanlanmış runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="8ae61-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8ae61-116">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8ae61-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="8ae61-117">Örnek 2: runbook ile ilişkili tüm zamanlamaları alma</span><span class="sxs-lookup"><span data-stu-id="8ae61-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="8ae61-118">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki runbook Runbk01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8ae61-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="8ae61-119">Örnek 3: zamanlamayla ilişkili tüm runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="8ae61-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="8ae61-120">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki zamanlama Schedule01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8ae61-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8ae61-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ae61-121">PARAMETERS</span></span>

### <span data-ttu-id="8ae61-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ae61-122">-AutomationAccountName</span></span>
<span data-ttu-id="8ae61-123">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ae61-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8ae61-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae61-124">-DefaultProfile</span></span>
<span data-ttu-id="8ae61-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8ae61-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ae61-126">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="8ae61-126">-JobScheduleId</span></span>
<span data-ttu-id="8ae61-127">Bu cmdlet 'in aldığı zamanlanmış iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ae61-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8ae61-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae61-128">-ResourceGroupName</span></span>
<span data-ttu-id="8ae61-129">Bu cmdlet 'in aldığı zamanlanmış runbook 'lar için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ae61-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8ae61-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="8ae61-130">-RunbookName</span></span>
<span data-ttu-id="8ae61-131">Bu cmdlet 'in zamanlanmış runbook 'ları aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ae61-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="8ae61-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="8ae61-132">-ScheduleName</span></span>
<span data-ttu-id="8ae61-133">Bu cmdlet 'in zamanlanmış runbook 'ları aldığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ae61-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="8ae61-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae61-134">CommonParameters</span></span>
<span data-ttu-id="8ae61-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ae61-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae61-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ae61-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae61-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ae61-137">INPUTS</span></span>

### <span data-ttu-id="8ae61-138">System. Nullable ' 1 [[System. Guid, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="8ae61-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="8ae61-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8ae61-139">System.String</span></span>

## <span data-ttu-id="8ae61-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ae61-140">OUTPUTS</span></span>

### <span data-ttu-id="8ae61-141">Microsoft. Azure. Commands. Automation. model. Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="8ae61-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="8ae61-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ae61-142">NOTES</span></span>

## <span data-ttu-id="8ae61-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ae61-143">RELATED LINKS</span></span>

[<span data-ttu-id="8ae61-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8ae61-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="8ae61-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8ae61-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)

