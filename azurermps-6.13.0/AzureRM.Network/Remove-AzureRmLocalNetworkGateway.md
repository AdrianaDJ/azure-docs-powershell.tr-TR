---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c09e812762867dc6aa89945f50d9658bb61bf5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588048"
---
# <span data-ttu-id="f727d-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f727d-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="f727d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f727d-102">SYNOPSIS</span></span>
<span data-ttu-id="f727d-103">Yerel ağ geçidi siler</span><span class="sxs-lookup"><span data-stu-id="f727d-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f727d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f727d-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f727d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f727d-105">DESCRIPTION</span></span>
<span data-ttu-id="f727d-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="f727d-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="f727d-107">**Remove-AzureRmLocalNetworkGateway** cmdlet 'i, şirket içi ağ geçidinizi temsil eden nesneyi ad ve kaynak grubu adına göre siler.</span><span class="sxs-lookup"><span data-stu-id="f727d-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f727d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f727d-108">EXAMPLES</span></span>

### <span data-ttu-id="f727d-109">1: yerel ağ ağ geçidini silme</span><span class="sxs-lookup"><span data-stu-id="f727d-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="f727d-110">Yerel ağ ağ geçidinin nesnesini, "myRG" kaynak grubundaki "myLocalGW" adıyla siler. öncelikle **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet 'Ini kullanarak yerel ağ ağ geçitindeki tüm bağlantıları silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f727d-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="f727d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f727d-111">PARAMETERS</span></span>

### <span data-ttu-id="f727d-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="f727d-112">-AsJob</span></span>
<span data-ttu-id="f727d-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f727d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f727d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f727d-114">-DefaultProfile</span></span>
<span data-ttu-id="f727d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f727d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f727d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f727d-116">-Force</span></span>
<span data-ttu-id="f727d-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="f727d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f727d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f727d-118">-Name</span></span>
<span data-ttu-id="f727d-119">Bu cmdlet 'in kaldırdığı yerel ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f727d-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f727d-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f727d-120">-PassThru</span></span>
<span data-ttu-id="f727d-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="f727d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f727d-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f727d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f727d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f727d-123">-ResourceGroupName</span></span>
<span data-ttu-id="f727d-124">Yerel ağ ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f727d-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="f727d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="f727d-125">-Confirm</span></span>
<span data-ttu-id="f727d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f727d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f727d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f727d-127">-WhatIf</span></span>
<span data-ttu-id="f727d-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f727d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f727d-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f727d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f727d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f727d-130">CommonParameters</span></span>
<span data-ttu-id="f727d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f727d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f727d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f727d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f727d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f727d-133">INPUTS</span></span>

### <span data-ttu-id="f727d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f727d-134">System.String</span></span>

## <span data-ttu-id="f727d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f727d-135">OUTPUTS</span></span>

### <span data-ttu-id="f727d-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f727d-136">System.Boolean</span></span>

## <span data-ttu-id="f727d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f727d-137">NOTES</span></span>

## <span data-ttu-id="f727d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f727d-138">RELATED LINKS</span></span>

[<span data-ttu-id="f727d-139">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f727d-139">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="f727d-140">Yeni-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f727d-140">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="f727d-141">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f727d-141">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


