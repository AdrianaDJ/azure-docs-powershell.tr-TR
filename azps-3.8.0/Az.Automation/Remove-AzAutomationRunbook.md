---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104925"
---
# <span data-ttu-id="72ca2-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="72ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="72ca2-103">Runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72ca2-103">Removes a runbook.</span></span>

## <span data-ttu-id="72ca2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72ca2-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72ca2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72ca2-105">DESCRIPTION</span></span>
<span data-ttu-id="72ca2-106">**Remove-AzAutomationRunbook** cmdlet 'ı, Azure Otomasyonu 'ndan runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72ca2-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="72ca2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72ca2-107">EXAMPLES</span></span>

### <span data-ttu-id="72ca2-108">Örnek 1: runbook 'u kaldırma</span><span class="sxs-lookup"><span data-stu-id="72ca2-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="72ca2-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki Runbook03 adındaki runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72ca2-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="72ca2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72ca2-110">PARAMETERS</span></span>

### <span data-ttu-id="72ca2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="72ca2-111">-AutomationAccountName</span></span>
<span data-ttu-id="72ca2-112">Bu cmdlet 'in runbook 'u kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72ca2-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="72ca2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ca2-113">-DefaultProfile</span></span>
<span data-ttu-id="72ca2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="72ca2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72ca2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="72ca2-115">-Force</span></span>
<span data-ttu-id="72ca2-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="72ca2-116">ps_force</span></span>

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

### <span data-ttu-id="72ca2-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="72ca2-117">-Name</span></span>
<span data-ttu-id="72ca2-118">Bu cmdlet 'in kaldırdığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72ca2-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ca2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72ca2-119">-ResourceGroupName</span></span>
<span data-ttu-id="72ca2-120">Bu cmdlet 'in runbook yayımladığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="72ca2-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="72ca2-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="72ca2-121">-Confirm</span></span>
<span data-ttu-id="72ca2-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="72ca2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72ca2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ca2-123">-WhatIf</span></span>
<span data-ttu-id="72ca2-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="72ca2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ca2-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="72ca2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72ca2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ca2-126">CommonParameters</span></span>
<span data-ttu-id="72ca2-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72ca2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ca2-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72ca2-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ca2-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72ca2-129">INPUTS</span></span>

### <span data-ttu-id="72ca2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="72ca2-130">System.String</span></span>

## <span data-ttu-id="72ca2-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72ca2-131">OUTPUTS</span></span>

### <span data-ttu-id="72ca2-132">System. void</span><span class="sxs-lookup"><span data-stu-id="72ca2-132">System.Void</span></span>

## <span data-ttu-id="72ca2-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72ca2-133">NOTES</span></span>

## <span data-ttu-id="72ca2-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72ca2-134">RELATED LINKS</span></span>

[<span data-ttu-id="72ca2-135">Dışarı aktarma-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="72ca2-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="72ca2-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="72ca2-138">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="72ca2-139">Yeni-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="72ca2-140">Yayımlama-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="72ca2-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="72ca2-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="72ca2-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


