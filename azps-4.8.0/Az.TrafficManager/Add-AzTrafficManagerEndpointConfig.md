---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 77bb21030c24d9fed159160262c23e1e821e0fe1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107444"
---
# <span data-ttu-id="6a515-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6a515-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="6a515-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a515-102">SYNOPSIS</span></span>
<span data-ttu-id="6a515-103">Yerel bir Traffic Manager profil nesnesine uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="6a515-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="6a515-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a515-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a515-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a515-105">DESCRIPTION</span></span>
<span data-ttu-id="6a515-106">**Add-AzTrafficManagerEndpointConfig** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="6a515-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="6a515-107">New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a515-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="6a515-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="6a515-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="6a515-109">Set-AzTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="6a515-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="6a515-110">Uç nokta oluşturmak ve değişikliği tek bir işlemde uygulamak için New-AzTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a515-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="6a515-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a515-111">EXAMPLES</span></span>

### <span data-ttu-id="6a515-112">Örnek 1: profile uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="6a515-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="6a515-113">İlk komut **Get-AzTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="6a515-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="6a515-114">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="6a515-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="6a515-115">İkinci komut, $TrafficManagerProfile depolanan profile contoso adlı bir uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="6a515-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="6a515-116">Komut uç nokta yapılandırma verilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="6a515-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="6a515-117">Bu komut yalnızca yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6a515-117">This command changes only the local object.</span></span>

<span data-ttu-id="6a515-118">Son komutu, Azure 'daki Traffic Manager profilini $TrafficManagerProfile yerel değerle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6a515-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="6a515-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a515-119">PARAMETERS</span></span>

### <span data-ttu-id="6a515-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="6a515-120">-CustomHeader</span></span>
<span data-ttu-id="6a515-121">Yoklama istekleri için özel üstbilgi adı ve değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="6a515-121">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a515-122">-DefaultProfile</span></span>
<span data-ttu-id="6a515-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6a515-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a515-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="6a515-124">-EndpointLocation</span></span>
<span data-ttu-id="6a515-125">Performans trafiği yönlendirme yönteminde kullanılacak uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="6a515-126">Bu parametre yalnızca ExternalEndpoints veya Nestedenvseçval türünün uç noktalarına uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="6a515-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="6a515-127">Performans trafiği yönlendirme yöntemi kullanıldığında bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6a515-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="6a515-128">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a515-128">Specify an Azure region name.</span></span>
<span data-ttu-id="6a515-129">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri http://azure.microsoft.com/regions/ ( http://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="6a515-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6a515-130">-EndpointName</span></span>
<span data-ttu-id="6a515-131">Bu cmdlet 'in eklediği Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="6a515-132">-EndpointStatus</span></span>
<span data-ttu-id="6a515-133">Uç noktasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="6a515-134">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="6a515-134">Valid values are:</span></span> 

- <span data-ttu-id="6a515-135">Etkin</span><span class="sxs-lookup"><span data-stu-id="6a515-135">Enabled</span></span> 
- <span data-ttu-id="6a515-136">DISABLED</span><span class="sxs-lookup"><span data-stu-id="6a515-136">Disabled</span></span> 

<span data-ttu-id="6a515-137">Durum etkinleştirilirse, uç nokta uç durumu için araştırılan ve trafik yönlendirme yöntemine dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="6a515-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="6a515-138">-GeoMapping</span></span>
<span data-ttu-id="6a515-139">' Coğrafi ' trafik yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş bölgelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="6a515-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="6a515-140">Lütfen [kabul edilen değerlerin tam listesi](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)Için lütfen Traffic Manager belgelerine başvurun.</span><span class="sxs-lookup"><span data-stu-id="6a515-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

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

