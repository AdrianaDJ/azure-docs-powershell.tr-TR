---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 70d110e9a539661d780c2dbce7fb8166a8f4ba97
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936603"
---
# <span data-ttu-id="c6824-101">Remove-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c6824-101">Remove-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="c6824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6824-102">SYNOPSIS</span></span>
<span data-ttu-id="c6824-103">Sanal ağ geçidi bağlantısını siler</span><span class="sxs-lookup"><span data-stu-id="c6824-103">Deletes a Virtual Network Gateway Connection</span></span>

## <span data-ttu-id="c6824-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6824-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6824-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6824-105">DESCRIPTION</span></span>
<span data-ttu-id="c6824-106">Sanal ağ geçidi bağlantısı, Azure 'daki sanal ağ geçidine bağlı olan IPSec tüneli (siteden siteye veya VNET arası) temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="c6824-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="c6824-107">**Remove-AzVirtualNetworkGatewayConnection** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak bağlantınızın nesnesini siler.</span><span class="sxs-lookup"><span data-stu-id="c6824-107">The **Remove-AzVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="c6824-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6824-108">EXAMPLES</span></span>

### <span data-ttu-id="c6824-109">1: sanal ağ geçidi bağlantısını silme</span><span class="sxs-lookup"><span data-stu-id="c6824-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="c6824-110">"MyRG" kaynak grubunda "myTunnel" adlı sanal ağ geçidi bağlantısı nesnesini siler</span><span class="sxs-lookup"><span data-stu-id="c6824-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="c6824-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6824-111">PARAMETERS</span></span>

### <span data-ttu-id="c6824-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6824-112">-DefaultProfile</span></span>
<span data-ttu-id="c6824-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6824-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6824-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c6824-114">-Force</span></span>
<span data-ttu-id="c6824-115">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c6824-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c6824-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6824-116">-Name</span></span>
<span data-ttu-id="c6824-117">Bu cmdlet 'in kaldırıldığı sanal ağ geçidi bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6824-117">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c6824-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c6824-118">-PassThru</span></span>
<span data-ttu-id="c6824-119">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c6824-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c6824-120">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c6824-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c6824-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6824-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6824-122">Sanal ağ geçidi bağlantısını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6824-122">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="c6824-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6824-123">-Confirm</span></span>
<span data-ttu-id="c6824-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6824-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6824-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6824-125">-WhatIf</span></span>
<span data-ttu-id="c6824-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6824-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6824-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6824-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6824-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6824-128">CommonParameters</span></span>
<span data-ttu-id="c6824-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6824-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6824-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6824-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6824-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6824-131">INPUTS</span></span>

## <span data-ttu-id="c6824-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6824-132">OUTPUTS</span></span>

## <span data-ttu-id="c6824-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6824-133">NOTES</span></span>

## <span data-ttu-id="c6824-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6824-134">RELATED LINKS</span></span>

[<span data-ttu-id="c6824-135">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c6824-135">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c6824-136">Yeni-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c6824-136">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="c6824-137">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c6824-137">Set-AzVirtualNetworkGatewayConnection</span></span>](./Set-AzVirtualNetworkGatewayConnection.md)


