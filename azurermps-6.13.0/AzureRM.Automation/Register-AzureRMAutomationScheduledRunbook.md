---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: deb6611fedbb1f88b9668b4750e096056ea8b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762807"
---
# <span data-ttu-id="65bf4-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="65bf4-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="65bf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="65bf4-103">Bir runbook 'u zamanlamaya ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65bf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65bf4-104">SYNTAX</span></span>

### <span data-ttu-id="65bf4-105">ByRunbookName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65bf4-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65bf4-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="65bf4-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65bf4-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="65bf4-107">DESCRIPTION</span></span>
<span data-ttu-id="65bf4-108">**Register-AzureRmAutomationScheduledRunbook** cmdlet 'ı bir Azure Otomasyonu runbook 'unu bir zamanlamayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="65bf4-109">Runbook, *ScheduleName* parametresini kullanarak belirttiğiniz zamanlamaya göre başlar.</span><span class="sxs-lookup"><span data-stu-id="65bf4-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="65bf4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65bf4-110">EXAMPLES</span></span>

### <span data-ttu-id="65bf4-111">Örnek 1: bir runbook 'u zamanlamayla Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="65bf4-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="65bf4-112">Bu komut, Runbk01 adlı runbook 'u Contoso17 adlı Azure Otomasyon hesabındaki Sched01 adlı zamanlamayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="65bf4-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65bf4-113">PARAMETERS</span></span>

### <span data-ttu-id="65bf4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65bf4-114">-AutomationAccountName</span></span>
<span data-ttu-id="65bf4-115">Bu cmdlet 'in üzerinde yaptığı runbook için bir Otomasyon hesabı belirtir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="65bf4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65bf4-116">-DefaultProfile</span></span>
<span data-ttu-id="65bf4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="65bf4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65bf4-118">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="65bf4-118">-Parameters</span></span>
<span data-ttu-id="65bf4-119">Anahtar/değer çiftleri karma tablosunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="65bf4-120">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="65bf4-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="65bf4-121">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="65bf4-122">Runbook ilişkili zamanlama tamamlandığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="65bf4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65bf4-123">-ResourceGroupName</span></span>
<span data-ttu-id="65bf4-124">Zamanlanmış runbook için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="65bf4-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="65bf4-125">-RunbookName</span></span>
<span data-ttu-id="65bf4-126">Bu cmdlet 'in zamanlamada ilişki kurduğu runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="65bf4-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="65bf4-127">-RunOn</span></span>
<span data-ttu-id="65bf4-128">Karma Runbook Worker grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="65bf4-128">The name of the hybrid runbook worker group.</span></span>

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

### <span data-ttu-id="65bf4-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="65bf4-129">-ScheduleName</span></span>
<span data-ttu-id="65bf4-130">Bu cmdlet 'in runbook 'u ilişkilendiren zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65bf4-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="65bf4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bf4-131">CommonParameters</span></span>
<span data-ttu-id="65bf4-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65bf4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bf4-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65bf4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bf4-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65bf4-134">INPUTS</span></span>

### <span data-ttu-id="65bf4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="65bf4-135">System.String</span></span>

## <span data-ttu-id="65bf4-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65bf4-136">OUTPUTS</span></span>

### <span data-ttu-id="65bf4-137">Microsoft. Azure. Commands. Automation. model. Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="65bf4-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="65bf4-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65bf4-138">NOTES</span></span>

## <span data-ttu-id="65bf4-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65bf4-139">RELATED LINKS</span></span>

[<span data-ttu-id="65bf4-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="65bf4-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="65bf4-141">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="65bf4-141">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


