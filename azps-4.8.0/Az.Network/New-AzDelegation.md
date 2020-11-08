---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268486"
---
# <span data-ttu-id="00829-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="00829-101">New-AzDelegation</span></span>

## <span data-ttu-id="00829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00829-102">SYNOPSIS</span></span>
<span data-ttu-id="00829-103">Hizmet temsilcisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00829-103">Creates a service delegation.</span></span>

## <span data-ttu-id="00829-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00829-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00829-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00829-105">DESCRIPTION</span></span>
<span data-ttu-id="00829-106">**New-Aztemsilci** cmdlet 'i, alt ağa eklenebilen bir hizmet temsilcisi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00829-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="00829-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00829-107">EXAMPLES</span></span>

### <span data-ttu-id="00829-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="00829-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="00829-109">İlk cmdlet, bir alt ağa eklenebilen bir temsilci oluşturur ve $delegation değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="00829-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="00829-110">İkinci ve üçüncü cmdlet 'ler, temsil edilecek alt ağı alır.</span><span class="sxs-lookup"><span data-stu-id="00829-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="00829-111">Dördüncü cmdlet, oluşturulan temsilciyi ilgili alt ağa ekler ve son cmdlet güncelleştirilmiş yapılandırmayı sunucuya gönderir.</span><span class="sxs-lookup"><span data-stu-id="00829-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="00829-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00829-112">PARAMETERS</span></span>

### <span data-ttu-id="00829-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00829-113">-DefaultProfile</span></span>
<span data-ttu-id="00829-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00829-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00829-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="00829-115">-Name</span></span>
<span data-ttu-id="00829-116">Temsilci adı</span><span class="sxs-lookup"><span data-stu-id="00829-116">The name of the delegation</span></span>

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

### <span data-ttu-id="00829-117">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="00829-117">-ServiceName</span></span>
<span data-ttu-id="00829-118">Alt ağın temsil ettiği hizmetin adı</span><span class="sxs-lookup"><span data-stu-id="00829-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="00829-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00829-119">CommonParameters</span></span>
<span data-ttu-id="00829-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00829-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00829-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00829-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00829-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00829-122">INPUTS</span></span>

### <span data-ttu-id="00829-123">System. String</span><span class="sxs-lookup"><span data-stu-id="00829-123">System.String</span></span>

## <span data-ttu-id="00829-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00829-124">OUTPUTS</span></span>

### <span data-ttu-id="00829-125">Microsoft.Azure.Commands.Network.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="00829-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="00829-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00829-126">NOTES</span></span>

## <span data-ttu-id="00829-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00829-127">RELATED LINKS</span></span>

<span data-ttu-id="00829-128">[Add-Aztemsilci](./Add-AzDelegation.md) 
 [Get-Aztemsilci](./Get-AzDelegation.md) 
 [Remove-Aztemsilci](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="00829-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>