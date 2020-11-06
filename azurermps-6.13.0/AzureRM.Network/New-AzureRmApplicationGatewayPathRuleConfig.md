---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: f8d9a4266474f18a2dd20fd4ddc0746320359f59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592302"
---
# <span data-ttu-id="24248-101">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24248-101">New-AzureRmApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="24248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24248-102">SYNOPSIS</span></span>
<span data-ttu-id="24248-103">Uygulama ağ geçidi yol kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24248-103">Creates an application gateway path rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24248-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="24248-104">SYNTAX</span></span>

### <span data-ttu-id="24248-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="24248-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24248-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="24248-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24248-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="24248-107">DESCRIPTION</span></span>
<span data-ttu-id="24248-108">**New-AzureRmApplicationGatewayPathRuleConfig** cmdlet 'i bir uygulama ağ geçidi yolu kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24248-108">The **New-AzureRmApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="24248-109">Bu cmdlet tarafından oluşturulan kurallar URL yol haritası yapılandırma ayarları koleksiyonuna eklenebilir ve ardından bir ağ geçidine atanabilir.</span><span class="sxs-lookup"><span data-stu-id="24248-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="24248-110">Yol haritası yapılandırma ayarları uygulama ağ geçidi yük dengelemesi 'nde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="24248-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="24248-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="24248-111">EXAMPLES</span></span>

### <span data-ttu-id="24248-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="24248-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="24248-113">Bu komutlar yeni bir uygulama ağ geçidi yol kuralı oluşturur ve ardından bu kuralı bir uygulama ağ geçidine atamak için **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="24248-113">These commands create a new application gateway path rule and then use the **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="24248-114">Bunu yapmak için ilk komut ağ geçidi ContosoApplicationGateway 'e bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="24248-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="24248-115">Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="24248-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="24248-116">Sonraki iki komut arka uç adres havuzu ve arka uç HTTP Ayarları nesnesi oluşturur; yol kuralı nesnesi oluşturmak için bu nesneler ($AddressPool ve $HttpSettings 'te depolanan) gereklidir.</span><span class="sxs-lookup"><span data-stu-id="24248-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="24248-117">Dördüncü komut, yol kuralı nesnesini oluşturur ve $PathRuleConfig adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="24248-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="24248-118">Beşinci komut, yapılandırma ayarlarını ve bu ayarlarda bulunan yeni yol kuralını ContosoApplicationGateway 'e eklemek için **Add-AzureRmApplicationGatewayUrlPathMapConfig** ' i kullanır.</span><span class="sxs-lookup"><span data-stu-id="24248-118">The fifth command uses **Add-AzureRmApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="24248-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="24248-119">PARAMETERS</span></span>

### <span data-ttu-id="24248-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24248-120">-BackendAddressPool</span></span>
<span data-ttu-id="24248-121">Ağ Geçidi yol kuralları yapılandırma ayarlarına eklenecek bir arka uç adres havuzu ayarları koleksiyonuna bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="24248-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="24248-122">Bu nesne başvurusunu, New-AzureRmApplicationGatewayBackendAddressPool cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz: `$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="24248-122">You can create this object reference by using the New-AzureRmApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="24248-123">Yukarıdaki komut, adres havuzuna iki IP adresi (192.16.1.1 ve 192.168.1.2) ekler.</span><span class="sxs-lookup"><span data-stu-id="24248-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="24248-124">IP adresinin tırnak işaretleri içine alındığına ve virgül kullanılarak ayrıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="24248-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="24248-125">Sonuç değişkeni $AddressPool, *Defaultbackendaddresspool* parametresinin parametre değeri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="24248-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="24248-126">Arka uç adres havuzu, arka uç sunucularındaki IP adreslerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="24248-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="24248-127">Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="24248-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="24248-128">Bu parametreyi kullanırsanız, *Defaultbackendaddresspoıd* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="24248-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="24248-129">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="24248-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="24248-130">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç adres havuzunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="24248-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="24248-131">Adres havuzu kimlikleri Get-AzureRmApplicationGatewayBackendAddressPool cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="24248-131">Address pool IDs can be returned by using the Get-AzureRmApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="24248-132">KIMLIĞI aldıktan sonra *defaultbackendaddresspool* parametresi yerine *Defaultbackendaddresspoıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="24248-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="24248-133">Örneğin:-Defaultbackendaddresspoıd "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" arka uç adres havuzu arka uç sunucularındaki IP adreslerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="24248-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="24248-134">Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="24248-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="24248-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24248-135">-BackendHttpSettings</span></span>
<span data-ttu-id="24248-136">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenecek bir arka uç HTTP ayarları koleksiyonuna bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="24248-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="24248-137">Bu nesne başvurusunu, New-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz: $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "Contosohttpseting"-port 80-Protocol "http"-, ıebasedaffinity "Disabled" sonuç değişkeni $HttpSettings, *Defaultbackendaddresspool* parametresi için parametre değeri olarak kullanılabilir:-DefaultBackendHttpSettings $HttpSettings arka uç havuzu için bağlantı noktası, protokol ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırma.</span><span class="sxs-lookup"><span data-stu-id="24248-137">You can create this object reference by using the New-AzureRmApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="24248-138">Bu parametreyi kullanırsanız, *Defaultbackendhttpsettingsid* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="24248-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="24248-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="24248-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="24248-140">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç HTTP ayarları koleksiyonunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="24248-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="24248-141">HTTP ayar kimlikleri, Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="24248-141">HTTP setting IDs can be returned by using the Get-AzureRmApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="24248-142">KIMLIĞI aldıktan sonra, *Defaultbackendhttpsettings* parametresi yerine *Defaultbackendhttpsettingsıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="24248-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="24248-143">Örneğin:-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" arka uç HTTP ayarları, bir arka uç havuzunun bağlantı noktası, protokolü ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="24248-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="24248-144">Bu parametreyi kullanırsanız, *Defaultbackendhttpsettings* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="24248-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="24248-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24248-145">-DefaultProfile</span></span>
<span data-ttu-id="24248-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="24248-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24248-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="24248-147">-Name</span></span>
<span data-ttu-id="24248-148">Bu cmdlet 'in oluşturduğu yol kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24248-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="24248-149">-Yollar</span><span class="sxs-lookup"><span data-stu-id="24248-149">-Paths</span></span>
<span data-ttu-id="24248-150">Bir veya daha fazla uygulama ağ geçidi yol kuralını belirtir.</span><span class="sxs-lookup"><span data-stu-id="24248-150">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24248-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="24248-151">-RedirectConfiguration</span></span>
<span data-ttu-id="24248-152">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="24248-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="24248-153">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="24248-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="24248-154">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="24248-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="24248-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24248-155">CommonParameters</span></span>
<span data-ttu-id="24248-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="24248-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24248-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24248-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24248-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="24248-158">INPUTS</span></span>

### <span data-ttu-id="24248-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="24248-159">None</span></span>

## <span data-ttu-id="24248-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="24248-160">OUTPUTS</span></span>

### <span data-ttu-id="24248-161">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="24248-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="24248-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="24248-162">NOTES</span></span>

## <span data-ttu-id="24248-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="24248-163">RELATED LINKS</span></span>

[<span data-ttu-id="24248-164">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="24248-164">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="24248-165">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="24248-165">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="24248-166">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="24248-166">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="24248-167">New-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="24248-167">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="24248-168">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="24248-168">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="24248-169">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="24248-169">New-AzureRmApplicationGatewayPathRuleConfig</span></span>](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="24248-170">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="24248-170">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="24248-171">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="24248-171">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="24248-172">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="24248-172">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


