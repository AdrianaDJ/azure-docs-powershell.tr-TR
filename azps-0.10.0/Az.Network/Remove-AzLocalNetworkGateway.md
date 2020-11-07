---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 0589fa3f5dd806149c243557b547455af35178b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935286"
---
# <span data-ttu-id="34eff-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="34eff-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="34eff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34eff-102">SYNOPSIS</span></span>
<span data-ttu-id="34eff-103">Yerel ağ geçidi siler</span><span class="sxs-lookup"><span data-stu-id="34eff-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="34eff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34eff-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34eff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34eff-105">DESCRIPTION</span></span>
<span data-ttu-id="34eff-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="34eff-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="34eff-107">**Remove-AzLocalNetworkGateway** cmdlet 'i, şirket içi ağ geçidinizi temsil eden nesneyi ad ve kaynak grubu adına göre siler.</span><span class="sxs-lookup"><span data-stu-id="34eff-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="34eff-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34eff-108">EXAMPLES</span></span>

### <span data-ttu-id="34eff-109">1: yerel ağ ağ geçidini silme</span><span class="sxs-lookup"><span data-stu-id="34eff-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="34eff-110">Yerel ağ geçidinin "myLocalGW" adlı nesnesini, "myRG" kaynak grubunda siler</span><span class="sxs-lookup"><span data-stu-id="34eff-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="34eff-111">Not: **Remove-AzVirtualNetworkGatewayConnection** cmdlet 'Ini kullanarak yerel ağ ağ geçitindeki tüm bağlantıları silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="34eff-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="34eff-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34eff-112">PARAMETERS</span></span>

### <span data-ttu-id="34eff-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="34eff-113">-AsJob</span></span>
<span data-ttu-id="34eff-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="34eff-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34eff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34eff-115">-DefaultProfile</span></span>
<span data-ttu-id="34eff-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34eff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34eff-117">-Force</span><span class="sxs-lookup"><span data-stu-id="34eff-117">-Force</span></span>
<span data-ttu-id="34eff-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="34eff-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34eff-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="34eff-119">-Name</span></span>
<span data-ttu-id="34eff-120">Bu cmdlet 'in kaldırdığı yerel ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34eff-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="34eff-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34eff-121">-PassThru</span></span>
<span data-ttu-id="34eff-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="34eff-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="34eff-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="34eff-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="34eff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34eff-124">-ResourceGroupName</span></span>
<span data-ttu-id="34eff-125">Yerel ağ ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34eff-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="34eff-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="34eff-126">-Confirm</span></span>
<span data-ttu-id="34eff-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34eff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34eff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34eff-128">-WhatIf</span></span>
<span data-ttu-id="34eff-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34eff-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34eff-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34eff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34eff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34eff-131">CommonParameters</span></span>
<span data-ttu-id="34eff-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34eff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34eff-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34eff-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34eff-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34eff-134">INPUTS</span></span>

## <span data-ttu-id="34eff-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34eff-135">OUTPUTS</span></span>

## <span data-ttu-id="34eff-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34eff-136">NOTES</span></span>

## <span data-ttu-id="34eff-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34eff-137">RELATED LINKS</span></span>

[<span data-ttu-id="34eff-138">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="34eff-138">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="34eff-139">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="34eff-139">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="34eff-140">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="34eff-140">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)


