---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594565"
---
# <span data-ttu-id="63ca2-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="63ca2-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="63ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="63ca2-103">Belirli bir ad alanı veya sıra veya konu için belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="63ca2-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63ca2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="63ca2-104">SYNTAX</span></span>

### <span data-ttu-id="63ca2-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="63ca2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ca2-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="63ca2-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63ca2-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="63ca2-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63ca2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="63ca2-108">DESCRIPTION</span></span>
<span data-ttu-id="63ca2-109">**Get-AzureRmServiceBusAuthorizationRule** cmdlet 'i, verilen ad alanında veya kuyrukta veya konuda belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="63ca2-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="63ca2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="63ca2-110">EXAMPLES</span></span>

### <span data-ttu-id="63ca2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="63ca2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="63ca2-112">Belirtilen ad alanı için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="63ca2-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="63ca2-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="63ca2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="63ca2-114">Belirtilen bir sıranın belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="63ca2-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="63ca2-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="63ca2-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="63ca2-116">Belirtilen bir konu için belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="63ca2-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="63ca2-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="63ca2-117">PARAMETERS</span></span>

### <span data-ttu-id="63ca2-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="63ca2-118">-Name</span></span>
<span data-ttu-id="63ca2-119">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="63ca2-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ca2-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="63ca2-120">-Namespace</span></span>
<span data-ttu-id="63ca2-121">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="63ca2-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ca2-122">-Sıra</span><span class="sxs-lookup"><span data-stu-id="63ca2-122">-Queue</span></span>
<span data-ttu-id="63ca2-123">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="63ca2-123">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ca2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ca2-124">-ResourceGroupName</span></span>
<span data-ttu-id="63ca2-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="63ca2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="63ca2-126">-Konu</span><span class="sxs-lookup"><span data-stu-id="63ca2-126">-Topic</span></span>
<span data-ttu-id="63ca2-127">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="63ca2-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63ca2-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ca2-128">-DefaultProfile</span></span>
<span data-ttu-id="63ca2-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="63ca2-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63ca2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ca2-130">CommonParameters</span></span>
<span data-ttu-id="63ca2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="63ca2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ca2-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ca2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ca2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="63ca2-133">INPUTS</span></span>

### <span data-ttu-id="63ca2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="63ca2-134">System.String</span></span>

## <span data-ttu-id="63ca2-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="63ca2-135">OUTPUTS</span></span>

### <span data-ttu-id="63ca2-136">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="63ca2-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="63ca2-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="63ca2-137">NOTES</span></span>
## <span data-ttu-id="63ca2-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63ca2-138">RELATED LINKS</span></span>

## <span data-ttu-id="63ca2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="63ca2-139">RELATED LINKS</span></span>

