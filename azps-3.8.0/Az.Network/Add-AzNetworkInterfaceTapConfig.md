---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937343"
---
# <span data-ttu-id="ec44f-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ec44f-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="ec44f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec44f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec44f-103">Bir NetworkInterface ile ilişkilendirilmiş bir TapConfiguration kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec44f-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="ec44f-104">Bu, var olan bir VirtualNetworkTap kaynağına başvurur.</span><span class="sxs-lookup"><span data-stu-id="ec44f-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="ec44f-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec44f-105">SYNTAX</span></span>

### <span data-ttu-id="ec44f-106">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec44f-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec44f-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="ec44f-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec44f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec44f-108">DESCRIPTION</span></span>
<span data-ttu-id="ec44f-109">**Add-Aznetworkınterfacetapconfig** cmdlet 'i, bir NetworkInterface ile Ilişkilendirilmiş bir tapconfiguration kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ec44f-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="ec44f-110">Bu, var olan bir VirtualNetworkTap kaynağına başvurur.</span><span class="sxs-lookup"><span data-stu-id="ec44f-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="ec44f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec44f-111">EXAMPLES</span></span>

### <span data-ttu-id="ec44f-112">Örnek 1: verilen bir ağ arabirimine TapConfiguration ekleme</span><span class="sxs-lookup"><span data-stu-id="ec44f-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="ec44f-113">Bir kaynak.</span><span class="sxs-lookup"><span data-stu-id="ec44f-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="ec44f-114">Sourcenıc VM 'nin trafiği vVirtualNetworkTap kaynağında başvurulan hedef VM 'ye yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="ec44f-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="ec44f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec44f-115">PARAMETERS</span></span>

### <span data-ttu-id="ec44f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec44f-116">-DefaultProfile</span></span>
<span data-ttu-id="ec44f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec44f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec44f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec44f-118">-Name</span></span>
<span data-ttu-id="ec44f-119">Dokunun yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="ec44f-119">Name of the tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec44f-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ec44f-120">-NetworkInterface</span></span>
<span data-ttu-id="ec44f-121">Ağ arabirim kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="ec44f-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec44f-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ec44f-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="ec44f-123">Sanal ağın başvurusu kaynak 'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="ec44f-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec44f-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="ec44f-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="ec44f-125">Sanal ağın başvurusu kaynak 'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="ec44f-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec44f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec44f-126">-Confirm</span></span>
<span data-ttu-id="ec44f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec44f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec44f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec44f-128">-WhatIf</span></span>
<span data-ttu-id="ec44f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec44f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec44f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec44f-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec44f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec44f-131">CommonParameters</span></span>
<span data-ttu-id="ec44f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec44f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec44f-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec44f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec44f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec44f-134">INPUTS</span></span>

### <span data-ttu-id="ec44f-135">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="ec44f-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="ec44f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ec44f-136">System.String</span></span>

### <span data-ttu-id="ec44f-137">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ec44f-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="ec44f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec44f-138">OUTPUTS</span></span>

### <span data-ttu-id="ec44f-139">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="ec44f-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ec44f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec44f-140">NOTES</span></span>

## <span data-ttu-id="ec44f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec44f-141">RELATED LINKS</span></span>

[<span data-ttu-id="ec44f-142">Get-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="ec44f-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ec44f-143">Remove-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="ec44f-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ec44f-144">Set-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="ec44f-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)