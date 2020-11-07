---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGateway.md
ms.openlocfilehash: 533eb9482c2e872c0b41552a5c59842a07fa0216
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764696"
---
# <span data-ttu-id="b80bd-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b80bd-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="b80bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b80bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b80bd-103">Sanal ağ geçidi siler</span><span class="sxs-lookup"><span data-stu-id="b80bd-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b80bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b80bd-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b80bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b80bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b80bd-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="b80bd-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="b80bd-107">**Get-AzureRmVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b80bd-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="b80bd-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b80bd-108">EXAMPLES</span></span>

### <span data-ttu-id="b80bd-109">1: sanal ağ geçidini silme</span><span class="sxs-lookup"><span data-stu-id="b80bd-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="b80bd-110">Sanal ağ geçidinin, "myRG" kaynak grubundaki "myGateway" adıyla</span><span class="sxs-lookup"><span data-stu-id="b80bd-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="b80bd-111">Not: **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet 'Ini kullanarak sanal ağ geçitindeki tüm bağlantıları silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="b80bd-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="b80bd-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b80bd-112">PARAMETERS</span></span>

### <span data-ttu-id="b80bd-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="b80bd-113">-AsJob</span></span>
<span data-ttu-id="b80bd-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="b80bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b80bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b80bd-115">-DefaultProfile</span></span>
<span data-ttu-id="b80bd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b80bd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b80bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b80bd-117">-Force</span></span>
<span data-ttu-id="b80bd-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b80bd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b80bd-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b80bd-119">-Name</span></span>
<span data-ttu-id="b80bd-120">Bu cmdlet 'in kaldırdığı sanal ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b80bd-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b80bd-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b80bd-121">-PassThru</span></span>
<span data-ttu-id="b80bd-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b80bd-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b80bd-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b80bd-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b80bd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b80bd-124">-ResourceGroupName</span></span>
<span data-ttu-id="b80bd-125">Sanal ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b80bd-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="b80bd-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="b80bd-126">-Confirm</span></span>
<span data-ttu-id="b80bd-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b80bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b80bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b80bd-128">-WhatIf</span></span>
<span data-ttu-id="b80bd-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b80bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b80bd-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b80bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b80bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b80bd-131">CommonParameters</span></span>
<span data-ttu-id="b80bd-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b80bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b80bd-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b80bd-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b80bd-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b80bd-134">INPUTS</span></span>

### <span data-ttu-id="b80bd-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b80bd-135">None</span></span>
<span data-ttu-id="b80bd-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b80bd-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b80bd-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b80bd-137">OUTPUTS</span></span>

## <span data-ttu-id="b80bd-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b80bd-138">NOTES</span></span>

## <span data-ttu-id="b80bd-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b80bd-139">RELATED LINKS</span></span>

