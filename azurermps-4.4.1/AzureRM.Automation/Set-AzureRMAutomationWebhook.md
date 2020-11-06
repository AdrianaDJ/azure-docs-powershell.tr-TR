---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588302"
---
# <span data-ttu-id="236e1-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="236e1-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="236e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="236e1-102">SYNOPSIS</span></span>
<span data-ttu-id="236e1-103">Bir Otomasyonu runbook için Web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="236e1-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="236e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="236e1-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="236e1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="236e1-105">DESCRIPTION</span></span>
<span data-ttu-id="236e1-106">**Set-Azurermautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook 'un web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="236e1-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="236e1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="236e1-107">EXAMPLES</span></span>

### <span data-ttu-id="236e1-108">Örnek 1: Web kancasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="236e1-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="236e1-109">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook01 adındaki Web kancasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="236e1-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="236e1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="236e1-110">PARAMETERS</span></span>

### <span data-ttu-id="236e1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="236e1-111">-AutomationAccountName</span></span>
<span data-ttu-id="236e1-112">Bu cmdlet 'in Web kancası değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="236e1-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="236e1-113">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="236e1-113">-IsEnabled</span></span>
<span data-ttu-id="236e1-114">Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="236e1-114">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="236e1-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="236e1-115">-Name</span></span>
<span data-ttu-id="236e1-116">Bu cmdlet 'in değiştirdiği bir Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="236e1-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="236e1-117">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="236e1-117">-Parameters</span></span>
<span data-ttu-id="236e1-118">Anahtar/değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="236e1-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="236e1-119">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="236e1-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="236e1-120">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="236e1-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="236e1-121">Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="236e1-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="236e1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236e1-122">-ResourceGroupName</span></span>
<span data-ttu-id="236e1-123">Bu cmdlet 'in bir Web kancasını değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="236e1-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="236e1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236e1-124">-DefaultProfile</span></span>
<span data-ttu-id="236e1-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="236e1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="236e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236e1-126">CommonParameters</span></span>
<span data-ttu-id="236e1-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="236e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236e1-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="236e1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236e1-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="236e1-129">INPUTS</span></span>

## <span data-ttu-id="236e1-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="236e1-130">OUTPUTS</span></span>

### <span data-ttu-id="236e1-131">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="236e1-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="236e1-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="236e1-132">NOTES</span></span>

## <span data-ttu-id="236e1-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="236e1-133">RELATED LINKS</span></span>

[<span data-ttu-id="236e1-134">Get-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="236e1-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="236e1-135">Yeni-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="236e1-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="236e1-136">Remove-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="236e1-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


