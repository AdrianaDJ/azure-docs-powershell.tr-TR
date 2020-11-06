---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591604"
---
# <span data-ttu-id="14925-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="14925-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="14925-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14925-102">SYNOPSIS</span></span>
<span data-ttu-id="14925-103">Sırayı belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="14925-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14925-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14925-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14925-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="14925-105">DESCRIPTION</span></span>
<span data-ttu-id="14925-106">**Remove-AzureRmServiceBusQueue** cmdlet 'i, sırayı belirtilen hizmet veri yolu ad alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="14925-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="14925-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14925-107">EXAMPLES</span></span>

### <span data-ttu-id="14925-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="14925-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="14925-109">Sırayı `SB-Queue_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="14925-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="14925-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14925-110">PARAMETERS</span></span>

### <span data-ttu-id="14925-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14925-111">-DefaultProfile</span></span>
<span data-ttu-id="14925-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14925-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14925-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="14925-113">-Name</span></span>
<span data-ttu-id="14925-114">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="14925-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14925-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="14925-115">-Namespace</span></span>
<span data-ttu-id="14925-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="14925-116">Namespace Name.</span></span>

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

### <span data-ttu-id="14925-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14925-117">-ResourceGroupName</span></span>
<span data-ttu-id="14925-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="14925-118">The name of the resource group</span></span>

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

### <span data-ttu-id="14925-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="14925-119">-Confirm</span></span>
<span data-ttu-id="14925-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14925-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14925-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14925-121">-WhatIf</span></span>
<span data-ttu-id="14925-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14925-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14925-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14925-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14925-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14925-124">CommonParameters</span></span>
<span data-ttu-id="14925-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14925-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14925-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14925-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14925-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14925-127">INPUTS</span></span>

### <span data-ttu-id="14925-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="14925-128">-ResourceGroup</span></span>
 <span data-ttu-id="14925-129">System. String</span><span class="sxs-lookup"><span data-stu-id="14925-129">System.String</span></span>

### <span data-ttu-id="14925-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="14925-130">-NamespaceName</span></span>
 <span data-ttu-id="14925-131">System. String</span><span class="sxs-lookup"><span data-stu-id="14925-131">System.String</span></span>

### <span data-ttu-id="14925-132">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="14925-132">-QueueName</span></span>
 <span data-ttu-id="14925-133">System. String</span><span class="sxs-lookup"><span data-stu-id="14925-133">System.String</span></span>

## <span data-ttu-id="14925-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14925-134">OUTPUTS</span></span>

### <span data-ttu-id="14925-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="14925-135">System.Object</span></span>

## <span data-ttu-id="14925-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14925-136">NOTES</span></span>

## <span data-ttu-id="14925-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14925-137">RELATED LINKS</span></span>

