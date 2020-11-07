---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: fe8d7b4407aa5afc3454d80e4cf45c102d9006bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595037"
---
# <span data-ttu-id="8f78a-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8f78a-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="8f78a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f78a-102">SYNOPSIS</span></span>
<span data-ttu-id="8f78a-103">Otomasyon Runbook 'ları ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="8f78a-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f78a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f78a-104">SYNTAX</span></span>

### <span data-ttu-id="8f78a-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f78a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f78a-106">Byjobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="8f78a-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f78a-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="8f78a-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f78a-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="8f78a-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8f78a-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="8f78a-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f78a-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f78a-110">DESCRIPTION</span></span>
<span data-ttu-id="8f78a-111">**Get-AzureRmAutomationScheduledRunbook** cmdlet 'i, bir veya daha fazla Azure Otomasyonu runbook 'u ve ilişkili zamanlamaları alır.</span><span class="sxs-lookup"><span data-stu-id="8f78a-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="8f78a-112">Varsayılan olarak, bu cmdlet tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8f78a-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="8f78a-113">Belirli runbook zamanlamalarını görmek için bir runbook veya zamanlamanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="8f78a-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="8f78a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f78a-114">EXAMPLES</span></span>

### <span data-ttu-id="8f78a-115">Örnek 1: tüm zamanlanmış runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="8f78a-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8f78a-116">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8f78a-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="8f78a-117">Örnek 2: runbook ile ilişkili tüm zamanlamaları alma</span><span class="sxs-lookup"><span data-stu-id="8f78a-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="8f78a-118">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki runbook Runbk01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8f78a-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="8f78a-119">Örnek 3: zamanlamayla ilişkili tüm runbook 'ları alma</span><span class="sxs-lookup"><span data-stu-id="8f78a-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="8f78a-120">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki zamanlama Schedule01 için tüm zamanlanmış runbook 'ları alır.</span><span class="sxs-lookup"><span data-stu-id="8f78a-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8f78a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f78a-121">PARAMETERS</span></span>

### <span data-ttu-id="8f78a-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8f78a-122">-AutomationAccountName</span></span>
<span data-ttu-id="8f78a-123">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f78a-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8f78a-124">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="8f78a-124">-JobScheduleId</span></span>
<span data-ttu-id="8f78a-125">Bu cmdlet 'in aldığı zamanlanmış iş KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f78a-125">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8f78a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f78a-126">-ResourceGroupName</span></span>
<span data-ttu-id="8f78a-127">Bu cmdlet 'in aldığı zamanlanmış runbook 'lar için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f78a-127">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8f78a-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="8f78a-128">-RunbookName</span></span>
<span data-ttu-id="8f78a-129">Bu cmdlet 'in zamanlanmış runbook 'ları aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f78a-129">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="8f78a-130">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="8f78a-130">-ScheduleName</span></span>
<span data-ttu-id="8f78a-131">Bu cmdlet 'in zamanlanmış runbook 'ları aldığı zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8f78a-131">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="8f78a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f78a-132">-DefaultProfile</span></span>
<span data-ttu-id="8f78a-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f78a-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f78a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f78a-134">CommonParameters</span></span>
<span data-ttu-id="8f78a-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f78a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f78a-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f78a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f78a-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f78a-137">INPUTS</span></span>

## <span data-ttu-id="8f78a-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f78a-138">OUTPUTS</span></span>

### <span data-ttu-id="8f78a-139">Microsoft. Azure. Commands. Automation. model. Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="8f78a-139">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="8f78a-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f78a-140">NOTES</span></span>

## <span data-ttu-id="8f78a-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f78a-141">RELATED LINKS</span></span>

[<span data-ttu-id="8f78a-142">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8f78a-142">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="8f78a-143">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8f78a-143">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)

