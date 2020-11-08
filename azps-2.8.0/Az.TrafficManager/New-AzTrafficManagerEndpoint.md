---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9e15979b7e54ef926e7b4355a70568f39594112f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932768"
---
# <span data-ttu-id="8192d-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8192d-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="8192d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8192d-102">SYNOPSIS</span></span>
<span data-ttu-id="8192d-103">Traffic Manager profilinde uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8192d-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="8192d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8192d-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8192d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8192d-105">DESCRIPTION</span></span>
<span data-ttu-id="8192d-106">**New-AzTrafficManagerEndpoint** cmdlet 'ı bir Azure Traffic Manager profilinde uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8192d-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="8192d-107">Bu cmdlet, her yeni uç noktayı Traffic Manager hizmetine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="8192d-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="8192d-108">Yerel bir Traffic Manager profil nesnesine birden çok uç nokta eklemek ve değişiklikleri tek bir işlemde uygulamak için Add-AzTrafficManagerEndpointConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8192d-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="8192d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8192d-109">EXAMPLES</span></span>

### <span data-ttu-id="8192d-110">Örnek 1: bir profil için dış uç nokta oluşturma</span><span class="sxs-lookup"><span data-stu-id="8192d-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="8192d-111">Bu komut, ResourceGroup11 adlı kaynak grubundaki ContosoProfile adlı profildeki contoso adlı bir dış uç nokta oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8192d-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="8192d-112">Örnek 2: bir profil için Azure uç noktası oluşturma</span><span class="sxs-lookup"><span data-stu-id="8192d-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="8192d-113">Bu komut, kaynak grup ResourceGroup11 ' nde ContosoProfile adlı profildeki contoso adlı bir Azure uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8192d-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="8192d-114">Azure Endpoint, Azure Resource Manager KIMLIĞI 'nin *Targetresourceıd* içindeki URI yolundan verildiği Azure Web App 'e işaret ediyor.</span><span class="sxs-lookup"><span data-stu-id="8192d-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="8192d-115">Web App kaynağı bu konumu sağladığı için, komut, *Endpointlocation* parametresini belirtmez.</span><span class="sxs-lookup"><span data-stu-id="8192d-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="8192d-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8192d-116">PARAMETERS</span></span>

### <span data-ttu-id="8192d-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="8192d-117">-CustomHeader</span></span>
<span data-ttu-id="8192d-118">Yoklama istekleri için özel üstbilgi adı ve değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="8192d-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="8192d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8192d-119">-DefaultProfile</span></span>
<span data-ttu-id="8192d-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8192d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8192d-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="8192d-121">-EndpointLocation</span></span>
<span data-ttu-id="8192d-122">Performans trafiği yönlendirme yönteminde kullanılacak uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="8192d-123">Bu parametre yalnızca ExternalEndpoints veya Nestedenvseçpoints türünün uç noktalarına uygulanabilir.</span><span class="sxs-lookup"><span data-stu-id="8192d-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="8192d-124">Performans trafiği yönlendirme yöntemi kullanıldığında bu parametreyi belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="8192d-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="8192d-125">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="8192d-125">Specify an Azure region name.</span></span>
<span data-ttu-id="8192d-126">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="8192d-126">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="8192d-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="8192d-127">-EndpointStatus</span></span>
<span data-ttu-id="8192d-128">Uç noktasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="8192d-129">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8192d-129">Valid values are:</span></span> 

- <span data-ttu-id="8192d-130">Etkin</span><span class="sxs-lookup"><span data-stu-id="8192d-130">Enabled</span></span> 
- <span data-ttu-id="8192d-131">DISABLED</span><span class="sxs-lookup"><span data-stu-id="8192d-131">Disabled</span></span> 

