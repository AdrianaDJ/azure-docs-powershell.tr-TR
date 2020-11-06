---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590160"
---
# <span data-ttu-id="7db15-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7db15-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="7db15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7db15-102">SYNOPSIS</span></span>
<span data-ttu-id="7db15-103">Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7db15-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7db15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7db15-104">SYNTAX</span></span>

### <span data-ttu-id="7db15-105">Sınıfını</span><span class="sxs-lookup"><span data-stu-id="7db15-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7db15-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7db15-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7db15-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7db15-107">DESCRIPTION</span></span>
<span data-ttu-id="7db15-108">**Yeni-Azurermexpressroutedevresi** , bir Azure Express Route devresi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7db15-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="7db15-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7db15-109">EXAMPLES</span></span>

### <span data-ttu-id="7db15-110">Örnek 1: yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7db15-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="7db15-111">Örnek 2: ExpressRoutePort 'ta yeni bir ExpressRoute devresi oluşturma</span><span class="sxs-lookup"><span data-stu-id="7db15-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="7db15-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7db15-112">PARAMETERS</span></span>

### <span data-ttu-id="7db15-113">-Allowclassıntericoperations</span><span class="sxs-lookup"><span data-stu-id="7db15-113">-AllowClassicOperations</span></span>
<span data-ttu-id="7db15-114">Bu parametrenin kullanılması, devreyi yönetmek için Classic Azure PowerShell cmdlet 'lerini kullanmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7db15-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="7db15-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="7db15-115">-AsJob</span></span>
<span data-ttu-id="7db15-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7db15-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7db15-117">-Yetkilendirme</span><span class="sxs-lookup"><span data-stu-id="7db15-117">-Authorization</span></span>
<span data-ttu-id="7db15-118">Devre yetkilendirmeleri listesi.</span><span class="sxs-lookup"><span data-stu-id="7db15-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="7db15-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="7db15-119">-BandwidthInGbps</span></span>
<span data-ttu-id="7db15-120">Bir ExpressRoutePort kaynağında bir devre sağlandığında devrenin bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="7db15-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db15-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="7db15-121">-BandwidthInMbps</span></span>
<span data-ttu-id="7db15-122">Devrenin bant genişliği.</span><span class="sxs-lookup"><span data-stu-id="7db15-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="7db15-123">Bu, hizmet sağlayıcısı tarafından desteklenen bir değer olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7db15-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db15-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7db15-124">-DefaultProfile</span></span>
<span data-ttu-id="7db15-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7db15-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7db15-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="7db15-126">-ExpressRoutePort</span></span>
<span data-ttu-id="7db15-127">Bir ExpressRoutePort kaynağında sağlanan devre hazırlandığında ExpressRoutePort kaynağının başvurusu.</span><span class="sxs-lookup"><span data-stu-id="7db15-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7db15-128">-Force</span><span class="sxs-lookup"><span data-stu-id="7db15-128">-Force</span></span>
<span data-ttu-id="7db15-129">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7db15-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7db15-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="7db15-130">-Location</span></span>
<span data-ttu-id="7db15-131">Devrenin konumu.</span><span class="sxs-lookup"><span data-stu-id="7db15-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="7db15-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="7db15-132">-Name</span></span>
<span data-ttu-id="7db15-133">Oluşturulan ExpressRoute devresi adı.</span><span class="sxs-lookup"><span data-stu-id="7db15-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="7db15-134">-Eşleme</span><span class="sxs-lookup"><span data-stu-id="7db15-134">-Peering</span></span>
<span data-ttu-id="7db15-135">Liste eşi yapılandırmaları.</span><span class="sxs-lookup"><span data-stu-id="7db15-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="7db15-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="7db15-136">-PeeringLocation</span></span>
<span data-ttu-id="7db15-137">Hizmet sağlayıcısı tarafından desteklenen eşleme konumunun adı.</span><span class="sxs-lookup"><span data-stu-id="7db15-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db15-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7db15-138">-ResourceGroupName</span></span>
<span data-ttu-id="7db15-139">Devreyi içerecek kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="7db15-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="7db15-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="7db15-140">-ServiceProviderName</span></span>
<span data-ttu-id="7db15-141">Devre hizmeti sağlayıcısının adı.</span><span class="sxs-lookup"><span data-stu-id="7db15-141">The name of the circuit service provider.</span></span> <span data-ttu-id="7db15-142">Bu, Get-AzureRmExpressRouteServiceProvider cmdlet tarafından listelenen bir adla eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="7db15-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7db15-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="7db15-143">-SkuFamily</span></span>
<span data-ttu-id="7db15-144">SKU ailesi Faturalandırma türünü belirler.</span><span class="sxs-lookup"><span data-stu-id="7db15-144">SKU family determines the billing type.</span></span> <span data-ttu-id="7db15-145">Bu parametre için olası değerler: `MeteredData` veya `UnlimitedData` .</span><span class="sxs-lookup"><span data-stu-id="7db15-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="7db15-146">MeteredData 'dan Unlimitedverilerine değiştirebilirsiniz, ancak UnlimitedData 'dan Type 'ı MeteredData olarak değiştiremezsiniz.</span><span class="sxs-lookup"><span data-stu-id="7db15-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="7db15-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="7db15-147">-SkuTier</span></span>
<span data-ttu-id="7db15-148">Devre için hizmet katmanı.</span><span class="sxs-lookup"><span data-stu-id="7db15-148">The tier of service for the circuit.</span></span> <span data-ttu-id="7db15-149">Bu parametre için olası değerler: `Standard` veya `Premium` .</span><span class="sxs-lookup"><span data-stu-id="7db15-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="7db15-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7db15-150">-Tag</span></span>
<span data-ttu-id="7db15-151">Karma tablo biçiminde anahtar-değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7db15-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7db15-152">Örneğin: @ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="7db15-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7db15-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="7db15-153">-Confirm</span></span>
<span data-ttu-id="7db15-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7db15-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7db15-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7db15-155">-WhatIf</span></span>
<span data-ttu-id="7db15-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7db15-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7db15-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7db15-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7db15-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7db15-158">CommonParameters</span></span>
<span data-ttu-id="7db15-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7db15-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7db15-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7db15-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7db15-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7db15-161">INPUTS</span></span>

### <span data-ttu-id="7db15-162">System. String</span><span class="sxs-lookup"><span data-stu-id="7db15-162">System.String</span></span>

### <span data-ttu-id="7db15-163">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7db15-163">System.Int32</span></span>

### <span data-ttu-id="7db15-164">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. pspe, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7db15-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7db15-165">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. Network. modeller. Psexpressroutedöngüye 6.4.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7db15-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7db15-166">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7db15-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7db15-167">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7db15-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7db15-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7db15-168">OUTPUTS</span></span>

### <span data-ttu-id="7db15-169">Microsoft. Azure. Commands. Network. model. Psexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="7db15-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7db15-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7db15-170">NOTES</span></span>

## <span data-ttu-id="7db15-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7db15-171">RELATED LINKS</span></span>

[<span data-ttu-id="7db15-172">Get-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="7db15-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7db15-173">Taşı-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="7db15-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7db15-174">Remove-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="7db15-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="7db15-175">Set-Azurermexpressroutedevresi</span><span class="sxs-lookup"><span data-stu-id="7db15-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
