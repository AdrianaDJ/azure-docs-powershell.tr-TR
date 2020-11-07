---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: df6fc949fe1aa105a84ede2329c71feb4b27a449
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753257"
---
# <span data-ttu-id="821cf-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="821cf-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="821cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="821cf-102">SYNOPSIS</span></span>
<span data-ttu-id="821cf-103">Bir runbook 'u zamanlamaya ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="821cf-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="821cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="821cf-104">SYNTAX</span></span>

### <span data-ttu-id="821cf-105">ByRunbookName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="821cf-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="821cf-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="821cf-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="821cf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="821cf-107">DESCRIPTION</span></span>
<span data-ttu-id="821cf-108">**Register-AzAutomationScheduledRunbook** cmdlet 'ı bir Azure Otomasyonu runbook 'unu bir zamanlamayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="821cf-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="821cf-109">Runbook, *ScheduleName* parametresini kullanarak belirttiğiniz zamanlamaya göre başlar.</span><span class="sxs-lookup"><span data-stu-id="821cf-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="821cf-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="821cf-110">EXAMPLES</span></span>

### <span data-ttu-id="821cf-111">Örnek 1: bir runbook 'u zamanlamayla Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="821cf-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="821cf-112">Bu komut, Runbk01 adlı runbook 'u Contoso17 adlı Azure Otomasyon hesabındaki Sched01 adlı zamanlamayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="821cf-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="821cf-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="821cf-113">PARAMETERS</span></span>

### <span data-ttu-id="821cf-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="821cf-114">-AutomationAccountName</span></span>
<span data-ttu-id="821cf-115">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="821cf-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="821cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="821cf-116">-DefaultProfile</span></span>
<span data-ttu-id="821cf-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="821cf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="821cf-118">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="821cf-118">-Parameters</span></span>
<span data-ttu-id="821cf-119">Anahtar/değer çiftleri karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="821cf-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="821cf-120">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="821cf-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="821cf-121">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="821cf-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="821cf-122">Runbook ilişkili zamanlama tamamlandığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="821cf-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="821cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="821cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="821cf-124">Zamanlanmış runbook için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="821cf-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="821cf-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="821cf-125">-RunbookName</span></span>
<span data-ttu-id="821cf-126">Bu cmdlet 'in zamanlamada ilişki kurduğu runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="821cf-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="821cf-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="821cf-127">-RunOn</span></span>
<span data-ttu-id="821cf-128">Karma Runbook Worker grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="821cf-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="821cf-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="821cf-129">-ScheduleName</span></span>
<span data-ttu-id="821cf-130">Bu cmdlet 'in runbook 'u ilişkilendiren zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="821cf-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="821cf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="821cf-131">CommonParameters</span></span>
<span data-ttu-id="821cf-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="821cf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="821cf-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="821cf-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="821cf-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="821cf-134">INPUTS</span></span>

### <span data-ttu-id="821cf-135">System. String</span><span class="sxs-lookup"><span data-stu-id="821cf-135">System.String</span></span>

## <span data-ttu-id="821cf-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="821cf-136">OUTPUTS</span></span>

### <span data-ttu-id="821cf-137">Microsoft. Azure. Commands. Automation. model. Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="821cf-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="821cf-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="821cf-138">NOTES</span></span>

## <span data-ttu-id="821cf-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="821cf-139">RELATED LINKS</span></span>

[<span data-ttu-id="821cf-140">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="821cf-140">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="821cf-141">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="821cf-141">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