<span data-ttu-id="8192d-132">Durum etkinleştirilirse, uç nokta uç durumu için araştırılan ve trafik yönlendirme yöntemine dahil edilmiştir.</span><span class="sxs-lookup"><span data-stu-id="8192d-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="8192d-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="8192d-133">-GeoMapping</span></span>
<span data-ttu-id="8192d-134">' Coğrafi ' trafik yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş bölgelerin listesi.</span><span class="sxs-lookup"><span data-stu-id="8192d-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="8192d-135">Lütfen kabul edilen değerlerin tam listesi için lütfen Traffic Manager belgelerine başvurun.</span><span class="sxs-lookup"><span data-stu-id="8192d-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="8192d-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="8192d-136">-MinChildEndpoints</span></span>
<span data-ttu-id="8192d-137">Azure bölgesi adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="8192d-137">Specify an Azure region name.</span></span>
<span data-ttu-id="8192d-138">Azure bölgelerinin tam listesi için bkz: Azure bölgeleri https://azure.microsoft.com/regions/ ( https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="8192d-138">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="8192d-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="8192d-139">-Name</span></span>
<span data-ttu-id="8192d-140">Bu cmdlet 'in oluşturduğu Traffic Manager uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8192d-141">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="8192d-141">-Priority</span></span>
<span data-ttu-id="8192d-142">Traffic Manager 'ın uç noktaya atadığı önceliği belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="8192d-143">Bu parametre, yalnızca Traffic Manager profili öncelik için öncelik için öncelik için yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8192d-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="8192d-144">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="8192d-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="8192d-145">Düşük değerler daha yüksek öncelikleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="8192d-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="8192d-146">Öncelik belirtirseniz, profildeki tüm uç noktalarda öncelikleri belirtmeniz gerekir ve iki uç nokta aynı öncelik değerini paylaşabilir.</span><span class="sxs-lookup"><span data-stu-id="8192d-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="8192d-147">Öncelikler belirtmezseniz, Traffic Manager uç noktalara, bir (1) başlayarak, profilin uç noktalarını listelerse, varsayılan öncelik değerlerini uç noktalara atar.</span><span class="sxs-lookup"><span data-stu-id="8192d-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="8192d-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8192d-148">-ProfileName</span></span>
<span data-ttu-id="8192d-149">Bu cmdlet 'in uç nokta eklediği bir Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="8192d-150">Profil edinmek için New-AzTrafficManagerProfile veya Get-AzTrafficManagerProfile cmdlet 'lerini kullanın.</span><span class="sxs-lookup"><span data-stu-id="8192d-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="8192d-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8192d-151">-ResourceGroupName</span></span>
<span data-ttu-id="8192d-152">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8192d-153">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8192d-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8192d-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="8192d-154">-SubnetMapping</span></span>
<span data-ttu-id="8192d-155">' Alt ağ ' trafiği yönlendirme yöntemi kullanılırken bu uç noktaya eşlenmiş adres aralıkları veya alt ağlar listesi.</span><span class="sxs-lookup"><span data-stu-id="8192d-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="8192d-156">-Hedef</span><span class="sxs-lookup"><span data-stu-id="8192d-156">-Target</span></span>
<span data-ttu-id="8192d-157">Uç noktanın tam DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="8192d-158">Traffic Manager trafiği bu uç noktaya yönlendirirse DNS yanıtlarında bu değeri döndürür.</span><span class="sxs-lookup"><span data-stu-id="8192d-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="8192d-159">Bu parametreyi yalnızca ExternalEndpoints uç noktası türü için belirtin.</span><span class="sxs-lookup"><span data-stu-id="8192d-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="8192d-160">Diğer uç nokta türleri için bunun yerine *Targetresourceıd* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8192d-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="8192d-161">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="8192d-161">-TargetResourceId</span></span>
<span data-ttu-id="8192d-162">Hedefin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="8192d-163">Bu parametreyi yalnızca AzureEndpoints ve Nestedenvseçpoints uç noktası türleri için belirtin.</span><span class="sxs-lookup"><span data-stu-id="8192d-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="8192d-164">ExternalEndpoints uç noktası türü için bunun yerine *target* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="8192d-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="8192d-165">-Tür</span><span class="sxs-lookup"><span data-stu-id="8192d-165">-Type</span></span>
<span data-ttu-id="8192d-166">Bu cmdlet 'in Traffic Manager profiline eklediği uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="8192d-167">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8192d-167">Valid values are:</span></span> 

- <span data-ttu-id="8192d-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="8192d-168">AzureEndpoints</span></span>
- <span data-ttu-id="8192d-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="8192d-169">ExternalEndpoints</span></span>
- <span data-ttu-id="8192d-170">Nestedenvseçpuanlar</span><span class="sxs-lookup"><span data-stu-id="8192d-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="8192d-171">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="8192d-171">-Weight</span></span>
<span data-ttu-id="8192d-172">Traffic Manager 'ın uç noktaya atadığı ağırlığı belirtir.</span><span class="sxs-lookup"><span data-stu-id="8192d-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="8192d-173">Geçerli değerler 1 ile 1000 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="8192d-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="8192d-174">Varsayılan değer bir (1) olur.</span><span class="sxs-lookup"><span data-stu-id="8192d-174">The default value is one (1).</span></span>
<span data-ttu-id="8192d-175">Bu parametre yalnızca, Traffic Manager profili ağırlıklı trafik yönlendirme yöntemiyle yapılandırılmışsa kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8192d-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="8192d-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8192d-176">CommonParameters</span></span>
<span data-ttu-id="8192d-177">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8192d-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8192d-178">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8192d-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8192d-179">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8192d-179">INPUTS</span></span>

### <span data-ttu-id="8192d-180">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8192d-180">None</span></span>

## <span data-ttu-id="8192d-181">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8192d-181">OUTPUTS</span></span>

### <span data-ttu-id="8192d-182">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8192d-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8192d-183">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8192d-183">NOTES</span></span>

## <span data-ttu-id="8192d-184">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8192d-184">RELATED LINKS</span></span>

[<span data-ttu-id="8192d-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8192d-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8192d-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8192d-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8192d-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8192d-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8192d-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8192d-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="8192d-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8192d-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="8192d-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8192d-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8192d-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8192d-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

