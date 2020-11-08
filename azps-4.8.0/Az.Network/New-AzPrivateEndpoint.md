---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268466"
---
# <span data-ttu-id="39c61-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39c61-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="39c61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39c61-102">SYNOPSIS</span></span>
<span data-ttu-id="39c61-103">Özel bir uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="39c61-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="39c61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39c61-104">SYNTAX</span></span>

### <span data-ttu-id="39c61-105">Tüm</span><span class="sxs-lookup"><span data-stu-id="39c61-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39c61-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="39c61-106">DESCRIPTION</span></span>

<span data-ttu-id="39c61-107">**New-AzPrivateEndpoint** cmdlet 'i özel bir uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="39c61-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="39c61-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39c61-108">EXAMPLES</span></span>

### <span data-ttu-id="39c61-109">Örnek 1: özel uç nokta oluşturma</span><span class="sxs-lookup"><span data-stu-id="39c61-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="39c61-110">Aşağıdaki örnek, sanal ağda belirtilen alt ağda belirli bir özel bağlantı hizmeti KIMLIĞI içeren özel bir uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="39c61-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="39c61-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39c61-111">PARAMETERS</span></span>

### <span data-ttu-id="39c61-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="39c61-112">-AsJob</span></span>

<span data-ttu-id="39c61-113">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="39c61-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="39c61-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="39c61-114">-ByManualRequest</span></span>

<span data-ttu-id="39c61-115">Bağlantıyı kurmak için el ile istek 'ı kullanın.</span><span class="sxs-lookup"><span data-stu-id="39c61-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="39c61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c61-116">-DefaultProfile</span></span>

<span data-ttu-id="39c61-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39c61-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39c61-118">-Force</span><span class="sxs-lookup"><span data-stu-id="39c61-118">-Force</span></span>

<span data-ttu-id="39c61-119">Kaynağın üzerine yazılmasını sorma.</span><span class="sxs-lookup"><span data-stu-id="39c61-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="39c61-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="39c61-120">-Location</span></span>

<span data-ttu-id="39c61-121">Özel uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="39c61-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="39c61-122">Bu parametrenin geçerli değerlerini belirlemek için [Get-AzLocation](/powershell/module/az.resources/get-azlocation) değerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="39c61-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="39c61-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="39c61-123">-Name</span></span>

<span data-ttu-id="39c61-124">Özel uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="39c61-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="39c61-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="39c61-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="39c61-126">Özel uç noktayı bağlamak için kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="39c61-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="39c61-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c61-127">-ResourceGroupName</span></span>

<span data-ttu-id="39c61-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="39c61-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="39c61-129">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="39c61-129">-Subnet</span></span>

<span data-ttu-id="39c61-130">Özel uç noktasının alt ağı.</span><span class="sxs-lookup"><span data-stu-id="39c61-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="39c61-131">Etiketli</span><span class="sxs-lookup"><span data-stu-id="39c61-131">-Tag</span></span>

<span data-ttu-id="39c61-132">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="39c61-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="39c61-133">Örneğin: @ {Key0 = ' value0 '; anahtar = $null; anahtar2 = ' değer2 '}</span><span class="sxs-lookup"><span data-stu-id="39c61-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="39c61-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="39c61-134">-Confirm</span></span>

<span data-ttu-id="39c61-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="39c61-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39c61-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c61-136">-WhatIf</span></span>

<span data-ttu-id="39c61-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="39c61-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c61-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="39c61-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39c61-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c61-139">CommonParameters</span></span>

<span data-ttu-id="39c61-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39c61-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c61-141">Daha fazla bilgi için [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)bakın.</span><span class="sxs-lookup"><span data-stu-id="39c61-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="39c61-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39c61-142">INPUTS</span></span>

### <span data-ttu-id="39c61-143">System. String</span><span class="sxs-lookup"><span data-stu-id="39c61-143">System.String</span></span>

### <span data-ttu-id="39c61-144">Microsoft. Azure. Commands. Network. modeller. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="39c61-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="39c61-145">Microsoft. Azure. Commands. Network. model. PSPrivateLinkServiceConnection []</span><span class="sxs-lookup"><span data-stu-id="39c61-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="39c61-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39c61-146">OUTPUTS</span></span>

### <span data-ttu-id="39c61-147">Microsoft. Azure. Commands. Network. model. PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39c61-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="39c61-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39c61-148">NOTES</span></span>

## <span data-ttu-id="39c61-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39c61-149">RELATED LINKS</span></span>

[<span data-ttu-id="39c61-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39c61-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="39c61-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="39c61-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="39c61-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="39c61-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)