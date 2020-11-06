---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: d0443d5c15dec1324a5fe306ddec7303426449b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591740"
---
# <span data-ttu-id="0b885-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="0b885-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="0b885-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b885-102">SYNOPSIS</span></span>
<span data-ttu-id="0b885-103">Bir Otomasyonu runbook için Web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b885-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b885-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b885-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b885-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b885-105">DESCRIPTION</span></span>
<span data-ttu-id="0b885-106">**Set-Azurermautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook 'un web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="0b885-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="0b885-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b885-107">EXAMPLES</span></span>

### <span data-ttu-id="0b885-108">Örnek 1: Web kancasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="0b885-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="0b885-109">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook01 adındaki Web kancasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="0b885-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="0b885-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b885-110">PARAMETERS</span></span>

### <span data-ttu-id="0b885-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0b885-111">-AutomationAccountName</span></span>
<span data-ttu-id="0b885-112">Bu cmdlet 'in Web kancası değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b885-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="0b885-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b885-113">-DefaultProfile</span></span>
<span data-ttu-id="0b885-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0b885-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b885-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="0b885-115">-IsEnabled</span></span>
<span data-ttu-id="0b885-116">Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b885-116">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b885-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0b885-117">-Name</span></span>
<span data-ttu-id="0b885-118">Bu cmdlet 'in değiştirdiği bir Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b885-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0b885-119">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="0b885-119">-Parameters</span></span>
<span data-ttu-id="0b885-120">Anahtar/değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b885-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="0b885-121">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="0b885-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="0b885-122">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="0b885-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="0b885-123">Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="0b885-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b885-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b885-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b885-125">Bu cmdlet 'in bir Web kancasını değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b885-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="0b885-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b885-126">CommonParameters</span></span>
<span data-ttu-id="0b885-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b885-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b885-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b885-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b885-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b885-129">INPUTS</span></span>

### <span data-ttu-id="0b885-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0b885-130">None</span></span>
<span data-ttu-id="0b885-131">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="0b885-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0b885-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b885-132">OUTPUTS</span></span>

### <span data-ttu-id="0b885-133">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="0b885-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="0b885-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b885-134">NOTES</span></span>

## <span data-ttu-id="0b885-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b885-135">RELATED LINKS</span></span>

[<span data-ttu-id="0b885-136">Get-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="0b885-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="0b885-137">Yeni-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="0b885-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="0b885-138">Remove-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="0b885-138">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


