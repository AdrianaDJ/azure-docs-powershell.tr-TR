---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592762"
---
# <span data-ttu-id="5e4c4-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="5e4c4-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="5e4c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="5e4c4-103">Verilen bir alt ağda bir temsilci (veya tüm temsilcileri) edinin.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e4c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e4c4-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e4c4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e4c4-105">DESCRIPTION</span></span>
<span data-ttu-id="5e4c4-106">**Get-Azurermtemsilci** cmdlet 'i alt ağdan adlandırılmış temsilciyi alır.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="5e4c4-107">Herhangi bir temsilci adı adlandırılmadıysa, sağlanan alt ağdaki tüm temsilcileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="5e4c4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e4c4-108">EXAMPLES</span></span>

### <span data-ttu-id="5e4c4-109">1: belirli bir temsilci alma</span><span class="sxs-lookup"><span data-stu-id="5e4c4-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="5e4c4-110">İlk satır ilgi alt ağını alır.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="5e4c4-111">İkinci satır "Benimtemsilci" adlı temsilci için temsilci bilgilerini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="5e4c4-112">2: tüm alt ağ temsilcileri alınıyor</span><span class="sxs-lookup"><span data-stu-id="5e4c4-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="5e4c4-113">İlk satır ilgi alt ağını alır.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="5e4c4-114">İkinci satır, _Mysubnet_ 'teki tüm temsilci listesini $Delegations değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="5e4c4-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e4c4-115">PARAMETERS</span></span>

### <span data-ttu-id="5e4c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e4c4-116">-DefaultProfile</span></span>
<span data-ttu-id="5e4c4-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4c4-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="5e4c4-118">-Name</span></span>
<span data-ttu-id="5e4c4-119">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="5e4c4-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e4c4-120">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="5e4c4-120">-Subnet</span></span>
<span data-ttu-id="5e4c4-121">Alt ağ</span><span class="sxs-lookup"><span data-stu-id="5e4c4-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e4c4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e4c4-122">CommonParameters</span></span>
<span data-ttu-id="5e4c4-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e4c4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5e4c4-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e4c4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e4c4-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e4c4-125">INPUTS</span></span>

### <span data-ttu-id="5e4c4-126">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5e4c4-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5e4c4-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e4c4-127">OUTPUTS</span></span>

### <span data-ttu-id="5e4c4-128">Microsoft.Azure.Commands.Network.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="5e4c4-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="5e4c4-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e4c4-129">NOTES</span></span>

## <span data-ttu-id="5e4c4-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e4c4-130">RELATED LINKS</span></span>
<span data-ttu-id="5e4c4-131">[Add-Azurermtemsilci](./Add-AzureRmDelegation.md) 
 [Yeni-Azurermtemsilci](./New-AzureRmDelegation.md) 
 [Remove-Azurermtemsilci](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="5e4c4-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
