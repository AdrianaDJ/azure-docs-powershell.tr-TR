---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 84FDB0F7-E6DE-4E1B-BD71-89535EDC6AA1
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azeffectiveroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzEffectiveRouteTable.md
ms.openlocfilehash: e7d65e7797fb606306f0f0cc1e7c394fcf3d1d3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266061"
---
# <span data-ttu-id="45fed-101">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="45fed-101">Get-AzEffectiveRouteTable</span></span>

## <span data-ttu-id="45fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45fed-102">SYNOPSIS</span></span>
<span data-ttu-id="45fed-103">Ağ arabiriminin etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="45fed-103">Gets the effective route table of a network interface.</span></span>

## <span data-ttu-id="45fed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="45fed-104">SYNTAX</span></span>

```
Get-AzEffectiveRouteTable -NetworkInterfaceName <String> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45fed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="45fed-105">DESCRIPTION</span></span>
<span data-ttu-id="45fed-106">**Get-AzEffectiveRouteTable** cmdlet 'i, bir ağ arabirimine uygulanan etkin yol tablosunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="45fed-106">The **Get-AzEffectiveRouteTable** cmdlet returns the effective route table that is applied on a network interface.</span></span>

## <span data-ttu-id="45fed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="45fed-107">EXAMPLES</span></span>

### <span data-ttu-id="45fed-108">Örnek 1: ağ arabiriminde etkin yol tablosunu alma</span><span class="sxs-lookup"><span data-stu-id="45fed-108">Example 1: Get the effective route table on a network interface</span></span>
```
PS C:\>Get-AzEffectiveRouteTable -NetworkInterfaceName "MyNetworkInterface" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="45fed-109">Bu komut MyResourceGroup adlı kaynak grubundaki MyNetworkInterface adlı ağ arabirimiyle ilişkili etkin yol tablosunu alır.</span><span class="sxs-lookup"><span data-stu-id="45fed-109">This command gets the effective route table associated with network interface named MyNetworkInterface in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="45fed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="45fed-110">PARAMETERS</span></span>

### <span data-ttu-id="45fed-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="45fed-111">-AsJob</span></span>
<span data-ttu-id="45fed-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="45fed-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45fed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fed-113">-DefaultProfile</span></span>
<span data-ttu-id="45fed-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="45fed-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45fed-115">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="45fed-115">-NetworkInterfaceName</span></span>
<span data-ttu-id="45fed-116">Ağ arabiriminin adı belirtildi.</span><span class="sxs-lookup"><span data-stu-id="45fed-116">Specified the name of a network interface.</span></span>

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

### <span data-ttu-id="45fed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45fed-117">-ResourceGroupName</span></span>
<span data-ttu-id="45fed-118">Ağ arabiriminin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="45fed-118">Specifies the resource group of a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fed-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fed-119">CommonParameters</span></span>
<span data-ttu-id="45fed-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="45fed-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fed-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="45fed-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fed-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="45fed-122">INPUTS</span></span>

### <span data-ttu-id="45fed-123">System. String</span><span class="sxs-lookup"><span data-stu-id="45fed-123">System.String</span></span>

## <span data-ttu-id="45fed-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="45fed-124">OUTPUTS</span></span>

### <span data-ttu-id="45fed-125">Microsoft. Azure. Commands. Network. modeller. PSEffectiveRoute</span><span class="sxs-lookup"><span data-stu-id="45fed-125">Microsoft.Azure.Commands.Network.Models.PSEffectiveRoute</span></span>

## <span data-ttu-id="45fed-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="45fed-126">NOTES</span></span>

## <span data-ttu-id="45fed-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="45fed-127">RELATED LINKS</span></span>

[<span data-ttu-id="45fed-128">Get-AzEffectiveNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="45fed-128">Get-AzEffectiveNetworkSecurityGroup</span></span>](./Get-AzEffectiveNetworkSecurityGroup.md)


