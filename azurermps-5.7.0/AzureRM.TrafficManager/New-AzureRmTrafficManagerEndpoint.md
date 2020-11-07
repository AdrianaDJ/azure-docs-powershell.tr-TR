---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763201"
---
# <span data-ttu-id="aac46-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aac46-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="aac46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac46-102">SYNOPSIS</span></span>
<span data-ttu-id="aac46-103">Traffic Manager profilinde uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac46-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aac46-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aac46-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aac46-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="aac46-105">DESCRIPTION</span></span>
<span data-ttu-id="aac46-106">**New-AzureRmTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profilinde uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac46-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="aac46-107">Bu cmdlet, her yeni uç noktayı Traffic Manager hizmetine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="aac46-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="aac46-108">Yerel bir Traffic Manager profil nesnesine birden çok uç nokta eklemek ve değişiklikleri tek bir işlemde uygulamak için Add-AzureRmTrafficManagerEndpointConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aac46-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="aac46-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aac46-109">EXAMPLES</span></span>

### <span data-ttu-id="aac46-110">Örnek 1: bir profil için dış uç nokta oluşturma</span><span class="sxs-lookup"><span data-stu-id="aac46-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="aac46-111">Bu komut, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profildeki contoso adlı bir dış uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac46-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="aac46-112">Örnek 2: bir profil için Azure uç noktası oluşturma</span><span class="sxs-lookup"><span data-stu-id="aac46-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="aac46-113">Bu komut, kaynak grup ResouceGroup11 ' nde ContosoProfile adlı profildeki contoso adlı bir Azure uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac46-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="aac46-114">Azure Endpoint, Azure Resource Manager KIMLIĞI 'nin *Targetresourceıd* içindeki URI yolundan verildiği Azure Web App 'e işaret ediyor.</span><span class="sxs-lookup"><span data-stu-id="aac46-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="aac46-115">Web App kaynağı bu konumu sağladığı için, komut, *Endpointlocation* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="aac46-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="aac46-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aac46-116">PARAMETERS</span></span>

### <span data-ttu-id="aac46-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac46-117">-DefaultProfile</span></span>
<span data-ttu-id="aac46-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aac46-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aac46-119">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="aac46-119">-EndpointLocation</span></span>
<span data-ttu-id="aac46-120">Performans trafiği yönlendirme yönteminde kullanılacak uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-120">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="aac46-121">Bu parametre yalnızca ExternalEndpoints veya Nestedenvseçpoints türünün uç noktalarına uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="aac46-121">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="aac46-122">Performans trafiği yönlendirme yöntemi kullanıldığında bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="aac46-122">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="aac46-123">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac46-123">Specify an Azure region name.</span></span>
<span data-ttu-id="aac46-124">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="aac46-124">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="aac46-125">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="aac46-125">-EndpointStatus</span></span>
<span data-ttu-id="aac46-126">Uç noktasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-126">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="aac46-127">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="aac46-127">Valid values are:</span></span> 

- <span data-ttu-id="aac46-128">Etkin</span><span class="sxs-lookup"><span data-stu-id="aac46-128">Enabled</span></span> 
- <span data-ttu-id="aac46-129">DISABLED</span><span class="sxs-lookup"><span data-stu-id="aac46-129">Disabled</span></span> 

<span data-ttu-id="aac46-130">Durum etkinleştirilirse, uç nokta uç durumu için araştırılan ve trafik yönlendirme yöntemine dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="aac46-130">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="aac46-131">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="aac46-131">-GeoMapping</span></span>
<span data-ttu-id="aac46-132">' Coğrafi ' trafik yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş bölgelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="aac46-132">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="aac46-133">Lütfen kabul edilen değerlerin tam listesi için lütfen Traffic Manager belgelerine başvurun.</span><span class="sxs-lookup"><span data-stu-id="aac46-133">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="aac46-134">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="aac46-134">-MinChildEndpoints</span></span>
<span data-ttu-id="aac46-135">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac46-135">Specify an Azure region name.</span></span>
<span data-ttu-id="aac46-136">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="aac46-136">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="aac46-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="aac46-137">-Name</span></span>
<span data-ttu-id="aac46-138">Bu cmdlet 'in oluşturduğu Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-138">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="aac46-139">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="aac46-139">-Priority</span></span>
<span data-ttu-id="aac46-140">Traffic Manager 'ın uç noktaya atadığı önceliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-140">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="aac46-141">Bu parametre, yalnızca Traffic Manager profili öncelik için öncelik için öncelik için yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aac46-141">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="aac46-142">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="aac46-142">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="aac46-143">Düşük değerler daha yüksek öncelikleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="aac46-143">Lower values represent higher priority.</span></span>

