---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusKey.md
ms.openlocfilehash: 28abf3ff725f5a1b124f99c96b46d03458b42f8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587792"
---
# <span data-ttu-id="a4389-101">Get-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="a4389-101">Get-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="a4389-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4389-102">SYNOPSIS</span></span>
<span data-ttu-id="a4389-103">Verilen ad alanı veya sıra veya konu için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="a4389-103">Gets the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4389-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4389-104">SYNTAX</span></span>

### <span data-ttu-id="a4389-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a4389-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4389-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4389-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4389-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4389-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4389-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4389-108">DESCRIPTION</span></span>
<span data-ttu-id="a4389-109">**Get-AzureRmServiceBusKey** cmdlet 'i, verilen ad alanı veya sıra veya konu için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a4389-109">The **Get-AzureRmServiceBusKey** cmdlet returns the primary and secondary connection strings for the given Namespace or Queue or Topic.</span></span> 

## <span data-ttu-id="a4389-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4389-110">EXAMPLES</span></span>

### <span data-ttu-id="a4389-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a4389-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="a4389-112">Belirtilen ad alanına birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a4389-112">Primary and secondary connection string to the specified namespace.</span></span>

### <span data-ttu-id="a4389-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a4389-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="a4389-114">Belirtilen sıraya birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a4389-114">Primary and secondary connection string to the specified queue.</span></span>

### <span data-ttu-id="a4389-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a4389-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="a4389-116">Belirtilen konuya birincil ve ikincil bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="a4389-116">Primary and secondary connection string to the specified topic.</span></span>

## <span data-ttu-id="a4389-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4389-117">PARAMETERS</span></span>

### <span data-ttu-id="a4389-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a4389-118">-Name</span></span>
<span data-ttu-id="a4389-119">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="a4389-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4389-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4389-120">-Namespace</span></span>
<span data-ttu-id="a4389-121">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a4389-121">Namespace Name.</span></span>

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

### <span data-ttu-id="a4389-122">-Sıra</span><span class="sxs-lookup"><span data-stu-id="a4389-122">-Queue</span></span>
<span data-ttu-id="a4389-123">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="a4389-123">Queue Name.</span></span>

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

### <span data-ttu-id="a4389-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4389-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4389-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a4389-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4389-126">-Konu</span><span class="sxs-lookup"><span data-stu-id="a4389-126">-Topic</span></span>
<span data-ttu-id="a4389-127">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="a4389-127">Topic Name.</span></span>

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

### <span data-ttu-id="a4389-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4389-128">-DefaultProfile</span></span>
<span data-ttu-id="a4389-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a4389-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4389-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4389-130">CommonParameters</span></span>
<span data-ttu-id="a4389-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4389-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4389-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4389-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4389-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4389-133">INPUTS</span></span>

### <span data-ttu-id="a4389-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4389-134">System.String</span></span>

## <span data-ttu-id="a4389-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4389-135">OUTPUTS</span></span>

### <span data-ttu-id="a4389-136">Microsoft. Azure. Commands. ServiceBus. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a4389-136">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="a4389-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4389-137">NOTES</span></span>

## <span data-ttu-id="a4389-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4389-138">RELATED LINKS</span></span>

