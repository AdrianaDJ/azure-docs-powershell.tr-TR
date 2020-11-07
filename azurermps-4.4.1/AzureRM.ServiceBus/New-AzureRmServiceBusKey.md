---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusKey.md
ms.openlocfilehash: 0483c60a1624374dc3e5b750439d905f19ceb2fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764230"
---
# <span data-ttu-id="c39c4-101">New-AzureRmServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="c39c4-101">New-AzureRmServiceBusKey</span></span>

## <span data-ttu-id="c39c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c39c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c39c4-103">Hizmet veri yolu ad alanı veya sıra veya konu için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39c4-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c39c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c39c4-104">SYNTAX</span></span>

### <span data-ttu-id="c39c4-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c39c4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39c4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c39c4-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c39c4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c39c4-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c39c4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c39c4-108">DESCRIPTION</span></span>
<span data-ttu-id="c39c4-109">**Yeni-AzureRmServiceBusKey** cmdlet 'i belirtilen ad alanı veya sıra veya konu ve yetkilendirme kuralı için yeni birincil veya ikincil bağlantı dizeleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39c4-109">The **New-AzureRmServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="c39c4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c39c4-110">EXAMPLES</span></span>

### <span data-ttu-id="c39c4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c39c4-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="c39c4-112">Ad alanı için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39c4-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="c39c4-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c39c4-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="c39c4-114">Sıranın birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39c4-114">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="c39c4-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c39c4-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="c39c4-116">Konu için birincil veya ikincil bağlantı dizelerini yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c39c4-116">Regenerates the primary or secondary connection strings for the topic.</span></span>

## <span data-ttu-id="c39c4-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c39c4-117">PARAMETERS</span></span>

### <span data-ttu-id="c39c4-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="c39c4-118">-Confirm</span></span>
<span data-ttu-id="c39c4-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c39c4-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39c4-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c39c4-120">-Name</span></span>
<span data-ttu-id="c39c4-121">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="c39c4-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c39c4-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c39c4-122">-Namespace</span></span>
<span data-ttu-id="c39c4-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="c39c4-123">Namespace Name.</span></span>

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

### <span data-ttu-id="c39c4-124">-Sıra</span><span class="sxs-lookup"><span data-stu-id="c39c4-124">-Queue</span></span>
<span data-ttu-id="c39c4-125">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="c39c4-125">Queue Name.</span></span>

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

### <span data-ttu-id="c39c4-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="c39c4-126">-RegenerateKey</span></span>
<span data-ttu-id="c39c4-127">Anahtarları yeniden üret-' PrimaryKey '/' SecondaryKey '.</span><span class="sxs-lookup"><span data-stu-id="c39c4-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39c4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c39c4-128">-ResourceGroupName</span></span>
<span data-ttu-id="c39c4-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c39c4-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="c39c4-130">-Konu</span><span class="sxs-lookup"><span data-stu-id="c39c4-130">-Topic</span></span>
<span data-ttu-id="c39c4-131">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="c39c4-131">Topic Name.</span></span>

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

### <span data-ttu-id="c39c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c39c4-132">-WhatIf</span></span>
<span data-ttu-id="c39c4-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c39c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c39c4-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c39c4-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c39c4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c39c4-135">-DefaultProfile</span></span>
<span data-ttu-id="c39c4-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c39c4-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c39c4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c39c4-137">CommonParameters</span></span>
<span data-ttu-id="c39c4-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c39c4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c39c4-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c39c4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c39c4-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c39c4-140">INPUTS</span></span>

### <span data-ttu-id="c39c4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c39c4-141">System.String</span></span>

## <span data-ttu-id="c39c4-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c39c4-142">OUTPUTS</span></span>

### <span data-ttu-id="c39c4-143">Microsoft. Azure. Commands. ServiceBus. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="c39c4-143">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="c39c4-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c39c4-144">NOTES</span></span>

## <span data-ttu-id="c39c4-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c39c4-145">RELATED LINKS</span></span>

