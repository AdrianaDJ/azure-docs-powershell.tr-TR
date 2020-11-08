---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104988"
---
# <span data-ttu-id="a1152-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a1152-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="a1152-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1152-102">SYNOPSIS</span></span>
<span data-ttu-id="a1152-103">Web kancaları 'nı otomasyondan alır.</span><span class="sxs-lookup"><span data-stu-id="a1152-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="a1152-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1152-104">SYNTAX</span></span>

### <span data-ttu-id="a1152-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a1152-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1152-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a1152-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1152-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="a1152-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1152-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1152-108">DESCRIPTION</span></span>
<span data-ttu-id="a1152-109">**Get-Azautomationwebkancası** cmdlet 'i Web kancaları alır.</span><span class="sxs-lookup"><span data-stu-id="a1152-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="a1152-110">Belirli Web kancaları edinmek için Web kancası adını belirtin veya bir Azure Otomasyonu runbook adını belirterek Web kancaları 'na bağlanın.</span><span class="sxs-lookup"><span data-stu-id="a1152-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="a1152-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1152-111">EXAMPLES</span></span>

### <span data-ttu-id="a1152-112">Örnek 1: runbook için tüm Web kancaları alma</span><span class="sxs-lookup"><span data-stu-id="a1152-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="a1152-113">Bu komut, ResourceGroup01 adındaki kaynak grubunda AutomationAccount01 adındaki Otomasyon hesabındaki Runbook03 adındaki runbook için tüm Web kancaları alır.</span><span class="sxs-lookup"><span data-stu-id="a1152-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a1152-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1152-114">PARAMETERS</span></span>

### <span data-ttu-id="a1152-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a1152-115">-AutomationAccountName</span></span>
<span data-ttu-id="a1152-116">Bu cmdlet 'in Web kancası aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1152-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="a1152-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1152-117">-DefaultProfile</span></span>
<span data-ttu-id="a1152-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a1152-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1152-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1152-119">-Name</span></span>
<span data-ttu-id="a1152-120">Bu cmdlet 'in aldığı Web kancası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1152-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1152-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1152-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1152-122">Bu cmdlet Web kancaları aldığı kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1152-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="a1152-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a1152-123">-RunbookName</span></span>
<span data-ttu-id="a1152-124">Bu cmdlet 'in Web kancaları aldığı runbook 'un adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1152-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1152-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1152-125">CommonParameters</span></span>
<span data-ttu-id="a1152-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1152-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1152-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1152-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1152-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1152-128">INPUTS</span></span>

### <span data-ttu-id="a1152-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a1152-129">System.String</span></span>

## <span data-ttu-id="a1152-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1152-130">OUTPUTS</span></span>

### <span data-ttu-id="a1152-131">Microsoft. Azure. Commands. Automation. model. Web kancası</span><span class="sxs-lookup"><span data-stu-id="a1152-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="a1152-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1152-132">NOTES</span></span>

## <span data-ttu-id="a1152-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1152-133">RELATED LINKS</span></span>

[<span data-ttu-id="a1152-134">Yeni-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a1152-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="a1152-135">Remove-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a1152-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="a1152-136">Set-Azautomationweb kancası</span><span class="sxs-lookup"><span data-stu-id="a1152-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


