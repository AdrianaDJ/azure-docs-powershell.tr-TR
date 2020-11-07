---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 6e20ceb2a6809e1e6010263563006468753cd41c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764228"
---
# <span data-ttu-id="f9864-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f9864-101">New-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="f9864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9864-102">SYNOPSIS</span></span>
<span data-ttu-id="f9864-103">Belirtilen hizmet veri yolu ad alanı için yeni bir yetkilendirme kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f9864-103">Creates a new authorization rule for the specified Service Bus namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9864-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9864-104">SYNTAX</span></span>

```
New-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Name <String>
 [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9864-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9864-105">DESCRIPTION</span></span>
<span data-ttu-id="f9864-106">**New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet 'ı belirtilen hizmet veri yolu ad alanı için yeni bir yetkilendirme kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f9864-106">The **New-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f9864-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9864-107">EXAMPLES</span></span>

### <span data-ttu-id="f9864-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f9864-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="f9864-109">`AuthoRule1`Ad alanı Için **dinleme** ve **gönderme** haklarıyla oluşturulur `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f9864-109">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="f9864-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9864-110">PARAMETERS</span></span>

### <span data-ttu-id="f9864-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9864-111">-ResourceGroup</span></span>
<span data-ttu-id="f9864-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f9864-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f9864-113">-Hak</span><span class="sxs-lookup"><span data-stu-id="f9864-113">-Rights</span></span>
<span data-ttu-id="f9864-114">Haklar; Örneğin, @ ("Dinle", "Gönder", "Yönet")</span><span class="sxs-lookup"><span data-stu-id="f9864-114">The Rights; for example, @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="f9864-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9864-115">-Confirm</span></span>
<span data-ttu-id="f9864-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9864-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9864-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9864-117">-WhatIf</span></span>
<span data-ttu-id="f9864-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9864-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9864-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9864-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9864-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9864-120">-DefaultProfile</span></span>
<span data-ttu-id="f9864-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9864-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9864-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9864-122">-Name</span></span>
<span data-ttu-id="f9864-123">AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="f9864-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f9864-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f9864-124">-Namespace</span></span>
<span data-ttu-id="f9864-125">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="f9864-125">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="f9864-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9864-126">CommonParameters</span></span>
<span data-ttu-id="f9864-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9864-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9864-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9864-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9864-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9864-129">INPUTS</span></span>

### <span data-ttu-id="f9864-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f9864-130">-ResourceGroup</span></span>
 <span data-ttu-id="f9864-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f9864-131">System.String</span></span>
 

### <span data-ttu-id="f9864-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f9864-132">-NamespaceName</span></span>
 <span data-ttu-id="f9864-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f9864-133">System.String</span></span>
 

### <span data-ttu-id="f9864-134">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f9864-134">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f9864-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f9864-135">System.String</span></span>
 

### <span data-ttu-id="f9864-136">-Hak</span><span class="sxs-lookup"><span data-stu-id="f9864-136">-Rights</span></span>
 <span data-ttu-id="f9864-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="f9864-137">System.String []</span></span>

## <span data-ttu-id="f9864-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9864-138">OUTPUTS</span></span>

### <span data-ttu-id="f9864-139">Microsoft. Azure. Commands. ServiceBus. model. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f9864-139">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="f9864-140">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tür: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 location: Etiketler: haklar: {Listen, gönder}</span><span class="sxs-lookup"><span data-stu-id="f9864-140">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f9864-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9864-141">NOTES</span></span>

## <span data-ttu-id="f9864-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9864-142">RELATED LINKS</span></span>

