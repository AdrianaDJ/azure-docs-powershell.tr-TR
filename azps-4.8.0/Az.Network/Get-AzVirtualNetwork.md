---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266520"
---
# <span data-ttu-id="0a022-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a022-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="0a022-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a022-102">SYNOPSIS</span></span>
<span data-ttu-id="0a022-103">Kaynak grubunda sanal ağ alır.</span><span class="sxs-lookup"><span data-stu-id="0a022-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="0a022-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a022-104">SYNTAX</span></span>

### <span data-ttu-id="0a022-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="0a022-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0a022-106">Geniþ</span><span class="sxs-lookup"><span data-stu-id="0a022-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a022-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a022-107">DESCRIPTION</span></span>
<span data-ttu-id="0a022-108">**Get-AzVirtualNetwork** cmdlet 'i bir veya daha fazla sanal ağı bir kaynak grubuna alır.</span><span class="sxs-lookup"><span data-stu-id="0a022-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="0a022-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a022-109">EXAMPLES</span></span>

### <span data-ttu-id="0a022-110">1: sanal ağ alma</span><span class="sxs-lookup"><span data-stu-id="0a022-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="0a022-111">Bu komut TestResourceGroup kaynak grubunda MyVirtualNetwork adındaki sanal ağı alır</span><span class="sxs-lookup"><span data-stu-id="0a022-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="0a022-112">2: filtre kullanarak sanal ağları listeleme</span><span class="sxs-lookup"><span data-stu-id="0a022-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="0a022-113">Bu komut, "MyVirtualNetwork" ile başlayan tüm sanal ağları alır.</span><span class="sxs-lookup"><span data-stu-id="0a022-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="0a022-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a022-114">PARAMETERS</span></span>

### <span data-ttu-id="0a022-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a022-115">-DefaultProfile</span></span>
<span data-ttu-id="0a022-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a022-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a022-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="0a022-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a022-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="0a022-118">-Name</span></span>
<span data-ttu-id="0a022-119">Bu cmdlet 'in aldığı sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a022-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0a022-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a022-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a022-121">Sanal ağın ait olduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a022-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0a022-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a022-122">CommonParameters</span></span>
<span data-ttu-id="0a022-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a022-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a022-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0a022-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a022-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a022-125">INPUTS</span></span>

### <span data-ttu-id="0a022-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0a022-126">System.String</span></span>

## <span data-ttu-id="0a022-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a022-127">OUTPUTS</span></span>

### <span data-ttu-id="0a022-128">Microsoft. Azure. Commands. Network. modeller. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a022-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="0a022-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a022-129">NOTES</span></span>

## <span data-ttu-id="0a022-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a022-130">RELATED LINKS</span></span>

[<span data-ttu-id="0a022-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a022-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="0a022-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a022-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="0a022-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a022-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