<span data-ttu-id="aac46-144">Öncelik belirtirseniz, profildeki tüm uç noktalarda öncelikleri belirtmeniz gerekir ve iki uç nokta aynı öncelik değerini paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="aac46-144">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="aac46-145">Öncelikler belirtmezseniz, Traffic Manager uç noktalara, bir (1) başlayarak, profilin uç noktalarını listelerse, varsayılan öncelik değerlerini uç noktalara atar.</span><span class="sxs-lookup"><span data-stu-id="aac46-145">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="aac46-146">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="aac46-146">-ProfileName</span></span>
<span data-ttu-id="aac46-147">Bu cmdlet 'in uç nokta eklediği bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-147">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="aac46-148">Profil edinmek için New-AzureRmTrafficManagerProfile veya Get-AzureRmTrafficManagerProfile cmdlet 'lerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aac46-148">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="aac46-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac46-149">-ResourceGroupName</span></span>
<span data-ttu-id="aac46-150">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="aac46-151">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="aac46-151">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aac46-152">-Hedef</span><span class="sxs-lookup"><span data-stu-id="aac46-152">-Target</span></span>
<span data-ttu-id="aac46-153">Uç noktanın tam DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-153">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="aac46-154">Traffic Manager trafiği bu uç noktaya yönlendirirse DNS yanıtlarında bu değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="aac46-154">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="aac46-155">Bu parametreyi yalnızca ExternalEndpoints uç noktası türü için belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac46-155">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="aac46-156">Diğer uç nokta türleri için bunun yerine *Targetresourceıd* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac46-156">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="aac46-157">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="aac46-157">-TargetResourceId</span></span>
<span data-ttu-id="aac46-158">Hedefin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-158">Specifies resource ID of the target.</span></span>
<span data-ttu-id="aac46-159">Bu parametreyi yalnızca AzureEndpoints ve Nestedenvseçpoints uç noktası türleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac46-159">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="aac46-160">ExternalEndpoints uç noktası türü için bunun yerine *target* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="aac46-160">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="aac46-161">-Tür</span><span class="sxs-lookup"><span data-stu-id="aac46-161">-Type</span></span>
<span data-ttu-id="aac46-162">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-162">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="aac46-163">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="aac46-163">Valid values are:</span></span> 

- <span data-ttu-id="aac46-164">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="aac46-164">AzureEndpoints</span></span>
- <span data-ttu-id="aac46-165">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="aac46-165">ExternalEndpoints</span></span>
- <span data-ttu-id="aac46-166">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="aac46-166">NestedEndpoints</span></span>

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

### <span data-ttu-id="aac46-167">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="aac46-167">-Weight</span></span>
<span data-ttu-id="aac46-168">Traffic Manager 'ın uç noktaya atadığı ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="aac46-168">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="aac46-169">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="aac46-169">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="aac46-170">Varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="aac46-170">The default value is one (1).</span></span>
<span data-ttu-id="aac46-171">Bu parametre yalnızca, Traffic Manager profili ağırlıklı trafik yönlendirme yöntemiyle yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="aac46-171">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="aac46-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac46-172">CommonParameters</span></span>
<span data-ttu-id="aac46-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aac46-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac46-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aac46-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac46-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aac46-175">INPUTS</span></span>

### <span data-ttu-id="aac46-176">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="aac46-176">None</span></span>
<span data-ttu-id="aac46-177">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="aac46-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aac46-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aac46-178">OUTPUTS</span></span>

### <span data-ttu-id="aac46-179">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aac46-179">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="aac46-180">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aac46-180">NOTES</span></span>

## <span data-ttu-id="aac46-181">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aac46-181">RELATED LINKS</span></span>

[<span data-ttu-id="aac46-182">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aac46-182">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="aac46-183">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aac46-183">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="aac46-184">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aac46-184">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="aac46-185">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aac46-185">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="aac46-186">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aac46-186">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="aac46-187">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="aac46-187">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="aac46-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="aac46-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


