---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586880"
---
# <span data-ttu-id="4a507-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="4a507-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="4a507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a507-102">SYNOPSIS</span></span>
<span data-ttu-id="4a507-103">Yerel bir Traffic Manager profil nesnesine uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="4a507-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a507-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a507-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a507-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a507-105">DESCRIPTION</span></span>
<span data-ttu-id="4a507-106">**Add-AzureRmTrafficManagerEndpointConfig** cmdlet 'i yerel bir Azure Traffic Manager profil nesnesine uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="4a507-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="4a507-107">New-AzureRmTrafficManagerProfile veya Get-AzureRmTrafficManagerProfile cmdlet 'lerini kullanarak profil alabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4a507-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="4a507-108">Bu cmdlet yerel profil nesnesinde çalışır.</span><span class="sxs-lookup"><span data-stu-id="4a507-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="4a507-109">Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak Traffic Manager profilindeki değişikliklerinizi kaydedin.</span><span class="sxs-lookup"><span data-stu-id="4a507-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="4a507-110">Uç nokta oluşturmak ve değişikliği tek bir işlemde uygulamak için New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4a507-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="4a507-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a507-111">EXAMPLES</span></span>

### <span data-ttu-id="4a507-112">Örnek 1: profile uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="4a507-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="4a507-113">İlk komut **Get-AzureRmTrafficManagerProfile** cmdlet 'ini kullanarak bir Azure Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="4a507-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="4a507-114">Komut, $TrafficManagerProfile değişkeninde yerel profili depolar.</span><span class="sxs-lookup"><span data-stu-id="4a507-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="4a507-115">İkinci komut, $TrafficManagerProfile depolanan profile contoso adlı bir uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="4a507-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="4a507-116">Komut uç nokta yapılandırma verilerini içerir.</span><span class="sxs-lookup"><span data-stu-id="4a507-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="4a507-117">Bu komut yalnızca yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4a507-117">This command changes only the local object.</span></span>

<span data-ttu-id="4a507-118">Son komutu, Azure 'daki Traffic Manager profilini $TrafficManagerProfile yerel değerle eşleşecek şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="4a507-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="4a507-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a507-119">PARAMETERS</span></span>

### <span data-ttu-id="4a507-120">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="4a507-120">-EndpointLocation</span></span>
<span data-ttu-id="4a507-121">Performans trafiği yönlendirme yönteminde kullanılacak uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-121">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="4a507-122">Bu parametre yalnızca ExternalEndpoints veya Nestedenvseçval türünün uç noktalarına uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="4a507-122">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="4a507-123">Performans trafiği yönlendirme yöntemi kullanıldığında bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4a507-123">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="4a507-124">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="4a507-124">Specify an Azure region name.</span></span>
<span data-ttu-id="4a507-125">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="4a507-125">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="4a507-126">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="4a507-126">-EndpointName</span></span>
<span data-ttu-id="4a507-127">Bu cmdlet 'in eklediği Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-127">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4a507-128">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="4a507-128">-EndpointStatus</span></span>
<span data-ttu-id="4a507-129">Uç noktasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-129">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="4a507-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="4a507-130">Valid values are:</span></span> 

- <span data-ttu-id="4a507-131">Etkin</span><span class="sxs-lookup"><span data-stu-id="4a507-131">Enabled</span></span> 
- <span data-ttu-id="4a507-132">DISABLED</span><span class="sxs-lookup"><span data-stu-id="4a507-132">Disabled</span></span> 

<span data-ttu-id="4a507-133">Durum etkinleştirilirse, uç nokta uç durumu için araştırılan ve trafik yönlendirme yöntemine dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="4a507-133">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="4a507-134">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="4a507-134">-GeoMapping</span></span>
<span data-ttu-id="4a507-135">' Coğrafi ' trafik yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş bölgelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="4a507-135">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="4a507-136">Lütfen [kabul edilen değerlerin tam listesi](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)Için lütfen Traffic Manager belgelerine başvurun.</span><span class="sxs-lookup"><span data-stu-id="4a507-136">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="4a507-137">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="4a507-137">-MinChildEndpoints</span></span>
<span data-ttu-id="4a507-138">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="4a507-138">Specify an Azure region name.</span></span>
<span data-ttu-id="4a507-139">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="4a507-139">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="4a507-140">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="4a507-140">-Priority</span></span>
<span data-ttu-id="4a507-141">Traffic Manager 'ın uç noktaya atadığı önceliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-141">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="4a507-142">Bu parametre, yalnızca Traffic Manager profili öncelik için öncelik için öncelik için yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4a507-142">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="4a507-143">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="4a507-143">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="4a507-144">Düşük değerler daha yüksek öncelikleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="4a507-144">Lower values represent higher priority.</span></span>

