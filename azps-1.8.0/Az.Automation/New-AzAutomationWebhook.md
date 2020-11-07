---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 94bc498caa5052df5aa9a9e7724ecb87d253d9f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761552"
---
# <span data-ttu-id="358a6-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="358a6-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="358a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="358a6-102">SYNOPSIS</span></span>
<span data-ttu-id="358a6-103">Otomasyon Runbook için Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="358a6-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="358a6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="358a6-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="358a6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="358a6-105">DESCRIPTION</span></span>
<span data-ttu-id="358a6-106">**Yeni-Azautomationweb kancası** cmdlet 'i, bir Azure Otomasyonu runbook için Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="358a6-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="358a6-107">Bu cmdlet 'in döndürdüğü Web kancası URL 'sini kaydettiğinizden emin olun, çünkü yeniden alamazsınız.</span><span class="sxs-lookup"><span data-stu-id="358a6-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="358a6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="358a6-108">EXAMPLES</span></span>

### <span data-ttu-id="358a6-109">Örnek 1: Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="358a6-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="358a6-110">Bu komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook06 adında bir Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="358a6-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="358a6-111">Komut, $Webhook değişkeninde Web kancasını depolar.</span><span class="sxs-lookup"><span data-stu-id="358a6-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="358a6-112">Web kancası etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="358a6-112">The webhook is enabled.</span></span>
<span data-ttu-id="358a6-113">Web kancası belirtilen zamanda sona erecek.</span><span class="sxs-lookup"><span data-stu-id="358a6-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="358a6-114">Bu komut Web kancası parametreleri için hiçbir değer sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="358a6-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="358a6-115">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="358a6-116">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="358a6-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="358a6-117">Örnek 2: parametrelerle bir Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="358a6-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="358a6-118">İlk komut, bir parametre sözlüğü oluşturur ve bunları $Params değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="358a6-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="358a6-119">İkinci komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook11 adında bir Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="358a6-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="358a6-120">Komut, $Params parametreleri Web kancası 'na atar.</span><span class="sxs-lookup"><span data-stu-id="358a6-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="358a6-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="358a6-121">PARAMETERS</span></span>

### <span data-ttu-id="358a6-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="358a6-122">-AutomationAccountName</span></span>
<span data-ttu-id="358a6-123">Bu cmdlet 'in Web kancası oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="358a6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358a6-124">-DefaultProfile</span></span>
<span data-ttu-id="358a6-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="358a6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="358a6-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="358a6-126">-ExpiryTime</span></span>
<span data-ttu-id="358a6-127">Web kancası için son kullanma süresini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="358a6-128">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize veya **TarihSaat** belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="358a6-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="358a6-129">-Force</span><span class="sxs-lookup"><span data-stu-id="358a6-129">-Force</span></span>
<span data-ttu-id="358a6-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="358a6-130">ps_force</span></span>

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

### <span data-ttu-id="358a6-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="358a6-131">-IsEnabled</span></span>
<span data-ttu-id="358a6-132">Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-132">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="358a6-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="358a6-133">-Name</span></span>
<span data-ttu-id="358a6-134">Web kancası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="358a6-135">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="358a6-135">-Parameters</span></span>
<span data-ttu-id="358a6-136">Anahtar/değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="358a6-137">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="358a6-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="358a6-138">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="358a6-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="358a6-139">Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="358a6-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="358a6-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358a6-140">-ResourceGroupName</span></span>
<span data-ttu-id="358a6-141">Bu cmdlet 'in Web kancası oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="358a6-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="358a6-142">-RunbookName</span></span>
<span data-ttu-id="358a6-143">Web kancası ile ilişkilendirilecek runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="358a6-143">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="358a6-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="358a6-144">-RunOn</span></span>
<span data-ttu-id="358a6-145">Runbook 'u yürütecek karma çalışanı grubunun isteğe bağlı adı</span><span class="sxs-lookup"><span data-stu-id="358a6-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="358a6-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="358a6-146">-Confirm</span></span>
<span data-ttu-id="358a6-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="358a6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="358a6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358a6-148">-WhatIf</span></span>
<span data-ttu-id="358a6-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="358a6-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="358a6-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="358a6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="358a6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358a6-151">CommonParameters</span></span>
<span data-ttu-id="358a6-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="358a6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358a6-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358a6-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358a6-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="358a6-154">INPUTS</span></span>

### <span data-ttu-id="358a6-155">System. String</span><span class="sxs-lookup"><span data-stu-id="358a6-155">System.String</span></span>

### <span data-ttu-id="358a6-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="358a6-156">System.Boolean</span></span>

### <span data-ttu-id="358a6-157">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="358a6-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="358a6-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="358a6-158">OUTPUTS</span></span>

### <span data-ttu-id="358a6-159">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="358a6-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="358a6-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="358a6-160">NOTES</span></span>

## <span data-ttu-id="358a6-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="358a6-161">RELATED LINKS</span></span>

[<span data-ttu-id="358a6-162">Get-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="358a6-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="358a6-163">Remove-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="358a6-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="358a6-164">Set-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="358a6-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)

