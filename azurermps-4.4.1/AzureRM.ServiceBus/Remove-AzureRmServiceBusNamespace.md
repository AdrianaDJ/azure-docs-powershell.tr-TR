---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 510b6bfcaf49d406a7be2f6e4f53b2227469566d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589106"
---
# <span data-ttu-id="450b1-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="450b1-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="450b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="450b1-102">SYNOPSIS</span></span>
<span data-ttu-id="450b1-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="450b1-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="450b1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="450b1-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroup] <String> [-NamespaceName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="450b1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="450b1-105">DESCRIPTION</span></span>
<span data-ttu-id="450b1-106">**Remove-AzureRmServiceBusNamespace** cmdlet 'i belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="450b1-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="450b1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="450b1-107">EXAMPLES</span></span>

### <span data-ttu-id="450b1-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="450b1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="450b1-109">Belirtilen kaynak grubundan hizmet veri yolu ad alanını kaldırır `SB-Example1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="450b1-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="450b1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="450b1-110">PARAMETERS</span></span>

### <span data-ttu-id="450b1-111">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="450b1-111">-NamespaceName</span></span>
<span data-ttu-id="450b1-112">Hizmet veri yolu ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="450b1-112">The Service Bus namespace name.</span></span>

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

### <span data-ttu-id="450b1-113">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="450b1-113">-ResourceGroup</span></span>
<span data-ttu-id="450b1-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="450b1-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="450b1-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="450b1-115">-Confirm</span></span>
<span data-ttu-id="450b1-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="450b1-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450b1-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450b1-117">-WhatIf</span></span>
<span data-ttu-id="450b1-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="450b1-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="450b1-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="450b1-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450b1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450b1-120">CommonParameters</span></span>
<span data-ttu-id="450b1-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="450b1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450b1-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450b1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450b1-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="450b1-123">INPUTS</span></span>

### <span data-ttu-id="450b1-124">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="450b1-124">-ResourceGroup</span></span>
 <span data-ttu-id="450b1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="450b1-125">System.String</span></span>

### <span data-ttu-id="450b1-126">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="450b1-126">-NamespaceName</span></span>
 <span data-ttu-id="450b1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="450b1-127">System.String</span></span>

## <span data-ttu-id="450b1-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="450b1-128">OUTPUTS</span></span>

### <span data-ttu-id="450b1-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="450b1-129">System.Object</span></span>

## <span data-ttu-id="450b1-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="450b1-130">NOTES</span></span>

## <span data-ttu-id="450b1-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="450b1-131">RELATED LINKS</span></span>

