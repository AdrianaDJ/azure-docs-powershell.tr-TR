---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273720"
---
# <span data-ttu-id="e9aac-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="e9aac-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="e9aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9aac-102">SYNOPSIS</span></span>
<span data-ttu-id="e9aac-103">Bir Otomasyonu runbook için Web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="e9aac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9aac-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9aac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9aac-105">DESCRIPTION</span></span>
<span data-ttu-id="e9aac-106">**Set-Azautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook 'un web kancasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="e9aac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9aac-107">EXAMPLES</span></span>

### <span data-ttu-id="e9aac-108">Örnek 1: Web kancasını devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e9aac-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="e9aac-109">Bu komut, AutomationAccount01 adındaki Otomasyon hesabında Webhook01 adındaki Web kancasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e9aac-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="e9aac-110">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e9aac-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="e9aac-111">Bu komut, Web kancası için Run değerini ayarlar ve Runbook 'un Windows adlı karma çalışan grubunda çalıştırılmasını zorlar.</span><span class="sxs-lookup"><span data-stu-id="e9aac-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="e9aac-112">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="e9aac-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="e9aac-113">Bu komut, Web kancası için Run değerini güncelleştirir ve Runbook 'u bir Azure runbook çalışanından çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e9aac-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="e9aac-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9aac-114">PARAMETERS</span></span>

### <span data-ttu-id="e9aac-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9aac-115">-AutomationAccountName</span></span>
<span data-ttu-id="e9aac-116">Bu cmdlet 'in Web kancası değiştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e9aac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9aac-117">-DefaultProfile</span></span>
<span data-ttu-id="e9aac-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9aac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9aac-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="e9aac-119">-IsEnabled</span></span>
<span data-ttu-id="e9aac-120">Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="e9aac-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9aac-121">-Name</span></span>
<span data-ttu-id="e9aac-122">Bu cmdlet 'in değiştirdiği bir Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e9aac-123">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="e9aac-123">-Parameters</span></span>
<span data-ttu-id="e9aac-124">Anahtar/değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="e9aac-125">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="e9aac-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="e9aac-126">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="e9aac-127">Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="e9aac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9aac-128">-ResourceGroupName</span></span>
<span data-ttu-id="e9aac-129">Bu cmdlet 'in bir Web kancasını değiştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9aac-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="e9aac-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="e9aac-130">-RunOn</span></span>
<span data-ttu-id="e9aac-131">Runbook 'u yürütecek karma aracının isteğe bağlı adı</span><span class="sxs-lookup"><span data-stu-id="e9aac-131">Optional name of the hybrid agent which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9aac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9aac-132">CommonParameters</span></span>
<span data-ttu-id="e9aac-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9aac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9aac-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e9aac-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9aac-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9aac-135">INPUTS</span></span>

### <span data-ttu-id="e9aac-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e9aac-136">System.String</span></span>

### <span data-ttu-id="e9aac-137">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="e9aac-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e9aac-138">System. topluluklar. IDictionary</span><span class="sxs-lookup"><span data-stu-id="e9aac-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="e9aac-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9aac-139">OUTPUTS</span></span>

### <span data-ttu-id="e9aac-140">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="e9aac-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="e9aac-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9aac-141">NOTES</span></span>

## <span data-ttu-id="e9aac-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9aac-142">RELATED LINKS</span></span>

[<span data-ttu-id="e9aac-143">Get-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="e9aac-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="e9aac-144">Yeni-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="e9aac-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="e9aac-145">Remove-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="e9aac-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


