---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936589"
---
# <span data-ttu-id="7ebc1-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7ebc1-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="7ebc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ebc1-102">SYNOPSIS</span></span>

## <span data-ttu-id="7ebc1-103">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ebc1-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ebc1-104">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ebc1-104">DESCRIPTION</span></span>

## <span data-ttu-id="7ebc1-105">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ebc1-105">EXAMPLES</span></span>

### <span data-ttu-id="7ebc1-106">2</span><span class="sxs-lookup"><span data-stu-id="7ebc1-106">1:</span></span>
```

```

## <span data-ttu-id="7ebc1-107">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ebc1-107">PARAMETERS</span></span>

### <span data-ttu-id="7ebc1-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ebc1-108">-DefaultProfile</span></span>
<span data-ttu-id="7ebc1-109">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ebc1-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ebc1-110">-Force</span><span class="sxs-lookup"><span data-stu-id="7ebc1-110">-Force</span></span>
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

### <span data-ttu-id="7ebc1-111">-KeyLength</span><span class="sxs-lookup"><span data-stu-id="7ebc1-111">-KeyLength</span></span>
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

### <span data-ttu-id="7ebc1-112">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ebc1-112">-Name</span></span>
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

### <span data-ttu-id="7ebc1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ebc1-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7ebc1-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ebc1-114">-Confirm</span></span>
<span data-ttu-id="7ebc1-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ebc1-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ebc1-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ebc1-116">-WhatIf</span></span>
<span data-ttu-id="7ebc1-117">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ebc1-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ebc1-118">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ebc1-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ebc1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ebc1-119">CommonParameters</span></span>
<span data-ttu-id="7ebc1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ebc1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ebc1-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ebc1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ebc1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ebc1-122">INPUTS</span></span>

## <span data-ttu-id="7ebc1-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ebc1-123">OUTPUTS</span></span>

### <span data-ttu-id="7ebc1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7ebc1-124">System.String</span></span>

## <span data-ttu-id="7ebc1-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ebc1-125">NOTES</span></span>

## <span data-ttu-id="7ebc1-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ebc1-126">RELATED LINKS</span></span>

[<span data-ttu-id="7ebc1-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7ebc1-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="7ebc1-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="7ebc1-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


