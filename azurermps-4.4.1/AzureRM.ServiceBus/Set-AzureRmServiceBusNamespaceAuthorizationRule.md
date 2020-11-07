---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764516"
---
# <span data-ttu-id="ce44f-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ce44f-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="ce44f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce44f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce44f-103">Verilen hizmet veri yolu ad alanı için belirtilen yetkilendirme kuralı açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ce44f-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce44f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce44f-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce44f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce44f-105">DESCRIPTION</span></span>
<span data-ttu-id="ce44f-106">**Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet 'i, verilen hizmet veri yolu ad alanında belirtilen yetkilendirme kuralının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="ce44f-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="ce44f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce44f-107">EXAMPLES</span></span>

### <span data-ttu-id="ce44f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ce44f-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="ce44f-109">Ad alanındaki yetkilendirme kuralının erişim haklarıyla **yönetimi** kaldırır `AuthoRule1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ce44f-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="ce44f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce44f-110">PARAMETERS</span></span>

### <span data-ttu-id="ce44f-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ce44f-111">-ResourceGroup</span></span>
<span data-ttu-id="ce44f-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ce44f-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="ce44f-113">-Hak</span><span class="sxs-lookup"><span data-stu-id="ce44f-113">-Rights</span></span>
<span data-ttu-id="ce44f-114">Larım Örneğin @ ("Dinle", "Gönder", "Yönet").</span><span class="sxs-lookup"><span data-stu-id="ce44f-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="ce44f-115">**Authruleobj** belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ce44f-115">Required if **AuthruleObj** is not specified.</span></span>

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

### <span data-ttu-id="ce44f-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce44f-116">-Confirm</span></span>
<span data-ttu-id="ce44f-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce44f-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce44f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce44f-118">-WhatIf</span></span>
<span data-ttu-id="ce44f-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce44f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce44f-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce44f-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce44f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce44f-121">-DefaultProfile</span></span>
<span data-ttu-id="ce44f-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ce44f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce44f-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="ce44f-123">-InputObj</span></span>
<span data-ttu-id="ce44f-124">ServiceBus ad alanı AuthorizationRule nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ce44f-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="ce44f-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ce44f-125">-Name</span></span>
<span data-ttu-id="ce44f-126">AuthorizationRule Name-' AuthruleObj ' belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="ce44f-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

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

### <span data-ttu-id="ce44f-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ce44f-127">-Namespace</span></span>
<span data-ttu-id="ce44f-128">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="ce44f-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="ce44f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce44f-129">CommonParameters</span></span>
<span data-ttu-id="ce44f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce44f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce44f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce44f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce44f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce44f-132">INPUTS</span></span>

### <span data-ttu-id="ce44f-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ce44f-133">-ResourceGroup</span></span>
 <span data-ttu-id="ce44f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ce44f-134">System.String</span></span>

### <span data-ttu-id="ce44f-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ce44f-135">-NamespaceName</span></span>
 <span data-ttu-id="ce44f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ce44f-136">System.String</span></span>

### <span data-ttu-id="ce44f-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="ce44f-137">-AuthRuleObj</span></span>
 <span data-ttu-id="ce44f-138">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ce44f-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ce44f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce44f-139">OUTPUTS</span></span>

### <span data-ttu-id="ce44f-140">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ce44f-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="ce44f-141">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 location: Etiketler: haklar: {Listen, gönder}</span><span class="sxs-lookup"><span data-stu-id="ce44f-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="ce44f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce44f-142">NOTES</span></span>

## <span data-ttu-id="ce44f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce44f-143">RELATED LINKS</span></span>