<span data-ttu-id="4a507-145">Öncelik belirtirseniz, profildeki tüm uç noktalarda öncelikleri belirtmeniz gerekir ve iki uç nokta aynı öncelik değerini paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="4a507-145">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="4a507-146">Öncelikler belirtmezseniz, Traffic Manager uç noktalara, bir (1) başlayarak, profilin uç noktalarını listelerse, varsayılan öncelik değerlerini uç noktalara atar.</span><span class="sxs-lookup"><span data-stu-id="4a507-146">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="4a507-147">-Hedef</span><span class="sxs-lookup"><span data-stu-id="4a507-147">-Target</span></span>
<span data-ttu-id="4a507-148">Uç noktanın tam DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-148">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="4a507-149">Traffic Manager trafiği bu uç noktaya yönlendirirse DNS yanıtlarında bu değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="4a507-149">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="4a507-150">Bu parametreyi yalnızca ExternalEndpoints uç noktası türü için belirtin.</span><span class="sxs-lookup"><span data-stu-id="4a507-150">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="4a507-151">Diğer uç nokta türleri için bunun yerine *Targetresourceıd* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4a507-151">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="4a507-152">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="4a507-152">-TargetResourceId</span></span>
<span data-ttu-id="4a507-153">Hedefin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-153">Specifies resource ID of the target.</span></span>
<span data-ttu-id="4a507-154">Bu parametreyi yalnızca AzureEndpoints ve Nestedenvseçpoints uç noktası türleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="4a507-154">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="4a507-155">ExternalEndpoints uç noktası türü için bunun yerine *target* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4a507-155">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="4a507-156">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4a507-156">-TrafficManagerProfile</span></span>
<span data-ttu-id="4a507-157">Yerel bir **TrafficManagerProfile** nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-157">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="4a507-158">Bu cmdlet bu yerel nesneyi değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4a507-158">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="4a507-159">**TrafficManagerProfile** nesnesi almak için Get-AzureRmTrafficManagerProfile cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4a507-159">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4a507-160">-Tür</span><span class="sxs-lookup"><span data-stu-id="4a507-160">-Type</span></span>
<span data-ttu-id="4a507-161">Bu cmdlet 'in Azure Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-161">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="4a507-162">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="4a507-162">Valid values are:</span></span> 

- <span data-ttu-id="4a507-163">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="4a507-163">AzureEndpoints</span></span>
- <span data-ttu-id="4a507-164">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="4a507-164">ExternalEndpoints</span></span>
- <span data-ttu-id="4a507-165">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="4a507-165">NestedEndpoints</span></span>

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

### <span data-ttu-id="4a507-166">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="4a507-166">-Weight</span></span>
<span data-ttu-id="4a507-167">Traffic Manager 'ın uç noktaya atadığı ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a507-167">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="4a507-168">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="4a507-168">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="4a507-169">Varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="4a507-169">The default value is one (1).</span></span>
<span data-ttu-id="4a507-170">Bu parametre yalnızca, Traffic Manager profili ağırlıklı trafik yönlendirme yöntemiyle yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4a507-170">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="4a507-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a507-171">-DefaultProfile</span></span>
<span data-ttu-id="4a507-172">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a507-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a507-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a507-173">CommonParameters</span></span>
<span data-ttu-id="4a507-174">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a507-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a507-175">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a507-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a507-176">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a507-176">INPUTS</span></span>

### <span data-ttu-id="4a507-177">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4a507-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="4a507-178">Bu cmdlet, bu cmdlet 'e bir **TrafficManagerProfile** nesnesi kabul eder.</span><span class="sxs-lookup"><span data-stu-id="4a507-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="4a507-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a507-179">OUTPUTS</span></span>

### <span data-ttu-id="4a507-180">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4a507-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="4a507-181">Bu cmdlet değiştirilmiş bir **TrafficManagerProfile** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="4a507-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="4a507-182">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a507-182">NOTES</span></span>

## <span data-ttu-id="4a507-183">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a507-183">RELATED LINKS</span></span>

[<span data-ttu-id="4a507-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4a507-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4a507-185">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4a507-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="4a507-186">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="4a507-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="4a507-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4a507-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


