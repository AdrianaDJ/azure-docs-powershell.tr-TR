---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: b27ad6bfc08f6c6d9304cc78f888870a8a2dbad4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593949"
---
# <span data-ttu-id="c614d-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c614d-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="c614d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c614d-102">SYNOPSIS</span></span>
<span data-ttu-id="c614d-103">Sanal ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c614d-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c614d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c614d-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c614d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c614d-105">DESCRIPTION</span></span>
<span data-ttu-id="c614d-106">**Remove-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c614d-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="c614d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c614d-107">EXAMPLES</span></span>

### <span data-ttu-id="c614d-108">1: sanal ağ oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="c614d-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="c614d-109">Bu örnekte, kaynak grubunda sanal bir ağ oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="c614d-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="c614d-110">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="c614d-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="c614d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c614d-111">PARAMETERS</span></span>

### <span data-ttu-id="c614d-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="c614d-112">-AsJob</span></span>
<span data-ttu-id="c614d-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c614d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c614d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c614d-114">-DefaultProfile</span></span>
<span data-ttu-id="c614d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c614d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c614d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c614d-116">-Force</span></span>
<span data-ttu-id="c614d-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c614d-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c614d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c614d-118">-Name</span></span>
<span data-ttu-id="c614d-119">Bu cmdlet 'in kaldırıldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c614d-119">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c614d-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c614d-120">-PassThru</span></span>
<span data-ttu-id="c614d-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="c614d-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c614d-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c614d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c614d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c614d-123">-ResourceGroupName</span></span>
<span data-ttu-id="c614d-124">Bu cmdlet 'in kaldırıldığı sanal ağı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c614d-124">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c614d-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="c614d-125">-Confirm</span></span>
<span data-ttu-id="c614d-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c614d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c614d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c614d-127">-WhatIf</span></span>
<span data-ttu-id="c614d-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c614d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c614d-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c614d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c614d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c614d-130">CommonParameters</span></span>
<span data-ttu-id="c614d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c614d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c614d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c614d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c614d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c614d-133">INPUTS</span></span>

### <span data-ttu-id="c614d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c614d-134">System.String</span></span>

## <span data-ttu-id="c614d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c614d-135">OUTPUTS</span></span>

### <span data-ttu-id="c614d-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c614d-136">System.Boolean</span></span>

## <span data-ttu-id="c614d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c614d-137">NOTES</span></span>

## <span data-ttu-id="c614d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c614d-138">RELATED LINKS</span></span>

[<span data-ttu-id="c614d-139">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c614d-139">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c614d-140">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c614d-140">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c614d-141">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c614d-141">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


