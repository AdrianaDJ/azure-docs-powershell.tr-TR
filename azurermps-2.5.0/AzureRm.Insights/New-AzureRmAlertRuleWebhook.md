---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
ms.openlocfilehash: d45624da172ecafba48354968d5a3ac5531be693
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940134"
---
# <span data-ttu-id="70a1f-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="70a1f-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="70a1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="70a1f-103">Uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a1f-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70a1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="70a1f-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70a1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="70a1f-105">DESCRIPTION</span></span>
<span data-ttu-id="70a1f-106">**Yeni-Azurermalertruleweb kancası** cmdlet 'i uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a1f-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="70a1f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="70a1f-107">EXAMPLES</span></span>

### <span data-ttu-id="70a1f-108">Örnek 1: uyarı kuralı Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="70a1f-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="70a1f-109">Bu komut yalnızca hizmet URI 'sini belirterek bir uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="70a1f-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="70a1f-110">Örnek 2: tek bir özellikle bir Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="70a1f-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="70a1f-111">Bu komut, bir özelliği olan Contoso.com için bir uyarı kuralı Web kancası oluşturur ve $Actual değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="70a1f-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="70a1f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="70a1f-112">PARAMETERS</span></span>

### <span data-ttu-id="70a1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a1f-113">-DefaultProfile</span></span>
<span data-ttu-id="70a1f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="70a1f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70a1f-115">-Özellik</span><span class="sxs-lookup"><span data-stu-id="70a1f-115">-Property</span></span>
<span data-ttu-id="70a1f-116">@ (Property1 = ' değer1 ',....) biçimindeki özelliklerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a1f-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70a1f-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="70a1f-117">-ServiceUri</span></span>
<span data-ttu-id="70a1f-118">Hizmet URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="70a1f-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="70a1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a1f-119">CommonParameters</span></span>
<span data-ttu-id="70a1f-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="70a1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a1f-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70a1f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a1f-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="70a1f-122">INPUTS</span></span>

### <span data-ttu-id="70a1f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="70a1f-123">System.String</span></span>

### <span data-ttu-id="70a1f-124">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="70a1f-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="70a1f-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="70a1f-125">OUTPUTS</span></span>

### <span data-ttu-id="70a1f-126">Microsoft. Azure. Management. Monitor. Management. modeller. Rulewebtakma Işlemi</span><span class="sxs-lookup"><span data-stu-id="70a1f-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="70a1f-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="70a1f-127">NOTES</span></span>

## <span data-ttu-id="70a1f-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="70a1f-128">RELATED LINKS</span></span>



[<span data-ttu-id="70a1f-129">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="70a1f-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="70a1f-130">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="70a1f-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="70a1f-131">Yeni-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="70a1f-131">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="70a1f-132">Yeni-Azurermautoscaleweb kancası</span><span class="sxs-lookup"><span data-stu-id="70a1f-132">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


