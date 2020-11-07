---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935427"
---
# <span data-ttu-id="977d9-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="977d9-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="977d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="977d9-102">SYNOPSIS</span></span>
<span data-ttu-id="977d9-103">Uygulama ağ geçidi yol kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="977d9-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="977d9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="977d9-104">SYNTAX</span></span>

### <span data-ttu-id="977d9-105">Setbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="977d9-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="977d9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="977d9-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="977d9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="977d9-107">DESCRIPTION</span></span>
<span data-ttu-id="977d9-108">**Yeni-AzApplicationGatewayPathRuleConfig** cmdlet 'i bir uygulama ağ geçidi yolu kuralı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="977d9-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="977d9-109">Bu cmdlet tarafından oluşturulan kurallar URL yol haritası yapılandırma ayarları koleksiyonuna eklenebilir ve ardından bir ağ geçidine atanabilir.</span><span class="sxs-lookup"><span data-stu-id="977d9-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="977d9-110">Yol haritası yapılandırma ayarları uygulama ağ geçidi yük dengelemesi 'nde kullanılır.</span><span class="sxs-lookup"><span data-stu-id="977d9-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="977d9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="977d9-111">EXAMPLES</span></span>

### <span data-ttu-id="977d9-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="977d9-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="977d9-113">Bu komutlar yeni bir uygulama ağ geçidi yol kuralı oluşturur ve ardından bu kuralı uygulama ağ geçidine atamak için **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="977d9-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="977d9-114">Bunu yapmak için ilk komut ağ geçidi ContosoApplicationGateway 'e bir nesne başvurusu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="977d9-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="977d9-115">Bu nesne başvurusu $Gateway adlı bir değişkende depolanır.</span><span class="sxs-lookup"><span data-stu-id="977d9-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="977d9-116">Sonraki iki komut arka uç adres havuzu ve arka uç HTTP Ayarları nesnesi oluşturur; yol kuralı nesnesi oluşturmak için bu nesneler ($AddressPool ve $HttpSettings 'te depolanan) gereklidir.</span><span class="sxs-lookup"><span data-stu-id="977d9-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="977d9-117">Dördüncü komut, yol kuralı nesnesini oluşturur ve $PathRuleConfig adlı bir değişkende saklanır.</span><span class="sxs-lookup"><span data-stu-id="977d9-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="977d9-118">Beşinci komut, yapılandırma ayarlarını ve bu ayarlarda bulunan yeni yol kuralını ContosoApplicationGateway 'e eklemek için **Add-AzApplicationGatewayUrlPathMapConfig** öğesini kullanır.</span><span class="sxs-lookup"><span data-stu-id="977d9-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="977d9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="977d9-119">PARAMETERS</span></span>

### <span data-ttu-id="977d9-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="977d9-120">-BackendAddressPool</span></span>
<span data-ttu-id="977d9-121">Ağ Geçidi yol kuralları yapılandırma ayarlarına eklenecek bir arka uç adres havuzu ayarları koleksiyonuna bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="977d9-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="977d9-122">Bu nesne başvurusunu, New-AzApplicationGatewayBackendAddressPool cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="977d9-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="977d9-123">Yukarıdaki komut, adres havuzuna iki IP adresi (192.16.1.1 ve 192.168.1.2) ekler.</span><span class="sxs-lookup"><span data-stu-id="977d9-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="977d9-124">IP adresinin tırnak işaretleri içine alındığına ve virgül kullanılarak ayrıldığına dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="977d9-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="977d9-125">Sonuç değişkeni $AddressPool, *Defaultbackendaddresspool* parametresinin parametre değeri olarak kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="977d9-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="977d9-126">Arka uç adres havuzu, arka uç sunucularındaki IP adreslerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="977d9-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="977d9-127">Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="977d9-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="977d9-128">Bu parametreyi kullanırsanız, *Defaultbackendaddresspoıd* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="977d9-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977d9-129">-Backendaddresspoıd</span><span class="sxs-lookup"><span data-stu-id="977d9-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="977d9-130">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç adres havuzunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="977d9-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="977d9-131">Adres havuzu kimlikleri Get-AzApplicationGatewayBackendAddressPool cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="977d9-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="977d9-132">KIMLIĞI aldıktan sonra *defaultbackendaddresspool* parametresi yerine *Defaultbackendaddresspoıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="977d9-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="977d9-133">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="977d9-133">For instance:</span></span>

