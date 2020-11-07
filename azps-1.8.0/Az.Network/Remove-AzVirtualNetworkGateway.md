---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkGateway.md
ms.openlocfilehash: 7815755d9ec5fffe973e0ecb044409f945ee5faa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760108"
---
# <span data-ttu-id="533f9-101">Remove-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="533f9-101">Remove-AzVirtualNetworkGateway</span></span>

## <span data-ttu-id="533f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="533f9-102">SYNOPSIS</span></span>
<span data-ttu-id="533f9-103">Sanal ağ geçidi siler</span><span class="sxs-lookup"><span data-stu-id="533f9-103">Deletes a Virtual Network Gateway</span></span>

## <span data-ttu-id="533f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="533f9-104">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="533f9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="533f9-105">DESCRIPTION</span></span>
<span data-ttu-id="533f9-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="533f9-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="533f9-107">**Get-AzVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="533f9-107">The **Get-AzVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="533f9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="533f9-108">EXAMPLES</span></span>

### <span data-ttu-id="533f9-109">1: sanal ağ geçidini silme</span><span class="sxs-lookup"><span data-stu-id="533f9-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="533f9-110">Sanal ağ geçidinin, "myRG" kaynak grubundaki "myGateway" adıyla olan nesnesini siler. öncelikle **Remove-AzVirtualNetworkGatewayConnection** cmdlet 'Ini kullanarak sanal ağ ağ geçitindeki tüm bağlantıları silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="533f9-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG" Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="533f9-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="533f9-111">PARAMETERS</span></span>

### <span data-ttu-id="533f9-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="533f9-112">-AsJob</span></span>
<span data-ttu-id="533f9-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="533f9-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="533f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="533f9-114">-DefaultProfile</span></span>
<span data-ttu-id="533f9-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="533f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="533f9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="533f9-116">-Force</span></span>
<span data-ttu-id="533f9-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="533f9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="533f9-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="533f9-118">-Name</span></span>
<span data-ttu-id="533f9-119">Bu cmdlet 'in kaldırdığı sanal ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="533f9-119">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="533f9-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="533f9-120">-PassThru</span></span>
<span data-ttu-id="533f9-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="533f9-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="533f9-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="533f9-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="533f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="533f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="533f9-124">Sanal ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="533f9-124">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="533f9-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="533f9-125">-Confirm</span></span>
<span data-ttu-id="533f9-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="533f9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="533f9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="533f9-127">-WhatIf</span></span>
<span data-ttu-id="533f9-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="533f9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="533f9-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="533f9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="533f9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="533f9-130">CommonParameters</span></span>
<span data-ttu-id="533f9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="533f9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="533f9-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="533f9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="533f9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="533f9-133">INPUTS</span></span>

### <span data-ttu-id="533f9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="533f9-134">System.String</span></span>

## <span data-ttu-id="533f9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="533f9-135">OUTPUTS</span></span>

### <span data-ttu-id="533f9-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="533f9-136">System.Boolean</span></span>

## <span data-ttu-id="533f9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="533f9-137">NOTES</span></span>

## <span data-ttu-id="533f9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="533f9-138">RELATED LINKS</span></span>

[<span data-ttu-id="533f9-139">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="533f9-139">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="533f9-140">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="533f9-140">New-AzVirtualNetworkGateway</span></span>](./New-AzVirtualNetworkGateway.md)

[<span data-ttu-id="533f9-141">Reset-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="533f9-141">Reset-AzVirtualNetworkGateway</span></span>](./Reset-AzVirtualNetworkGateway.md)

[<span data-ttu-id="533f9-142">Resize-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="533f9-142">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)

[<span data-ttu-id="533f9-143">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="533f9-143">Set-AzVirtualNetworkGateway</span></span>](./Set-AzVirtualNetworkGateway.md)
