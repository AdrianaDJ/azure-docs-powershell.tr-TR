---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: a73233908f37463c591aeb2e3d6b00eeb3c511ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760400"
---
# <span data-ttu-id="694c5-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="694c5-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="694c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="694c5-102">SYNOPSIS</span></span>
<span data-ttu-id="694c5-103">Uygulama ağ geçidi yol kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="694c5-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="694c5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="694c5-104">SYNTAX</span></span>

### <span data-ttu-id="694c5-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="694c5-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="694c5-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="694c5-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="694c5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="694c5-107">DESCRIPTION</span></span>
<span data-ttu-id="694c5-108">**Yeni-AzApplicationGatewayPathRuleConfig** cmdlet 'i bir uygulama ağ geçidi yolu kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="694c5-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="694c5-109">Bu cmdlet tarafından oluşturulan kurallar URL yol haritası yapılandırma ayarları koleksiyonuna eklenebilir ve ardından bir ağ geçidine atanabilir.</span><span class="sxs-lookup"><span data-stu-id="694c5-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="694c5-110">Yol haritası yapılandırma ayarları uygulama ağ geçidi yük dengelemesi 'nde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="694c5-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="694c5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="694c5-111">EXAMPLES</span></span>

### <span data-ttu-id="694c5-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="694c5-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="694c5-113">Bu komutlar yeni bir uygulama ağ geçidi yol kuralı oluşturur ve ardından bu kuralı uygulama ağ geçidine atamak için **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="694c5-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="694c5-114">Bunu yapmak için ilk komut ağ geçidi ContosoApplicationGateway 'e bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="694c5-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="694c5-115">Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="694c5-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="694c5-116">Sonraki iki komut arka uç adres havuzu ve arka uç HTTP Ayarları nesnesi oluşturur; yol kuralı nesnesi oluşturmak için bu nesneler ($AddressPool ve $HttpSettings 'te depolanan) gereklidir.</span><span class="sxs-lookup"><span data-stu-id="694c5-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="694c5-117">Dördüncü komut, yol kuralı nesnesini oluşturur ve $PathRuleConfig adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="694c5-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="694c5-118">Beşinci komut, yapılandırma ayarlarını ve bu ayarlarda bulunan yeni yol kuralını ContosoApplicationGateway 'e eklemek için **Add-AzApplicationGatewayUrlPathMapConfig** öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="694c5-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="694c5-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="694c5-119">PARAMETERS</span></span>

### <span data-ttu-id="694c5-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="694c5-120">-BackendAddressPool</span></span>
<span data-ttu-id="694c5-121">Ağ Geçidi yol kuralları yapılandırma ayarlarına eklenecek bir arka uç adres havuzu ayarları koleksiyonuna bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="694c5-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="694c5-122">Bu nesne başvurusunu, New-AzApplicationGatewayBackendAddressPool cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="694c5-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="694c5-123">Yukarıdaki komut, adres havuzuna iki IP adresi (192.16.1.1 ve 192.168.1.2) ekler.</span><span class="sxs-lookup"><span data-stu-id="694c5-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="694c5-124">IP adresinin tırnak işaretleri içine alındığına ve virgül kullanılarak ayrıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="694c5-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="694c5-125">Sonuç değişkeni $AddressPool, *Defaultbackendaddresspool* parametresinin parametre değeri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="694c5-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="694c5-126">Arka uç adres havuzu, arka uç sunucularındaki IP adreslerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="694c5-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="694c5-127">Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="694c5-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="694c5-128">Bu parametreyi kullanırsanız, *Defaultbackendaddresspoıd* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="694c5-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-129">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="694c5-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="694c5-130">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç adres havuzunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="694c5-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="694c5-131">Adres havuzu kimlikleri Get-AzApplicationGatewayBackendAddressPool cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="694c5-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="694c5-132">KIMLIĞI aldıktan sonra *defaultbackendaddresspool* parametresi yerine *Defaultbackendaddresspoıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="694c5-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="694c5-133">Örneğin:-Defaultbackendaddresspoıd "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" arka uç adres havuzu arka uç sunucularındaki IP adreslerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="694c5-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="694c5-134">Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="694c5-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="694c5-135">-BackendHttpSettings</span></span>
<span data-ttu-id="694c5-136">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenecek bir arka uç HTTP ayarları koleksiyonuna bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="694c5-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="694c5-137">Bu nesne başvurusunu, New-AzApplicationGatewayBackendHttpSettings cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "Contosohttpseting"-port 80-Protocol "http"-, ıebasedaffinity "Disabled" sonuç değişkeni $HttpSettings, *Defaultbackendaddresspool* parametresi için parametre değeri olarak kullanılabilir:-DefaultBackendHttpSettings $HttpSettings arka uç havuzu için bağlantı noktası, protokol ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="694c5-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="694c5-138">Bu parametreyi kullanırsanız, *Defaultbackendhttpsettingsid* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="694c5-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="694c5-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="694c5-140">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç HTTP ayarları koleksiyonunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="694c5-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="694c5-141">HTTP ayar kimlikleri, Get-AzApplicationGatewayBackendHttpSettings cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="694c5-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="694c5-142">KIMLIĞI aldıktan sonra, *Defaultbackendhttpsettings* parametresi yerine *Defaultbackendhttpsettingsıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="694c5-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="694c5-143">Örneğin:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" arka uç HTTP ayarları, bir arka uç havuzunun bağlantı noktası, protokolü ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="694c5-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="694c5-144">Bu parametreyi kullanırsanız, *Defaultbackendhttpsettings* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="694c5-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694c5-145">-DefaultProfile</span></span>
<span data-ttu-id="694c5-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="694c5-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="694c5-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="694c5-147">-Name</span></span>
<span data-ttu-id="694c5-148">Bu cmdlet 'in oluşturduğu yol kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="694c5-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="694c5-149">-Yollar</span><span class="sxs-lookup"><span data-stu-id="694c5-149">-Paths</span></span>
<span data-ttu-id="694c5-150">Bir veya daha fazla uygulama ağ geçidi yol kuralını belirtir.</span><span class="sxs-lookup"><span data-stu-id="694c5-150">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="694c5-151">-RedirectConfiguration</span></span>
<span data-ttu-id="694c5-152">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="694c5-152">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-153">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="694c5-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="694c5-154">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="694c5-154">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="694c5-155">-RewriteRuleSet</span></span>
<span data-ttu-id="694c5-156">Uygulama ağ geçidi Rewriterset</span><span class="sxs-lookup"><span data-stu-id="694c5-156">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="694c5-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="694c5-158">Uygulama ağ geçidi Rewriterset 'in KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="694c5-158">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694c5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694c5-159">CommonParameters</span></span>
<span data-ttu-id="694c5-160">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="694c5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694c5-161">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694c5-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694c5-162">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="694c5-162">INPUTS</span></span>

### <span data-ttu-id="694c5-163">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="694c5-163">None</span></span>

## <span data-ttu-id="694c5-164">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="694c5-164">OUTPUTS</span></span>

### <span data-ttu-id="694c5-165">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="694c5-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="694c5-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="694c5-166">NOTES</span></span>

## <span data-ttu-id="694c5-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="694c5-167">RELATED LINKS</span></span>

[<span data-ttu-id="694c5-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="694c5-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="694c5-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="694c5-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="694c5-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="694c5-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="694c5-171">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="694c5-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="694c5-172">Yeni-AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="694c5-172">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="694c5-173">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="694c5-173">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="694c5-174">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="694c5-174">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="694c5-175">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="694c5-175">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="694c5-176">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="694c5-176">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


