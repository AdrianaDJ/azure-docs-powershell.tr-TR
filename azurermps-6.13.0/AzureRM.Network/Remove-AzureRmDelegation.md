---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764338"
---
# <span data-ttu-id="f3db3-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="f3db3-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="f3db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3db3-102">SYNOPSIS</span></span>
<span data-ttu-id="f3db3-103">Sağlanan alt ağdan bir hizmet temsilcisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3db3-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3db3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3db3-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3db3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3db3-105">DESCRIPTION</span></span>
<span data-ttu-id="f3db3-106">**Remove-Azurermtemsilci** cmdlet 'i, temsilcileri olan bir alt ağı alır ve bu alt ağdan adlandırılmış temsilciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f3db3-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="f3db3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3db3-107">EXAMPLES</span></span>

### <span data-ttu-id="f3db3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3db3-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="f3db3-109">Bu örnekte, ilk yarısı ( _"varolan bir alt ağa Temsilci Ekle"_ altında bulunan), [-Azurermtemsilci ekleme](./Add-AzureRmDelegation.md)ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="f3db3-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="f3db3-110">İkinci yarısında, ilk iki cmdlet ilgilendiğiniz alt ağı alır ve Yerel kopyayı sunucuda olduğu gibi yenileyin.</span><span class="sxs-lookup"><span data-stu-id="f3db3-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="f3db3-111">Üçüncü cmdlet _mysubnet_ 'den ilk yarısı oluşturulmuş temsilciyi kaldırır ve güncelleştirilen alt ağı _$subnet_ olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="f3db3-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="f3db3-112">Son cmdlet, sunucuyu kaldırılan temsilciyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f3db3-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="f3db3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3db3-113">PARAMETERS</span></span>

### <span data-ttu-id="f3db3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3db3-114">-DefaultProfile</span></span>
<span data-ttu-id="f3db3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3db3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3db3-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3db3-116">-Name</span></span>
<span data-ttu-id="f3db3-117">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="f3db3-117">The name of the delegation</span></span>

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

### <span data-ttu-id="f3db3-118">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="f3db3-118">-ServiceName</span></span>
<span data-ttu-id="f3db3-119">Alt ağın temsil ettiği hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="f3db3-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="f3db3-120">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="f3db3-120">-Subnet</span></span>
<span data-ttu-id="f3db3-121">Temsilci seçiminin kaldırılacağı alt ağ</span><span class="sxs-lookup"><span data-stu-id="f3db3-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="f3db3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3db3-122">CommonParameters</span></span>
<span data-ttu-id="f3db3-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3db3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3db3-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3db3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3db3-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3db3-125">INPUTS</span></span>

### <span data-ttu-id="f3db3-126">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f3db3-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="f3db3-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f3db3-127">System.String</span></span>
## <span data-ttu-id="f3db3-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3db3-128">OUTPUTS</span></span>

### <span data-ttu-id="f3db3-129">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f3db3-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="f3db3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3db3-130">NOTES</span></span>

## <span data-ttu-id="f3db3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3db3-131">RELATED LINKS</span></span>

<span data-ttu-id="f3db3-132">[Add-Azurermtemsilci](./Add-AzureRmDelegation.md) 
 [Get-Azurermtemsilci](./Get-AzureRmDelegation.md) 
 [Yeni-Azurermtemsilci](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="f3db3-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>