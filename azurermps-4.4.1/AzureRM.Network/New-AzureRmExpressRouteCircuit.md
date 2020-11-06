---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 4a5c59f6cc561bdd5f12462aab1e4cd634e70fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589965"
---
# <span data-ttu-id="69561-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="69561-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="69561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69561-102">SYNOPSIS</span></span>
<span data-ttu-id="69561-103">Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69561-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69561-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69561-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69561-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69561-105">DESCRIPTION</span></span>
<span data-ttu-id="69561-106">**Yeni-Azurermexpressroutedevresi** , bir Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="69561-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="69561-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69561-107">EXAMPLES</span></span>

### <span data-ttu-id="69561-108">Örnek 1: yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="69561-108">Example 1: Create a new ExpressRoute circuit</span></span>
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

## <span data-ttu-id="69561-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69561-109">PARAMETERS</span></span>

### <span data-ttu-id="69561-110">-Allowclassıntericoperations</span><span class="sxs-lookup"><span data-stu-id="69561-110">-AllowClassicOperations</span></span>
<span data-ttu-id="69561-111">Bu parametrenin kullanılması, devreyi yönetmek için Classic Azure PowerShell cmdlet 'lerini kullanmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="69561-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="69561-112">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="69561-112">-Authorization</span></span>
<span data-ttu-id="69561-113">Devre yetkilendirmeleri listesi.</span><span class="sxs-lookup"><span data-stu-id="69561-113">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="69561-114">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="69561-114">-BandwidthInMbps</span></span>
<span data-ttu-id="69561-115">Devrenin bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="69561-115">The bandwidth of the circuit.</span></span> <span data-ttu-id="69561-116">Bu, hizmet sağlayıcısı tarafından desteklenen bir değer olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="69561-116">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="69561-117">-Force</span><span class="sxs-lookup"><span data-stu-id="69561-117">-Force</span></span>
<span data-ttu-id="69561-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="69561-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="69561-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="69561-119">-Location</span></span>
<span data-ttu-id="69561-120">Devrenin konumu.</span><span class="sxs-lookup"><span data-stu-id="69561-120">The location of the circuit.</span></span>

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

### <span data-ttu-id="69561-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="69561-121">-Name</span></span>
<span data-ttu-id="69561-122">Oluşturulan ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="69561-122">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="69561-123">-Eşleme</span><span class="sxs-lookup"><span data-stu-id="69561-123">-Peering</span></span>
<span data-ttu-id="69561-124">Liste eşi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="69561-124">A list peer configurations.</span></span>

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

### <span data-ttu-id="69561-125">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="69561-125">-PeeringLocation</span></span>
<span data-ttu-id="69561-126">Hizmet sağlayıcısı tarafından desteklenen eşleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="69561-126">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="69561-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69561-127">-ResourceGroupName</span></span>
<span data-ttu-id="69561-128">Devreyi içerecek kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="69561-128">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="69561-129">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="69561-129">-ServiceProviderName</span></span>
<span data-ttu-id="69561-130">Devre hizmeti sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="69561-130">The name of the circuit service provider.</span></span> <span data-ttu-id="69561-131">Bu, Get-AzureRmExpressRouteServiceProvider cmdlet tarafından listelenen bir adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="69561-131">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="69561-132">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="69561-132">-SkuFamily</span></span>
<span data-ttu-id="69561-133">SKU ailesi Faturalandırma türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="69561-133">SKU family determines the billing type.</span></span> <span data-ttu-id="69561-134">Bu parametre için olası değerler: `MeteredData` veya `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="69561-134">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="69561-135">MeteredData 'dan Unlimitedverilerine değiştirebilirsiniz, ancak UnlimitedData 'dan Type 'ı MeteredData olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="69561-135">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="69561-136">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="69561-136">-SkuTier</span></span>
<span data-ttu-id="69561-137">Devre için hizmet katmanı.</span><span class="sxs-lookup"><span data-stu-id="69561-137">The tier of service for the circuit.</span></span> <span data-ttu-id="69561-138">Bu parametre için olası değerler: `Standard` veya `Premium` .</span><span class="sxs-lookup"><span data-stu-id="69561-138">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69561-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="69561-139">-Tag</span></span>
<span data-ttu-id="69561-140">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="69561-140">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="69561-141">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="69561-141">For example:</span></span>

<span data-ttu-id="69561-142">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="69561-142">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="69561-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="69561-143">-Confirm</span></span>
<span data-ttu-id="69561-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69561-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69561-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69561-145">-WhatIf</span></span>
<span data-ttu-id="69561-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69561-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69561-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69561-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69561-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69561-148">-DefaultProfile</span></span>
<span data-ttu-id="69561-149">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69561-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69561-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69561-150">CommonParameters</span></span>
<span data-ttu-id="69561-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69561-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69561-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69561-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69561-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69561-153">INPUTS</span></span>

## <span data-ttu-id="69561-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69561-154">OUTPUTS</span></span>

### <span data-ttu-id="69561-155">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="69561-155">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="69561-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69561-156">NOTES</span></span>

## <span data-ttu-id="69561-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69561-157">RELATED LINKS</span></span>

[<span data-ttu-id="69561-158">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="69561-158">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="69561-159">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="69561-159">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="69561-160">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="69561-160">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="69561-161">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="69561-161">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
