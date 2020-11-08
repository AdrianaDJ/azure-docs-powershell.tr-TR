---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0f767b2c59a7cbf297c652873d4be1c064aec296
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096573"
---
# <span data-ttu-id="fc18c-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="fc18c-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="fc18c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc18c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc18c-103">Belirtilen hizmet veri yolu ad alanından bir konuya aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc18c-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fc18c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc18c-104">SYNTAX</span></span>

### <span data-ttu-id="fc18c-105">Subscriptionset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fc18c-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fc18c-106">Subscriptionınputobjectset</span><span class="sxs-lookup"><span data-stu-id="fc18c-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc18c-107">Subscriptionresourceıdset</span><span class="sxs-lookup"><span data-stu-id="fc18c-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc18c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc18c-108">DESCRIPTION</span></span>
<span data-ttu-id="fc18c-109">**Remove-AzServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir konuya aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fc18c-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fc18c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc18c-110">EXAMPLES</span></span>

### <span data-ttu-id="fc18c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fc18c-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="fc18c-112">`SB-TopicSubscription-Example1` `SB-Topic_exampl1` Belirtilen hizmet veri yolu ad alanındaki konuya aboneliği kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="fc18c-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="fc18c-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="fc18c-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="fc18c-114">Örnek 2,2-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="fc18c-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="fc18c-115">Örnek 3,1-RESOURCEID-değişken kullanarak:</span><span class="sxs-lookup"><span data-stu-id="fc18c-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="fc18c-116">Örnek 3,2-RESOURCEID-dize değeri kullanma:</span><span class="sxs-lookup"><span data-stu-id="fc18c-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="fc18c-117">$Resourceid/String for-RESOURCEID parametresindeki ARM kimliği aracılığıyla sağlanan aboneliği kaldırır</span><span class="sxs-lookup"><span data-stu-id="fc18c-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="fc18c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc18c-118">PARAMETERS</span></span>

### <span data-ttu-id="fc18c-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="fc18c-119">-AsJob</span></span>
<span data-ttu-id="fc18c-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fc18c-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc18c-121">-DefaultProfile</span></span>
<span data-ttu-id="fc18c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc18c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc18c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc18c-123">-InputObject</span></span>
<span data-ttu-id="fc18c-124">Hizmet veri yolu aboneliği nesnesi</span><span class="sxs-lookup"><span data-stu-id="fc18c-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc18c-125">-Name</span></span>
<span data-ttu-id="fc18c-126">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="fc18c-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc18c-127">-Namespace</span></span>
<span data-ttu-id="fc18c-128">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="fc18c-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fc18c-129">-PassThru</span></span>
<span data-ttu-id="fc18c-130">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc18c-130">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc18c-131">-ResourceGroupName</span></span>
<span data-ttu-id="fc18c-132">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="fc18c-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fc18c-133">-ResourceId</span></span>
<span data-ttu-id="fc18c-134">Hizmet veri yolu aboneliği kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fc18c-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-135">-Konu</span><span class="sxs-lookup"><span data-stu-id="fc18c-135">-Topic</span></span>
<span data-ttu-id="fc18c-136">Konu adı</span><span class="sxs-lookup"><span data-stu-id="fc18c-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc18c-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="fc18c-137">-Confirm</span></span>
<span data-ttu-id="fc18c-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fc18c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc18c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc18c-139">-WhatIf</span></span>
<span data-ttu-id="fc18c-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fc18c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc18c-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fc18c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc18c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc18c-142">CommonParameters</span></span>
<span data-ttu-id="fc18c-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc18c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc18c-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc18c-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc18c-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc18c-145">INPUTS</span></span>

### <span data-ttu-id="fc18c-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fc18c-146">System.String</span></span>

### <span data-ttu-id="fc18c-147">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="fc18c-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="fc18c-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc18c-148">OUTPUTS</span></span>

### <span data-ttu-id="fc18c-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc18c-149">System.Boolean</span></span>

## <span data-ttu-id="fc18c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc18c-150">NOTES</span></span>

## <span data-ttu-id="fc18c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc18c-151">RELATED LINKS</span></span>
