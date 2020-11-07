---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937672"
---
# <span data-ttu-id="fbee5-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee5-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="fbee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbee5-102">SYNOPSIS</span></span>
<span data-ttu-id="fbee5-103">Azure ExpressRoutePort oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fbee5-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="fbee5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fbee5-104">SYNTAX</span></span>

### <span data-ttu-id="fbee5-105">ResourceNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fbee5-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbee5-106">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fbee5-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbee5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fbee5-107">DESCRIPTION</span></span>
<span data-ttu-id="fbee5-108">**Yeni-AzExpressRoutePort** cmdlet 'ı Azure expressrouteport oluşturur</span><span class="sxs-lookup"><span data-stu-id="fbee5-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="fbee5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fbee5-109">EXAMPLES</span></span>

### <span data-ttu-id="fbee5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fbee5-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="fbee5-111">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="fbee5-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="fbee5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fbee5-112">PARAMETERS</span></span>

### <span data-ttu-id="fbee5-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="fbee5-113">-AsJob</span></span>
<span data-ttu-id="fbee5-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fbee5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbee5-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="fbee5-115">-BandwidthInGbps</span></span>
<span data-ttu-id="fbee5-116">Gbps cinsinden procured bağlantı noktalarının bant genişliği</span><span class="sxs-lookup"><span data-stu-id="fbee5-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="fbee5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbee5-117">-DefaultProfile</span></span>
<span data-ttu-id="fbee5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fbee5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbee5-119">-Kapsülleme</span><span class="sxs-lookup"><span data-stu-id="fbee5-119">-Encapsulation</span></span>
<span data-ttu-id="fbee5-120">Fiziksel bağlantı noktalarında kapsülleme yöntemi.</span><span class="sxs-lookup"><span data-stu-id="fbee5-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="fbee5-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fbee5-121">-Force</span></span>
<span data-ttu-id="fbee5-122">Kaynağın üzerine yazmak istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="fbee5-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fbee5-123">-Kimlik</span><span class="sxs-lookup"><span data-stu-id="fbee5-123">-Identity</span></span>
<span data-ttu-id="fbee5-124">Okuma MacSec yapılandırması için Kullanıcı tarafından atanan kimlik</span><span class="sxs-lookup"><span data-stu-id="fbee5-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbee5-125">-Bağlantı</span><span class="sxs-lookup"><span data-stu-id="fbee5-125">-Link</span></span>
<span data-ttu-id="fbee5-126">ExpressRoutePort kaynağının fiziksel bağlantı kümesi</span><span class="sxs-lookup"><span data-stu-id="fbee5-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbee5-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="fbee5-127">-Location</span></span>
<span data-ttu-id="fbee5-128">Konum.</span><span class="sxs-lookup"><span data-stu-id="fbee5-128">The location.</span></span>

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

### <span data-ttu-id="fbee5-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="fbee5-129">-Name</span></span>
<span data-ttu-id="fbee5-130">ExpressRoutePort adı.</span><span class="sxs-lookup"><span data-stu-id="fbee5-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="fbee5-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="fbee5-131">-PeeringLocation</span></span>
<span data-ttu-id="fbee5-132">ExpressRoutePort 'un fiziksel olarak eşlendiği eşleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="fbee5-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="fbee5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbee5-133">-ResourceGroupName</span></span>
<span data-ttu-id="fbee5-134">ExpressRoutePort kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fbee5-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="fbee5-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fbee5-135">-ResourceId</span></span>
<span data-ttu-id="fbee5-136">Hızlı rota bağlantı noktasının RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="fbee5-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="fbee5-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fbee5-137">-Tag</span></span>
<span data-ttu-id="fbee5-138">Kaynak etiketlerini temsil eden bir Hashtable.</span><span class="sxs-lookup"><span data-stu-id="fbee5-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fbee5-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="fbee5-139">-Confirm</span></span>
<span data-ttu-id="fbee5-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fbee5-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbee5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbee5-141">-WhatIf</span></span>
<span data-ttu-id="fbee5-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fbee5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbee5-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fbee5-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbee5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbee5-144">CommonParameters</span></span>
<span data-ttu-id="fbee5-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fbee5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbee5-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbee5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbee5-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fbee5-147">INPUTS</span></span>

### <span data-ttu-id="fbee5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="fbee5-148">System.String</span></span>

### <span data-ttu-id="fbee5-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fbee5-149">System.Int32</span></span>

### <span data-ttu-id="fbee5-150">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbee5-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="fbee5-151">Microsoft. Azure. Commands. Network. model. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="fbee5-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="fbee5-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fbee5-152">OUTPUTS</span></span>

### <span data-ttu-id="fbee5-153">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee5-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="fbee5-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fbee5-154">NOTES</span></span>

## <span data-ttu-id="fbee5-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fbee5-155">RELATED LINKS</span></span>

[<span data-ttu-id="fbee5-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee5-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="fbee5-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee5-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="fbee5-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="fbee5-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
