---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 0369d6bac19d2d2180c54f3c4244101df3a7bb42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932454"
---
# <span data-ttu-id="3a4d9-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="3a4d9-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="3a4d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="3a4d9-103">Belirtilen hizmet veri yolu ad alanından bir konuya aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3a4d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3a4d9-104">SYNTAX</span></span>

### <span data-ttu-id="3a4d9-105">Subscriptionset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3a4d9-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a4d9-106">Subscriptionınputobjectset</span><span class="sxs-lookup"><span data-stu-id="3a4d9-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a4d9-107">Subscriptionresourceıdset</span><span class="sxs-lookup"><span data-stu-id="3a4d9-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a4d9-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3a4d9-108">DESCRIPTION</span></span>
<span data-ttu-id="3a4d9-109">**Remove-AzServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir konuya aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3a4d9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3a4d9-110">EXAMPLES</span></span>

### <span data-ttu-id="3a4d9-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3a4d9-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="3a4d9-112">`SB-TopicSubscription-Example1` `SB-Topic_exampl1` Belirtilen hizmet veri yolu ad alanındaki konuya aboneliği kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3a4d9-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="3a4d9-113">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="3a4d9-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="3a4d9-114">Örnek 2,2-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="3a4d9-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="3a4d9-115">Örnek 3,1-RESOURCEID-değişken kullanarak:</span><span class="sxs-lookup"><span data-stu-id="3a4d9-115">Example 3.1 - ResourceId - Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="3a4d9-116">Örnek 3,2-RESOURCEID-dize değeri kullanma:</span><span class="sxs-lookup"><span data-stu-id="3a4d9-116">Example 3.2 - ResourceId - Using string value:</span></span>
```
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="3a4d9-117">$Resourceid/String for-RESOURCEID parametresindeki ARM kimliği aracılığıyla sağlanan aboneliği kaldırır</span><span class="sxs-lookup"><span data-stu-id="3a4d9-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="3a4d9-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3a4d9-118">PARAMETERS</span></span>

### <span data-ttu-id="3a4d9-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="3a4d9-119">-AsJob</span></span>
<span data-ttu-id="3a4d9-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3a4d9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a4d9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a4d9-121">-DefaultProfile</span></span>
<span data-ttu-id="3a4d9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a4d9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a4d9-123">-InputObject</span></span>
<span data-ttu-id="3a4d9-124">Hizmet veri yolu aboneliği nesnesi</span><span class="sxs-lookup"><span data-stu-id="3a4d9-124">Service Bus Subscription Object</span></span>

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

### <span data-ttu-id="3a4d9-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="3a4d9-125">-Name</span></span>
<span data-ttu-id="3a4d9-126">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="3a4d9-126">Subscription Name</span></span>

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

### <span data-ttu-id="3a4d9-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3a4d9-127">-Namespace</span></span>
<span data-ttu-id="3a4d9-128">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="3a4d9-128">Namespace Name</span></span>

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

### <span data-ttu-id="3a4d9-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3a4d9-129">-PassThru</span></span>
<span data-ttu-id="3a4d9-130">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="3a4d9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a4d9-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a4d9-132">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3a4d9-132">The name of the resource group</span></span>

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

### <span data-ttu-id="3a4d9-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3a4d9-133">-ResourceId</span></span>
<span data-ttu-id="3a4d9-134">Hizmet veri yolu aboneliği kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3a4d9-134">Service Bus Subscription Resource Id</span></span>

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

### <span data-ttu-id="3a4d9-135">-Konu</span><span class="sxs-lookup"><span data-stu-id="3a4d9-135">-Topic</span></span>
<span data-ttu-id="3a4d9-136">Konu adı</span><span class="sxs-lookup"><span data-stu-id="3a4d9-136">Topic Name</span></span>

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

### <span data-ttu-id="3a4d9-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="3a4d9-137">-Confirm</span></span>
<span data-ttu-id="3a4d9-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a4d9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a4d9-139">-WhatIf</span></span>
<span data-ttu-id="3a4d9-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a4d9-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a4d9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a4d9-142">CommonParameters</span></span>
<span data-ttu-id="3a4d9-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3a4d9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a4d9-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a4d9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a4d9-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3a4d9-145">INPUTS</span></span>

### <span data-ttu-id="3a4d9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3a4d9-146">System.String</span></span>

### <span data-ttu-id="3a4d9-147">Microsoft. Azure. Commands. ServiceBus. model. PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="3a4d9-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="3a4d9-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3a4d9-148">OUTPUTS</span></span>

### <span data-ttu-id="3a4d9-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3a4d9-149">System.Boolean</span></span>

## <span data-ttu-id="3a4d9-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3a4d9-150">NOTES</span></span>

## <span data-ttu-id="3a4d9-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3a4d9-151">RELATED LINKS</span></span>
