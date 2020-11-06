---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: f1062f1e827e27ff891f5b2797fcda95e60f3427
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591827"
---
# <span data-ttu-id="5138a-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="5138a-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="5138a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5138a-102">SYNOPSIS</span></span>
<span data-ttu-id="5138a-103">Otomasyon Runbook için Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5138a-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5138a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5138a-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5138a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5138a-105">DESCRIPTION</span></span>
<span data-ttu-id="5138a-106">**Yeni-Azurermautomationkancai** cmdlet 'i, bir Azure Otomasyonu runbook için Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5138a-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="5138a-107">Bu cmdlet 'in döndürdüğü Web kancası URL 'sini kaydettiğinizden emin olun, çünkü yeniden alamazsınız.</span><span class="sxs-lookup"><span data-stu-id="5138a-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="5138a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5138a-108">EXAMPLES</span></span>

### <span data-ttu-id="5138a-109">Örnek 1: Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="5138a-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="5138a-110">Bu komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook06 adında bir Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5138a-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="5138a-111">Komut, $Webhook değişkeninde Web kancasını depolar.</span><span class="sxs-lookup"><span data-stu-id="5138a-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="5138a-112">Web kancası etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="5138a-112">The webhook is enabled.</span></span>
<span data-ttu-id="5138a-113">Web kancası belirtilen zamanda sona erecek.</span><span class="sxs-lookup"><span data-stu-id="5138a-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="5138a-114">Bu komut Web kancası parametreleri için hiçbir değer sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="5138a-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="5138a-115">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="5138a-116">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="5138a-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="5138a-117">Örnek 2: parametrelerle bir Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="5138a-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="5138a-118">İlk komut, bir parametre sözlüğü oluşturur ve bunları $Params değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5138a-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="5138a-119">İkinci komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook11 adında bir Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5138a-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="5138a-120">Komut, $Params parametreleri Web kancası 'na atar.</span><span class="sxs-lookup"><span data-stu-id="5138a-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="5138a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5138a-121">PARAMETERS</span></span>

### <span data-ttu-id="5138a-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5138a-122">-AutomationAccountName</span></span>
<span data-ttu-id="5138a-123">Bu cmdlet 'in Web kancası oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="5138a-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="5138a-124">-ExpiryTime</span></span>
<span data-ttu-id="5138a-125">Web kancası için son kullanma süresini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-125">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="5138a-126">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize veya **TarihSaat** belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5138a-126">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5138a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="5138a-127">-Force</span></span>
<span data-ttu-id="5138a-128">ps_force</span><span class="sxs-lookup"><span data-stu-id="5138a-128">ps_force</span></span>

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

### <span data-ttu-id="5138a-129">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="5138a-129">-IsEnabled</span></span>
<span data-ttu-id="5138a-130">Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-130">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5138a-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="5138a-131">-Name</span></span>
<span data-ttu-id="5138a-132">Web kancası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-132">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="5138a-133">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="5138a-133">-Parameters</span></span>
<span data-ttu-id="5138a-134">Anahtar/değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-134">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="5138a-135">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="5138a-135">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="5138a-136">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="5138a-136">The values are the runbook parameter values.</span></span>
<span data-ttu-id="5138a-137">Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="5138a-137">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5138a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5138a-138">-ResourceGroupName</span></span>
<span data-ttu-id="5138a-139">Bu cmdlet 'in Web kancası oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-139">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="5138a-140">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5138a-140">-RunbookName</span></span>
<span data-ttu-id="5138a-141">Web kancası ile ilişkilendirilecek runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5138a-141">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5138a-142">-RunOn</span><span class="sxs-lookup"><span data-stu-id="5138a-142">-RunOn</span></span>
<span data-ttu-id="5138a-143">Runbook 'u yürütecek karma aracının isteğe bağlı adı</span><span class="sxs-lookup"><span data-stu-id="5138a-143">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="5138a-144">-Onay</span><span class="sxs-lookup"><span data-stu-id="5138a-144">-Confirm</span></span>
<span data-ttu-id="5138a-145">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5138a-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5138a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5138a-146">-WhatIf</span></span>
<span data-ttu-id="5138a-147">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5138a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5138a-148">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5138a-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5138a-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5138a-149">-DefaultProfile</span></span>
<span data-ttu-id="5138a-150">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5138a-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5138a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5138a-151">CommonParameters</span></span>
<span data-ttu-id="5138a-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5138a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5138a-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5138a-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5138a-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5138a-154">INPUTS</span></span>

## <span data-ttu-id="5138a-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5138a-155">OUTPUTS</span></span>

### <span data-ttu-id="5138a-156">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="5138a-156">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="5138a-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5138a-157">NOTES</span></span>

## <span data-ttu-id="5138a-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5138a-158">RELATED LINKS</span></span>

[<span data-ttu-id="5138a-159">Get-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="5138a-159">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="5138a-160">Remove-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="5138a-160">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="5138a-161">Set-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="5138a-161">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


