---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589104"
---
# <span data-ttu-id="2ef22-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="2ef22-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="2ef22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ef22-102">SYNOPSIS</span></span>
<span data-ttu-id="2ef22-103">Belirtilen hizmet veri yolu ad alanından bir sıranın yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ef22-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ef22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2ef22-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ef22-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2ef22-105">DESCRIPTION</span></span>
<span data-ttu-id="2ef22-106">**Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet 'i, belirtilen hizmet veri yolu ad alanındaki bir sıranın yetkilendirme kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="2ef22-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2ef22-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2ef22-107">EXAMPLES</span></span>

### <span data-ttu-id="2ef22-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2ef22-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="2ef22-109">Sıranın yetkilendirme kuralını `SBAuthoRule1` `SB-Queue_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="2ef22-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="2ef22-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2ef22-110">PARAMETERS</span></span>

### <span data-ttu-id="2ef22-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2ef22-111">-ResourceGroup</span></span>
<span data-ttu-id="2ef22-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2ef22-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="2ef22-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="2ef22-113">-Confirm</span></span>
<span data-ttu-id="2ef22-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2ef22-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ef22-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ef22-115">-WhatIf</span></span>
<span data-ttu-id="2ef22-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2ef22-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ef22-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2ef22-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ef22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ef22-118">-DefaultProfile</span></span>
<span data-ttu-id="2ef22-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2ef22-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ef22-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="2ef22-120">-Name</span></span>
<span data-ttu-id="2ef22-121">Sıra AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="2ef22-121">Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="2ef22-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2ef22-122">-Namespace</span></span>
<span data-ttu-id="2ef22-123">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="2ef22-123">Namespace Name.</span></span>

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

### <span data-ttu-id="2ef22-124">-Sıra</span><span class="sxs-lookup"><span data-stu-id="2ef22-124">-Queue</span></span>
<span data-ttu-id="2ef22-125">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="2ef22-125">Queue Name.</span></span>

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

### <span data-ttu-id="2ef22-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ef22-126">CommonParameters</span></span>
<span data-ttu-id="2ef22-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2ef22-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ef22-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ef22-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ef22-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2ef22-129">INPUTS</span></span>

### <span data-ttu-id="2ef22-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2ef22-130">-ResourceGroup</span></span>
 <span data-ttu-id="2ef22-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2ef22-131">System.String</span></span>

### <span data-ttu-id="2ef22-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="2ef22-132">-NamespaceName</span></span>
 <span data-ttu-id="2ef22-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2ef22-133">System.String</span></span>

### <span data-ttu-id="2ef22-134">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="2ef22-134">-QueueName</span></span>
 <span data-ttu-id="2ef22-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2ef22-135">System.String</span></span>

### <span data-ttu-id="2ef22-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="2ef22-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="2ef22-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2ef22-137">System.String</span></span>

## <span data-ttu-id="2ef22-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2ef22-138">OUTPUTS</span></span>

### <span data-ttu-id="2ef22-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="2ef22-139">System.Object</span></span>

## <span data-ttu-id="2ef22-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2ef22-140">NOTES</span></span>

## <span data-ttu-id="2ef22-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2ef22-141">RELATED LINKS</span></span>

