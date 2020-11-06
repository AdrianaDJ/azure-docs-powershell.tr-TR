---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589115"
---
# <span data-ttu-id="64d2f-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="64d2f-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="64d2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64d2f-102">SYNOPSIS</span></span>
<span data-ttu-id="64d2f-103">Belirli bir hizmet veri yolu kuyruğu için belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="64d2f-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64d2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64d2f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64d2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64d2f-105">DESCRIPTION</span></span>
<span data-ttu-id="64d2f-106">**Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet 'i, verilen hizmet veri yolu sırasındaki belirtilen yetkilendirme kuralının açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="64d2f-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="64d2f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64d2f-107">EXAMPLES</span></span>

### <span data-ttu-id="64d2f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="64d2f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="64d2f-109">Verilen hizmet veri yolu sırasının belirtilen yetkilendirme kuralı açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="64d2f-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="64d2f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64d2f-110">PARAMETERS</span></span>

### <span data-ttu-id="64d2f-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64d2f-111">-ResourceGroup</span></span>
<span data-ttu-id="64d2f-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="64d2f-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="64d2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64d2f-113">-DefaultProfile</span></span>
<span data-ttu-id="64d2f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64d2f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64d2f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="64d2f-115">-Name</span></span>
<span data-ttu-id="64d2f-116">EventHub AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="64d2f-116">EventHub AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="64d2f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="64d2f-117">-Namespace</span></span>
<span data-ttu-id="64d2f-118">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="64d2f-118">Namespace Name.</span></span>

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

### <span data-ttu-id="64d2f-119">-Sıra</span><span class="sxs-lookup"><span data-stu-id="64d2f-119">-Queue</span></span>
<span data-ttu-id="64d2f-120">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="64d2f-120">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64d2f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64d2f-121">CommonParameters</span></span>
<span data-ttu-id="64d2f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64d2f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64d2f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64d2f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64d2f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64d2f-124">INPUTS</span></span>

### <span data-ttu-id="64d2f-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64d2f-125">-ResourceGroup</span></span>
 <span data-ttu-id="64d2f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="64d2f-126">System.String</span></span>
 

### <span data-ttu-id="64d2f-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="64d2f-127">-NamespaceName</span></span>
 <span data-ttu-id="64d2f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="64d2f-128">System.String</span></span>
 

### <span data-ttu-id="64d2f-129">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="64d2f-129">-QueueName</span></span>
 <span data-ttu-id="64d2f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="64d2f-130">System.String</span></span>
 

### <span data-ttu-id="64d2f-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="64d2f-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="64d2f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="64d2f-132">System.String</span></span>

## <span data-ttu-id="64d2f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64d2f-133">OUTPUTS</span></span>

### <span data-ttu-id="64d2f-134">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. ServiceBus. modeller. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="64d2f-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="64d2f-135">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizatı Irules/SBAuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 location: Batı US Etiketler: haklar: {Listen, gönder}</span><span class="sxs-lookup"><span data-stu-id="64d2f-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="64d2f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64d2f-136">NOTES</span></span>

## <span data-ttu-id="64d2f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64d2f-137">RELATED LINKS</span></span>

