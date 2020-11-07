---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: be59f9ec0728b60314f137dcc5a57c7883935e52
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939687"
---
# <span data-ttu-id="06f90-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="06f90-101">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="06f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06f90-102">SYNOPSIS</span></span>
<span data-ttu-id="06f90-103">Sanal Ağ Geçidi bağlantısının paylaşılan anahtarını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="06f90-103">Configures the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06f90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06f90-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06f90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06f90-105">DESCRIPTION</span></span>
<span data-ttu-id="06f90-106">**Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet 'i sanal ağ geçidi bağlantısının paylaşılan anahtarını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="06f90-106">The **Set-AzureRmVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="06f90-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06f90-107">EXAMPLES</span></span>

### <span data-ttu-id="06f90-108">2</span><span class="sxs-lookup"><span data-stu-id="06f90-108">1:</span></span>
```

```

## <span data-ttu-id="06f90-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06f90-109">PARAMETERS</span></span>

### <span data-ttu-id="06f90-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06f90-110">-DefaultProfile</span></span>
<span data-ttu-id="06f90-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06f90-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06f90-112">-Force</span><span class="sxs-lookup"><span data-stu-id="06f90-112">-Force</span></span>
<span data-ttu-id="06f90-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="06f90-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06f90-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="06f90-114">-Name</span></span>
<span data-ttu-id="06f90-115">Sanal ağ geçidi paylaşılan anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="06f90-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="06f90-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06f90-116">-ResourceGroupName</span></span>
<span data-ttu-id="06f90-117">Sanal ağ geçidinin ait olduğu kaynak grubunun adını belirtir</span><span class="sxs-lookup"><span data-stu-id="06f90-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="06f90-118">-Değer</span><span class="sxs-lookup"><span data-stu-id="06f90-118">-Value</span></span>
<span data-ttu-id="06f90-119">Paylaşılan anahtarın değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="06f90-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="06f90-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="06f90-120">-Confirm</span></span>
<span data-ttu-id="06f90-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="06f90-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06f90-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06f90-122">-WhatIf</span></span>
<span data-ttu-id="06f90-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="06f90-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06f90-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="06f90-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06f90-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06f90-125">CommonParameters</span></span>
<span data-ttu-id="06f90-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06f90-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06f90-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06f90-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06f90-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06f90-128">INPUTS</span></span>

## <span data-ttu-id="06f90-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06f90-129">OUTPUTS</span></span>

### <span data-ttu-id="06f90-130">System. String</span><span class="sxs-lookup"><span data-stu-id="06f90-130">System.String</span></span>

## <span data-ttu-id="06f90-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06f90-131">NOTES</span></span>

## <span data-ttu-id="06f90-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06f90-132">RELATED LINKS</span></span>

[<span data-ttu-id="06f90-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="06f90-133">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="06f90-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="06f90-134">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


