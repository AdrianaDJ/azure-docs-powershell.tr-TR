---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: dc75d9895d5e56f7cd7915947ff8a63ac54f2a3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590862"
---
# <span data-ttu-id="26988-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="26988-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="26988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26988-102">SYNOPSIS</span></span>
<span data-ttu-id="26988-103">Verilen bir aboneliğin spealmi kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26988-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26988-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26988-104">SYNTAX</span></span>

### <span data-ttu-id="26988-105">RulePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26988-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26988-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="26988-106">RuleResourceIdSet</span></span>
```
Remove-AzureRmServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26988-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="26988-107">DESCRIPTION</span></span>
<span data-ttu-id="26988-108">**Remove-AzureRmServiceBusRule** cmdlet 'i, verilen konunun aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="26988-108">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="26988-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26988-109">EXAMPLES</span></span>

### <span data-ttu-id="26988-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26988-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="26988-111">`SBRule` `SBSubscription` Belirtilen konu aboneliğini kaldırır `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="26988-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="26988-112">Örnek 2,1-InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="26988-112">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="26988-113">$İnputobject-InputObject parametresinde sağlanan kuralı kaldırır</span><span class="sxs-lookup"><span data-stu-id="26988-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="26988-114">Örnek 2,2-InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="26988-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzureRmServiceBusRule <params> | Remove-AzureRmServiceBusRule
```

### <span data-ttu-id="26988-115">Örnek 3,1-RESOURCEID-değişken kullanma</span><span class="sxs-lookup"><span data-stu-id="26988-115">Example 3.1 - ResourceId - Using Variable</span></span>
```
PS C:\> $resourceid = Get-AzureRmServiceBusRule <params>
PS C:\> Remove-AzureRmServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="26988-116">Örnek 3,1-RESOURCEID-dize değeri kullanma</span><span class="sxs-lookup"><span data-stu-id="26988-116">Example 3.1 - ResourceId - Using string value</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="26988-117">$Resourceid/String for-RESOURCEID parametresindeki ARM kimliği aracılığıyla sağlanan kuralı kaldırır</span><span class="sxs-lookup"><span data-stu-id="26988-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="26988-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26988-118">PARAMETERS</span></span>

### <span data-ttu-id="26988-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="26988-119">-AsJob</span></span>
<span data-ttu-id="26988-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="26988-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26988-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26988-121">-DefaultProfile</span></span>
<span data-ttu-id="26988-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26988-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26988-123">-Force</span><span class="sxs-lookup"><span data-stu-id="26988-123">-Force</span></span>
<span data-ttu-id="26988-124">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="26988-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="26988-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26988-125">-InputObject</span></span>
<span data-ttu-id="26988-126">Hizmet veri yolu kuralı nesnesi</span><span class="sxs-lookup"><span data-stu-id="26988-126">Service Bus Rule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26988-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="26988-127">-Name</span></span>
<span data-ttu-id="26988-128">Kural adı</span><span class="sxs-lookup"><span data-stu-id="26988-128">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26988-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="26988-129">-Namespace</span></span>
<span data-ttu-id="26988-130">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="26988-130">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26988-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="26988-131">-PassThru</span></span>
<span data-ttu-id="26988-132">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="26988-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="26988-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26988-133">-ResourceGroupName</span></span>
<span data-ttu-id="26988-134">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="26988-134">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26988-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="26988-135">-ResourceId</span></span>
<span data-ttu-id="26988-136">Hizmet veri yolu kuralı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="26988-136">Service Bus Rule Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: RuleResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26988-137">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="26988-137">-Subscription</span></span>
<span data-ttu-id="26988-138">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="26988-138">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26988-139">-Konu</span><span class="sxs-lookup"><span data-stu-id="26988-139">-Topic</span></span>
<span data-ttu-id="26988-140">Konu adı</span><span class="sxs-lookup"><span data-stu-id="26988-140">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: RulePropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26988-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="26988-141">-Confirm</span></span>
<span data-ttu-id="26988-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26988-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26988-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26988-143">-WhatIf</span></span>
<span data-ttu-id="26988-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26988-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26988-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26988-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26988-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26988-146">CommonParameters</span></span>
<span data-ttu-id="26988-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26988-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26988-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26988-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26988-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26988-149">INPUTS</span></span>

### <span data-ttu-id="26988-150">System. String</span><span class="sxs-lookup"><span data-stu-id="26988-150">System.String</span></span>

### <span data-ttu-id="26988-151">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="26988-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>
<span data-ttu-id="26988-152">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="26988-152">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="26988-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26988-153">OUTPUTS</span></span>

### <span data-ttu-id="26988-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26988-154">System.Boolean</span></span>

## <span data-ttu-id="26988-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26988-155">NOTES</span></span>

## <span data-ttu-id="26988-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26988-156">RELATED LINKS</span></span>
