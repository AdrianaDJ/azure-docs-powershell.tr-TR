---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 0c611edc0ef8cb117e556a19e22f93d1f8db96ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592079"
---
# <span data-ttu-id="fe938-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="fe938-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="fe938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe938-102">SYNOPSIS</span></span>
<span data-ttu-id="fe938-103">Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe938-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe938-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe938-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe938-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe938-105">DESCRIPTION</span></span>
<span data-ttu-id="fe938-106">**Yeni-Azurermexpressroutedevresi** , bir Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fe938-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="fe938-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe938-107">EXAMPLES</span></span>

### <span data-ttu-id="fe938-108">Örnek 1: yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="fe938-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="fe938-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe938-109">PARAMETERS</span></span>

### <span data-ttu-id="fe938-110">-Allowclassıntericoperations</span><span class="sxs-lookup"><span data-stu-id="fe938-110">-AllowClassicOperations</span></span>
<span data-ttu-id="fe938-111">Bu parametrenin kullanılması, devreyi yönetmek için Classic Azure PowerShell cmdlet 'lerini kullanmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="fe938-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="fe938-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="fe938-112">-AsJob</span></span>
<span data-ttu-id="fe938-113">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fe938-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe938-114">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="fe938-114">-Authorization</span></span>
<span data-ttu-id="fe938-115">Devre yetkilendirmeleri listesi.</span><span class="sxs-lookup"><span data-stu-id="fe938-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="fe938-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="fe938-116">-BandwidthInMbps</span></span>
<span data-ttu-id="fe938-117">Devrenin bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="fe938-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="fe938-118">Bu, hizmet sağlayıcısı tarafından desteklenen bir değer olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fe938-118">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="fe938-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe938-119">-DefaultProfile</span></span>
<span data-ttu-id="fe938-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe938-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe938-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fe938-121">-Force</span></span>
<span data-ttu-id="fe938-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fe938-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fe938-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="fe938-123">-Location</span></span>
<span data-ttu-id="fe938-124">Devrenin konumu.</span><span class="sxs-lookup"><span data-stu-id="fe938-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="fe938-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe938-125">-Name</span></span>
<span data-ttu-id="fe938-126">Oluşturulan ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="fe938-126">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="fe938-127">-Eşleme</span><span class="sxs-lookup"><span data-stu-id="fe938-127">-Peering</span></span>
<span data-ttu-id="fe938-128">Liste eşi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="fe938-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="fe938-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="fe938-129">-PeeringLocation</span></span>
<span data-ttu-id="fe938-130">Hizmet sağlayıcısı tarafından desteklenen eşleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="fe938-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="fe938-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe938-131">-ResourceGroupName</span></span>
<span data-ttu-id="fe938-132">Devreyi içerecek kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="fe938-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="fe938-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="fe938-133">-ServiceProviderName</span></span>
<span data-ttu-id="fe938-134">Devre hizmeti sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="fe938-134">The name of the circuit service provider.</span></span> <span data-ttu-id="fe938-135">Bu, Get-AzureRmExpressRouteServiceProvider cmdlet tarafından listelenen bir adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="fe938-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="fe938-136">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="fe938-136">-SkuFamily</span></span>
<span data-ttu-id="fe938-137">SKU ailesi Faturalandırma türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="fe938-137">SKU family determines the billing type.</span></span> <span data-ttu-id="fe938-138">Bu parametre için olası değerler: `MeteredData` veya `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="fe938-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="fe938-139">MeteredData 'dan Unlimitedverilerine değiştirebilirsiniz, ancak UnlimitedData 'dan Type 'ı MeteredData olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="fe938-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="fe938-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fe938-140">-SkuTier</span></span>
<span data-ttu-id="fe938-141">Devre için hizmet katmanı.</span><span class="sxs-lookup"><span data-stu-id="fe938-141">The tier of service for the circuit.</span></span> <span data-ttu-id="fe938-142">Bu parametre için olası değerler: `Standard` veya `Premium` .</span><span class="sxs-lookup"><span data-stu-id="fe938-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="fe938-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fe938-143">-Tag</span></span>
<span data-ttu-id="fe938-144">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="fe938-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="fe938-145">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="fe938-145">For example:</span></span>

<span data-ttu-id="fe938-146">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="fe938-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fe938-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe938-147">-Confirm</span></span>
<span data-ttu-id="fe938-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe938-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe938-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe938-149">-WhatIf</span></span>
<span data-ttu-id="fe938-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe938-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe938-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe938-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe938-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe938-152">CommonParameters</span></span>
<span data-ttu-id="fe938-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe938-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe938-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe938-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe938-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe938-155">INPUTS</span></span>

### <span data-ttu-id="fe938-156">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="fe938-156">None</span></span>
<span data-ttu-id="fe938-157">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="fe938-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe938-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe938-158">OUTPUTS</span></span>

### <span data-ttu-id="fe938-159">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="fe938-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="fe938-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe938-160">NOTES</span></span>

## <span data-ttu-id="fe938-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe938-161">RELATED LINKS</span></span>

[<span data-ttu-id="fe938-162">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="fe938-162">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fe938-163">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="fe938-163">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fe938-164">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="fe938-164">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="fe938-165">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="fe938-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
