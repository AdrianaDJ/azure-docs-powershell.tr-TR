---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: e9e6817d9a290acf1e91067edfd90cdf8081f1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592375"
---
# <span data-ttu-id="bc922-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="bc922-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="bc922-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc922-102">SYNOPSIS</span></span>
<span data-ttu-id="bc922-103">Yerel bir Traffic Manager profil nesnesine uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="bc922-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc922-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bc922-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc922-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bc922-105">DESCRIPTION</span></span>
<span data-ttu-id="bc922-106">**Add-AzureRmTrafficManagerEndpointConfig** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="bc922-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="bc922-107">New-AzureRmTrafficManagerProfile veya Get-AzureRmTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bc922-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="bc922-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="bc922-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="bc922-109">Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="bc922-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="bc922-110">Uç nokta oluşturmak ve değişikliği tek bir işlemde uygulamak için New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc922-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="bc922-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bc922-111">EXAMPLES</span></span>

### <span data-ttu-id="bc922-112">Örnek 1: profile uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="bc922-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="bc922-113">İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="bc922-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="bc922-114">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="bc922-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="bc922-115">İkinci komut, $TrafficManagerProfile depolanan profile contoso adlı bir uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="bc922-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="bc922-116">Komut uç nokta yapılandırma verilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="bc922-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="bc922-117">Bu komut yalnızca yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bc922-117">This command changes only the local object.</span></span>

<span data-ttu-id="bc922-118">Son komutu, Azure 'daki Traffic Manager profilini $TrafficManagerProfile yerel değerle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="bc922-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="bc922-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bc922-119">PARAMETERS</span></span>

### <span data-ttu-id="bc922-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc922-120">-DefaultProfile</span></span>
<span data-ttu-id="bc922-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bc922-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc922-122">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="bc922-122">-EndpointLocation</span></span>
<span data-ttu-id="bc922-123">Performans trafiği yönlendirme yönteminde kullanılacak uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-123">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="bc922-124">Bu parametre yalnızca ExternalEndpoints veya Nestedenvseçval türünün uç noktalarına uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="bc922-124">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="bc922-125">Performans trafiği yönlendirme yöntemi kullanıldığında bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bc922-125">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="bc922-126">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="bc922-126">Specify an Azure region name.</span></span>
<span data-ttu-id="bc922-127">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="bc922-127">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-128">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bc922-128">-EndpointName</span></span>
<span data-ttu-id="bc922-129">Bu cmdlet 'in eklediği Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-129">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-130">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="bc922-130">-EndpointStatus</span></span>
<span data-ttu-id="bc922-131">Uç noktasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-131">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="bc922-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="bc922-132">Valid values are:</span></span> 

- <span data-ttu-id="bc922-133">Etkin</span><span class="sxs-lookup"><span data-stu-id="bc922-133">Enabled</span></span> 
- <span data-ttu-id="bc922-134">DISABLED</span><span class="sxs-lookup"><span data-stu-id="bc922-134">Disabled</span></span> 

<span data-ttu-id="bc922-135">Durum etkinleştirilirse, uç nokta uç durumu için araştırılan ve trafik yönlendirme yöntemine dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bc922-135">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-136">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="bc922-136">-GeoMapping</span></span>
<span data-ttu-id="bc922-137">' Coğrafi ' trafik yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş bölgelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="bc922-137">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="bc922-138">Lütfen [kabul edilen değerlerin tam listesi](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)Için lütfen Traffic Manager belgelerine başvurun.</span><span class="sxs-lookup"><span data-stu-id="bc922-138">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-139">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="bc922-139">-MinChildEndpoints</span></span>
<span data-ttu-id="bc922-140">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="bc922-140">Specify an Azure region name.</span></span>
<span data-ttu-id="bc922-141">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="bc922-141">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-142">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="bc922-142">-Priority</span></span>
<span data-ttu-id="bc922-143">Traffic Manager 'ın uç noktaya atadığı önceliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-143">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="bc922-144">Bu parametre, yalnızca Traffic Manager profili öncelik için öncelik için öncelik için yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc922-144">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="bc922-145">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="bc922-145">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="bc922-146">Düşük değerler daha yüksek öncelikleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="bc922-146">Lower values represent higher priority.</span></span>

