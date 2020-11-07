---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: c5c2481244de752a76eb1a1863d1fcc49d93ddb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932083"
---
# <span data-ttu-id="91d80-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="91d80-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="91d80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91d80-102">SYNOPSIS</span></span>
<span data-ttu-id="91d80-103">Bir NetworkInterface ile ilişkilendirilmiş bir TapConfiguration kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91d80-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="91d80-104">Bu, var olan bir VirtualNetworkTap kaynağına başvurur.</span><span class="sxs-lookup"><span data-stu-id="91d80-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="91d80-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91d80-105">SYNTAX</span></span>

### <span data-ttu-id="91d80-106">SetByResource (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91d80-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91d80-107">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="91d80-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91d80-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="91d80-108">DESCRIPTION</span></span>
<span data-ttu-id="91d80-109">**Add-Aznetworkınterfacetapconfig** cmdlet 'i, bir NetworkInterface ile Ilişkilendirilmiş bir tapconfiguration kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="91d80-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="91d80-110">Bu, var olan bir VirtualNetworkTap kaynağına başvurur.</span><span class="sxs-lookup"><span data-stu-id="91d80-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="91d80-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91d80-111">EXAMPLES</span></span>

### <span data-ttu-id="91d80-112">Örnek 1: verilen bir ağ arabirimine TapConfiguration ekleme</span><span class="sxs-lookup"><span data-stu-id="91d80-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="91d80-113">Bir kaynak.</span><span class="sxs-lookup"><span data-stu-id="91d80-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="91d80-114">Sourcenıc VM 'nin trafiği vVirtualNetworkTap kaynağında başvurulan hedef VM 'ye yansıtılır.</span><span class="sxs-lookup"><span data-stu-id="91d80-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="91d80-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91d80-115">PARAMETERS</span></span>

### <span data-ttu-id="91d80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d80-116">-DefaultProfile</span></span>
<span data-ttu-id="91d80-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91d80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d80-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="91d80-118">-Name</span></span>
<span data-ttu-id="91d80-119">Dokunun yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="91d80-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="91d80-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="91d80-120">-NetworkInterface</span></span>
<span data-ttu-id="91d80-121">Ağ arabirim kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="91d80-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="91d80-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="91d80-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="91d80-123">Sanal ağın başvurusu kaynak 'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="91d80-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="91d80-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="91d80-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="91d80-125">Sanal ağın başvurusu kaynak 'a dokunun.</span><span class="sxs-lookup"><span data-stu-id="91d80-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="91d80-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="91d80-126">-Confirm</span></span>
<span data-ttu-id="91d80-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91d80-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d80-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d80-128">-WhatIf</span></span>
<span data-ttu-id="91d80-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91d80-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91d80-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91d80-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91d80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d80-131">CommonParameters</span></span>
<span data-ttu-id="91d80-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91d80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d80-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91d80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d80-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91d80-134">INPUTS</span></span>

### <span data-ttu-id="91d80-135">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="91d80-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="91d80-136">System. String</span><span class="sxs-lookup"><span data-stu-id="91d80-136">System.String</span></span>

### <span data-ttu-id="91d80-137">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="91d80-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="91d80-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91d80-138">OUTPUTS</span></span>

### <span data-ttu-id="91d80-139">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="91d80-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="91d80-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91d80-140">NOTES</span></span>

## <span data-ttu-id="91d80-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91d80-141">RELATED LINKS</span></span>

[<span data-ttu-id="91d80-142">Get-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="91d80-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="91d80-143">Remove-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="91d80-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="91d80-144">Set-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="91d80-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)