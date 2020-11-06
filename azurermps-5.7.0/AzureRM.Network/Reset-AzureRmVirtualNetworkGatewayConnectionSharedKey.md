---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594459"
---
# <span data-ttu-id="c036d-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c036d-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="c036d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c036d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c036d-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c036d-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c036d-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="c036d-104">DESCRIPTION</span></span>

## <span data-ttu-id="c036d-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c036d-105">EXAMPLES</span></span>

## <span data-ttu-id="c036d-106">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c036d-106">PARAMETERS</span></span>

### <span data-ttu-id="c036d-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c036d-107">-DefaultProfile</span></span>
<span data-ttu-id="c036d-108">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c036d-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c036d-109">-Force</span><span class="sxs-lookup"><span data-stu-id="c036d-109">-Force</span></span>
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

### <span data-ttu-id="c036d-110">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="c036d-110">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c036d-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="c036d-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c036d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c036d-112">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c036d-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="c036d-113">-Confirm</span></span>
<span data-ttu-id="c036d-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c036d-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c036d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c036d-115">-WhatIf</span></span>
<span data-ttu-id="c036d-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c036d-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c036d-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c036d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c036d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c036d-118">CommonParameters</span></span>
<span data-ttu-id="c036d-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c036d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c036d-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c036d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c036d-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c036d-121">INPUTS</span></span>

### <span data-ttu-id="c036d-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c036d-122">None</span></span>
<span data-ttu-id="c036d-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c036d-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c036d-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c036d-124">OUTPUTS</span></span>

### <span data-ttu-id="c036d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c036d-125">System.String</span></span>

## <span data-ttu-id="c036d-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c036d-126">NOTES</span></span>

## <span data-ttu-id="c036d-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c036d-127">RELATED LINKS</span></span>

[<span data-ttu-id="c036d-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c036d-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="c036d-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c036d-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


