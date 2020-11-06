---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: f191176433a5ac12507d2b29a6d52c73a1d61e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591813"
---
# <span data-ttu-id="a1478-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a1478-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="a1478-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1478-102">SYNOPSIS</span></span>
<span data-ttu-id="a1478-103">Bir Web kancasını Otomasyon Runbook 'tan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a1478-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1478-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1478-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1478-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1478-105">DESCRIPTION</span></span>
<span data-ttu-id="a1478-106">**Remove-Azurermautomationkancası** cmdlet 'i, bir Azure Otomasyonu runbook 'tan bir Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a1478-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="a1478-107">Web kancası silindi.</span><span class="sxs-lookup"><span data-stu-id="a1478-107">The webhook is deleted.</span></span>

## <span data-ttu-id="a1478-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1478-108">EXAMPLES</span></span>

### <span data-ttu-id="a1478-109">Örnek 1: Web kancasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="a1478-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a1478-110">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook11 adındaki Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a1478-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a1478-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1478-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a1478-112">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="a1478-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a1478-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1478-113">PARAMETERS</span></span>

### <span data-ttu-id="a1478-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1478-114">-AutomationAccountName</span></span>
<span data-ttu-id="a1478-115">Bu cmdlet 'in Web kancası kaldırıldığı bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1478-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="a1478-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1478-116">-Name</span></span>
<span data-ttu-id="a1478-117">Bu cmdlet 'in kaldırdığı Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1478-117">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a1478-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1478-118">-ResourceGroupName</span></span>
<span data-ttu-id="a1478-119">Bu cmdlet 'in Web kancasını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1478-119">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="a1478-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1478-120">-Confirm</span></span>
<span data-ttu-id="a1478-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1478-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1478-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1478-122">-WhatIf</span></span>
<span data-ttu-id="a1478-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1478-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1478-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1478-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1478-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1478-125">-DefaultProfile</span></span>
<span data-ttu-id="a1478-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1478-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1478-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1478-127">CommonParameters</span></span>
<span data-ttu-id="a1478-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1478-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1478-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1478-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1478-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1478-130">INPUTS</span></span>

## <span data-ttu-id="a1478-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1478-131">OUTPUTS</span></span>

## <span data-ttu-id="a1478-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1478-132">NOTES</span></span>

## <span data-ttu-id="a1478-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1478-133">RELATED LINKS</span></span>

[<span data-ttu-id="a1478-134">Get-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a1478-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="a1478-135">Yeni-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a1478-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="a1478-136">Set-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a1478-136">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


