---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0C156A1C-72DC-4B3C-9033-1B985139A732
online version: ''
schema: 2.0.0
ms.openlocfilehash: 43f371e44876c8927edc4f30fcfe0095a28cb27b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106171"
---
# <span data-ttu-id="0f28c-101">Remove-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f28c-101">Remove-AzureAutomationRunbook</span></span>

## <span data-ttu-id="0f28c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f28c-102">SYNOPSIS</span></span>

<span data-ttu-id="0f28c-103">Runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f28c-103">Removes a runbook.</span></span>

## <span data-ttu-id="0f28c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f28c-104">SYNTAX</span></span>

```
Remove-AzureAutomationRunbook -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f28c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f28c-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0f28c-106">**Remove-AzureAutomationRunbook** cmdlet 'ı, Microsoft Azure Otomasyonu 'ndan runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f28c-106">The **Remove-AzureAutomationRunbook** cmdlet removes a runbook from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="0f28c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f28c-107">EXAMPLES</span></span>

### <span data-ttu-id="0f28c-108">Örnek 1: runbook 'u kaldırma</span><span class="sxs-lookup"><span data-stu-id="0f28c-108">Example 1: Remove a runbook</span></span>
```
PS C:\> Remove-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook"
```

<span data-ttu-id="0f28c-109">Bu komut, Contoso17 adlı Otomasyon hesabındaki MyRunbook adındaki runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0f28c-109">This command removes the runbook named MyRunbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0f28c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f28c-110">PARAMETERS</span></span>

### <span data-ttu-id="0f28c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0f28c-111">-AutomationAccountName</span></span>
<span data-ttu-id="0f28c-112">Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f28c-112">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="0f28c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0f28c-113">-Force</span></span>
<span data-ttu-id="0f28c-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="0f28c-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f28c-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="0f28c-115">-Name</span></span>
<span data-ttu-id="0f28c-116">Kaldırılacak runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f28c-116">Specifies the name of the runbook to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f28c-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="0f28c-117">-Profile</span></span>
<span data-ttu-id="0f28c-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0f28c-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f28c-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0f28c-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f28c-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f28c-120">-Confirm</span></span>
<span data-ttu-id="0f28c-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f28c-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f28c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f28c-122">-WhatIf</span></span>
<span data-ttu-id="0f28c-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f28c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f28c-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f28c-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f28c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f28c-125">CommonParameters</span></span>
<span data-ttu-id="0f28c-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f28c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f28c-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f28c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f28c-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f28c-128">INPUTS</span></span>

## <span data-ttu-id="0f28c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f28c-129">OUTPUTS</span></span>

## <span data-ttu-id="0f28c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f28c-130">NOTES</span></span>

## <span data-ttu-id="0f28c-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f28c-131">RELATED LINKS</span></span>

[<span data-ttu-id="0f28c-132">Get-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f28c-132">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="0f28c-133">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f28c-133">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="0f28c-134">Publish-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f28c-134">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="0f28c-135">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f28c-135">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="0f28c-136">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0f28c-136">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


