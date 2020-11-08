---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279629"
---
# <span data-ttu-id="7eb03-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7eb03-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="7eb03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eb03-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb03-103">Uygulama ağ geçidi için geri açılan HTTP ayarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="7eb03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7eb03-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eb03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7eb03-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb03-106">Set-AzApplicationGatewayBackendHttpSetting cmdlet 'i bir Azure uygulama ağ geçidi için arka uç Köprü Metni Aktarım Protokolü (HTTP) ayarlarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="7eb03-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7eb03-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="7eb03-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7eb03-108">EXAMPLES</span></span>

### <span data-ttu-id="7eb03-109">Örnek 1: uygulama ağ geçidi için arka uç HTTP ayarlarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="7eb03-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="7eb03-110">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7eb03-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7eb03-111">İkinci komut $AppGw değişkeninde uygulama ağ geçidinin HTTP ayarlarını, bağlantı noktası 88, HTTP protokolünü ve tanımlama bilgisi tabanlı Benzeşmeyi kullanacak şekilde güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="7eb03-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7eb03-112">PARAMETERS</span></span>

### <span data-ttu-id="7eb03-113">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="7eb03-113">-AffinityCookieName</span></span>
<span data-ttu-id="7eb03-114">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="7eb03-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="7eb03-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eb03-115">-ApplicationGateway</span></span>
<span data-ttu-id="7eb03-116">Bu cmdlet 'in geri dönüş HTTP ayarlarını ilişkilendiren bir uygulama ağ geçidi nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eb03-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="7eb03-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="7eb03-118">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-118">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb03-119">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="7eb03-119">-ConnectionDraining</span></span>
<span data-ttu-id="7eb03-120">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="7eb03-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="7eb03-121">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="7eb03-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="7eb03-122">Temel sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="7eb03-123">Bu parametre için kabul edilebilir değerler: devre dışı veya etkin.</span><span class="sxs-lookup"><span data-stu-id="7eb03-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="7eb03-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb03-124">-DefaultProfile</span></span>
<span data-ttu-id="7eb03-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7eb03-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eb03-126">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="7eb03-126">-HostName</span></span>
<span data-ttu-id="7eb03-127">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7eb03-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="7eb03-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="7eb03-128">-Name</span></span>
<span data-ttu-id="7eb03-129">Arka uç HTTP ayarları nesnesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="7eb03-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="7eb03-130">-Path</span></span>
<span data-ttu-id="7eb03-131">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="7eb03-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="7eb03-132">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="7eb03-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="7eb03-133">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="7eb03-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="7eb03-134">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="7eb03-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="7eb03-135">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="7eb03-135">-Port</span></span>
<span data-ttu-id="7eb03-136">Arka uç sunucu havuzundaki her sunucu için kullanılacak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="7eb03-137">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="7eb03-137">-Probe</span></span>
<span data-ttu-id="7eb03-138">Arka uç HTTP ayarlarıyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="7eb03-139">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="7eb03-139">-ProbeId</span></span>
<span data-ttu-id="7eb03-140">Arka uç HTTP ayarlarıyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="7eb03-141">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="7eb03-141">-Protocol</span></span>
<span data-ttu-id="7eb03-142">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="7eb03-143">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="7eb03-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="7eb03-144">Bu parametre büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="7eb03-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="7eb03-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="7eb03-145">-RequestTimeout</span></span>
<span data-ttu-id="7eb03-146">İstek zaman aşımı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="7eb03-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="7eb03-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7eb03-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="7eb03-148">Uygulama ağ geçidi güvenilen kök sertifikaları</span><span class="sxs-lookup"><span data-stu-id="7eb03-148">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eb03-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb03-149">CommonParameters</span></span>
<span data-ttu-id="7eb03-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7eb03-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb03-151">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eb03-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb03-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7eb03-152">INPUTS</span></span>

### <span data-ttu-id="7eb03-153">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eb03-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7eb03-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7eb03-154">OUTPUTS</span></span>

### <span data-ttu-id="7eb03-155">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7eb03-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7eb03-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7eb03-156">NOTES</span></span>

## <span data-ttu-id="7eb03-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7eb03-157">RELATED LINKS</span></span>

[<span data-ttu-id="7eb03-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7eb03-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7eb03-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7eb03-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7eb03-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7eb03-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="7eb03-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="7eb03-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

