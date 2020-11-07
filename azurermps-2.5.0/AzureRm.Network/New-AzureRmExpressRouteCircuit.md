---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
ms.openlocfilehash: 43084ab54ed20a094cc292eca2bf133598171f09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938929"
---
# <span data-ttu-id="a022f-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a022f-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="a022f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a022f-102">SYNOPSIS</span></span>
<span data-ttu-id="a022f-103">Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a022f-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a022f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a022f-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a022f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a022f-105">DESCRIPTION</span></span>
<span data-ttu-id="a022f-106">**Yeni-Azurermexpressroutedevresi** , bir Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a022f-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="a022f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a022f-107">EXAMPLES</span></span>

### <span data-ttu-id="a022f-108">Örnek 1: yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a022f-108">Example 1: Create a new ExpressRoute circuit</span></span>
```
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="a022f-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a022f-109">PARAMETERS</span></span>

### <span data-ttu-id="a022f-110">-Allowclassıntericoperations</span><span class="sxs-lookup"><span data-stu-id="a022f-110">-AllowClassicOperations</span></span>
<span data-ttu-id="a022f-111">Bu parametrenin kullanılması, devreyi yönetmek için Classic Azure PowerShell cmdlet 'lerini kullanmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a022f-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="a022f-112">-AsJob</span></span>
<span data-ttu-id="a022f-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="a022f-113">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-114">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="a022f-114">-Authorization</span></span>
<span data-ttu-id="a022f-115">Devre yetkilendirmeleri listesi.</span><span class="sxs-lookup"><span data-stu-id="a022f-115">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="a022f-116">-BandwidthInMbps</span></span>
<span data-ttu-id="a022f-117">Devrenin bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="a022f-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="a022f-118">Bu, hizmet sağlayıcısı tarafından desteklenen bir değer olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a022f-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a022f-119">-DefaultProfile</span></span>
<span data-ttu-id="a022f-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a022f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a022f-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a022f-121">-Force</span></span>
<span data-ttu-id="a022f-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a022f-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="a022f-123">-Location</span></span>
<span data-ttu-id="a022f-124">Devrenin konumu.</span><span class="sxs-lookup"><span data-stu-id="a022f-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="a022f-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a022f-125">-Name</span></span>
<span data-ttu-id="a022f-126">Oluşturulan ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="a022f-126">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-127">-Eşleme</span><span class="sxs-lookup"><span data-stu-id="a022f-127">-Peering</span></span>
<span data-ttu-id="a022f-128">Liste eşi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="a022f-128">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="a022f-129">-PeeringLocation</span></span>
<span data-ttu-id="a022f-130">Hizmet sağlayıcısı tarafından desteklenen eşleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="a022f-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="a022f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a022f-131">-ResourceGroupName</span></span>
<span data-ttu-id="a022f-132">Devreyi içerecek kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="a022f-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="a022f-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="a022f-133">-ServiceProviderName</span></span>
<span data-ttu-id="a022f-134">Devre hizmeti sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="a022f-134">The name of the circuit service provider.</span></span> <span data-ttu-id="a022f-135">Bu, Get-AzureRmExpressRouteServiceProvider cmdlet tarafından listelenen bir adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="a022f-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="a022f-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="a022f-136">-SkuFamily</span></span>
<span data-ttu-id="a022f-137">SKU ailesi Faturalandırma türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="a022f-137">SKU family determines the billing type.</span></span> <span data-ttu-id="a022f-138">Bu parametre için olası değerler: `MeteredData` veya `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="a022f-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="a022f-139">MeteredData 'dan Unlimitedverilerine değiştirebilirsiniz, ancak UnlimitedData 'dan Type 'ı MeteredData olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="a022f-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="a022f-140">-SkuTier</span></span>
<span data-ttu-id="a022f-141">Devre için hizmet katmanı.</span><span class="sxs-lookup"><span data-stu-id="a022f-141">The tier of service for the circuit.</span></span> <span data-ttu-id="a022f-142">Bu parametre için olası değerler: `Standard` veya `Premium` .</span><span class="sxs-lookup"><span data-stu-id="a022f-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a022f-143">-Tag</span></span>
<span data-ttu-id="a022f-144">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="a022f-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a022f-145">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="a022f-145">For example:</span></span>

<span data-ttu-id="a022f-146">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="a022f-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="a022f-147">-Confirm</span></span>
<span data-ttu-id="a022f-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a022f-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a022f-149">-WhatIf</span></span>
<span data-ttu-id="a022f-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a022f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a022f-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a022f-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a022f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a022f-152">CommonParameters</span></span>
<span data-ttu-id="a022f-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a022f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a022f-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a022f-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a022f-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a022f-155">INPUTS</span></span>

## <span data-ttu-id="a022f-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a022f-156">OUTPUTS</span></span>

### <span data-ttu-id="a022f-157">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a022f-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a022f-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a022f-158">NOTES</span></span>

## <span data-ttu-id="a022f-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a022f-159">RELATED LINKS</span></span>

[<span data-ttu-id="a022f-160">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a022f-160">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a022f-161">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a022f-161">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a022f-162">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a022f-162">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="a022f-163">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="a022f-163">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
