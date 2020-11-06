---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591605"
---
# <span data-ttu-id="cb19f-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="cb19f-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="cb19f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb19f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb19f-103">Verilen bir aboneliğin spealmi kuralını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb19f-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb19f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb19f-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb19f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb19f-105">DESCRIPTION</span></span>
<span data-ttu-id="cb19f-106">**Remove-AzureRmServiceBusRule** cmdlet 'i, verilen konunun aboneliğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cb19f-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="cb19f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb19f-107">EXAMPLES</span></span>

### <span data-ttu-id="cb19f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb19f-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="cb19f-109">`SBRule` `SBSubscription` Belirtilen konu aboneliğini kaldırır `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="cb19f-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="cb19f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb19f-110">PARAMETERS</span></span>

### <span data-ttu-id="cb19f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb19f-111">-DefaultProfile</span></span>
<span data-ttu-id="cb19f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb19f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cb19f-113">-Force</span></span>
<span data-ttu-id="cb19f-114">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="cb19f-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb19f-115">-Name</span></span>
<span data-ttu-id="cb19f-116">Kural adı.</span><span class="sxs-lookup"><span data-stu-id="cb19f-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cb19f-117">-Namespace</span></span>
<span data-ttu-id="cb19f-118">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="cb19f-118">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cb19f-119">-PassThru</span></span>
<span data-ttu-id="cb19f-120">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="cb19f-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb19f-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb19f-122">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="cb19f-122">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-123">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="cb19f-123">-Subscription</span></span>
<span data-ttu-id="cb19f-124">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="cb19f-124">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-125">-Konu</span><span class="sxs-lookup"><span data-stu-id="cb19f-125">-Topic</span></span>
<span data-ttu-id="cb19f-126">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="cb19f-126">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb19f-127">-Confirm</span></span>
<span data-ttu-id="cb19f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb19f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb19f-129">-WhatIf</span></span>
<span data-ttu-id="cb19f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb19f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb19f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb19f-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb19f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb19f-132">CommonParameters</span></span>
<span data-ttu-id="cb19f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb19f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb19f-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb19f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb19f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb19f-135">INPUTS</span></span>

### <span data-ttu-id="cb19f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb19f-136">System.String</span></span>

## <span data-ttu-id="cb19f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb19f-137">OUTPUTS</span></span>

### <span data-ttu-id="cb19f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb19f-138">System.Boolean</span></span>

## <span data-ttu-id="cb19f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb19f-139">NOTES</span></span>

## <span data-ttu-id="cb19f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb19f-140">RELATED LINKS</span></span>

