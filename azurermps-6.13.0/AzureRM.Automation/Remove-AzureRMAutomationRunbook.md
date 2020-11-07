---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: b84daa4041b8e27351d3b3b63eae4c7599881eae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763184"
---
# <span data-ttu-id="a915c-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="a915c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a915c-102">SYNOPSIS</span></span>
<span data-ttu-id="a915c-103">Runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a915c-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a915c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a915c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a915c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a915c-105">DESCRIPTION</span></span>
<span data-ttu-id="a915c-106">**Remove-AzureRmAutomationRunbook** cmdlet 'i, bir runbook 'U Azure Otomasyonu 'ndan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a915c-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="a915c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a915c-107">EXAMPLES</span></span>

### <span data-ttu-id="a915c-108">Örnek 1: runbook 'u kaldırma</span><span class="sxs-lookup"><span data-stu-id="a915c-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a915c-109">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki Runbook03 adındaki runbook 'u kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a915c-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a915c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a915c-110">PARAMETERS</span></span>

### <span data-ttu-id="a915c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a915c-111">-AutomationAccountName</span></span>
<span data-ttu-id="a915c-112">Bu cmdlet 'in runbook 'u kaldırdığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a915c-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="a915c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a915c-113">-DefaultProfile</span></span>
<span data-ttu-id="a915c-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a915c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a915c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a915c-115">-Force</span></span>
<span data-ttu-id="a915c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a915c-116">ps_force</span></span>

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

### <span data-ttu-id="a915c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a915c-117">-Name</span></span>
<span data-ttu-id="a915c-118">Bu cmdlet 'in kaldırdığı runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a915c-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a915c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a915c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a915c-120">Bu cmdlet 'in runbook yayımladığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a915c-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a915c-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="a915c-121">-Confirm</span></span>
<span data-ttu-id="a915c-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a915c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a915c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a915c-123">-WhatIf</span></span>
<span data-ttu-id="a915c-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a915c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a915c-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a915c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a915c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a915c-126">CommonParameters</span></span>
<span data-ttu-id="a915c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a915c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a915c-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a915c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a915c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a915c-129">INPUTS</span></span>

### <span data-ttu-id="a915c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a915c-130">System.String</span></span>

## <span data-ttu-id="a915c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a915c-131">OUTPUTS</span></span>

### <span data-ttu-id="a915c-132">System. void</span><span class="sxs-lookup"><span data-stu-id="a915c-132">System.Void</span></span>

## <span data-ttu-id="a915c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a915c-133">NOTES</span></span>

## <span data-ttu-id="a915c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a915c-134">RELATED LINKS</span></span>

[<span data-ttu-id="a915c-135">Dışarı aktarma-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a915c-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a915c-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a915c-138">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a915c-139">Yeni-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a915c-140">Yayımlama-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a915c-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="a915c-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a915c-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


