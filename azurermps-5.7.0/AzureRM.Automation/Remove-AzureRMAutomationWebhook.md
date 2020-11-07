---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 465e3ecd3f80b03eecb58309b18c91cd69c0d5a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765112"
---
# <span data-ttu-id="0e9e3-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0e9e3-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="0e9e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e9e3-102">SYNOPSIS</span></span>
<span data-ttu-id="0e9e3-103">Bir Web kancasını Otomasyon Runbook 'tan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e9e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e9e3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e9e3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e9e3-105">DESCRIPTION</span></span>
<span data-ttu-id="0e9e3-106">**Remove-Azurermautomationkancası** cmdlet 'i, bir Azure Otomasyonu runbook 'tan bir Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="0e9e3-107">Web kancası silindi.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-107">The webhook is deleted.</span></span>

## <span data-ttu-id="0e9e3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e9e3-108">EXAMPLES</span></span>

### <span data-ttu-id="0e9e3-109">Örnek 1: Web kancasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0e9e3-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="0e9e3-110">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook11 adındaki Web kancasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="0e9e3-111">Komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0e9e3-112">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0e9e3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e9e3-113">PARAMETERS</span></span>

### <span data-ttu-id="0e9e3-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e9e3-114">-AutomationAccountName</span></span>
<span data-ttu-id="0e9e3-115">Bu cmdlet 'in Web kancası kaldırıldığı bir Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e9e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e9e3-116">-DefaultProfile</span></span>
<span data-ttu-id="0e9e3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0e9e3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e9e3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0e9e3-118">-Name</span></span>
<span data-ttu-id="0e9e3-119">Bu cmdlet 'in kaldırdığı Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e9e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e9e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="0e9e3-121">Bu cmdlet 'in Web kancasını kaldırdığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e9e3-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="0e9e3-122">-Confirm</span></span>
<span data-ttu-id="0e9e3-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e9e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e9e3-124">-WhatIf</span></span>
<span data-ttu-id="0e9e3-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e9e3-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e9e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e9e3-127">CommonParameters</span></span>
<span data-ttu-id="0e9e3-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e9e3-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e9e3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e9e3-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e9e3-130">INPUTS</span></span>

### <span data-ttu-id="0e9e3-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0e9e3-131">None</span></span>
<span data-ttu-id="0e9e3-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0e9e3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e9e3-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e9e3-133">OUTPUTS</span></span>

## <span data-ttu-id="0e9e3-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e9e3-134">NOTES</span></span>

## <span data-ttu-id="0e9e3-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e9e3-135">RELATED LINKS</span></span>

[<span data-ttu-id="0e9e3-136">Get-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="0e9e3-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="0e9e3-137">Yeni-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="0e9e3-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="0e9e3-138">Set-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="0e9e3-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


