---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 4b6f253da0c2494db49883402be8f39f5ef80ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932037"
---
# <span data-ttu-id="60e1b-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="60e1b-101">Get-AzDelegation</span></span>

## <span data-ttu-id="60e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="60e1b-103">Verilen bir alt ağda bir temsilci (veya tüm temsilcileri) edinin.</span><span class="sxs-lookup"><span data-stu-id="60e1b-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="60e1b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60e1b-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60e1b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="60e1b-105">DESCRIPTION</span></span>
<span data-ttu-id="60e1b-106">**Get-aztemsilci** cmdlet 'i, bir alt ağdan adlandırılmış temsilciyi alır.</span><span class="sxs-lookup"><span data-stu-id="60e1b-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="60e1b-107">Herhangi bir temsilci adı adlandırılmadıysa, sağlanan alt ağdaki tüm temsilcileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="60e1b-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="60e1b-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60e1b-108">EXAMPLES</span></span>

### <span data-ttu-id="60e1b-109">1: belirli bir temsilci alma</span><span class="sxs-lookup"><span data-stu-id="60e1b-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="60e1b-110">İlk satır ilgi alt ağını alır.</span><span class="sxs-lookup"><span data-stu-id="60e1b-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="60e1b-111">İkinci satır "Benimtemsilci" adlı temsilci için temsilci bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="60e1b-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="60e1b-112">2: tüm alt ağ temsilcileri alınıyor</span><span class="sxs-lookup"><span data-stu-id="60e1b-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="60e1b-113">İlk satır ilgi alt ağını alır.</span><span class="sxs-lookup"><span data-stu-id="60e1b-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="60e1b-114">İkinci satır, _Mysubnet_ 'teki tüm temsilci listesini $Delegations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="60e1b-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="60e1b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60e1b-115">PARAMETERS</span></span>

### <span data-ttu-id="60e1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e1b-116">-DefaultProfile</span></span>
<span data-ttu-id="60e1b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60e1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e1b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="60e1b-118">-Name</span></span>
<span data-ttu-id="60e1b-119">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="60e1b-119">The name of the delegation</span></span>

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

### <span data-ttu-id="60e1b-120">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="60e1b-120">-Subnet</span></span>
<span data-ttu-id="60e1b-121">Alt ağ</span><span class="sxs-lookup"><span data-stu-id="60e1b-121">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60e1b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e1b-122">CommonParameters</span></span>
<span data-ttu-id="60e1b-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60e1b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e1b-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="60e1b-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e1b-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60e1b-125">INPUTS</span></span>

### <span data-ttu-id="60e1b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="60e1b-126">System.String</span></span>

### <span data-ttu-id="60e1b-127">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="60e1b-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="60e1b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60e1b-128">OUTPUTS</span></span>

### <span data-ttu-id="60e1b-129">Microsoft.Azure.Commands.Network.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="60e1b-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="60e1b-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60e1b-130">NOTES</span></span>

## <span data-ttu-id="60e1b-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60e1b-131">RELATED LINKS</span></span>

<span data-ttu-id="60e1b-132">[Add-Aztemsilci](./Add-AzDelegation.md) 
 [Yeni-Aztemsilci](./New-AzDelegation.md) 
 [Remove-Aztemsilci](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="60e1b-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>