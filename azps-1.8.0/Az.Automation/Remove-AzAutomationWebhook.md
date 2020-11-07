---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 5f3ba7d2bdc573e7a08976e575e86dcf05ae3400
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761516"
---
# <span data-ttu-id="a179f-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a179f-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="a179f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a179f-102">SYNOPSIS</span></span>
<span data-ttu-id="a179f-103">Bir Web kancasını Otomasyon Runbook 'tan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a179f-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="a179f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a179f-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a179f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a179f-105">DESCRIPTION</span></span>
<span data-ttu-id="a179f-106">**Remove-Azautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook 'tan bir Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a179f-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="a179f-107">Web kancası silindi.</span><span class="sxs-lookup"><span data-stu-id="a179f-107">The webhook is deleted.</span></span>

## <span data-ttu-id="a179f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a179f-108">EXAMPLES</span></span>

### <span data-ttu-id="a179f-109">Örnek 1: Web kancasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a179f-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a179f-110">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook11 adındaki Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a179f-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a179f-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a179f-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a179f-112">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="a179f-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a179f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a179f-113">PARAMETERS</span></span>

### <span data-ttu-id="a179f-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a179f-114">-AutomationAccountName</span></span>
<span data-ttu-id="a179f-115">Bu cmdlet 'in Web kancası kaldırıldığı bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a179f-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="a179f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a179f-116">-DefaultProfile</span></span>
<span data-ttu-id="a179f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a179f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a179f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a179f-118">-Name</span></span>
<span data-ttu-id="a179f-119">Bu cmdlet 'in kaldırdığı Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a179f-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a179f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a179f-120">-ResourceGroupName</span></span>
<span data-ttu-id="a179f-121">Bu cmdlet 'in Web kancasını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a179f-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="a179f-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="a179f-122">-Confirm</span></span>
<span data-ttu-id="a179f-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a179f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a179f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a179f-124">-WhatIf</span></span>
<span data-ttu-id="a179f-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a179f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a179f-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a179f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a179f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a179f-127">CommonParameters</span></span>
<span data-ttu-id="a179f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a179f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a179f-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a179f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a179f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a179f-130">INPUTS</span></span>

### <span data-ttu-id="a179f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a179f-131">System.String</span></span>

## <span data-ttu-id="a179f-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a179f-132">OUTPUTS</span></span>

### <span data-ttu-id="a179f-133">System. void</span><span class="sxs-lookup"><span data-stu-id="a179f-133">System.Void</span></span>

## <span data-ttu-id="a179f-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a179f-134">NOTES</span></span>

## <span data-ttu-id="a179f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a179f-135">RELATED LINKS</span></span>

[<span data-ttu-id="a179f-136">Get-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a179f-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="a179f-137">Yeni-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a179f-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="a179f-138">Set-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a179f-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)

