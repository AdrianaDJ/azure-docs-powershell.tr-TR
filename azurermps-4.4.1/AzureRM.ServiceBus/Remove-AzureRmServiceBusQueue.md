---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c5c614a041ff0e4ab9bc4fdc0aea944901d1efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589103"
---
# <span data-ttu-id="1f372-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="1f372-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="1f372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f372-102">SYNOPSIS</span></span>
<span data-ttu-id="1f372-103">Sırayı belirtilen hizmet veri yolu ad boşluğundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1f372-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f372-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f372-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f372-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f372-105">DESCRIPTION</span></span>
<span data-ttu-id="1f372-106">**Remove-AzureRmServiceBusQueue** cmdlet 'i, sırayı belirtilen hizmet veri yolu ad alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1f372-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1f372-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f372-107">EXAMPLES</span></span>

### <span data-ttu-id="1f372-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f372-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="1f372-109">Sırayı `SB-Queue_exampl1` ad alanından kaldırır `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="1f372-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="1f372-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f372-110">PARAMETERS</span></span>

### <span data-ttu-id="1f372-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="1f372-111">-Confirm</span></span>
<span data-ttu-id="1f372-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1f372-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f372-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f372-113">-WhatIf</span></span>
<span data-ttu-id="1f372-114">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1f372-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f372-115">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1f372-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f372-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f372-116">-DefaultProfile</span></span>
<span data-ttu-id="1f372-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f372-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f372-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f372-118">-Name</span></span>
<span data-ttu-id="1f372-119">Sıra adı.</span><span class="sxs-lookup"><span data-stu-id="1f372-119">Queue Name.</span></span>

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

### <span data-ttu-id="1f372-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1f372-120">-Namespace</span></span>
<span data-ttu-id="1f372-121">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="1f372-121">Namespace Name.</span></span>

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

### <span data-ttu-id="1f372-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f372-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f372-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="1f372-123">The name of the resource group</span></span>

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

### <span data-ttu-id="1f372-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f372-124">CommonParameters</span></span>
<span data-ttu-id="1f372-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f372-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f372-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f372-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f372-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f372-127">INPUTS</span></span>

### <span data-ttu-id="1f372-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1f372-128">-ResourceGroup</span></span>
 <span data-ttu-id="1f372-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1f372-129">System.String</span></span>

### <span data-ttu-id="1f372-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="1f372-130">-NamespaceName</span></span>
 <span data-ttu-id="1f372-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1f372-131">System.String</span></span>

### <span data-ttu-id="1f372-132">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="1f372-132">-QueueName</span></span>
 <span data-ttu-id="1f372-133">System. String</span><span class="sxs-lookup"><span data-stu-id="1f372-133">System.String</span></span>

## <span data-ttu-id="1f372-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f372-134">OUTPUTS</span></span>

### <span data-ttu-id="1f372-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="1f372-135">System.Object</span></span>

## <span data-ttu-id="1f372-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f372-136">NOTES</span></span>

## <span data-ttu-id="1f372-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f372-137">RELATED LINKS</span></span>

