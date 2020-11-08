---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940024"
---
# <span data-ttu-id="8a4cc-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8a4cc-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="8a4cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a4cc-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a4cc-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8a4cc-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a4cc-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="8a4cc-104">DESCRIPTION</span></span>

## <span data-ttu-id="8a4cc-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8a4cc-105">EXAMPLES</span></span>

### <span data-ttu-id="8a4cc-106">2</span><span class="sxs-lookup"><span data-stu-id="8a4cc-106">1:</span></span>
```

```

## <span data-ttu-id="8a4cc-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8a4cc-107">PARAMETERS</span></span>

### <span data-ttu-id="8a4cc-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4cc-108">-DefaultProfile</span></span>
<span data-ttu-id="8a4cc-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8a4cc-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a4cc-110">-Force</span><span class="sxs-lookup"><span data-stu-id="8a4cc-110">-Force</span></span>
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

### <span data-ttu-id="8a4cc-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="8a4cc-111">-KeyLength</span></span>
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

### <span data-ttu-id="8a4cc-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="8a4cc-112">-Name</span></span>
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

### <span data-ttu-id="8a4cc-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a4cc-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8a4cc-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="8a4cc-114">-Confirm</span></span>
<span data-ttu-id="8a4cc-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8a4cc-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a4cc-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a4cc-116">-WhatIf</span></span>
<span data-ttu-id="8a4cc-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8a4cc-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a4cc-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8a4cc-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a4cc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4cc-119">CommonParameters</span></span>
<span data-ttu-id="8a4cc-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8a4cc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a4cc-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a4cc-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4cc-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8a4cc-122">INPUTS</span></span>

## <span data-ttu-id="8a4cc-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8a4cc-123">OUTPUTS</span></span>

### <span data-ttu-id="8a4cc-124">System. String</span><span class="sxs-lookup"><span data-stu-id="8a4cc-124">System.String</span></span>

## <span data-ttu-id="8a4cc-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8a4cc-125">NOTES</span></span>

## <span data-ttu-id="8a4cc-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8a4cc-126">RELATED LINKS</span></span>

[<span data-ttu-id="8a4cc-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8a4cc-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="8a4cc-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8a4cc-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

