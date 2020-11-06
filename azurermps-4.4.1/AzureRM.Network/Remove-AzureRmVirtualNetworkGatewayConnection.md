---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 15958F3D-291A-4E49-A667-9792E9A1577A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayConnection.md
ms.openlocfilehash: d2068273c6f46c058ad7586083f6bfa0db037cab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589248"
---
# <span data-ttu-id="57020-101">Remove-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="57020-101">Remove-AzureRmVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="57020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57020-102">SYNOPSIS</span></span>
<span data-ttu-id="57020-103">Sanal ağ geçidi bağlantısını siler</span><span class="sxs-lookup"><span data-stu-id="57020-103">Deletes a Virtual Network Gateway Connection</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57020-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57020-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayConnection -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57020-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57020-105">DESCRIPTION</span></span>
<span data-ttu-id="57020-106">Sanal ağ geçidi bağlantısı, Azure 'daki sanal ağ geçidine bağlı olan IPSec tüneli (siteden siteye veya VNET arası) temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="57020-106">The Virtual Network Gateway Connection is the object representing the IPsec tunnel (Site-to-Site or Vnet-to-Vnet) connected to your Virtual Network Gateway in Azure.</span></span>

<span data-ttu-id="57020-107">**Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak bağlantınızın nesnesini siler.</span><span class="sxs-lookup"><span data-stu-id="57020-107">The **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet deletes the object of your connection based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="57020-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57020-108">EXAMPLES</span></span>

### <span data-ttu-id="57020-109">1: sanal ağ geçidi bağlantısını silme</span><span class="sxs-lookup"><span data-stu-id="57020-109">1: Delete a Virtual Network Gateway Connection</span></span>
```
Remove-AzureRmVirtualNetworkGatewayConnection -Name myTunnel -ResourceGroupName myRG
```

<span data-ttu-id="57020-110">"MyRG" kaynak grubunda "myTunnel" adlı sanal ağ geçidi bağlantısı nesnesini siler</span><span class="sxs-lookup"><span data-stu-id="57020-110">Deletes the object of the Virtual Network Gateway Connection with the name "myTunnel" within the resource group "myRG"</span></span>

## <span data-ttu-id="57020-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57020-111">PARAMETERS</span></span>

### <span data-ttu-id="57020-112">-Force</span><span class="sxs-lookup"><span data-stu-id="57020-112">-Force</span></span>
<span data-ttu-id="57020-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="57020-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="57020-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="57020-114">-Name</span></span>
<span data-ttu-id="57020-115">Bu cmdlet 'in kaldırıldığı sanal ağ geçidi bağlantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57020-115">Specifies the name of the virtual network gateway connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="57020-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="57020-116">-PassThru</span></span>
<span data-ttu-id="57020-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="57020-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="57020-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="57020-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="57020-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57020-119">-ResourceGroupName</span></span>
<span data-ttu-id="57020-120">Sanal ağ geçidi bağlantısını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57020-120">Specifies the name of the resource group that contains the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="57020-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="57020-121">-Confirm</span></span>
<span data-ttu-id="57020-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="57020-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57020-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57020-123">-WhatIf</span></span>
<span data-ttu-id="57020-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="57020-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57020-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="57020-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57020-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57020-126">-DefaultProfile</span></span>
<span data-ttu-id="57020-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57020-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57020-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57020-128">CommonParameters</span></span>
<span data-ttu-id="57020-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57020-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57020-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57020-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57020-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57020-131">INPUTS</span></span>

## <span data-ttu-id="57020-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57020-132">OUTPUTS</span></span>

## <span data-ttu-id="57020-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57020-133">NOTES</span></span>

## <span data-ttu-id="57020-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57020-134">RELATED LINKS</span></span>

[<span data-ttu-id="57020-135">Get-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="57020-135">Get-AzureRmVirtualNetworkGatewayConnection</span></span>](./Get-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="57020-136">Yeni-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="57020-136">New-AzureRmVirtualNetworkGatewayConnection</span></span>](./New-AzureRmVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="57020-137">Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="57020-137">Set-AzureRmVirtualNetworkGatewayConnection</span></span>](./Set-AzureRmVirtualNetworkGatewayConnection.md)


