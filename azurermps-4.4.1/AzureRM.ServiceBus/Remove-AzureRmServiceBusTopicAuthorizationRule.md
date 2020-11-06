---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594177"
---
# <span data-ttu-id="3948e-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="3948e-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="3948e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3948e-102">SYNOPSIS</span></span>
<span data-ttu-id="3948e-103">Belirtilen hizmet veri yolu ad boşluğundan bir konunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3948e-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3948e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3948e-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3948e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3948e-105">DESCRIPTION</span></span>
<span data-ttu-id="3948e-106">**Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir konunun yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3948e-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="3948e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3948e-107">EXAMPLES</span></span>

### <span data-ttu-id="3948e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3948e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="3948e-109">Konu uzayındaki yetkilendirme kuralını kaldırır `SBTopicAuthoRule1` `SB-Topic_exampl1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="3948e-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="3948e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3948e-110">PARAMETERS</span></span>

### <span data-ttu-id="3948e-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3948e-111">-ResourceGroup</span></span>
<span data-ttu-id="3948e-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3948e-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="3948e-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="3948e-113">-Confirm</span></span>
<span data-ttu-id="3948e-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3948e-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3948e-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3948e-115">-WhatIf</span></span>
<span data-ttu-id="3948e-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3948e-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3948e-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3948e-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3948e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3948e-118">-DefaultProfile</span></span>
<span data-ttu-id="3948e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3948e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3948e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="3948e-120">-Name</span></span>
<span data-ttu-id="3948e-121">Konu AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="3948e-121">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="3948e-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3948e-122">-Namespace</span></span>
<span data-ttu-id="3948e-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="3948e-123">Namespace Name.</span></span>

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

### <span data-ttu-id="3948e-124">-Konu</span><span class="sxs-lookup"><span data-stu-id="3948e-124">-Topic</span></span>
<span data-ttu-id="3948e-125">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="3948e-125">Topic Name.</span></span>

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

### <span data-ttu-id="3948e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3948e-126">CommonParameters</span></span>
<span data-ttu-id="3948e-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3948e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3948e-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3948e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3948e-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3948e-129">INPUTS</span></span>

### <span data-ttu-id="3948e-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3948e-130">-ResourceGroup</span></span>
 <span data-ttu-id="3948e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3948e-131">System.String</span></span>

### <span data-ttu-id="3948e-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="3948e-132">-NamespaceName</span></span>
 <span data-ttu-id="3948e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3948e-133">System.String</span></span>

### <span data-ttu-id="3948e-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3948e-134">-TopicName</span></span>
 <span data-ttu-id="3948e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3948e-135">System.String</span></span>

### <span data-ttu-id="3948e-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="3948e-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="3948e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3948e-137">System.String</span></span>

## <span data-ttu-id="3948e-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3948e-138">OUTPUTS</span></span>

### <span data-ttu-id="3948e-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="3948e-139">System.Object</span></span>

## <span data-ttu-id="3948e-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3948e-140">NOTES</span></span>

## <span data-ttu-id="3948e-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3948e-141">RELATED LINKS</span></span>

