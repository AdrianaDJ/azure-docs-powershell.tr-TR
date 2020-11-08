---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268485"
---
# <span data-ttu-id="01410-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="01410-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="01410-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01410-102">SYNOPSIS</span></span>
<span data-ttu-id="01410-103">Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01410-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="01410-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01410-104">SYNTAX</span></span>

### <span data-ttu-id="01410-105">ServiceProvider (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="01410-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01410-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="01410-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01410-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="01410-107">DESCRIPTION</span></span>
<span data-ttu-id="01410-108">**Yeni-Azexpressroutedevdevi** bir Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="01410-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="01410-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01410-109">EXAMPLES</span></span>

### <span data-ttu-id="01410-110">Örnek 1: yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="01410-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

### <span data-ttu-id="01410-111">Örnek 2: ExpressRoutePort 'ta yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="01410-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="01410-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01410-112">PARAMETERS</span></span>

### <span data-ttu-id="01410-113">-Allowclassıntericoperations</span><span class="sxs-lookup"><span data-stu-id="01410-113">-AllowClassicOperations</span></span>
<span data-ttu-id="01410-114">Bu parametrenin kullanılması, devreyi yönetmek için Classic Azure PowerShell cmdlet 'lerini kullanmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="01410-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="01410-115">-AsJob</span></span>
<span data-ttu-id="01410-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="01410-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01410-117">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="01410-117">-Authorization</span></span>
<span data-ttu-id="01410-118">Devre yetkilendirmeleri listesi.</span><span class="sxs-lookup"><span data-stu-id="01410-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="01410-119">-BandwidthInGbps</span></span>
<span data-ttu-id="01410-120">Bir ExpressRoutePort kaynağında bir devre sağlandığında devrenin bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="01410-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="01410-121">-BandwidthInMbps</span></span>
<span data-ttu-id="01410-122">Devrenin bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="01410-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="01410-123">Bu, hizmet sağlayıcısı tarafından desteklenen bir değer olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="01410-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01410-124">-DefaultProfile</span></span>
<span data-ttu-id="01410-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="01410-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01410-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="01410-126">-ExpressRoutePort</span></span>
<span data-ttu-id="01410-127">Bir ExpressRoutePort kaynağında sağlanan devre hazırlandığında ExpressRoutePort kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="01410-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-128">-Force</span><span class="sxs-lookup"><span data-stu-id="01410-128">-Force</span></span>
<span data-ttu-id="01410-129">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="01410-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="01410-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="01410-130">-Location</span></span>
<span data-ttu-id="01410-131">Devrenin konumu.</span><span class="sxs-lookup"><span data-stu-id="01410-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="01410-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="01410-132">-Name</span></span>
<span data-ttu-id="01410-133">Oluşturulan ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="01410-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="01410-134">-Eşleme</span><span class="sxs-lookup"><span data-stu-id="01410-134">-Peering</span></span>
<span data-ttu-id="01410-135">Liste eşi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="01410-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="01410-136">-PeeringLocation</span></span>
<span data-ttu-id="01410-137">Hizmet sağlayıcısı tarafından desteklenen eşleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="01410-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01410-138">-ResourceGroupName</span></span>
<span data-ttu-id="01410-139">Devreyi içerecek kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="01410-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="01410-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="01410-140">-ServiceProviderName</span></span>
<span data-ttu-id="01410-141">Devre hizmeti sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="01410-141">The name of the circuit service provider.</span></span> <span data-ttu-id="01410-142">Bu, Get-AzExpressRouteServiceProvider cmdlet tarafından listelenen bir adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="01410-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="01410-143">-SkuFamily</span></span>
<span data-ttu-id="01410-144">SKU ailesi Faturalandırma türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="01410-144">SKU family determines the billing type.</span></span> <span data-ttu-id="01410-145">Bu parametre için olası değerler: `MeteredData` veya `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="01410-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="01410-146">MeteredData 'dan Unlimitedverilerine değiştirebilirsiniz, ancak UnlimitedData 'dan Type 'ı MeteredData olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="01410-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="01410-147">-SkuTier</span></span>
<span data-ttu-id="01410-148">Devre için hizmet katmanı.</span><span class="sxs-lookup"><span data-stu-id="01410-148">The tier of service for the circuit.</span></span> <span data-ttu-id="01410-149">Bu parametre için olası değerler: `Standard` `Premium` veya `Local` .</span><span class="sxs-lookup"><span data-stu-id="01410-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01410-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="01410-150">-Tag</span></span>
<span data-ttu-id="01410-151">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="01410-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="01410-152">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="01410-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="01410-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="01410-153">-Confirm</span></span>
<span data-ttu-id="01410-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01410-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01410-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01410-155">-WhatIf</span></span>
<span data-ttu-id="01410-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01410-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01410-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01410-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01410-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01410-158">CommonParameters</span></span>
<span data-ttu-id="01410-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01410-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01410-160">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01410-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01410-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01410-161">INPUTS</span></span>

### <span data-ttu-id="01410-162">System. String</span><span class="sxs-lookup"><span data-stu-id="01410-162">System.String</span></span>

### <span data-ttu-id="01410-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="01410-163">System.Int32</span></span>

### <span data-ttu-id="01410-164">Microsoft. Azure. Commands. Network. model. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="01410-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="01410-165">System. Double</span><span class="sxs-lookup"><span data-stu-id="01410-165">System.Double</span></span>

### <span data-ttu-id="01410-166">Microsoft. Azure. Commands. Network. model. pspe, []</span><span class="sxs-lookup"><span data-stu-id="01410-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="01410-167">Microsoft. Azure. Commands. Network. model. Psexpressrouteter</span><span class="sxs-lookup"><span data-stu-id="01410-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="01410-168">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="01410-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="01410-169">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="01410-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="01410-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01410-170">OUTPUTS</span></span>

### <span data-ttu-id="01410-171">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="01410-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="01410-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01410-172">NOTES</span></span>

## <span data-ttu-id="01410-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01410-173">RELATED LINKS</span></span>

[<span data-ttu-id="01410-174">Get-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="01410-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="01410-175">Taşıma-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="01410-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="01410-176">Remove-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="01410-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="01410-177">Set-Azexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="01410-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
