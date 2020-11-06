---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: f2d295d31b0112a2adf73e2e4be064164df8fbb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593409"
---
# <span data-ttu-id="6d65a-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="6d65a-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="6d65a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d65a-102">SYNOPSIS</span></span>
<span data-ttu-id="6d65a-103">Belirtilen hizmet veri yolu ad boşluğundan konuyu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d65a-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d65a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d65a-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d65a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d65a-105">DESCRIPTION</span></span>
<span data-ttu-id="6d65a-106">**Remove-AzureRmServiceBusTopic** cmdlet 'i, konuyu belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6d65a-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6d65a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d65a-107">EXAMPLES</span></span>

### <span data-ttu-id="6d65a-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6d65a-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="6d65a-109">Başlığı `SB-Topic_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="6d65a-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="6d65a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d65a-110">PARAMETERS</span></span>

### <span data-ttu-id="6d65a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d65a-111">-DefaultProfile</span></span>
<span data-ttu-id="6d65a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d65a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d65a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d65a-113">-Name</span></span>
<span data-ttu-id="6d65a-114">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="6d65a-114">Topic Name.</span></span>

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

### <span data-ttu-id="6d65a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6d65a-115">-Namespace</span></span>
<span data-ttu-id="6d65a-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="6d65a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="6d65a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d65a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6d65a-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="6d65a-118">The name of the resource group</span></span>

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

### <span data-ttu-id="6d65a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6d65a-119">-Confirm</span></span>
<span data-ttu-id="6d65a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6d65a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d65a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d65a-121">-WhatIf</span></span>
<span data-ttu-id="6d65a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6d65a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d65a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6d65a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d65a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d65a-124">CommonParameters</span></span>
<span data-ttu-id="6d65a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d65a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d65a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d65a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d65a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d65a-127">INPUTS</span></span>

### <span data-ttu-id="6d65a-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6d65a-128">-ResourceGroup</span></span>
 <span data-ttu-id="6d65a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6d65a-129">System.String</span></span>

### <span data-ttu-id="6d65a-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6d65a-130">-NamespaceName</span></span>
 <span data-ttu-id="6d65a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6d65a-131">System.String</span></span>

### <span data-ttu-id="6d65a-132">-TopicName</span><span class="sxs-lookup"><span data-stu-id="6d65a-132">-TopicName</span></span>
 <span data-ttu-id="6d65a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6d65a-133">System.String</span></span>

## <span data-ttu-id="6d65a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d65a-134">OUTPUTS</span></span>

### <span data-ttu-id="6d65a-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="6d65a-135">System.Object</span></span>

## <span data-ttu-id="6d65a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d65a-136">NOTES</span></span>

## <span data-ttu-id="6d65a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d65a-137">RELATED LINKS</span></span>

