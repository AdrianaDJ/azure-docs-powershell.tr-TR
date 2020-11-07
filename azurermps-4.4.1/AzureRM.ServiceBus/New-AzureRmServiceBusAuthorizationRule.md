---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: be2b841511669ffa2ac3ffd416fd86072edcfb52
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764229"
---
# <span data-ttu-id="c543f-101">New-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c543f-101">New-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="c543f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c543f-102">SYNOPSIS</span></span>
<span data-ttu-id="c543f-103">Belirtilen hizmet veri yolu için ad alanı veya sıra veya konu için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c543f-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c543f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c543f-104">SYNTAX</span></span>

### <span data-ttu-id="c543f-105">NamespaceAuthorizationRuleSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c543f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c543f-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c543f-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c543f-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c543f-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c543f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c543f-108">DESCRIPTION</span></span>
<span data-ttu-id="c543f-109">**New-AzureRmServiceBusAuthorizationRule** cmdlet 'ı belirtilen hizmet veri yolu ad alanı veya kuyruğu veya konusu için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c543f-109">The **New-AzureRmServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="c543f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c543f-110">EXAMPLES</span></span>

### <span data-ttu-id="c543f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c543f-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="c543f-112">`AuthoRule1`Ad alanı Için **dinleme** ve **gönderme** haklarıyla oluşturulur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="c543f-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="c543f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c543f-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="c543f-114">`AuthoRule1`Sıra Için **dinleme** ve **gönderme** haklarıyla oluşturulur `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="c543f-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="c543f-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c543f-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="c543f-116">`AuthoRule1`Konu Için **dinleme** ve **gönderme** haklarıyla oluşturulur `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="c543f-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="c543f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c543f-117">PARAMETERS</span></span>

### <span data-ttu-id="c543f-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="c543f-118">-Confirm</span></span>
<span data-ttu-id="c543f-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c543f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c543f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="c543f-120">-Name</span></span>
<span data-ttu-id="c543f-121">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="c543f-121">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="c543f-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c543f-122">-Namespace</span></span>
<span data-ttu-id="c543f-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="c543f-123">Namespace Name.</span></span>

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

### <span data-ttu-id="c543f-124">-Sıra</span><span class="sxs-lookup"><span data-stu-id="c543f-124">-Queue</span></span>
<span data-ttu-id="c543f-125">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="c543f-125">Queue Name.</span></span>

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

### <span data-ttu-id="c543f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c543f-126">-ResourceGroupName</span></span>
<span data-ttu-id="c543f-127">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c543f-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c543f-128">-Hak</span><span class="sxs-lookup"><span data-stu-id="c543f-128">-Rights</span></span>
<span data-ttu-id="c543f-129">Haklar, örneğin, "Dinle", "Gönder", "Yönet"</span><span class="sxs-lookup"><span data-stu-id="c543f-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c543f-130">-Konu</span><span class="sxs-lookup"><span data-stu-id="c543f-130">-Topic</span></span>
<span data-ttu-id="c543f-131">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="c543f-131">Topic Name.</span></span>

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

### <span data-ttu-id="c543f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c543f-132">-WhatIf</span></span>
<span data-ttu-id="c543f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c543f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c543f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c543f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c543f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c543f-135">-DefaultProfile</span></span>
<span data-ttu-id="c543f-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c543f-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c543f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c543f-137">CommonParameters</span></span>
<span data-ttu-id="c543f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c543f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c543f-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c543f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c543f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c543f-140">INPUTS</span></span>

### <span data-ttu-id="c543f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c543f-141">System.String</span></span>
<span data-ttu-id="c543f-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="c543f-142">System.String[]</span></span>

## <span data-ttu-id="c543f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c543f-143">OUTPUTS</span></span>

### <span data-ttu-id="c543f-144">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c543f-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c543f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c543f-145">NOTES</span></span>

## <span data-ttu-id="c543f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c543f-146">RELATED LINKS</span></span>

