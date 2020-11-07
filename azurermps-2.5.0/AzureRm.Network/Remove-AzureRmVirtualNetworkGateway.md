---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A35BB728-A7EF-4ADF-B1A9-25A156434E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgateway
schema: 2.0.0
ms.openlocfilehash: 958ddffb02aaa6c8ac81f413cca6453f7f87c3a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939699"
---
# <span data-ttu-id="5892f-101">Remove-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5892f-101">Remove-AzureRmVirtualNetworkGateway</span></span>

## <span data-ttu-id="5892f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5892f-102">SYNOPSIS</span></span>
<span data-ttu-id="5892f-103">Sanal ağ geçidi siler</span><span class="sxs-lookup"><span data-stu-id="5892f-103">Deletes a Virtual Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5892f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5892f-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5892f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5892f-105">DESCRIPTION</span></span>
<span data-ttu-id="5892f-106">Sanal ağ geçidi, Azure 'daki ağ geçidini temsil eden nesnedir.</span><span class="sxs-lookup"><span data-stu-id="5892f-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>

<span data-ttu-id="5892f-107">**Get-AzureRmVirtualNetworkGateway** cmdlet 'ı, ad ve kaynak grubu adına dayalı olarak Azure 'daki ağ geçidinizin nesnesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5892f-107">The **Get-AzureRmVirtualNetworkGateway** cmdlet returns the object of your gateway in Azure based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="5892f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5892f-108">EXAMPLES</span></span>

### <span data-ttu-id="5892f-109">1: sanal ağ geçidini silme</span><span class="sxs-lookup"><span data-stu-id="5892f-109">1: Delete a Virtual Network Gateway</span></span>
```
Remove-AzureRmVirtualNetworkGateway -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="5892f-110">Sanal ağ geçidinin, "myRG" kaynak grubundaki "myGateway" adıyla</span><span class="sxs-lookup"><span data-stu-id="5892f-110">Deletes the object of the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

<span data-ttu-id="5892f-111">Not: **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet 'Ini kullanarak sanal ağ geçitindeki tüm bağlantıları silmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="5892f-111">Note: You must first delete all connections to the Virtual Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="5892f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5892f-112">PARAMETERS</span></span>

### <span data-ttu-id="5892f-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="5892f-113">-AsJob</span></span>
<span data-ttu-id="5892f-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5892f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5892f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5892f-115">-DefaultProfile</span></span>
<span data-ttu-id="5892f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5892f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5892f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5892f-117">-Force</span></span>
<span data-ttu-id="5892f-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5892f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5892f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="5892f-119">-Name</span></span>
<span data-ttu-id="5892f-120">Bu cmdlet 'in kaldırdığı sanal ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5892f-120">Specifies the name of the virtual network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5892f-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="5892f-121">-PassThru</span></span>
<span data-ttu-id="5892f-122">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="5892f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5892f-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5892f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5892f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5892f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5892f-125">Sanal ağ geçidini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5892f-125">Specifies the name of the resource group that contains the virtual network gateway.</span></span>

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

### <span data-ttu-id="5892f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="5892f-126">-Confirm</span></span>
<span data-ttu-id="5892f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5892f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5892f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5892f-128">-WhatIf</span></span>
<span data-ttu-id="5892f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5892f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5892f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5892f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5892f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5892f-131">CommonParameters</span></span>
<span data-ttu-id="5892f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5892f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5892f-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5892f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5892f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5892f-134">INPUTS</span></span>

## <span data-ttu-id="5892f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5892f-135">OUTPUTS</span></span>

## <span data-ttu-id="5892f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5892f-136">NOTES</span></span>

## <span data-ttu-id="5892f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5892f-137">RELATED LINKS</span></span>

