---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594360"
---
# <span data-ttu-id="afc31-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="afc31-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="afc31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afc31-102">SYNOPSIS</span></span>
<span data-ttu-id="afc31-103">Sanal ağ seçeneğine dokunun.</span><span class="sxs-lookup"><span data-stu-id="afc31-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afc31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afc31-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afc31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="afc31-105">DESCRIPTION</span></span>
<span data-ttu-id="afc31-106">**Set-AzureRmVirtualNetworkTap** , bir Azure sanal ağ öğesine dokunun.</span><span class="sxs-lookup"><span data-stu-id="afc31-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="afc31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afc31-107">EXAMPLES</span></span>

### <span data-ttu-id="afc31-108">Örnek 1: sanal bir ağ yapılandırma</span><span class="sxs-lookup"><span data-stu-id="afc31-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="afc31-109">Komut hedef IP yapılandırması 'nı güncelleştirir ve sanal ağı dokunun.</span><span class="sxs-lookup"><span data-stu-id="afc31-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="afc31-110">Başvuruda bulunan herhangi bir dokun yapılandırması varsa, tüm kaynak trafiği, yeni hedef IP yapılandırması sonrası güncellemesine başlatılmaz.</span><span class="sxs-lookup"><span data-stu-id="afc31-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="afc31-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afc31-111">PARAMETERS</span></span>

### <span data-ttu-id="afc31-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="afc31-112">-AsJob</span></span>
<span data-ttu-id="afc31-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="afc31-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afc31-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afc31-114">-DefaultProfile</span></span>
<span data-ttu-id="afc31-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afc31-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afc31-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="afc31-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="afc31-117">Sanal ağ</span><span class="sxs-lookup"><span data-stu-id="afc31-117">The virtual network tap</span></span>

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

### <span data-ttu-id="afc31-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="afc31-118">-Confirm</span></span>
<span data-ttu-id="afc31-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afc31-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afc31-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afc31-120">-WhatIf</span></span>
<span data-ttu-id="afc31-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afc31-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afc31-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afc31-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afc31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afc31-123">CommonParameters</span></span>
<span data-ttu-id="afc31-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afc31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afc31-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afc31-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afc31-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afc31-126">INPUTS</span></span>

### <span data-ttu-id="afc31-127">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="afc31-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="afc31-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afc31-128">OUTPUTS</span></span>

### <span data-ttu-id="afc31-129">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="afc31-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="afc31-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afc31-130">NOTES</span></span>

## <span data-ttu-id="afc31-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afc31-131">RELATED LINKS</span></span>
