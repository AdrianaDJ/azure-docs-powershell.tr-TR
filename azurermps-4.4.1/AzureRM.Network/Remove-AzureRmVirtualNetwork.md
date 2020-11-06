---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C48E204D-D7EC-4EFD-ADC5-C6F593313B9B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1ab783b4b5a49793b4f4c91f2f7bc9f5410e5ddd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587839"
---
# <span data-ttu-id="e3a93-101">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3a93-101">Remove-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="e3a93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a93-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a93-103">Sanal ağı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3a93-103">Removes a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3a93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e3a93-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e3a93-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a93-106">**Remove-AzureRmVirtualNetwork** cmdlet 'ı bir Azure sanal ağını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e3a93-106">The **Remove-AzureRmVirtualNetwork** cmdlet removes an Azure virtual network.</span></span>

## <span data-ttu-id="e3a93-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e3a93-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a93-108">1: sanal ağ oluşturma ve silme</span><span class="sxs-lookup"><span data-stu-id="e3a93-108">1: Create and delete a virtual network</span></span>
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

<span data-ttu-id="e3a93-109">Bu örnekte, kaynak grubunda sanal bir ağ oluşturulur ve hemen silinir.</span><span class="sxs-lookup"><span data-stu-id="e3a93-109">This example creates a virtual network in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="e3a93-110">Sanal ağı silerken istemi bastırmak için,-Force bayrağını kullanın.</span><span class="sxs-lookup"><span data-stu-id="e3a93-110">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="e3a93-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e3a93-111">PARAMETERS</span></span>

### <span data-ttu-id="e3a93-112">-Force</span><span class="sxs-lookup"><span data-stu-id="e3a93-112">-Force</span></span>
<span data-ttu-id="e3a93-113">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e3a93-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e3a93-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="e3a93-114">-Name</span></span>
<span data-ttu-id="e3a93-115">Bu cmdlet 'in kaldırıldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a93-115">Specifies the name of the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e3a93-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e3a93-116">-PassThru</span></span>
<span data-ttu-id="e3a93-117">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="e3a93-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e3a93-118">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e3a93-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3a93-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3a93-119">-ResourceGroupName</span></span>
<span data-ttu-id="e3a93-120">Bu cmdlet 'in kaldırıldığı sanal ağı içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e3a93-120">Specifies the name of the resource group that contains the virtual network that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e3a93-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="e3a93-121">-Confirm</span></span>
<span data-ttu-id="e3a93-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e3a93-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a93-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a93-123">-WhatIf</span></span>
<span data-ttu-id="e3a93-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e3a93-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a93-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e3a93-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a93-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a93-126">-DefaultProfile</span></span>
<span data-ttu-id="e3a93-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e3a93-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3a93-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a93-128">CommonParameters</span></span>
<span data-ttu-id="e3a93-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e3a93-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a93-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a93-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a93-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e3a93-131">INPUTS</span></span>

## <span data-ttu-id="e3a93-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e3a93-132">OUTPUTS</span></span>

## <span data-ttu-id="e3a93-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e3a93-133">NOTES</span></span>

## <span data-ttu-id="e3a93-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e3a93-134">RELATED LINKS</span></span>

[<span data-ttu-id="e3a93-135">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3a93-135">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e3a93-136">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3a93-136">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="e3a93-137">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3a93-137">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


