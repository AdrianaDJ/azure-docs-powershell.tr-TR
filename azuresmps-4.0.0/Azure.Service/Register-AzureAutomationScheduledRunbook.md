---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105873"
---
# <span data-ttu-id="8fe39-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8fe39-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="8fe39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe39-102">SYNOPSIS</span></span>

<span data-ttu-id="8fe39-103">Runbook 'u bir zamanlamayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="8fe39-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="8fe39-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8fe39-104">SYNTAX</span></span>

### <span data-ttu-id="8fe39-105">ByRunbookName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8fe39-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fe39-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="8fe39-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8fe39-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8fe39-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="8fe39-108">**Register-AzureAutomationScheduledRunbook** cmdlet 'i bir runbook ile ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="8fe39-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="8fe39-109">Runbook, *ScheduleName* parametresini kullanarak belirttiğiniz zamanlamaya göre başlar.</span><span class="sxs-lookup"><span data-stu-id="8fe39-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="8fe39-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8fe39-110">EXAMPLES</span></span>

### <span data-ttu-id="8fe39-111">Örnek 1: bir runbook 'u zamanlamayla Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="8fe39-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="8fe39-112">Bu komut, Runbk01 adlı runbook 'u Contoso17 adlı Azure Otomasyon hesabındaki Sched01 adlı zamanlamayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="8fe39-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="8fe39-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8fe39-113">PARAMETERS</span></span>

### <span data-ttu-id="8fe39-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8fe39-114">-AutomationAccountName</span></span>
<span data-ttu-id="8fe39-115">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe39-115">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-116">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="8fe39-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="8fe39-117">-Profile</span></span>
<span data-ttu-id="8fe39-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe39-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8fe39-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="8fe39-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="8fe39-120">-RunbookName</span></span>
<span data-ttu-id="8fe39-121">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe39-121">Specifies the name of the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="8fe39-122">-ScheduleName</span></span>
<span data-ttu-id="8fe39-123">Zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8fe39-123">Specifies the name of the schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe39-124">CommonParameters</span></span>
<span data-ttu-id="8fe39-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8fe39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe39-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fe39-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe39-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8fe39-127">INPUTS</span></span>

## <span data-ttu-id="8fe39-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8fe39-128">OUTPUTS</span></span>

### <span data-ttu-id="8fe39-129">Microsoft. Azure. Commands. Automation. model. Jobzamanlama</span><span class="sxs-lookup"><span data-stu-id="8fe39-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="8fe39-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8fe39-130">NOTES</span></span>

## <span data-ttu-id="8fe39-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8fe39-131">RELATED LINKS</span></span>

[<span data-ttu-id="8fe39-132">Yeni-Azureautomationzamanlama</span><span class="sxs-lookup"><span data-stu-id="8fe39-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="8fe39-133">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="8fe39-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


