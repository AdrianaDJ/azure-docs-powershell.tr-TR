---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593802"
---
# <span data-ttu-id="14f8b-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="14f8b-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="14f8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14f8b-102">SYNOPSIS</span></span>
<span data-ttu-id="14f8b-103">Verilen konu için belirtilen yetkilendirme kuralı açıklamasının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="14f8b-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14f8b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14f8b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14f8b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14f8b-105">DESCRIPTION</span></span>
<span data-ttu-id="14f8b-106">**Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet 'i, verilen hizmet veri yolu konusundaki belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="14f8b-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="14f8b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14f8b-107">EXAMPLES</span></span>

### <span data-ttu-id="14f8b-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14f8b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="14f8b-109">Verilen konu için belirtilen yetkilendirme kuralının açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="14f8b-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="14f8b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14f8b-110">PARAMETERS</span></span>

### <span data-ttu-id="14f8b-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="14f8b-111">-ResourceGroup</span></span>
<span data-ttu-id="14f8b-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="14f8b-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="14f8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f8b-113">-DefaultProfile</span></span>
<span data-ttu-id="14f8b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14f8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14f8b-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="14f8b-115">-Name</span></span>
<span data-ttu-id="14f8b-116">Konu AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="14f8b-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="14f8b-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="14f8b-117">-Namespace</span></span>
<span data-ttu-id="14f8b-118">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="14f8b-118">Namespace Name.</span></span>

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

### <span data-ttu-id="14f8b-119">-Konu</span><span class="sxs-lookup"><span data-stu-id="14f8b-119">-Topic</span></span>
<span data-ttu-id="14f8b-120">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="14f8b-120">Topic Name.</span></span>

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

### <span data-ttu-id="14f8b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f8b-121">CommonParameters</span></span>
<span data-ttu-id="14f8b-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14f8b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f8b-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f8b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f8b-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14f8b-124">INPUTS</span></span>

### <span data-ttu-id="14f8b-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="14f8b-125">-ResourceGroup</span></span>
 <span data-ttu-id="14f8b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="14f8b-126">System.String</span></span>
 

### <span data-ttu-id="14f8b-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="14f8b-127">-NamespaceName</span></span>
 <span data-ttu-id="14f8b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="14f8b-128">System.String</span></span>
 

### <span data-ttu-id="14f8b-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="14f8b-129">-TopicName</span></span>
 <span data-ttu-id="14f8b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="14f8b-130">System.String</span></span>
 

### <span data-ttu-id="14f8b-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="14f8b-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="14f8b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="14f8b-132">System.String</span></span>

## <span data-ttu-id="14f8b-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14f8b-133">OUTPUTS</span></span>

### <span data-ttu-id="14f8b-134">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="14f8b-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="14f8b-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizatı Irules/SBTopicAuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 location: Batı US Etiketler: haklar: {Listen, gönder}</span><span class="sxs-lookup"><span data-stu-id="14f8b-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="14f8b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14f8b-136">NOTES</span></span>

## <span data-ttu-id="14f8b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14f8b-137">RELATED LINKS</span></span>

