---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762837"
---
# <span data-ttu-id="30972-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="30972-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="30972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30972-102">SYNOPSIS</span></span>
<span data-ttu-id="30972-103">Belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30972-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30972-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="30972-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30972-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="30972-105">DESCRIPTION</span></span>
<span data-ttu-id="30972-106">**Remove-AzureRmServiceBusNamespace** cmdlet 'i belirtilen kaynak grubundan ad alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="30972-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="30972-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="30972-107">EXAMPLES</span></span>

### <span data-ttu-id="30972-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="30972-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="30972-109">Belirtilen kaynak grubundan hizmet veri yolu ad alanını kaldırır `SB-Example1` `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="30972-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="30972-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="30972-110">PARAMETERS</span></span>

### <span data-ttu-id="30972-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30972-111">-DefaultProfile</span></span>
<span data-ttu-id="30972-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="30972-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30972-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="30972-113">-Name</span></span>
<span data-ttu-id="30972-114">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="30972-114">Namespace Name.</span></span>

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

### <span data-ttu-id="30972-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30972-115">-ResourceGroupName</span></span>
<span data-ttu-id="30972-116">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="30972-116">The name of the resource group</span></span>

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

### <span data-ttu-id="30972-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="30972-117">-Confirm</span></span>
<span data-ttu-id="30972-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="30972-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30972-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30972-119">-WhatIf</span></span>
<span data-ttu-id="30972-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="30972-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30972-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="30972-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30972-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30972-122">CommonParameters</span></span>
<span data-ttu-id="30972-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="30972-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30972-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30972-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30972-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="30972-125">INPUTS</span></span>

### <span data-ttu-id="30972-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30972-126">-ResourceGroup</span></span>
 <span data-ttu-id="30972-127">System. String</span><span class="sxs-lookup"><span data-stu-id="30972-127">System.String</span></span>

### <span data-ttu-id="30972-128">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="30972-128">-NamespaceName</span></span>
 <span data-ttu-id="30972-129">System. String</span><span class="sxs-lookup"><span data-stu-id="30972-129">System.String</span></span>

## <span data-ttu-id="30972-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="30972-130">OUTPUTS</span></span>

### <span data-ttu-id="30972-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="30972-131">System.Object</span></span>

## <span data-ttu-id="30972-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="30972-132">NOTES</span></span>

## <span data-ttu-id="30972-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="30972-133">RELATED LINKS</span></span>

