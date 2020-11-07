---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: aa287095405e48550153e58049f750d78a9ed877
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93931871"
---
# <span data-ttu-id="321b2-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="321b2-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="321b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="321b2-102">SYNOPSIS</span></span>
<span data-ttu-id="321b2-103">Uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="321b2-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="321b2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="321b2-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="321b2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="321b2-105">DESCRIPTION</span></span>
<span data-ttu-id="321b2-106">**Yeni-Azalertrulekancalı** cmdlet, bir uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="321b2-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="321b2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="321b2-107">EXAMPLES</span></span>

### <span data-ttu-id="321b2-108">Örnek 1: uyarı kuralı Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="321b2-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="321b2-109">Bu komut yalnızca hizmet URI 'sini belirterek bir uyarı kuralı Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="321b2-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="321b2-110">Örnek 2: tek bir özellikle bir Web kancası oluşturma</span><span class="sxs-lookup"><span data-stu-id="321b2-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="321b2-111">Bu komut, bir özelliği olan Contoso.com için bir uyarı kuralı Web kancası oluşturur ve $Actual değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="321b2-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="321b2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="321b2-112">PARAMETERS</span></span>

### <span data-ttu-id="321b2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="321b2-113">-DefaultProfile</span></span>
<span data-ttu-id="321b2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="321b2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="321b2-115">-Özellik</span><span class="sxs-lookup"><span data-stu-id="321b2-115">-Property</span></span>
<span data-ttu-id="321b2-116">@ (Property1 = ' değer1 ',....) biçimindeki özelliklerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="321b2-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="321b2-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="321b2-117">-ServiceUri</span></span>
<span data-ttu-id="321b2-118">Hizmet URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="321b2-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="321b2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="321b2-119">CommonParameters</span></span>
<span data-ttu-id="321b2-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="321b2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="321b2-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="321b2-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="321b2-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="321b2-122">INPUTS</span></span>

### <span data-ttu-id="321b2-123">System. String</span><span class="sxs-lookup"><span data-stu-id="321b2-123">System.String</span></span>

### <span data-ttu-id="321b2-124">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="321b2-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="321b2-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="321b2-125">OUTPUTS</span></span>

### <span data-ttu-id="321b2-126">Microsoft. Azure. Management. Monitor. Management. modeller. Rulewebtakma Işlemi</span><span class="sxs-lookup"><span data-stu-id="321b2-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="321b2-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="321b2-127">NOTES</span></span>

## <span data-ttu-id="321b2-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="321b2-128">RELATED LINKS</span></span>

[<span data-ttu-id="321b2-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="321b2-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="321b2-130">Add-Azmetrik ıalertrule</span><span class="sxs-lookup"><span data-stu-id="321b2-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="321b2-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="321b2-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="321b2-132">Yeni-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="321b2-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="321b2-133">Yeni-Azautoscaleweb kancası</span><span class="sxs-lookup"><span data-stu-id="321b2-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


