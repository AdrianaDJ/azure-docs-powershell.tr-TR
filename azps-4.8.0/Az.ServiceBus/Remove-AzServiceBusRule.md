---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusRule.md
ms.openlocfilehash: a3fc0d37e48ddeba41b6870edfe1732eeecfaa14
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107610"
---
# <span data-ttu-id="a7cf5-101">Remove-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="a7cf5-101">Remove-AzServiceBusRule</span></span>

## <span data-ttu-id="a7cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="a7cf5-103">Belirli bir aboneliğin belirtilen kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-103">Removes the specified rule of a given subscription .</span></span>

## <span data-ttu-id="a7cf5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7cf5-104">SYNTAX</span></span>

### <span data-ttu-id="a7cf5-105">RulePropertiesSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7cf5-105">RulePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7cf5-106">RuleResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a7cf5-106">RuleResourceIdSet</span></span>
```
Remove-AzServiceBusRule [-InputObject] <PSTopicAttributes> [-ResourceId] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7cf5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7cf5-107">DESCRIPTION</span></span>
<span data-ttu-id="a7cf5-108">**Remove-AzServiceBusRule** cmdlet 'i, verilen konunun aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-108">The **Remove-AzServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="a7cf5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7cf5-109">EXAMPLES</span></span>

### <span data-ttu-id="a7cf5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7cf5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="a7cf5-111">`SBRule` `SBSubscription` Belirtilen konu aboneliğini kaldırır `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="a7cf5-111">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

### <span data-ttu-id="a7cf5-112">Örnek 2: InputObject-değişken kullanan:</span><span class="sxs-lookup"><span data-stu-id="a7cf5-112">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -InputObject $inputobject
```

<span data-ttu-id="a7cf5-113">$İnputobject-InputObject parametresinde sağlanan kuralı kaldırır</span><span class="sxs-lookup"><span data-stu-id="a7cf5-113">Removes the rule provided through $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="a7cf5-114">Örnek 3: InputObject-boru kullanarak:</span><span class="sxs-lookup"><span data-stu-id="a7cf5-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusRule <params> | Remove-AzServiceBusRule
```

### <span data-ttu-id="a7cf5-115">Örnek 4: RESOURCEID-değişken kullanma</span><span class="sxs-lookup"><span data-stu-id="a7cf5-115">Example 4: ResourceId - Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusRule <params>
PS C:\> Remove-AzServiceBusRule -ResourceId $resourceid.Id
```

### <span data-ttu-id="a7cf5-116">Örnek 5: RESOURCEID-dize değeri kullanma</span><span class="sxs-lookup"><span data-stu-id="a7cf5-116">Example 5: ResourceId - Using string value</span></span>
```powershell
PS C:\> Remove-AzServiceBusRule -ResourceId "/subscriptions/xxx-xxxxx-xxxxxx-xxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName/rules/RuleName"
```

<span data-ttu-id="a7cf5-117">$Resourceid/String for-RESOURCEID parametresindeki ARM kimliği aracılığıyla sağlanan kuralı kaldırır</span><span class="sxs-lookup"><span data-stu-id="a7cf5-117">Removes the rule provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="a7cf5-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7cf5-118">PARAMETERS</span></span>

### <span data-ttu-id="a7cf5-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="a7cf5-119">-AsJob</span></span>
<span data-ttu-id="a7cf5-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a7cf5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7cf5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7cf5-121">-DefaultProfile</span></span>
<span data-ttu-id="a7cf5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7cf5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a7cf5-123">-Force</span></span>
<span data-ttu-id="a7cf5-124">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a7cf5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7cf5-125">-InputObject</span></span>
<span data-ttu-id="a7cf5-126">Hizmet veri yolu kuralı nesnesi</span><span class="sxs-lookup"><span data-stu-id="a7cf5-126">Service Bus Rule Object</span></span>

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

### <span data-ttu-id="a7cf5-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7cf5-127">-Name</span></span>
<span data-ttu-id="a7cf5-128">Kural adı</span><span class="sxs-lookup"><span data-stu-id="a7cf5-128">Rule Name</span></span>

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

### <span data-ttu-id="a7cf5-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a7cf5-129">-Namespace</span></span>
<span data-ttu-id="a7cf5-130">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="a7cf5-130">Namespace Name</span></span>

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

### <span data-ttu-id="a7cf5-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7cf5-131">-PassThru</span></span>
<span data-ttu-id="a7cf5-132">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a7cf5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7cf5-133">-ResourceGroupName</span></span>
<span data-ttu-id="a7cf5-134">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a7cf5-134">The name of the resource group</span></span>

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

### <span data-ttu-id="a7cf5-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7cf5-135">-ResourceId</span></span>
<span data-ttu-id="a7cf5-136">Hizmet veri yolu kuralı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a7cf5-136">Service Bus Rule Resource Id</span></span>

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

### <span data-ttu-id="a7cf5-137">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="a7cf5-137">-Subscription</span></span>
<span data-ttu-id="a7cf5-138">Abonelik adı</span><span class="sxs-lookup"><span data-stu-id="a7cf5-138">Subscription Name</span></span>

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

### <span data-ttu-id="a7cf5-139">-Konu</span><span class="sxs-lookup"><span data-stu-id="a7cf5-139">-Topic</span></span>
<span data-ttu-id="a7cf5-140">Konu adı</span><span class="sxs-lookup"><span data-stu-id="a7cf5-140">Topic Name</span></span>

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

### <span data-ttu-id="a7cf5-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7cf5-141">-Confirm</span></span>
<span data-ttu-id="a7cf5-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7cf5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7cf5-143">-WhatIf</span></span>
<span data-ttu-id="a7cf5-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7cf5-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7cf5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7cf5-146">CommonParameters</span></span>
<span data-ttu-id="a7cf5-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7cf5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7cf5-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7cf5-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7cf5-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7cf5-149">INPUTS</span></span>

### <span data-ttu-id="a7cf5-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a7cf5-150">System.String</span></span>

### <span data-ttu-id="a7cf5-151">Microsoft. Azure. Commands. ServiceBus. model. PSTopicAttributes öznitelikleri</span><span class="sxs-lookup"><span data-stu-id="a7cf5-151">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="a7cf5-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7cf5-152">OUTPUTS</span></span>

### <span data-ttu-id="a7cf5-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7cf5-153">System.Boolean</span></span>

## <span data-ttu-id="a7cf5-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7cf5-154">NOTES</span></span>

## <span data-ttu-id="a7cf5-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7cf5-155">RELATED LINKS</span></span>