<span data-ttu-id="977d9-134">-Defaultbackendaddresspoıd "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="977d9-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="977d9-135">Arka uç adres havuzu, arka uç sunucularındaki IP adreslerini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="977d9-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="977d9-136">Bu IP adresleri sanal ağ alt ağına dahil olmalıdır veya ortak IP adresleri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="977d9-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977d9-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="977d9-137">-BackendHttpSettings</span></span>
<span data-ttu-id="977d9-138">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenecek bir arka uç HTTP ayarları koleksiyonuna bir nesne başvurusu belirtir.</span><span class="sxs-lookup"><span data-stu-id="977d9-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="977d9-139">Bu nesne başvurusunu, New-AzApplicationGatewayBackendHttpSetting cmdlet 'i ve buna benzer sözdizimini kullanarak oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="977d9-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="977d9-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-Name "Contosohttpsetler"-port 80-Protocol "http"-Bina ıebasedaffinity "Disabled"</span><span class="sxs-lookup"><span data-stu-id="977d9-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="977d9-141">Sonuç değişkeni $HttpSettings, *Defaultbackendaddresspool* parametresinin parametre değeri olarak kullanılabilir:</span><span class="sxs-lookup"><span data-stu-id="977d9-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="977d9-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="977d9-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="977d9-143">Arka uç HTTP ayarları, bir arka uç havuzunun bağlantı noktası, protokolü ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="977d9-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="977d9-144">Bu parametreyi kullanırsanız, *Defaultbackendhttpsettingsid* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="977d9-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977d9-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="977d9-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="977d9-146">Ağ Geçidi yol kuralı yapılandırma ayarlarına eklenebilen varolan bir arka uç HTTP ayarları koleksiyonunun KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="977d9-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="977d9-147">HTTP ayar kimlikleri, Get-AzApplicationGatewayBackendHttpSetting cmdlet kullanılarak döndürülebilir.</span><span class="sxs-lookup"><span data-stu-id="977d9-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="977d9-148">KIMLIĞI aldıktan sonra, *Defaultbackendhttpsettings* parametresi yerine *Defaultbackendhttpsettingsıd* parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="977d9-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="977d9-149">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="977d9-149">For instance:</span></span>

<span data-ttu-id="977d9-150">-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="977d9-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="977d9-151">Arka uç HTTP ayarları, bir arka uç havuzunun bağlantı noktası, protokolü ve tanımlama bilgisi tabanlı benzeşim gibi özellikleri yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="977d9-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="977d9-152">Bu parametreyi kullanırsanız, *Defaultbackendhttpsettings* parametresini aynı komutta kullanamazsınız.</span><span class="sxs-lookup"><span data-stu-id="977d9-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977d9-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977d9-153">-DefaultProfile</span></span>
<span data-ttu-id="977d9-154">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="977d9-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="977d9-155">-Ad</span><span class="sxs-lookup"><span data-stu-id="977d9-155">-Name</span></span>
<span data-ttu-id="977d9-156">Bu cmdlet 'in oluşturduğu yol kuralı yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="977d9-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="977d9-157">-Yollar</span><span class="sxs-lookup"><span data-stu-id="977d9-157">-Paths</span></span>
<span data-ttu-id="977d9-158">Bir veya daha fazla uygulama ağ geçidi yol kuralını belirtir.</span><span class="sxs-lookup"><span data-stu-id="977d9-158">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="977d9-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="977d9-159">-RedirectConfiguration</span></span>
<span data-ttu-id="977d9-160">Uygulama ağ geçidi Redirectyapılandırması</span><span class="sxs-lookup"><span data-stu-id="977d9-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977d9-161">-Redirectconfigurationıd</span><span class="sxs-lookup"><span data-stu-id="977d9-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="977d9-162">Uygulama ağ geçidi Redirectyapılandırmasının KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="977d9-162">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977d9-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977d9-163">CommonParameters</span></span>
<span data-ttu-id="977d9-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="977d9-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977d9-165">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="977d9-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977d9-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="977d9-166">INPUTS</span></span>

###  
<span data-ttu-id="977d9-167">**New-AzApplicationGatewayPathRuleConfig** , ardışık düzen girişini kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="977d9-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="977d9-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="977d9-168">OUTPUTS</span></span>

###  
<span data-ttu-id="977d9-169">**New-AzApplicationGatewayPathRuleConfig** , **Microsoft. Azure. Commands. Network. model. PSApplicationGatewayPathRule** nesnesinin yeni örneklerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="977d9-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="977d9-170">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="977d9-170">NOTES</span></span>

## <span data-ttu-id="977d9-171">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="977d9-171">RELATED LINKS</span></span>

[<span data-ttu-id="977d9-172">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="977d9-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="977d9-173">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="977d9-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="977d9-174">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="977d9-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="977d9-175">Yeni-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="977d9-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="977d9-176">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="977d9-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="977d9-177">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="977d9-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="977d9-178">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="977d9-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="977d9-179">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="977d9-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="977d9-180">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="977d9-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


