---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: e1623f645c9a45d0b92b682646b0821729fce6fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096138"
---
# <span data-ttu-id="699ce-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="699ce-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="699ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="699ce-102">SYNOPSIS</span></span>
<span data-ttu-id="699ce-103">Sanal Ağ Geçidi bağlantısının paylaşılan anahtarını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="699ce-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="699ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="699ce-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="699ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="699ce-105">DESCRIPTION</span></span>
<span data-ttu-id="699ce-106">**Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet 'i sanal ağ geçidi bağlantısının paylaşılan anahtarını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="699ce-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="699ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="699ce-107">EXAMPLES</span></span>

### <span data-ttu-id="699ce-108">Örnek 1:</span><span class="sxs-lookup"><span data-stu-id="699ce-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="699ce-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="699ce-109">PARAMETERS</span></span>

### <span data-ttu-id="699ce-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699ce-110">-DefaultProfile</span></span>
<span data-ttu-id="699ce-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="699ce-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ce-112">-Force</span><span class="sxs-lookup"><span data-stu-id="699ce-112">-Force</span></span>
<span data-ttu-id="699ce-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="699ce-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ce-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="699ce-114">-Name</span></span>
<span data-ttu-id="699ce-115">Sanal ağ geçidi paylaşılan anahtarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="699ce-115">Specifies the name of the virtual network gateway shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ce-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699ce-116">-ResourceGroupName</span></span>
<span data-ttu-id="699ce-117">Sanal ağ geçidinin ait olduğu kaynak grubunun adını belirtir</span><span class="sxs-lookup"><span data-stu-id="699ce-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ce-118">-Değer</span><span class="sxs-lookup"><span data-stu-id="699ce-118">-Value</span></span>
<span data-ttu-id="699ce-119">Paylaşılan anahtarın değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="699ce-119">Specifies the value of the shared key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ce-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="699ce-120">-Confirm</span></span>
<span data-ttu-id="699ce-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="699ce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="699ce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="699ce-122">-WhatIf</span></span>
<span data-ttu-id="699ce-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="699ce-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="699ce-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="699ce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="699ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699ce-125">CommonParameters</span></span>
<span data-ttu-id="699ce-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="699ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699ce-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699ce-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699ce-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="699ce-128">INPUTS</span></span>

### <span data-ttu-id="699ce-129">System. String</span><span class="sxs-lookup"><span data-stu-id="699ce-129">System.String</span></span>

## <span data-ttu-id="699ce-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="699ce-130">OUTPUTS</span></span>

### <span data-ttu-id="699ce-131">System. String</span><span class="sxs-lookup"><span data-stu-id="699ce-131">System.String</span></span>

## <span data-ttu-id="699ce-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="699ce-132">NOTES</span></span>

## <span data-ttu-id="699ce-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="699ce-133">RELATED LINKS</span></span>

[<span data-ttu-id="699ce-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="699ce-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="699ce-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="699ce-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
