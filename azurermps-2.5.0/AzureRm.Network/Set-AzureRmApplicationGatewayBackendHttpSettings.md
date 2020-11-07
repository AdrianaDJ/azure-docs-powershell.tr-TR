---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: c20faf9ca89892d952d553d0f85cfa28b90ac590
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939272"
---
# <span data-ttu-id="00924-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00924-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="00924-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00924-102">SYNOPSIS</span></span>
<span data-ttu-id="00924-103">Uygulama ağ geçidi için geri açılan HTTP ayarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="00924-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00924-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00924-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00924-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00924-105">DESCRIPTION</span></span>
<span data-ttu-id="00924-106">Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i bir Azure uygulama ağ geçidi için arka uç Köprü Metni Aktarım Protokolü (HTTP) ayarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="00924-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="00924-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="00924-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="00924-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00924-108">EXAMPLES</span></span>

### <span data-ttu-id="00924-109">Örnek 1: uygulama ağ geçidi için arka uç HTTP ayarlarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="00924-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="00924-110">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="00924-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="00924-111">İkinci komut $AppGw değişkeninde uygulama ağ geçidinin HTTP ayarlarını, bağlantı noktası 88, HTTP protokolünü ve tanımlama bilgisi tabanlı Benzeşmeyi kullanacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="00924-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="00924-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00924-112">PARAMETERS</span></span>

### <span data-ttu-id="00924-113">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="00924-113">-AffinityCookieName</span></span>
<span data-ttu-id="00924-114">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="00924-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="00924-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00924-115">-ApplicationGateway</span></span>
<span data-ttu-id="00924-116">Bu cmdlet 'in geri dönüş HTTP ayarlarını ilişkilendiren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00924-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="00924-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="00924-118">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-118">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-119">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="00924-119">-ConnectionDraining</span></span>
<span data-ttu-id="00924-120">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="00924-120">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-121">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="00924-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="00924-122">Temel sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="00924-123">Bu parametre için kabul edilebilir değerler: devre dışı veya etkin.</span><span class="sxs-lookup"><span data-stu-id="00924-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="00924-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00924-124">-DefaultProfile</span></span>
<span data-ttu-id="00924-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00924-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00924-126">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="00924-126">-HostName</span></span>
<span data-ttu-id="00924-127">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="00924-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="00924-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="00924-128">-Name</span></span>
<span data-ttu-id="00924-129">Arka uç HTTP ayarları nesnesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="00924-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="00924-130">-Path</span></span>
<span data-ttu-id="00924-131">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="00924-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="00924-132">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="00924-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="00924-133">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="00924-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="00924-134">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="00924-134">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-135">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="00924-135">-Port</span></span>
<span data-ttu-id="00924-136">Arka uç sunucu havuzundaki her sunucu için kullanılacak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-136">Specifies the port to use for each server in the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-137">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="00924-137">-Probe</span></span>
<span data-ttu-id="00924-138">Arka uç HTTP ayarlarıyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="00924-139">-ProbeEnabled</span></span>
<span data-ttu-id="00924-140">Yoklama etkin olması gerekiyorsa bayrak.</span><span class="sxs-lookup"><span data-stu-id="00924-140">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-141">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="00924-141">-ProbeId</span></span>
<span data-ttu-id="00924-142">Arka uç HTTP ayarlarıyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="00924-143">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="00924-143">-Protocol</span></span>
<span data-ttu-id="00924-144">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="00924-145">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="00924-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="00924-146">Bu parametre büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="00924-146">This parameter is case-sensitive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="00924-147">-RequestTimeout</span></span>
<span data-ttu-id="00924-148">İstek zaman aşımı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="00924-148">Specifies a request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00924-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00924-149">CommonParameters</span></span>
<span data-ttu-id="00924-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00924-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00924-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00924-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00924-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00924-152">INPUTS</span></span>

### <span data-ttu-id="00924-153">System. String</span><span class="sxs-lookup"><span data-stu-id="00924-153">System.String</span></span>

## <span data-ttu-id="00924-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00924-154">OUTPUTS</span></span>

### <span data-ttu-id="00924-155">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="00924-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="00924-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00924-156">NOTES</span></span>

## <span data-ttu-id="00924-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00924-157">RELATED LINKS</span></span>

[<span data-ttu-id="00924-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00924-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="00924-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00924-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="00924-160">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00924-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="00924-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="00924-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

