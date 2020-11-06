---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589465"
---
# <span data-ttu-id="d3f55-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d3f55-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="d3f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f55-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f55-103">Azure ExpressRoutePort oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d3f55-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3f55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d3f55-104">SYNTAX</span></span>

### <span data-ttu-id="d3f55-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d3f55-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f55-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d3f55-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f55-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d3f55-107">DESCRIPTION</span></span>
<span data-ttu-id="d3f55-108">**Yeni-AzureRmExpressRoutePort** cmdlet 'i, bir Azure expressrouteport oluşturur</span><span class="sxs-lookup"><span data-stu-id="d3f55-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="d3f55-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d3f55-109">EXAMPLES</span></span>

### <span data-ttu-id="d3f55-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d3f55-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="d3f55-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d3f55-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="d3f55-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d3f55-112">PARAMETERS</span></span>

### <span data-ttu-id="d3f55-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="d3f55-113">-AsJob</span></span>
<span data-ttu-id="d3f55-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d3f55-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3f55-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="d3f55-115">-BandwidthInGbps</span></span>
<span data-ttu-id="d3f55-116">Gbps cinsinden procured bağlantı noktalarının bant genişliği</span><span class="sxs-lookup"><span data-stu-id="d3f55-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f55-117">-DefaultProfile</span></span>
<span data-ttu-id="d3f55-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d3f55-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f55-119">-Kapsülleme</span><span class="sxs-lookup"><span data-stu-id="d3f55-119">-Encapsulation</span></span>
<span data-ttu-id="d3f55-120">Fiziksel bağlantı noktalarında kapsülleme yöntemi.</span><span class="sxs-lookup"><span data-stu-id="d3f55-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="d3f55-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d3f55-121">-Force</span></span>
<span data-ttu-id="d3f55-122">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="d3f55-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d3f55-123">-Bağlantı</span><span class="sxs-lookup"><span data-stu-id="d3f55-123">-Link</span></span>
<span data-ttu-id="d3f55-124">ExpressRoutePort kaynağının fiziksel bağlantı kümesi</span><span class="sxs-lookup"><span data-stu-id="d3f55-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f55-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="d3f55-125">-Location</span></span>
<span data-ttu-id="d3f55-126">Konum.</span><span class="sxs-lookup"><span data-stu-id="d3f55-126">The location.</span></span>

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

### <span data-ttu-id="d3f55-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="d3f55-127">-Name</span></span>
<span data-ttu-id="d3f55-128">ExpressRoutePort adı.</span><span class="sxs-lookup"><span data-stu-id="d3f55-128">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f55-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="d3f55-129">-PeeringLocation</span></span>
<span data-ttu-id="d3f55-130">ExpressRoutePort 'un fiziksel olarak eşlendiği eşleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="d3f55-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="d3f55-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f55-131">-ResourceGroupName</span></span>
<span data-ttu-id="d3f55-132">ExpressRoutePort kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d3f55-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f55-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d3f55-133">-ResourceId</span></span>
<span data-ttu-id="d3f55-134">Hızlı rota bağlantı noktasının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="d3f55-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f55-135">Etiketli</span><span class="sxs-lookup"><span data-stu-id="d3f55-135">-Tag</span></span>
<span data-ttu-id="d3f55-136">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="d3f55-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d3f55-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="d3f55-137">-Confirm</span></span>
<span data-ttu-id="d3f55-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d3f55-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f55-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f55-139">-WhatIf</span></span>
<span data-ttu-id="d3f55-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d3f55-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f55-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d3f55-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f55-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f55-142">CommonParameters</span></span>
<span data-ttu-id="d3f55-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d3f55-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f55-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f55-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f55-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d3f55-145">INPUTS</span></span>

### <span data-ttu-id="d3f55-146">System. String</span><span class="sxs-lookup"><span data-stu-id="d3f55-146">System.String</span></span>

### <span data-ttu-id="d3f55-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d3f55-147">System.Int32</span></span>

### <span data-ttu-id="d3f55-148">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d3f55-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d3f55-149">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. PSExpressRouteLink, Microsoft. Azure. Commands. Network, Version = 6.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d3f55-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d3f55-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d3f55-150">OUTPUTS</span></span>

### <span data-ttu-id="d3f55-151">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d3f55-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d3f55-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d3f55-152">NOTES</span></span>

## <span data-ttu-id="d3f55-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d3f55-153">RELATED LINKS</span></span>
