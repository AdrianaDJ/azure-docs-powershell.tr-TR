---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106587"
---
# <span data-ttu-id="3b7de-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3b7de-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="3b7de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b7de-102">SYNOPSIS</span></span>

<span data-ttu-id="3b7de-103">Runbook ile zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b7de-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="3b7de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b7de-104">SYNTAX</span></span>

### <span data-ttu-id="3b7de-105">Byjobscheduleıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b7de-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3b7de-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="3b7de-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3b7de-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b7de-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3b7de-108">**Unregister-AzureAutomationScheduledRunbook** cmdlet 'ı, Microsoft Azure Otomasyonu runbook 'u ve zamanlama tetiklendiğinde runbook 'un başlamasını durduran bir zamanlama arasındaki ilişkilendirmeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b7de-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="3b7de-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b7de-109">EXAMPLES</span></span>

### <span data-ttu-id="3b7de-110">Örnek 1: runbook ile zamanlama arasındaki ilişkiyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="3b7de-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="3b7de-111">Bu komut, Runbk01 adındaki runbook ile Runbk01Sched adlı zamanlama arasındaki ilişkiyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3b7de-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="3b7de-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b7de-112">PARAMETERS</span></span>

### <span data-ttu-id="3b7de-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3b7de-113">-AutomationAccountName</span></span>
<span data-ttu-id="3b7de-114">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b7de-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3b7de-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3b7de-115">-Force</span></span>
<span data-ttu-id="3b7de-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3b7de-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b7de-117">-Jobscheduleıd</span><span class="sxs-lookup"><span data-stu-id="3b7de-117">-JobScheduleId</span></span>
<span data-ttu-id="3b7de-118">Zamanlanmış bir runbook 'un KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b7de-118">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b7de-119">-Profil</span><span class="sxs-lookup"><span data-stu-id="3b7de-119">-Profile</span></span>
<span data-ttu-id="3b7de-120">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b7de-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b7de-121">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="3b7de-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b7de-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="3b7de-122">-RunbookName</span></span>
<span data-ttu-id="3b7de-123">Runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b7de-123">Specifies the name of a runbook.</span></span>

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

### <span data-ttu-id="3b7de-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="3b7de-124">-ScheduleName</span></span>
<span data-ttu-id="3b7de-125">Bir zamanlamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b7de-125">Specifies the name of a schedule.</span></span>

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

### <span data-ttu-id="3b7de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7de-126">CommonParameters</span></span>
<span data-ttu-id="3b7de-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b7de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b7de-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b7de-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7de-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b7de-129">INPUTS</span></span>

## <span data-ttu-id="3b7de-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b7de-130">OUTPUTS</span></span>

## <span data-ttu-id="3b7de-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b7de-131">NOTES</span></span>

## <span data-ttu-id="3b7de-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b7de-132">RELATED LINKS</span></span>

[<span data-ttu-id="3b7de-133">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3b7de-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


