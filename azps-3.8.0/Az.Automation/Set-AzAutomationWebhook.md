---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 66019f050325ef3cdea73eedc9664d05afa2a2e3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938396"
---
# <span data-ttu-id="bcd3a-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="bcd3a-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="bcd3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd3a-103">Bir Otomasyonu runbook için Web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="bcd3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bcd3a-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcd3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bcd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd3a-106">**Set-Azautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook 'un web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="bcd3a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bcd3a-107">EXAMPLES</span></span>

### <span data-ttu-id="bcd3a-108">Örnek 1: Web kancasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="bcd3a-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="bcd3a-109">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook01 adındaki Web kancasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="bcd3a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bcd3a-110">PARAMETERS</span></span>

### <span data-ttu-id="bcd3a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bcd3a-111">-AutomationAccountName</span></span>
<span data-ttu-id="bcd3a-112">Bu cmdlet 'in Web kancası değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="bcd3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd3a-113">-DefaultProfile</span></span>
<span data-ttu-id="bcd3a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="bcd3a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcd3a-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="bcd3a-115">-IsEnabled</span></span>
<span data-ttu-id="bcd3a-116">Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="bcd3a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="bcd3a-117">-Name</span></span>
<span data-ttu-id="bcd3a-118">Bu cmdlet 'in değiştirdiği bir Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bcd3a-119">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="bcd3a-119">-Parameters</span></span>
<span data-ttu-id="bcd3a-120">Anahtar/değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="bcd3a-121">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="bcd3a-122">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="bcd3a-123">Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="bcd3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcd3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="bcd3a-125">Bu cmdlet 'in bir Web kancasını değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="bcd3a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd3a-126">CommonParameters</span></span>
<span data-ttu-id="bcd3a-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bcd3a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd3a-128">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd3a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd3a-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bcd3a-129">INPUTS</span></span>

### <span data-ttu-id="bcd3a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bcd3a-130">System.String</span></span>

### <span data-ttu-id="bcd3a-131">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="bcd3a-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bcd3a-132">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="bcd3a-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="bcd3a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bcd3a-133">OUTPUTS</span></span>

### <span data-ttu-id="bcd3a-134">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="bcd3a-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="bcd3a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bcd3a-135">NOTES</span></span>

## <span data-ttu-id="bcd3a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bcd3a-136">RELATED LINKS</span></span>

[<span data-ttu-id="bcd3a-137">Get-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="bcd3a-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="bcd3a-138">Yeni-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="bcd3a-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="bcd3a-139">Remove-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="bcd3a-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


