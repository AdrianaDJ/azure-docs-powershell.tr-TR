---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594170"
---
# <span data-ttu-id="a5e33-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a5e33-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="a5e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e33-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e33-103">Verilen hizmet veri yolu kuyruğu için belirtilen yetkilendirme kuralı açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5e33-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5e33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5e33-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5e33-105">DESCRIPTION</span></span>
<span data-ttu-id="a5e33-106">**Set-Azurermservicebusiauthorizationrule** cmdlet 'i, verilen hizmet veri yolu sırasının belirtilen yetkilendirme kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="a5e33-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="a5e33-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5e33-107">EXAMPLES</span></span>

### <span data-ttu-id="a5e33-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a5e33-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="a5e33-109">Kuyruktaki yetkilendirme kuralının erişim haklarına **Yönet** ekler `SBAuthoRule1` `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="a5e33-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="a5e33-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5e33-110">PARAMETERS</span></span>

### <span data-ttu-id="a5e33-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a5e33-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="a5e33-112">Yetkilendirme kuralı adı.</span><span class="sxs-lookup"><span data-stu-id="a5e33-112">The authorization rule name.</span></span> <span data-ttu-id="a5e33-113">Gerekli Eğer **-authruleobj** belirtilmemişse.</span><span class="sxs-lookup"><span data-stu-id="a5e33-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e33-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="a5e33-114">-AuthRuleObj</span></span>
<span data-ttu-id="a5e33-115">Hizmet yol sırası yetkilendirme kuralı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a5e33-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e33-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a5e33-116">-NamespaceName</span></span>
<span data-ttu-id="a5e33-117">Hizmet veri yolu ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="a5e33-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e33-118">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="a5e33-118">-QueueName</span></span>
<span data-ttu-id="a5e33-119">Hizmet veri yolu sıra adı.</span><span class="sxs-lookup"><span data-stu-id="a5e33-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e33-120">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5e33-120">-ResourceGroup</span></span>
<span data-ttu-id="a5e33-121">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a5e33-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="a5e33-122">-Hak</span><span class="sxs-lookup"><span data-stu-id="a5e33-122">-Rights</span></span>
<span data-ttu-id="a5e33-123">Haklar; Örneğin @ ("Dinle", "Gönder", "Yönet").</span><span class="sxs-lookup"><span data-stu-id="a5e33-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="a5e33-124">' AuthruleObj ' belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="a5e33-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e33-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5e33-125">-Confirm</span></span>
<span data-ttu-id="a5e33-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5e33-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e33-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e33-127">-WhatIf</span></span>
<span data-ttu-id="a5e33-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5e33-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e33-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5e33-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e33-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e33-130">CommonParameters</span></span>
<span data-ttu-id="a5e33-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5e33-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e33-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5e33-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e33-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5e33-133">INPUTS</span></span>

### <span data-ttu-id="a5e33-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a5e33-134">-ResourceGroup</span></span>
 <span data-ttu-id="a5e33-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e33-135">System.String</span></span>

### <span data-ttu-id="a5e33-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a5e33-136">-NamespaceName</span></span>
 <span data-ttu-id="a5e33-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e33-137">System.String</span></span>

### <span data-ttu-id="a5e33-138">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="a5e33-138">-QueueName</span></span>
 <span data-ttu-id="a5e33-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a5e33-139">System.String</span></span>

### <span data-ttu-id="a5e33-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="a5e33-140">-AuthRuleObj</span></span>
 <span data-ttu-id="a5e33-141">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a5e33-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a5e33-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5e33-142">OUTPUTS</span></span>

### <span data-ttu-id="a5e33-143">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a5e33-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a5e33-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5e33-144">NOTES</span></span>

## <span data-ttu-id="a5e33-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5e33-145">RELATED LINKS</span></span>

