---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268958"
---
# <span data-ttu-id="e5bee-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e5bee-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="e5bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5bee-102">SYNOPSIS</span></span>
<span data-ttu-id="e5bee-103">Uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5bee-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="e5bee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5bee-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5bee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5bee-105">DESCRIPTION</span></span>
<span data-ttu-id="e5bee-106">**Yeni-Azalertrulekancalı** cmdlet, bir uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5bee-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="e5bee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5bee-107">EXAMPLES</span></span>

### <span data-ttu-id="e5bee-108">Örnek 1: uyarı kuralı Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5bee-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="e5bee-109">Bu komut yalnızca hizmet URI 'sini belirterek bir uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e5bee-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="e5bee-110">Örnek 2: tek bir özellikle bir Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="e5bee-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="e5bee-111">Bu komut, bir özelliği olan Contoso.com için bir uyarı kuralı Web kancası oluşturur ve $Actual değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="e5bee-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="e5bee-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5bee-112">PARAMETERS</span></span>

### <span data-ttu-id="e5bee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5bee-113">-DefaultProfile</span></span>
<span data-ttu-id="e5bee-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e5bee-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5bee-115">-Özellik</span><span class="sxs-lookup"><span data-stu-id="e5bee-115">-Property</span></span>
<span data-ttu-id="e5bee-116">@ (Property1 = ' değer1 ',....) biçimindeki özelliklerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5bee-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="e5bee-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e5bee-117">-ServiceUri</span></span>
<span data-ttu-id="e5bee-118">Hizmet URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e5bee-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="e5bee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5bee-119">CommonParameters</span></span>
<span data-ttu-id="e5bee-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5bee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5bee-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e5bee-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5bee-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5bee-122">INPUTS</span></span>

### <span data-ttu-id="e5bee-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e5bee-123">System.String</span></span>

### <span data-ttu-id="e5bee-124">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e5bee-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e5bee-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5bee-125">OUTPUTS</span></span>

### <span data-ttu-id="e5bee-126">Microsoft. Azure. Management. Monitor. Management. modeller. Rulewebtakma Işlemi</span><span class="sxs-lookup"><span data-stu-id="e5bee-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="e5bee-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5bee-127">NOTES</span></span>

## <span data-ttu-id="e5bee-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5bee-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5bee-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e5bee-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="e5bee-130">Add-Azmetrik ıalertrule</span><span class="sxs-lookup"><span data-stu-id="e5bee-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="e5bee-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e5bee-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="e5bee-132">Yeni-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e5bee-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="e5bee-133">Yeni-Azautoscaleweb kancası</span><span class="sxs-lookup"><span data-stu-id="e5bee-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