<span data-ttu-id="bc922-147">Öncelik belirtirseniz, profildeki tüm uç noktalarda öncelikleri belirtmeniz gerekir ve iki uç nokta aynı öncelik değerini paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="bc922-147">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="bc922-148">Öncelikler belirtmezseniz, Traffic Manager uç noktalara, bir (1) başlayarak, profilin uç noktalarını listelerse, varsayılan öncelik değerlerini uç noktalara atar.</span><span class="sxs-lookup"><span data-stu-id="bc922-148">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-149">-Hedef</span><span class="sxs-lookup"><span data-stu-id="bc922-149">-Target</span></span>
<span data-ttu-id="bc922-150">Uç noktanın tam DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-150">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="bc922-151">Traffic Manager trafiği bu uç noktaya yönlendirirse DNS yanıtlarında bu değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="bc922-151">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="bc922-152">Bu parametreyi yalnızca ExternalEndpoints uç noktası türü için belirtin.</span><span class="sxs-lookup"><span data-stu-id="bc922-152">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="bc922-153">Diğer uç nokta türleri için bunun yerine *Targetresourceıd* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="bc922-153">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-154">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="bc922-154">-TargetResourceId</span></span>
<span data-ttu-id="bc922-155">Hedefin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-155">Specifies resource ID of the target.</span></span>
<span data-ttu-id="bc922-156">Bu parametreyi yalnızca AzureEndpoints ve Nestedenvseçpoints uç noktası türleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="bc922-156">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="bc922-157">ExternalEndpoints uç noktası türü için bunun yerine *target* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="bc922-157">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-158">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc922-158">-TrafficManagerProfile</span></span>
<span data-ttu-id="bc922-159">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-159">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="bc922-160">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bc922-160">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="bc922-161">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="bc922-161">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-162">-Tür</span><span class="sxs-lookup"><span data-stu-id="bc922-162">-Type</span></span>
<span data-ttu-id="bc922-163">Bu cmdlet 'in Azure Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-163">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="bc922-164">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="bc922-164">Valid values are:</span></span> 

- <span data-ttu-id="bc922-165">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="bc922-165">AzureEndpoints</span></span>
- <span data-ttu-id="bc922-166">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="bc922-166">ExternalEndpoints</span></span>
- <span data-ttu-id="bc922-167">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="bc922-167">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-168">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="bc922-168">-Weight</span></span>
<span data-ttu-id="bc922-169">Traffic Manager 'ın uç noktaya atadığı ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="bc922-169">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="bc922-170">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="bc922-170">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="bc922-171">Varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="bc922-171">The default value is one (1).</span></span>
<span data-ttu-id="bc922-172">Bu parametre yalnızca, Traffic Manager profili ağırlıklı trafik yönlendirme yöntemiyle yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="bc922-172">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc922-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc922-173">CommonParameters</span></span>
<span data-ttu-id="bc922-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bc922-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc922-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc922-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc922-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bc922-176">INPUTS</span></span>

### <span data-ttu-id="bc922-177">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc922-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="bc922-178">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="bc922-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="bc922-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bc922-179">OUTPUTS</span></span>

### <span data-ttu-id="bc922-180">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc922-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="bc922-181">Bu cmdlet değiştirilmiş bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="bc922-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="bc922-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bc922-182">NOTES</span></span>

## <span data-ttu-id="bc922-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bc922-183">RELATED LINKS</span></span>

[<span data-ttu-id="bc922-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc922-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="bc922-185">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bc922-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="bc922-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="bc922-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="bc922-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bc922-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


