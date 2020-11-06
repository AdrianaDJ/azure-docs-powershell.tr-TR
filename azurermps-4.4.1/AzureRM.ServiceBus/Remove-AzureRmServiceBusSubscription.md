---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589100"
---
# <span data-ttu-id="462c7-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="462c7-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="462c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="462c7-102">SYNOPSIS</span></span>
<span data-ttu-id="462c7-103">Belirtilen hizmet veri yolu ad alanından bir konuya aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="462c7-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="462c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="462c7-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="462c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="462c7-105">DESCRIPTION</span></span>
<span data-ttu-id="462c7-106">**Remove-AzureRmServiceBusSubscription** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir konuya aboneliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="462c7-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="462c7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="462c7-107">EXAMPLES</span></span>

### <span data-ttu-id="462c7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="462c7-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="462c7-109">`SB-TopicSubscription-Example1` `SB-Topic_exampl1` Belirtilen hizmet veri yolu ad alanındaki konuya aboneliği kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="462c7-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="462c7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="462c7-110">PARAMETERS</span></span>

### <span data-ttu-id="462c7-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="462c7-111">-Confirm</span></span>
<span data-ttu-id="462c7-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="462c7-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="462c7-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="462c7-113">-WhatIf</span></span>
<span data-ttu-id="462c7-114">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="462c7-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="462c7-115">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="462c7-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="462c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="462c7-116">-DefaultProfile</span></span>
<span data-ttu-id="462c7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="462c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="462c7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="462c7-118">-Name</span></span>
<span data-ttu-id="462c7-119">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="462c7-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462c7-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="462c7-120">-Namespace</span></span>
<span data-ttu-id="462c7-121">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="462c7-121">Namespace Name.</span></span>

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

### <span data-ttu-id="462c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="462c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="462c7-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="462c7-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="462c7-124">-Konu</span><span class="sxs-lookup"><span data-stu-id="462c7-124">-Topic</span></span>
<span data-ttu-id="462c7-125">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="462c7-125">Topic Name.</span></span>

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

### <span data-ttu-id="462c7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="462c7-126">CommonParameters</span></span>
<span data-ttu-id="462c7-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="462c7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="462c7-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="462c7-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="462c7-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="462c7-129">INPUTS</span></span>

### <span data-ttu-id="462c7-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="462c7-130">-ResourceGroup</span></span>
 <span data-ttu-id="462c7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="462c7-131">System.String</span></span>

### <span data-ttu-id="462c7-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="462c7-132">-NamespaceName</span></span>
 <span data-ttu-id="462c7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="462c7-133">System.String</span></span>

### <span data-ttu-id="462c7-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="462c7-134">-TopicName</span></span>
 <span data-ttu-id="462c7-135">System. String</span><span class="sxs-lookup"><span data-stu-id="462c7-135">System.String</span></span>

### <span data-ttu-id="462c7-136">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="462c7-136">-SubscriptionName</span></span>
 <span data-ttu-id="462c7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="462c7-137">System.String</span></span>

## <span data-ttu-id="462c7-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="462c7-138">OUTPUTS</span></span>

### <span data-ttu-id="462c7-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="462c7-139">System.Boolean</span></span>

## <span data-ttu-id="462c7-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="462c7-140">NOTES</span></span>

## <span data-ttu-id="462c7-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="462c7-141">RELATED LINKS</span></span>

