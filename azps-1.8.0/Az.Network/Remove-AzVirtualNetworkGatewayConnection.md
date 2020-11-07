---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 3a2cd6b4fd4cefdfda10e3491aef31ed9a138383
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760105"
---
# <span data-ttu-id="b3e5f-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b3e5f-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="b3e5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e5f-103">Sanal ağ geçidi bağlantısını siler</span><span class="sxs-lookup"><span data-stu-id="b3e5f-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="b3e5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3e5f-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3e5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3e5f-105">DESCRIPTION</span></span>
<span data-ttu-id="b3e5f-106">Sanal ağ geçidi bağlantısı, Azure 'daki sanal ağ geçidine bağlı olan IPSec tüneli (siteden siteye veya VNET arası) temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>
<span data-ttu-id="b3e5f-107">**Remove-AzVirtualNetworkGatewayConnection** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak bağlantınızın nesnesini siler.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b3e5f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3e5f-108">EXAMPLES</span></span>

### <span data-ttu-id="b3e5f-109">1: sanal ağ geçidi bağlantısını silme</span><span class="sxs-lookup"><span data-stu-id="b3e5f-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="b3e5f-110">"MyRG" kaynak grubunda "myTunnel" adlı sanal ağ geçidi bağlantısı nesnesini siler</span><span class="sxs-lookup"><span data-stu-id="b3e5f-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="b3e5f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3e5f-111">PARAMETERS</span></span>

### <span data-ttu-id="b3e5f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e5f-112">-DefaultProfile</span></span>
<span data-ttu-id="b3e5f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3e5f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b3e5f-114">-Force</span></span>
<span data-ttu-id="b3e5f-115">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3e5f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="b3e5f-116">-Name</span></span>
<span data-ttu-id="b3e5f-117">Bu cmdlet 'in kaldırıldığı sanal ağ geçidi bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b3e5f-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b3e5f-118">-PassThru</span></span>
<span data-ttu-id="b3e5f-119">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3e5f-120">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3e5f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e5f-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3e5f-122">Sanal ağ geçidi bağlantısını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="b3e5f-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3e5f-123">-Confirm</span></span>
<span data-ttu-id="b3e5f-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3e5f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3e5f-125">-WhatIf</span></span>
<span data-ttu-id="b3e5f-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3e5f-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3e5f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e5f-128">CommonParameters</span></span>
<span data-ttu-id="b3e5f-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3e5f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e5f-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e5f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e5f-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3e5f-131">INPUTS</span></span>

### <span data-ttu-id="b3e5f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b3e5f-132">System.String</span></span>

## <span data-ttu-id="b3e5f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3e5f-133">OUTPUTS</span></span>

### <span data-ttu-id="b3e5f-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3e5f-134">System.Boolean</span></span>

## <span data-ttu-id="b3e5f-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3e5f-135">NOTES</span></span>

## <span data-ttu-id="b3e5f-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3e5f-136">RELATED LINKS</span></span>

[<span data-ttu-id="b3e5f-137">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b3e5f-137">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b3e5f-138">Yeni-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b3e5f-138">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="b3e5f-139">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="b3e5f-139">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)
