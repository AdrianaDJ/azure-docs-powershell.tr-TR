---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetwork.md
ms.openlocfilehash: 777e03a570f3915d6e0ebe4cbb5c84f9c1824120
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323638"
---
# <span data-ttu-id="e4ad7-101">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4ad7-101">Remove-AzVirtualNetwork</span></span>

## <span data-ttu-id="e4ad7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="e4ad7-103">Sanal ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-103">Removes a virtual network.</span></span>

## <span data-ttu-id="e4ad7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4ad7-104">SYNTAX</span></span>

```
Remove-AzVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4ad7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4ad7-105">DESCRIPTION</span></span>
<span data-ttu-id="e4ad7-106">**Remove-AzVirtualNetwork** cmdlet 'ı bir Azure sanal ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-106">The **Remove-AzVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="e4ad7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4ad7-107">EXAMPLES</span></span>

### <span data-ttu-id="e4ad7-108">1: sanal ağ oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="e4ad7-108">1: Create and delete a virtual network</span></span>
```
New-AzResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"
    $backendSubnet = New-AzVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

New-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup 
    -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
    
Remove-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="e4ad7-109">Bu örnekte, kaynak grubunda sanal bir ağ oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e4ad7-110">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e4ad7-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4ad7-111">PARAMETERS</span></span>

### <span data-ttu-id="e4ad7-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="e4ad7-112">-AsJob</span></span>
<span data-ttu-id="e4ad7-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e4ad7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4ad7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4ad7-114">-DefaultProfile</span></span>
<span data-ttu-id="e4ad7-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4ad7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e4ad7-116">-Force</span></span>
<span data-ttu-id="e4ad7-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4ad7-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4ad7-118">-Name</span></span>
<span data-ttu-id="e4ad7-119">Bu cmdlet 'in kaldırıldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4ad7-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e4ad7-120">-PassThru</span></span>
<span data-ttu-id="e4ad7-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4ad7-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4ad7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4ad7-123">-ResourceGroupName</span></span>
<span data-ttu-id="e4ad7-124">Bu cmdlet 'in kaldırıldığı sanal ağı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4ad7-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="e4ad7-125">-Confirm</span></span>
<span data-ttu-id="e4ad7-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4ad7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4ad7-127">-WhatIf</span></span>
<span data-ttu-id="e4ad7-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4ad7-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4ad7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4ad7-130">CommonParameters</span></span>
<span data-ttu-id="e4ad7-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4ad7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4ad7-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4ad7-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4ad7-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4ad7-133">INPUTS</span></span>

### <span data-ttu-id="e4ad7-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e4ad7-134">System.String</span></span>

## <span data-ttu-id="e4ad7-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4ad7-135">OUTPUTS</span></span>

### <span data-ttu-id="e4ad7-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e4ad7-136">System.Boolean</span></span>

## <span data-ttu-id="e4ad7-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4ad7-137">NOTES</span></span>

## <span data-ttu-id="e4ad7-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4ad7-138">RELATED LINKS</span></span>

[<span data-ttu-id="e4ad7-139">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4ad7-139">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)

[<span data-ttu-id="e4ad7-140">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4ad7-140">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="e4ad7-141">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e4ad7-141">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


