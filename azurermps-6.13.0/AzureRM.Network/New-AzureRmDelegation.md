---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592296"
---
# <span data-ttu-id="4ee31-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="4ee31-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="4ee31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee31-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee31-103">Hizmet temsilcisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ee31-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ee31-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ee31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ee31-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee31-106">**Yeni-Azurermtemsilci** cmdlet 'i, alt ağa eklenebilen bir hizmet temsilcisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4ee31-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="4ee31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ee31-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee31-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4ee31-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="4ee31-109">İlk cmdlet, bir alt ağa eklenebilen bir temsilci oluşturur ve $delegation değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4ee31-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="4ee31-110">İkinci ve üçüncü cmdlet 'ler, temsil edilecek alt ağı alır.</span><span class="sxs-lookup"><span data-stu-id="4ee31-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="4ee31-111">Dördüncü cmdlet, oluşturulan temsilciyi ilgili alt ağa ekler ve son cmdlet güncelleştirilmiş yapılandırmayı sunucuya gönderir.</span><span class="sxs-lookup"><span data-stu-id="4ee31-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="4ee31-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ee31-112">PARAMETERS</span></span>

### <span data-ttu-id="4ee31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee31-113">-DefaultProfile</span></span>
<span data-ttu-id="4ee31-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ee31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ee31-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ee31-115">-Name</span></span>
<span data-ttu-id="4ee31-116">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="4ee31-116">The name of the delegation</span></span>

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

### <span data-ttu-id="4ee31-117">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="4ee31-117">-ServiceName</span></span>
<span data-ttu-id="4ee31-118">Alt ağın temsil ettiği hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="4ee31-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="4ee31-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee31-119">CommonParameters</span></span>
<span data-ttu-id="4ee31-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ee31-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4ee31-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee31-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee31-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ee31-122">INPUTS</span></span>

### <span data-ttu-id="4ee31-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee31-123">System.String</span></span>

## <span data-ttu-id="4ee31-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ee31-124">OUTPUTS</span></span>

### <span data-ttu-id="4ee31-125">Microsoft.Azure.Commands.Network.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="4ee31-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="4ee31-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ee31-126">NOTES</span></span>

## <span data-ttu-id="4ee31-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ee31-127">RELATED LINKS</span></span>
<span data-ttu-id="4ee31-128">[Add-Azurermtemsilci](./Add-AzureRmDelegation.md) 
 [Get-Azurermtemsilci](./Get-AzureRmDelegation.md) 
 [Remove-Azurermtemsilci](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="4ee31-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
