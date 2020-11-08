---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279646"
---
# <span data-ttu-id="c5616-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="c5616-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="c5616-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5616-102">SYNOPSIS</span></span>
<span data-ttu-id="c5616-103">Sağlanan alt ağdan bir hizmet temsilcisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5616-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="c5616-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5616-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5616-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5616-105">DESCRIPTION</span></span>
<span data-ttu-id="c5616-106">**Remove-Aztemsilci** cmdlet 'i, temsilcileri olan bir alt ağı alır ve bu alt ağdan adlandırılmış temsilciyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c5616-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="c5616-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5616-107">EXAMPLES</span></span>

### <span data-ttu-id="c5616-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c5616-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="c5616-109">Bu örnekte, ilk yarısı ( _"var olan alt ağa Temsilci Ekle"_ nın altında bulunan), [Add-aztemsilci](./Add-AzDelegation.md)ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="c5616-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="c5616-110">İkinci yarısında, ilk iki cmdlet ilgilendiğiniz alt ağı alır ve Yerel kopyayı sunucuda olduğu gibi yenileyin.</span><span class="sxs-lookup"><span data-stu-id="c5616-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="c5616-111">Üçüncü cmdlet _mysubnet_ 'den ilk yarısı oluşturulmuş temsilciyi kaldırır ve güncelleştirilen alt ağı _$subnet_ olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="c5616-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="c5616-112">Son cmdlet, sunucuyu kaldırılan temsilciyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c5616-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="c5616-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5616-113">PARAMETERS</span></span>

### <span data-ttu-id="c5616-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5616-114">-DefaultProfile</span></span>
<span data-ttu-id="c5616-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c5616-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5616-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5616-116">-Name</span></span>
<span data-ttu-id="c5616-117">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="c5616-117">The name of the delegation</span></span>

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

### <span data-ttu-id="c5616-118">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="c5616-118">-Subnet</span></span>
<span data-ttu-id="c5616-119">Temsilci seçiminin kaldırılacağı alt ağ</span><span class="sxs-lookup"><span data-stu-id="c5616-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="c5616-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5616-120">CommonParameters</span></span>
<span data-ttu-id="c5616-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5616-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5616-122">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5616-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5616-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5616-123">INPUTS</span></span>

### <span data-ttu-id="c5616-124">System. String</span><span class="sxs-lookup"><span data-stu-id="c5616-124">System.String</span></span>

### <span data-ttu-id="c5616-125">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c5616-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c5616-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5616-126">OUTPUTS</span></span>

### <span data-ttu-id="c5616-127">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c5616-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c5616-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5616-128">NOTES</span></span>

## <span data-ttu-id="c5616-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5616-129">RELATED LINKS</span></span>

<span data-ttu-id="c5616-130">[Add-Aztemsilci](./Add-AzDelegation.md) 
 [Get-Aztemsilci](./Get-AzDelegation.md) 
 [Yeni-Aztemsilci](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="c5616-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>