### <span data-ttu-id="6a515-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="6a515-141">-MinChildEndpoints</span></span>
<span data-ttu-id="6a515-142">Üst profildeki Iç Içe uç noktasının kullanılabilir kabul edildiği, alt profilde kullanılması gereken en az uç nokta sayısı.</span><span class="sxs-lookup"><span data-stu-id="6a515-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="6a515-143">Yalnızca ' Nestedenvseçın ' türünde uç noktaya uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="6a515-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-144">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="6a515-144">-Priority</span></span>
<span data-ttu-id="6a515-145">Traffic Manager 'ın uç noktaya atadığı önceliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="6a515-146">Bu parametre, yalnızca Traffic Manager profili öncelik için öncelik için öncelik için yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6a515-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="6a515-147">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="6a515-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="6a515-148">Düşük değerler daha yüksek öncelikleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="6a515-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="6a515-149">Öncelik belirtirseniz, profildeki tüm uç noktalarda öncelikleri belirtmeniz gerekir ve iki uç nokta aynı öncelik değerini paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="6a515-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="6a515-150">Öncelikler belirtmezseniz, Traffic Manager uç noktalara, bir (1) başlayarak, profilin uç noktalarını listelerse, varsayılan öncelik değerlerini uç noktalara atar.</span><span class="sxs-lookup"><span data-stu-id="6a515-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="6a515-151">-SubnetMapping</span></span>
<span data-ttu-id="6a515-152">' Alt ağ ' trafiği yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş adres aralıkları veya alt ağlar listesi.</span><span class="sxs-lookup"><span data-stu-id="6a515-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-153">-Hedef</span><span class="sxs-lookup"><span data-stu-id="6a515-153">-Target</span></span>
<span data-ttu-id="6a515-154">Uç noktanın tam DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="6a515-155">Traffic Manager trafiği bu uç noktaya yönlendirirse DNS yanıtlarında bu değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="6a515-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="6a515-156">Bu parametreyi yalnızca ExternalEndpoints uç noktası türü için belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a515-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="6a515-157">Diğer uç nokta türleri için bunun yerine *Targetresourceıd* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a515-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-158">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="6a515-158">-TargetResourceId</span></span>
<span data-ttu-id="6a515-159">Hedefin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="6a515-160">Bu parametreyi yalnızca AzureEndpoints ve Nestedenvseçpoints uç noktası türleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a515-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="6a515-161">ExternalEndpoints uç noktası türü için bunun yerine *target* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6a515-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a515-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="6a515-163">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="6a515-164">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="6a515-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6a515-165">**TrafficManagerProfile** nesnesi almak için Get-AzTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a515-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-166">-Tür</span><span class="sxs-lookup"><span data-stu-id="6a515-166">-Type</span></span>
<span data-ttu-id="6a515-167">Bu cmdlet 'in Azure Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="6a515-168">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="6a515-168">Valid values are:</span></span> 

- <span data-ttu-id="6a515-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="6a515-169">AzureEndpoints</span></span>
- <span data-ttu-id="6a515-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="6a515-170">ExternalEndpoints</span></span>
- <span data-ttu-id="6a515-171">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="6a515-171">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-172">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="6a515-172">-Weight</span></span>
<span data-ttu-id="6a515-173">Traffic Manager 'ın uç noktaya atadığı ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a515-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="6a515-174">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="6a515-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="6a515-175">Varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="6a515-175">The default value is one (1).</span></span>
<span data-ttu-id="6a515-176">Bu parametre yalnızca, Traffic Manager profili ağırlıklı trafik yönlendirme yöntemiyle yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6a515-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a515-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a515-177">CommonParameters</span></span>
<span data-ttu-id="6a515-178">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a515-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a515-179">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a515-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a515-180">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a515-180">INPUTS</span></span>

### <span data-ttu-id="6a515-181">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a515-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6a515-182">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a515-182">OUTPUTS</span></span>

### <span data-ttu-id="6a515-183">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a515-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="6a515-184">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a515-184">NOTES</span></span>

## <span data-ttu-id="6a515-185">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a515-185">RELATED LINKS</span></span>

[<span data-ttu-id="6a515-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a515-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="6a515-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a515-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6a515-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="6a515-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="6a515-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6a515-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


