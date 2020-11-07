---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762409"
---
# <span data-ttu-id="b9c75-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b9c75-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="b9c75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c75-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c75-103">Belirtilen Service Bus konusu için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b9c75-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9c75-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b9c75-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c75-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b9c75-105">DESCRIPTION</span></span>
<span data-ttu-id="b9c75-106">**Yeni-AzureRmServiceBusTopicAuthorizationRule** cmdlet 'i, belirtilen hizmet veri yolu konusu için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b9c75-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="b9c75-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b9c75-107">EXAMPLES</span></span>

### <span data-ttu-id="b9c75-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b9c75-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="b9c75-109">`SBTopicAuthoRule1`Konu Için **dinleme** ve **gönderme** haklarıyla yetkilendirme kuralı oluşturur `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="b9c75-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="b9c75-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b9c75-110">PARAMETERS</span></span>

### <span data-ttu-id="b9c75-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9c75-111">-ResourceGroup</span></span>
<span data-ttu-id="b9c75-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b9c75-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9c75-113">-Hak</span><span class="sxs-lookup"><span data-stu-id="b9c75-113">-Rights</span></span>
<span data-ttu-id="b9c75-114">Haklar; Örneğin, @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="b9c75-114">The rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="b9c75-115">-Confirm</span></span>
<span data-ttu-id="b9c75-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b9c75-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c75-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c75-117">-WhatIf</span></span>
<span data-ttu-id="b9c75-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b9c75-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9c75-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b9c75-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c75-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c75-120">-DefaultProfile</span></span>
<span data-ttu-id="b9c75-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b9c75-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9c75-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="b9c75-122">-Name</span></span>
<span data-ttu-id="b9c75-123">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="b9c75-123">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b9c75-124">-Namespace</span></span>
<span data-ttu-id="b9c75-125">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="b9c75-125">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-126">-Konu</span><span class="sxs-lookup"><span data-stu-id="b9c75-126">-Topic</span></span>
<span data-ttu-id="b9c75-127">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="b9c75-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c75-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c75-128">CommonParameters</span></span>
<span data-ttu-id="b9c75-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b9c75-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c75-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c75-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c75-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b9c75-131">INPUTS</span></span>

### <span data-ttu-id="b9c75-132">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9c75-132">-ResourceGroup</span></span>
 <span data-ttu-id="b9c75-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c75-133">System.String</span></span>
 

### <span data-ttu-id="b9c75-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b9c75-134">-NamespaceName</span></span>
 <span data-ttu-id="b9c75-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c75-135">System.String</span></span>
 

### <span data-ttu-id="b9c75-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b9c75-136">-TopicName</span></span>
 <span data-ttu-id="b9c75-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c75-137">System.String</span></span>
 

### <span data-ttu-id="b9c75-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b9c75-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b9c75-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b9c75-139">System.String</span></span>

## <span data-ttu-id="b9c75-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b9c75-140">OUTPUTS</span></span>

### <span data-ttu-id="b9c75-141">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b9c75-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="b9c75-142">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizatı Irules/SBTopicAuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 location: Batı US Etiketler: haklar: {Listen, gönder}</span><span class="sxs-lookup"><span data-stu-id="b9c75-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="b9c75-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b9c75-143">NOTES</span></span>

## <span data-ttu-id="b9c75-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b9c75-144">RELATED LINKS</span></span>

