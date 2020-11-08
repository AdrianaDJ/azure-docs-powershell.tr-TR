---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096130"
---
# <span data-ttu-id="acbba-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="acbba-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="acbba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acbba-102">SYNOPSIS</span></span>
<span data-ttu-id="acbba-103">Sanal bir ağı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="acbba-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="acbba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acbba-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acbba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acbba-105">DESCRIPTION</span></span>
<span data-ttu-id="acbba-106">**Set-AzVirtualNetworkTap** cmdlet 'i sanal bir ağ öğesine dokunun.</span><span class="sxs-lookup"><span data-stu-id="acbba-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="acbba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acbba-107">EXAMPLES</span></span>

### <span data-ttu-id="acbba-108">Örnek 1: sanal bir ağ yapılandırma</span><span class="sxs-lookup"><span data-stu-id="acbba-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="acbba-109">Komut hedef IP yapılandırması 'nı güncelleştirir ve sanal ağı dokunun.</span><span class="sxs-lookup"><span data-stu-id="acbba-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="acbba-110">Başvuruda bulunan herhangi bir dokun yapılandırması varsa, tüm kaynak trafiği, yeni hedef IP yapılandırması sonrası güncellemesine başlatılmaz.</span><span class="sxs-lookup"><span data-stu-id="acbba-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="acbba-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acbba-111">PARAMETERS</span></span>

### <span data-ttu-id="acbba-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="acbba-112">-AsJob</span></span>
<span data-ttu-id="acbba-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="acbba-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="acbba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbba-114">-DefaultProfile</span></span>
<span data-ttu-id="acbba-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="acbba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acbba-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="acbba-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="acbba-117">Sanal ağ</span><span class="sxs-lookup"><span data-stu-id="acbba-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="acbba-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="acbba-118">-Confirm</span></span>
<span data-ttu-id="acbba-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acbba-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acbba-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acbba-120">-WhatIf</span></span>
<span data-ttu-id="acbba-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acbba-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acbba-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acbba-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acbba-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbba-123">CommonParameters</span></span>
<span data-ttu-id="acbba-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acbba-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbba-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acbba-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbba-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acbba-126">INPUTS</span></span>

### <span data-ttu-id="acbba-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="acbba-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="acbba-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acbba-128">OUTPUTS</span></span>

### <span data-ttu-id="acbba-129">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="acbba-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="acbba-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acbba-130">NOTES</span></span>

## <span data-ttu-id="acbba-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acbba-131">RELATED LINKS</span></span>

[<span data-ttu-id="acbba-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="acbba-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="acbba-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="acbba-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="acbba-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="acbba-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)