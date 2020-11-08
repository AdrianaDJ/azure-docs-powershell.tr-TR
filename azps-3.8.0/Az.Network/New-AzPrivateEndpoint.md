---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: 6e83def7c4956e4936e8e3c55f96aab1da0d451d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097248"
---
# <span data-ttu-id="5ad4a-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad4a-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="5ad4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ad4a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ad4a-103">Özel bir uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="5ad4a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5ad4a-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ad4a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5ad4a-105">DESCRIPTION</span></span>
<span data-ttu-id="5ad4a-106">**New-AzPrivateEndpoint** cmdlet 'i özel bir uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="5ad4a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5ad4a-107">EXAMPLES</span></span>

### <span data-ttu-id="5ad4a-108">1: özel uç nokta oluşturma</span><span class="sxs-lookup"><span data-stu-id="5ad4a-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="5ad4a-109">Bu örnekte, sanal ağdaki belirli bir alt ağda belirli bir özel bağlantı hizmeti kimliği ile özel bir uç nokta oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="5ad4a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5ad4a-110">PARAMETERS</span></span>

### <span data-ttu-id="5ad4a-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="5ad4a-111">-AsJob</span></span>
<span data-ttu-id="5ad4a-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5ad4a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ad4a-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="5ad4a-113">-ByManualRequest</span></span>
<span data-ttu-id="5ad4a-114">El ile talep kullanma.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-114">Using manual request.</span></span>

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

### <span data-ttu-id="5ad4a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ad4a-115">-DefaultProfile</span></span>
<span data-ttu-id="5ad4a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ad4a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ad4a-117">-Force</span></span>
<span data-ttu-id="5ad4a-118">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="5ad4a-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5ad4a-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="5ad4a-119">-Location</span></span>
<span data-ttu-id="5ad4a-120">konumuyla.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-120">location.</span></span>

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

### <span data-ttu-id="5ad4a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="5ad4a-121">-Name</span></span>
<span data-ttu-id="5ad4a-122">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad4a-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5ad4a-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="5ad4a-124">Özel bağlantı hizmeti bağlantısı.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-124">The private link service connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad4a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ad4a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5ad4a-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-126">The resource group name.</span></span>

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

### <span data-ttu-id="5ad4a-127">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="5ad4a-127">-Subnet</span></span>
<span data-ttu-id="5ad4a-128">Özel uç noktasının alt ağı</span><span class="sxs-lookup"><span data-stu-id="5ad4a-128">The subnet of the private endpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad4a-129">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5ad4a-129">-Tag</span></span>
<span data-ttu-id="5ad4a-130">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5ad4a-131">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="5ad4a-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ad4a-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="5ad4a-132">-Confirm</span></span>
<span data-ttu-id="5ad4a-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad4a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ad4a-134">-WhatIf</span></span>
<span data-ttu-id="5ad4a-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ad4a-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ad4a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ad4a-137">CommonParameters</span></span>
<span data-ttu-id="5ad4a-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ad4a-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5ad4a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ad4a-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5ad4a-140">INPUTS</span></span>

### <span data-ttu-id="5ad4a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5ad4a-141">System.String</span></span>

### <span data-ttu-id="5ad4a-142">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5ad4a-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="5ad4a-143">Microsoft. Azure. Commands. Network. model. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="5ad4a-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="5ad4a-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5ad4a-144">OUTPUTS</span></span>

### <span data-ttu-id="5ad4a-145">Microsoft. Azure. Commands. Network. model. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad4a-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="5ad4a-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5ad4a-146">NOTES</span></span>

## <span data-ttu-id="5ad4a-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5ad4a-147">RELATED LINKS</span></span>

[<span data-ttu-id="5ad4a-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad4a-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="5ad4a-149">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ad4a-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="5ad4a-150">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="5ad4a-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)