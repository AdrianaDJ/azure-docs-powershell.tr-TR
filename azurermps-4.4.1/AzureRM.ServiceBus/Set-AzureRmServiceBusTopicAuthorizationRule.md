---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764226"
---
# <span data-ttu-id="7533c-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7533c-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="7533c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7533c-102">SYNOPSIS</span></span>
<span data-ttu-id="7533c-103">Verilen hizmet veri yolu konusu için belirtilen yetkilendirme kuralı açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7533c-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7533c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7533c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7533c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7533c-105">DESCRIPTION</span></span>
<span data-ttu-id="7533c-106">**Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet 'i, verilen hizmet veri yolu konusunun belirtilen yetkilendirme kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7533c-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="7533c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7533c-107">EXAMPLES</span></span>

### <span data-ttu-id="7533c-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7533c-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="7533c-109">Konu başlığı altındaki yetkilendirme kuralının erişim haklarına **Yönet** ekler `SBTopicAuthoRule1` `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="7533c-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="7533c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7533c-110">PARAMETERS</span></span>

### <span data-ttu-id="7533c-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7533c-111">-ResourceGroup</span></span>
<span data-ttu-id="7533c-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7533c-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="7533c-113">-Hak</span><span class="sxs-lookup"><span data-stu-id="7533c-113">-Rights</span></span>
<span data-ttu-id="7533c-114">Larım Örneğin, @ ("Dinle", "Gönder", "Yönet").</span><span class="sxs-lookup"><span data-stu-id="7533c-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="7533c-115">Gerekli Eğer **-authruleobj** belirtilmemişse.</span><span class="sxs-lookup"><span data-stu-id="7533c-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7533c-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="7533c-116">-Confirm</span></span>
<span data-ttu-id="7533c-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7533c-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7533c-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7533c-118">-WhatIf</span></span>
<span data-ttu-id="7533c-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7533c-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7533c-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7533c-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7533c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7533c-121">-DefaultProfile</span></span>
<span data-ttu-id="7533c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7533c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7533c-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="7533c-123">-InputObj</span></span>
<span data-ttu-id="7533c-124">ServiceBus konu AuthorizationRule nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7533c-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7533c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="7533c-125">-Name</span></span>
<span data-ttu-id="7533c-126">AuthorizationRule Name-' AuthruleObj ' belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="7533c-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7533c-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7533c-127">-Namespace</span></span>
<span data-ttu-id="7533c-128">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="7533c-128">Namespace Name.</span></span>

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

### <span data-ttu-id="7533c-129">-Konu</span><span class="sxs-lookup"><span data-stu-id="7533c-129">-Topic</span></span>
<span data-ttu-id="7533c-130">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="7533c-130">Topic Name.</span></span>

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

### <span data-ttu-id="7533c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7533c-131">CommonParameters</span></span>
<span data-ttu-id="7533c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7533c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7533c-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7533c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7533c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7533c-134">INPUTS</span></span>

### <span data-ttu-id="7533c-135">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7533c-135">-ResourceGroup</span></span>
 <span data-ttu-id="7533c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7533c-136">System.String</span></span>

### <span data-ttu-id="7533c-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7533c-137">-NamespaceName</span></span>
 <span data-ttu-id="7533c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7533c-138">System.String</span></span>

### <span data-ttu-id="7533c-139">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7533c-139">-TopicName</span></span>
 <span data-ttu-id="7533c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7533c-140">System.String</span></span>

### <span data-ttu-id="7533c-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="7533c-141">-AuthRuleObj</span></span>
 <span data-ttu-id="7533c-142">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7533c-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7533c-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7533c-143">OUTPUTS</span></span>

### <span data-ttu-id="7533c-144">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7533c-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="7533c-145">Kimlik:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/Authorization Rules/SBTopicAuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 location: Batı US Etiketler: haklar: {Listen, gönder, Yönet}</span><span class="sxs-lookup"><span data-stu-id="7533c-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="7533c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7533c-146">NOTES</span></span>

## <span data-ttu-id="7533c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7533c-147">RELATED LINKS</span></span>

