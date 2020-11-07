---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 89f0be5dbb0ba6b4e24e76be1eb75c375f0ebcd5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939081"
---
# <span data-ttu-id="a91ab-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a91ab-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="a91ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a91ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a91ab-103">Sanal ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a91ab-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a91ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a91ab-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a91ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a91ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a91ab-106">**Remove-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a91ab-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="a91ab-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a91ab-107">EXAMPLES</span></span>

### <span data-ttu-id="a91ab-108">1: sanal ağ oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="a91ab-108">1: Create and delete a virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="a91ab-109">Bu örnekte, kaynak grubunda sanal bir ağ oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="a91ab-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="a91ab-110">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="a91ab-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="a91ab-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a91ab-111">PARAMETERS</span></span>

### <span data-ttu-id="a91ab-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="a91ab-112">-AsJob</span></span>
<span data-ttu-id="a91ab-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a91ab-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a91ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a91ab-114">-DefaultProfile</span></span>
<span data-ttu-id="a91ab-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a91ab-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a91ab-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a91ab-116">-Force</span></span>
<span data-ttu-id="a91ab-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a91ab-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a91ab-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a91ab-118">-Name</span></span>
<span data-ttu-id="a91ab-119">Bu cmdlet 'in kaldırıldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a91ab-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a91ab-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a91ab-120">-PassThru</span></span>
<span data-ttu-id="a91ab-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a91ab-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a91ab-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a91ab-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a91ab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a91ab-123">-ResourceGroupName</span></span>
<span data-ttu-id="a91ab-124">Bu cmdlet 'in kaldırıldığı sanal ağı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a91ab-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a91ab-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a91ab-125">-Confirm</span></span>
<span data-ttu-id="a91ab-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a91ab-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a91ab-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a91ab-127">-WhatIf</span></span>
<span data-ttu-id="a91ab-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a91ab-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a91ab-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a91ab-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a91ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91ab-130">CommonParameters</span></span>
<span data-ttu-id="a91ab-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a91ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91ab-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91ab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91ab-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a91ab-133">INPUTS</span></span>

## <span data-ttu-id="a91ab-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a91ab-134">OUTPUTS</span></span>

## <span data-ttu-id="a91ab-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a91ab-135">NOTES</span></span>

## <span data-ttu-id="a91ab-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a91ab-136">RELATED LINKS</span></span>

[<span data-ttu-id="a91ab-137">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a91ab-137">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="a91ab-138">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a91ab-138">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="a91ab-139">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a91ab-139">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


