---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: fffc77c4cfdd74a910086befb88d665351ae36a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760463"
---
# <span data-ttu-id="e6f71-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="e6f71-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="e6f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f71-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f71-103">Sanal ağ geçerli kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="e6f71-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="e6f71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6f71-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6f71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6f71-105">DESCRIPTION</span></span>
<span data-ttu-id="e6f71-106">**Get-AzVirtualNetworkUsageList** cmdlet 'i belirtilen sanal ağın alt ağ kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="e6f71-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="e6f71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6f71-107">EXAMPLES</span></span>

### <span data-ttu-id="e6f71-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6f71-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="e6f71-109">Usage test sanal ağı için alt ağ başına geçerli değer değerlerini alır.</span><span class="sxs-lookup"><span data-stu-id="e6f71-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="e6f71-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6f71-110">PARAMETERS</span></span>

### <span data-ttu-id="e6f71-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f71-111">-DefaultProfile</span></span>
<span data-ttu-id="e6f71-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e6f71-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6f71-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e6f71-113">-Name</span></span>
<span data-ttu-id="e6f71-114">Kullanımları gösterilecek sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6f71-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="e6f71-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f71-115">-ResourceGroupName</span></span>
<span data-ttu-id="e6f71-116">Sanal ağın ait olduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e6f71-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="e6f71-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f71-117">CommonParameters</span></span>
<span data-ttu-id="e6f71-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6f71-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f71-119">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e6f71-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f71-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6f71-120">INPUTS</span></span>

### <span data-ttu-id="e6f71-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f71-121">System.String</span></span>

## <span data-ttu-id="e6f71-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6f71-122">OUTPUTS</span></span>

### <span data-ttu-id="e6f71-123">Microsoft. Azure. Commands. Network. model. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="e6f71-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="e6f71-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6f71-124">NOTES</span></span>

## <span data-ttu-id="e6f71-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6f71-125">RELATED LINKS</span></span>
