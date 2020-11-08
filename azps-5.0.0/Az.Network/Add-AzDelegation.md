---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzDelegation.md
ms.openlocfilehash: c915f2e95c8912a071fd949a6c231a1eff79b97b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275266"
---
# <span data-ttu-id="c925b-101">Add-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="c925b-101">Add-AzDelegation</span></span>

## <span data-ttu-id="c925b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c925b-102">SYNOPSIS</span></span>
<span data-ttu-id="c925b-103">Alt ağa temsilci ekler.</span><span class="sxs-lookup"><span data-stu-id="c925b-103">Adds a delegation to a subnet.</span></span>

## <span data-ttu-id="c925b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c925b-104">SYNTAX</span></span>

```
Add-AzDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c925b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c925b-105">DESCRIPTION</span></span>
<span data-ttu-id="c925b-106">**Add-Aztemsilci** cmdlet 'i, bir Azure alt ağına bir hizmet temsilcisi ekler.</span><span class="sxs-lookup"><span data-stu-id="c925b-106">The **Add-AzDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="c925b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c925b-107">EXAMPLES</span></span>

### <span data-ttu-id="c925b-108">Örnek 1: temsilci ekleme</span><span class="sxs-lookup"><span data-stu-id="c925b-108">Example 1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="c925b-109">İlk komut, alt ağın bulunduğu sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="c925b-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="c925b-110">İkinci komut faiz alt ağını, temsilci seçmek istediğiniz alt ağı yalıtır.</span><span class="sxs-lookup"><span data-stu-id="c925b-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="c925b-111">Üçüncü komut, alt ağa bir temsilci ekler.</span><span class="sxs-lookup"><span data-stu-id="c925b-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="c925b-112">Bu belirli örnek, SQL 'i bu alt ağda arabirim uç noktaları oluşturacak şekilde etkinleştirmek istediğinizde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="c925b-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="c925b-113">Son komutu, alt ağı gerçekten güncelleştirmek için güncelleştirilmiş alt ağı sunucuya gönderir.</span><span class="sxs-lookup"><span data-stu-id="c925b-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="c925b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c925b-114">PARAMETERS</span></span>

### <span data-ttu-id="c925b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c925b-115">-DefaultProfile</span></span>
<span data-ttu-id="c925b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c925b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c925b-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c925b-117">-Name</span></span>
<span data-ttu-id="c925b-118">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="c925b-118">The name of the delegation</span></span>

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

### <span data-ttu-id="c925b-119">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="c925b-119">-ServiceName</span></span>
<span data-ttu-id="c925b-120">Alt ağın temsil ettiği hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="c925b-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="c925b-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="c925b-121">-Subnet</span></span>
<span data-ttu-id="c925b-122">Alt ağ</span><span class="sxs-lookup"><span data-stu-id="c925b-122">The subnet</span></span>

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

### <span data-ttu-id="c925b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c925b-123">CommonParameters</span></span>
<span data-ttu-id="c925b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c925b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c925b-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c925b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c925b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c925b-126">INPUTS</span></span>

### <span data-ttu-id="c925b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c925b-127">System.String</span></span>

### <span data-ttu-id="c925b-128">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c925b-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c925b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c925b-129">OUTPUTS</span></span>

### <span data-ttu-id="c925b-130">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="c925b-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="c925b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c925b-131">NOTES</span></span>

## <span data-ttu-id="c925b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c925b-132">RELATED LINKS</span></span>

<span data-ttu-id="c925b-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="c925b-133">[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>