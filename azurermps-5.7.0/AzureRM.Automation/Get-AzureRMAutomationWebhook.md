---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: e695495b13cbad32cbf1d945a7de4080a88cc49c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595121"
---
# <span data-ttu-id="c3df9-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c3df9-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="c3df9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3df9-102">SYNOPSIS</span></span>
<span data-ttu-id="c3df9-103">Web kancaları 'nı otomasyondan alır.</span><span class="sxs-lookup"><span data-stu-id="c3df9-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3df9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3df9-104">SYNTAX</span></span>

### <span data-ttu-id="c3df9-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c3df9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3df9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c3df9-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3df9-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c3df9-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3df9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3df9-108">DESCRIPTION</span></span>
<span data-ttu-id="c3df9-109">**Get-Azurermautomationweb** kancaları Web kancaları alır.</span><span class="sxs-lookup"><span data-stu-id="c3df9-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="c3df9-110">Belirli Web kancaları edinmek için Web kancası adını belirtin veya bir Azure Otomasyonu runbook adını belirterek Web kancaları 'na bağlanın.</span><span class="sxs-lookup"><span data-stu-id="c3df9-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="c3df9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3df9-111">EXAMPLES</span></span>

### <span data-ttu-id="c3df9-112">Örnek 1: runbook için tüm Web kancaları alma</span><span class="sxs-lookup"><span data-stu-id="c3df9-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="c3df9-113">Bu komut, ResourceGroup01 adındaki kaynak grubunda AutomationAccount01 adındaki Otomasyon hesabındaki Runbook03 adındaki runbook için tüm Web kancaları alır.</span><span class="sxs-lookup"><span data-stu-id="c3df9-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c3df9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3df9-114">PARAMETERS</span></span>

### <span data-ttu-id="c3df9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c3df9-115">-AutomationAccountName</span></span>
<span data-ttu-id="c3df9-116">Bu cmdlet 'in Web kancası aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3df9-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="c3df9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3df9-117">-DefaultProfile</span></span>
<span data-ttu-id="c3df9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c3df9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3df9-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c3df9-119">-Name</span></span>
<span data-ttu-id="c3df9-120">Bu cmdlet 'in aldığı Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3df9-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3df9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3df9-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3df9-122">Bu cmdlet Web kancaları aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3df9-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="c3df9-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c3df9-123">-RunbookName</span></span>
<span data-ttu-id="c3df9-124">Bu cmdlet 'in Web kancaları aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3df9-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3df9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3df9-125">CommonParameters</span></span>
<span data-ttu-id="c3df9-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3df9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3df9-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3df9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3df9-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3df9-128">INPUTS</span></span>

### <span data-ttu-id="c3df9-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c3df9-129">None</span></span>
<span data-ttu-id="c3df9-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c3df9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3df9-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3df9-131">OUTPUTS</span></span>

### <span data-ttu-id="c3df9-132">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="c3df9-132">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="c3df9-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3df9-133">NOTES</span></span>

## <span data-ttu-id="c3df9-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3df9-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3df9-135">Yeni-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="c3df9-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="c3df9-136">Remove-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="c3df9-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="c3df9-137">Set-Azurermautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="c3df9-137">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


