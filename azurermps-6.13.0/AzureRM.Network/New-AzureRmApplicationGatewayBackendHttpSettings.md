---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 3b292b70e96c8da57a87834ecc4c095c9ca3f55c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588471"
---
# <span data-ttu-id="317c2-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="317c2-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="317c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="317c2-102">SYNOPSIS</span></span>
<span data-ttu-id="317c2-103">Uygulama ağ geçidi için arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c2-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="317c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="317c2-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="317c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="317c2-105">DESCRIPTION</span></span>
<span data-ttu-id="317c2-106">New-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i uygulama ağ geçidi için arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c2-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="317c2-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="317c2-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="317c2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="317c2-108">EXAMPLES</span></span>

### <span data-ttu-id="317c2-109">Örnek 1: arka uç HTTP ayarları oluşturma</span><span class="sxs-lookup"><span data-stu-id="317c2-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="317c2-110">Bu komut, Setting01 adlı bağlantı noktası 80, tanımlama bilgisi tabanlı benzeşim devre dışı olan HTTP protokolünü kullanarak arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="317c2-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="317c2-111">Ayarlar $Setting değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="317c2-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="317c2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="317c2-112">PARAMETERS</span></span>

### <span data-ttu-id="317c2-113">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="317c2-113">-AffinityCookieName</span></span>
<span data-ttu-id="317c2-114">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="317c2-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="317c2-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="317c2-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="317c2-116">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="317c2-117">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="317c2-117">-ConnectionDraining</span></span>
<span data-ttu-id="317c2-118">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="317c2-118">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317c2-119">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="317c2-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="317c2-120">Arka uç sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="317c2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317c2-121">-DefaultProfile</span></span>
<span data-ttu-id="317c2-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="317c2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="317c2-123">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="317c2-123">-HostName</span></span>
<span data-ttu-id="317c2-124">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="317c2-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="317c2-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="317c2-125">-Name</span></span>
<span data-ttu-id="317c2-126">Bu cmdlet 'in oluşturduğu arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="317c2-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="317c2-127">-Path</span></span>
<span data-ttu-id="317c2-128">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="317c2-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="317c2-129">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="317c2-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="317c2-130">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="317c2-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="317c2-131">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="317c2-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="317c2-132">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="317c2-132">-Port</span></span>
<span data-ttu-id="317c2-133">Arka uç sunucu havuzunun bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-133">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317c2-134">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="317c2-134">-Probe</span></span>
<span data-ttu-id="317c2-135">Arka uç sunucu havuzuyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-135">Specifies a probe to associate with the back-end server pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317c2-136">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="317c2-136">-ProbeId</span></span>
<span data-ttu-id="317c2-137">Arka uç sunucu havuzuyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="317c2-138">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="317c2-138">-Protocol</span></span>
<span data-ttu-id="317c2-139">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="317c2-140">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="317c2-140">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317c2-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="317c2-141">-RequestTimeout</span></span>
<span data-ttu-id="317c2-142">İstek zaman aşımı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="317c2-142">Specifies a request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317c2-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="317c2-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="317c2-144">Uygulama ağ geçidi güvenilen kök sertifikaları</span><span class="sxs-lookup"><span data-stu-id="317c2-144">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317c2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317c2-145">CommonParameters</span></span>
<span data-ttu-id="317c2-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="317c2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317c2-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317c2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317c2-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="317c2-148">INPUTS</span></span>

### <span data-ttu-id="317c2-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="317c2-149">None</span></span>

## <span data-ttu-id="317c2-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="317c2-150">OUTPUTS</span></span>

### <span data-ttu-id="317c2-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="317c2-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="317c2-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="317c2-152">NOTES</span></span>

## <span data-ttu-id="317c2-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="317c2-153">RELATED LINKS</span></span>

[<span data-ttu-id="317c2-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="317c2-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="317c2-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="317c2-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="317c2-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="317c2-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="317c2-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="317c2-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

