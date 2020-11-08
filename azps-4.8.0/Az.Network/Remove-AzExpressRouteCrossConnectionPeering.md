---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 4309550557480211560e108489b14850672ee1f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274093"
---
# <span data-ttu-id="ca599-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ca599-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ca599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca599-102">SYNOPSIS</span></span>
<span data-ttu-id="ca599-103">ExpressRoute çapraz bağlantı eşlemesi yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca599-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ca599-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca599-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca599-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca599-105">DESCRIPTION</span></span>
<span data-ttu-id="ca599-106">**Remove-Azexpressroutecrossconnectioneşlemecmdlet** 'ı bir ExpressRoute çapraz bağlantı eşlemesi yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca599-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ca599-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca599-107">EXAMPLES</span></span>

### <span data-ttu-id="ca599-108">Örnek 1: ExpressRoute çapraz bağlantısından eşleme yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ca599-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="ca599-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca599-109">PARAMETERS</span></span>

### <span data-ttu-id="ca599-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca599-110">-DefaultProfile</span></span>
<span data-ttu-id="ca599-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca599-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca599-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca599-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ca599-113">Kaldırılacak eşleme yapılandırmasını içeren ExpressRoute çapraz bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="ca599-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca599-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ca599-114">-Force</span></span>
<span data-ttu-id="ca599-115">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="ca599-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="ca599-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca599-116">-Name</span></span>
<span data-ttu-id="ca599-117">Kaldırılacak olan eşleme yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="ca599-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca599-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ca599-118">-PeerAddressType</span></span>
<span data-ttu-id="ca599-119">Eşün adres ailesi</span><span class="sxs-lookup"><span data-stu-id="ca599-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca599-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca599-120">-Confirm</span></span>
<span data-ttu-id="ca599-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca599-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca599-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca599-122">-WhatIf</span></span>
<span data-ttu-id="ca599-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca599-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca599-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca599-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca599-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca599-125">CommonParameters</span></span>
<span data-ttu-id="ca599-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca599-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca599-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca599-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca599-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca599-128">INPUTS</span></span>

### <span data-ttu-id="ca599-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca599-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ca599-130">' ExpressRouteCrossConnection ' parametresi ardışık düzenin ' PSExpressRouteCrossConnection ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ca599-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ca599-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca599-131">OUTPUTS</span></span>

### <span data-ttu-id="ca599-132">Microsoft. Azure. Commands. Network. model. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca599-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="ca599-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca599-133">NOTES</span></span>

## <span data-ttu-id="ca599-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca599-134">RELATED LINKS</span></span>

[<span data-ttu-id="ca599-135">Add-azexpressroutecrossconnectioneşleme</span><span class="sxs-lookup"><span data-stu-id="ca599-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ca599-136">Get-azexpressroutecrossconnectioneşleme</span><span class="sxs-lookup"><span data-stu-id="ca599-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ca599-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca599-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ca599-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ca599-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
