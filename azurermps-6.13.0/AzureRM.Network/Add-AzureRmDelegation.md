---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593218"
---
# <span data-ttu-id="61864-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="61864-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="61864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61864-102">SYNOPSIS</span></span>
<span data-ttu-id="61864-103">Alt ağa temsilci ekler.</span><span class="sxs-lookup"><span data-stu-id="61864-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61864-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61864-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61864-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61864-105">DESCRIPTION</span></span>
<span data-ttu-id="61864-106">**Add-Azurermtemsilci** cmdlet 'ı bir Azure alt ağına bir hizmet temsilcisi ekler.</span><span class="sxs-lookup"><span data-stu-id="61864-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="61864-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61864-107">EXAMPLES</span></span>

### <span data-ttu-id="61864-108">1: temsilci ekleme</span><span class="sxs-lookup"><span data-stu-id="61864-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="61864-109">İlk komut, alt ağın bulunduğu sanal ağı alır.</span><span class="sxs-lookup"><span data-stu-id="61864-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="61864-110">İkinci komut faiz alt ağını, temsilci seçmek istediğiniz alt ağı yalıtır.</span><span class="sxs-lookup"><span data-stu-id="61864-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="61864-111">Üçüncü komut, alt ağa bir temsilci ekler.</span><span class="sxs-lookup"><span data-stu-id="61864-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="61864-112">Bu belirli örnek, SQL 'i bu alt ağda arabirim uç noktaları oluşturacak şekilde etkinleştirmek istediğinizde yararlı olabilir.</span><span class="sxs-lookup"><span data-stu-id="61864-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="61864-113">Son komutu, alt ağı gerçekten güncelleştirmek için güncelleştirilmiş alt ağı sunucuya gönderir.</span><span class="sxs-lookup"><span data-stu-id="61864-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="61864-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61864-114">PARAMETERS</span></span>

### <span data-ttu-id="61864-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61864-115">-DefaultProfile</span></span>
<span data-ttu-id="61864-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61864-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61864-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="61864-117">-Name</span></span>
<span data-ttu-id="61864-118">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="61864-118">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61864-119">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="61864-119">-ServiceName</span></span>
<span data-ttu-id="61864-120">Alt ağın temsil ettiği hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="61864-120">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61864-121">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="61864-121">-Subnet</span></span>
<span data-ttu-id="61864-122">Alt ağ</span><span class="sxs-lookup"><span data-stu-id="61864-122">The subnet</span></span>

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

### <span data-ttu-id="61864-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61864-123">CommonParameters</span></span>
<span data-ttu-id="61864-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61864-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="61864-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61864-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61864-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61864-126">INPUTS</span></span>

### <span data-ttu-id="61864-127">System. String</span><span class="sxs-lookup"><span data-stu-id="61864-127">System.String</span></span>

### <span data-ttu-id="61864-128">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="61864-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="61864-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61864-129">OUTPUTS</span></span>

### <span data-ttu-id="61864-130">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="61864-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="61864-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61864-131">NOTES</span></span>

## <span data-ttu-id="61864-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61864-132">RELATED LINKS</span></span>
<span data-ttu-id="61864-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="61864-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
