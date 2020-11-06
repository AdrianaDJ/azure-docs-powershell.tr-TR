---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: ddc269ecd6f5cb4d1a1d377f656d47b0d18c6c00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586893"
---
# <span data-ttu-id="9c30a-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9c30a-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="9c30a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c30a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c30a-103">Yerel ağ geçidi siler</span><span class="sxs-lookup"><span data-stu-id="9c30a-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c30a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c30a-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c30a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c30a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c30a-106">Yerel ağ geçidi, VPN cihazınızı şirket Içinde temsil eden bir nesnedir.</span><span class="sxs-lookup"><span data-stu-id="9c30a-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="9c30a-107">**Remove-AzureRmLocalNetworkGateway** cmdlet 'i, şirket içi ağ geçidinizi temsil eden nesneyi ad ve kaynak grubu adına göre siler.</span><span class="sxs-lookup"><span data-stu-id="9c30a-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="9c30a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c30a-108">EXAMPLES</span></span>

### <span data-ttu-id="9c30a-109">1: yerel ağ ağ geçidini silme</span><span class="sxs-lookup"><span data-stu-id="9c30a-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="9c30a-110">Yerel ağ geçidinin "myLocalGW" adlı nesnesini, "myRG" kaynak grubunda siler</span><span class="sxs-lookup"><span data-stu-id="9c30a-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="9c30a-111">Not: **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet 'Ini kullanarak yerel ağ ağ geçitindeki tüm bağlantıları silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="9c30a-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="9c30a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c30a-112">PARAMETERS</span></span>

### <span data-ttu-id="9c30a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="9c30a-113">-Force</span></span>
<span data-ttu-id="9c30a-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9c30a-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c30a-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c30a-115">-Name</span></span>
<span data-ttu-id="9c30a-116">Bu cmdlet 'in kaldırdığı yerel ağ ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c30a-116">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9c30a-117">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9c30a-117">-PassThru</span></span>
<span data-ttu-id="9c30a-118">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="9c30a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c30a-119">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="9c30a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c30a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c30a-120">-ResourceGroupName</span></span>
<span data-ttu-id="9c30a-121">Yerel ağ ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c30a-121">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="9c30a-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c30a-122">-Confirm</span></span>
<span data-ttu-id="9c30a-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c30a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c30a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c30a-124">-WhatIf</span></span>
<span data-ttu-id="9c30a-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c30a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c30a-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c30a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c30a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c30a-127">-DefaultProfile</span></span>
<span data-ttu-id="9c30a-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c30a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c30a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c30a-129">CommonParameters</span></span>
<span data-ttu-id="9c30a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c30a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c30a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c30a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c30a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c30a-132">INPUTS</span></span>

## <span data-ttu-id="9c30a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c30a-133">OUTPUTS</span></span>

## <span data-ttu-id="9c30a-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c30a-134">NOTES</span></span>

## <span data-ttu-id="9c30a-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c30a-135">RELATED LINKS</span></span>

[<span data-ttu-id="9c30a-136">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9c30a-136">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="9c30a-137">Yeni-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9c30a-137">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="9c30a-138">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9c30a-138">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


