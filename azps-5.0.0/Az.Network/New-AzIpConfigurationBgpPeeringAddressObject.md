---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277272"
---
# <span data-ttu-id="86abb-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="86abb-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="86abb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86abb-102">SYNOPSIS</span></span>
<span data-ttu-id="86abb-103">Yeni bir ıpconfigurationbgppeeringaddressobject oluşturur</span><span class="sxs-lookup"><span data-stu-id="86abb-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="86abb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="86abb-104">SYNTAX</span></span>

### <span data-ttu-id="86abb-105">Varsayılan (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="86abb-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="86abb-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="86abb-106">DESCRIPTION</span></span>
<span data-ttu-id="86abb-107">**New-Azıpconfigurationbgppeeringaddressobject** , sanal ağ geçidi bıgpsettings 'Unuzda BgpPeeringAddresses 'i temsil eden bir ıpconfigurationbgppeeringaddressobject nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="86abb-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="86abb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="86abb-108">EXAMPLES</span></span>

### <span data-ttu-id="86abb-109">1: AzIpConfigurationBgpPeeringAddressObject oluşturma</span><span class="sxs-lookup"><span data-stu-id="86abb-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="86abb-110">Yukarıdaki, bir ıpconfigurationbgppeeringaddressobject oluşturur. bu yeni nesne gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="86abb-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="86abb-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="86abb-111">PARAMETERS</span></span>

### <span data-ttu-id="86abb-112">-Onay</span><span class="sxs-lookup"><span data-stu-id="86abb-112">-Confirm</span></span>
<span data-ttu-id="86abb-113">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="86abb-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86abb-114">-Customadresi</span><span class="sxs-lookup"><span data-stu-id="86abb-114">-CustomAddress</span></span>
<span data-ttu-id="86abb-115">BgpPeeringAddresses için sanal ağ geçidi CustomAddress listesi.</span><span class="sxs-lookup"><span data-stu-id="86abb-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86abb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86abb-116">-DefaultProfile</span></span>
<span data-ttu-id="86abb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="86abb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86abb-118">-Ipconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="86abb-118">-IpConfigurationId</span></span>
<span data-ttu-id="86abb-119">BgpPeeringAddresses için sanal ağ geçidi ıpconfigurationıd.</span><span class="sxs-lookup"><span data-stu-id="86abb-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86abb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86abb-120">-WhatIf</span></span>
<span data-ttu-id="86abb-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="86abb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86abb-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="86abb-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86abb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86abb-123">CommonParameters</span></span>
<span data-ttu-id="86abb-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="86abb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86abb-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="86abb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86abb-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="86abb-126">INPUTS</span></span>

### <span data-ttu-id="86abb-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="86abb-127">None</span></span>

## <span data-ttu-id="86abb-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="86abb-128">OUTPUTS</span></span>

### <span data-ttu-id="86abb-129">Microsoft. Azure. Commands. Network. model. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="86abb-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="86abb-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="86abb-130">NOTES</span></span>

## <span data-ttu-id="86abb-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="86abb-131">RELATED LINKS</span></span>
