---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 497ffc1c213cf95f5b2c96053ced6144f63371b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593412"
---
# <span data-ttu-id="0459e-101">New-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0459e-101">New-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="0459e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0459e-102">SYNOPSIS</span></span>
<span data-ttu-id="0459e-103">Belirtilen hizmet veri yolu için ad alanı veya sıra veya konu için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0459e-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0459e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0459e-104">SYNTAX</span></span>

### <span data-ttu-id="0459e-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0459e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0459e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0459e-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0459e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0459e-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0459e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0459e-108">DESCRIPTION</span></span>
<span data-ttu-id="0459e-109">**New-AzureRmServiceBusAuthorizationRule** cmdlet 'ı belirtilen hizmet veri yolu ad alanı veya kuyruğu veya konusu için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0459e-109">The **New-AzureRmServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="0459e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0459e-110">EXAMPLES</span></span>

### <span data-ttu-id="0459e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0459e-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="0459e-112">`AuthoRule1`Ad alanı Için **dinleme** ve **gönderme** haklarıyla oluşturulur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0459e-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="0459e-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="0459e-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="0459e-114">`AuthoRule1`Sıra Için **dinleme** ve **gönderme** haklarıyla oluşturulur `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="0459e-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="0459e-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="0459e-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="0459e-116">`AuthoRule1`Konu Için **dinleme** ve **gönderme** haklarıyla oluşturulur `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="0459e-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="0459e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0459e-117">PARAMETERS</span></span>

### <span data-ttu-id="0459e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0459e-118">-DefaultProfile</span></span>
<span data-ttu-id="0459e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0459e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0459e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="0459e-120">-Name</span></span>
<span data-ttu-id="0459e-121">AuthorizationRule adı</span><span class="sxs-lookup"><span data-stu-id="0459e-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0459e-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0459e-122">-Namespace</span></span>
<span data-ttu-id="0459e-123">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="0459e-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0459e-124">-Sıra</span><span class="sxs-lookup"><span data-stu-id="0459e-124">-Queue</span></span>
<span data-ttu-id="0459e-125">Sıra adı</span><span class="sxs-lookup"><span data-stu-id="0459e-125">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0459e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0459e-126">-ResourceGroupName</span></span>
<span data-ttu-id="0459e-127">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="0459e-127">Resource Group Name</span></span>

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

### <span data-ttu-id="0459e-128">-Hak</span><span class="sxs-lookup"><span data-stu-id="0459e-128">-Rights</span></span>
<span data-ttu-id="0459e-129">Haklar, örneğin, "Dinle", "Gönder", "Yönet"</span><span class="sxs-lookup"><span data-stu-id="0459e-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0459e-130">-Konu</span><span class="sxs-lookup"><span data-stu-id="0459e-130">-Topic</span></span>
<span data-ttu-id="0459e-131">Konu adı</span><span class="sxs-lookup"><span data-stu-id="0459e-131">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0459e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="0459e-132">-Confirm</span></span>
<span data-ttu-id="0459e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0459e-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0459e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0459e-134">-WhatIf</span></span>
<span data-ttu-id="0459e-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0459e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0459e-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0459e-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0459e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0459e-137">CommonParameters</span></span>
<span data-ttu-id="0459e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0459e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0459e-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0459e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0459e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0459e-140">INPUTS</span></span>

### <span data-ttu-id="0459e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0459e-141">System.String</span></span>
<span data-ttu-id="0459e-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="0459e-142">System.String[]</span></span>


## <span data-ttu-id="0459e-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0459e-143">OUTPUTS</span></span>

### <span data-ttu-id="0459e-144">Microsoft. Azure. Commands. ServiceBus. model. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0459e-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="0459e-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0459e-145">NOTES</span></span>

## <span data-ttu-id="0459e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0459e-146">RELATED LINKS</span></span>
