---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 417ab3f7f787a76041caceebbfcf32f9733717b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594502"
---
# <span data-ttu-id="4b5d4-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="4b5d4-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="4b5d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5d4-103">Otomasyon Runbook için Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b5d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b5d4-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b5d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b5d4-105">DESCRIPTION</span></span>
<span data-ttu-id="4b5d4-106">**Yeni-Azurermautomationkancai** cmdlet 'i, bir Azure Otomasyonu runbook için Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="4b5d4-107">Bu cmdlet 'in döndürdüğü Web kancası URL 'sini kaydettiğinizden emin olun, çünkü yeniden alamazsınız.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="4b5d4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b5d4-108">EXAMPLES</span></span>

### <span data-ttu-id="4b5d4-109">Örnek 1: Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4b5d4-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="4b5d4-110">Bu komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook06 adında bir Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="4b5d4-111">Komut, $Webhook değişkeninde Web kancasını depolar.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="4b5d4-112">Web kancası etkinleştirildi.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-112">The webhook is enabled.</span></span>
<span data-ttu-id="4b5d4-113">Web kancası belirtilen zamanda sona erecek.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="4b5d4-114">Bu komut Web kancası parametreleri için hiçbir değer sağlamaz.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="4b5d4-115">Bu komut *Force* parametresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="4b5d4-116">Bu nedenle sizden onay istemez.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4b5d4-117">Örnek 2: parametrelerle bir Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="4b5d4-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="4b5d4-118">İlk komut, bir parametre sözlüğü oluşturur ve bunları $Params değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="4b5d4-119">İkinci komut AutomationAccount01 adındaki Otomasyon hesabındaki ContosoRunbook adındaki runbook için Webhook11 adında bir Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="4b5d4-120">Komut, $Params parametreleri Web kancası 'na atar.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="4b5d4-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b5d4-121">PARAMETERS</span></span>

### <span data-ttu-id="4b5d4-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4b5d4-122">-AutomationAccountName</span></span>
<span data-ttu-id="4b5d4-123">Bu cmdlet 'in Web kancası oluşturduğu Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="4b5d4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5d4-124">-DefaultProfile</span></span>
<span data-ttu-id="4b5d4-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="4b5d4-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b5d4-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4b5d4-126">-ExpiryTime</span></span>
<span data-ttu-id="4b5d4-127">Web kancası için son kullanma süresini **DateTimeOffset** nesnesi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="4b5d4-128">Geçerli bir **DateTimeOffset** 'e dönüştürülebilecek bir dize veya **TarihSaat** belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-129">-Force</span><span class="sxs-lookup"><span data-stu-id="4b5d4-129">-Force</span></span>
<span data-ttu-id="4b5d4-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="4b5d4-130">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="4b5d4-131">-IsEnabled</span></span>
<span data-ttu-id="4b5d4-132">Web kancası 'nun etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-133">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b5d4-133">-Name</span></span>
<span data-ttu-id="4b5d4-134">Web kancası için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="4b5d4-135">-Parametreler</span><span class="sxs-lookup"><span data-stu-id="4b5d4-135">-Parameters</span></span>
<span data-ttu-id="4b5d4-136">Anahtar/değer çiftleri sözlüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="4b5d4-137">Anahtarlar, runbook parametre adlarıdır.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="4b5d4-138">Değerler runbook parametre değerleridir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="4b5d4-139">Runbook bir Web kancası karşılığında başlatıldığında, bu parametreler runbook 'a geçirilir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5d4-140">-ResourceGroupName</span></span>
<span data-ttu-id="4b5d4-141">Bu cmdlet 'in Web kancası oluşturduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="4b5d4-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="4b5d4-142">-RunbookName</span></span>
<span data-ttu-id="4b5d4-143">Web kancası ile ilişkilendirilecek runbook adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="4b5d4-144">-RunOn</span></span>
<span data-ttu-id="4b5d4-145">Runbook 'u yürütecek karma çalışanı grubunun isteğe bağlı adı</span><span class="sxs-lookup"><span data-stu-id="4b5d4-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b5d4-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b5d4-146">-Confirm</span></span>
<span data-ttu-id="4b5d4-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b5d4-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b5d4-148">-WhatIf</span></span>
<span data-ttu-id="4b5d4-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b5d4-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b5d4-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5d4-151">CommonParameters</span></span>
<span data-ttu-id="4b5d4-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5d4-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5d4-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5d4-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b5d4-154">INPUTS</span></span>

### <span data-ttu-id="4b5d4-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4b5d4-155">None</span></span>
<span data-ttu-id="4b5d4-156">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4b5d4-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b5d4-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b5d4-157">OUTPUTS</span></span>

### <span data-ttu-id="4b5d4-158">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="4b5d4-158">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="4b5d4-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b5d4-159">NOTES</span></span>

## <span data-ttu-id="4b5d4-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b5d4-160">RELATED LINKS</span></span>

[<span data-ttu-id="4b5d4-161">Get-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="4b5d4-161">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="4b5d4-162">Remove-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="4b5d4-162">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="4b5d4-163">Set-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="4b5d4-163">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


