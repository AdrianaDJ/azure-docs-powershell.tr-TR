---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096053"
---
# <span data-ttu-id="b513b-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b513b-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="b513b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b513b-102">SYNOPSIS</span></span>
<span data-ttu-id="b513b-103">Bir Web kancasını Otomasyon Runbook 'tan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b513b-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="b513b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b513b-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b513b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b513b-105">DESCRIPTION</span></span>
<span data-ttu-id="b513b-106">**Remove-Azautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook 'tan bir Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b513b-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="b513b-107">Web kancası silindi.</span><span class="sxs-lookup"><span data-stu-id="b513b-107">The webhook is deleted.</span></span>

## <span data-ttu-id="b513b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b513b-108">EXAMPLES</span></span>

### <span data-ttu-id="b513b-109">Örnek 1: Web kancasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="b513b-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="b513b-110">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook11 adındaki Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b513b-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="b513b-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b513b-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="b513b-112">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="b513b-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="b513b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b513b-113">PARAMETERS</span></span>

### <span data-ttu-id="b513b-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b513b-114">-AutomationAccountName</span></span>
<span data-ttu-id="b513b-115">Bu cmdlet 'in Web kancası kaldırıldığı bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b513b-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="b513b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b513b-116">-DefaultProfile</span></span>
<span data-ttu-id="b513b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b513b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b513b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b513b-118">-Name</span></span>
<span data-ttu-id="b513b-119">Bu cmdlet 'in kaldırdığı Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b513b-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b513b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b513b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b513b-121">Bu cmdlet 'in Web kancasını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b513b-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="b513b-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="b513b-122">-Confirm</span></span>
<span data-ttu-id="b513b-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b513b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b513b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b513b-124">-WhatIf</span></span>
<span data-ttu-id="b513b-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b513b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b513b-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b513b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b513b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b513b-127">CommonParameters</span></span>
<span data-ttu-id="b513b-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b513b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b513b-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b513b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b513b-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b513b-130">INPUTS</span></span>

### <span data-ttu-id="b513b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b513b-131">System.String</span></span>

## <span data-ttu-id="b513b-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b513b-132">OUTPUTS</span></span>

### <span data-ttu-id="b513b-133">System. void</span><span class="sxs-lookup"><span data-stu-id="b513b-133">System.Void</span></span>

## <span data-ttu-id="b513b-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b513b-134">NOTES</span></span>

## <span data-ttu-id="b513b-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b513b-135">RELATED LINKS</span></span>

[<span data-ttu-id="b513b-136">Get-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="b513b-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="b513b-137">Yeni-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="b513b-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="b513b-138">Set-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="b513b-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)

