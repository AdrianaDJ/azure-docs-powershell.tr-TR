---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 07820860f1a6a43f51f8436fa3ba28d6238de087
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593225"
---
# <span data-ttu-id="569fa-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="569fa-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="569fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="569fa-102">SYNOPSIS</span></span>
<span data-ttu-id="569fa-103">Uygulama ağ geçidine arka uç HTTP ayarları ekler.</span><span class="sxs-lookup"><span data-stu-id="569fa-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="569fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="569fa-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-TrustedRootCertificate <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="569fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="569fa-105">DESCRIPTION</span></span>
<span data-ttu-id="569fa-106">Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i uygulama ağ geçidine arka uç HTTP ayarları ekler.</span><span class="sxs-lookup"><span data-stu-id="569fa-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="569fa-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="569fa-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="569fa-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="569fa-108">EXAMPLES</span></span>

### <span data-ttu-id="569fa-109">Örnek 1: uygulama ağ geçidine arka uç HTTP ayarları ekleme</span><span class="sxs-lookup"><span data-stu-id="569fa-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="569fa-110">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine arka uç HTTP ayarları ekler, bağlantı noktasını 88 olarak ve protokol HTTP olarak ayarlanarak ayarlar Setting02.</span><span class="sxs-lookup"><span data-stu-id="569fa-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="569fa-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="569fa-111">PARAMETERS</span></span>

### <span data-ttu-id="569fa-112">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="569fa-112">-AffinityCookieName</span></span>
<span data-ttu-id="569fa-113">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="569fa-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="569fa-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="569fa-114">-ApplicationGateway</span></span>
<span data-ttu-id="569fa-115">Bu cmdlet 'in ayarları eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="569fa-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="569fa-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="569fa-117">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="569fa-118">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="569fa-118">-ConnectionDraining</span></span>
<span data-ttu-id="569fa-119">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="569fa-119">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="569fa-120">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="569fa-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="569fa-121">Temel sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="569fa-122">Bu parametre için kabul edilebilir değerler: devre dışı, etkin.</span><span class="sxs-lookup"><span data-stu-id="569fa-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

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

### <span data-ttu-id="569fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="569fa-123">-DefaultProfile</span></span>
<span data-ttu-id="569fa-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="569fa-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="569fa-125">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="569fa-125">-HostName</span></span>
<span data-ttu-id="569fa-126">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="569fa-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="569fa-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="569fa-127">-Name</span></span>
<span data-ttu-id="569fa-128">Bu cmdlet 'in eklediği arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="569fa-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="569fa-129">-Path</span></span>
<span data-ttu-id="569fa-130">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="569fa-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="569fa-131">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="569fa-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="569fa-132">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="569fa-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="569fa-133">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="569fa-133">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="569fa-134">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="569fa-134">-Port</span></span>
<span data-ttu-id="569fa-135">Arka uç sunucu havuzunun bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-135">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="569fa-136">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="569fa-136">-Probe</span></span>
<span data-ttu-id="569fa-137">Arka uç sunucusuyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-137">Specifies a probe to associate with a back-end server.</span></span>

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

### <span data-ttu-id="569fa-138">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="569fa-138">-ProbeId</span></span>
<span data-ttu-id="569fa-139">Arka uç sunucusuyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="569fa-140">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="569fa-140">-Protocol</span></span>
<span data-ttu-id="569fa-141">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde iletişim kuralını belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="569fa-142">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="569fa-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="569fa-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="569fa-143">-RequestTimeout</span></span>
<span data-ttu-id="569fa-144">İstek zaman aşımı değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="569fa-144">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="569fa-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="569fa-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="569fa-146">Uygulama ağ geçidi güvenilen kök sertifikaları</span><span class="sxs-lookup"><span data-stu-id="569fa-146">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="569fa-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="569fa-147">CommonParameters</span></span>
<span data-ttu-id="569fa-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="569fa-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="569fa-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="569fa-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="569fa-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="569fa-150">INPUTS</span></span>

### <span data-ttu-id="569fa-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="569fa-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="569fa-152">Parametreler: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="569fa-152">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="569fa-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="569fa-153">OUTPUTS</span></span>

### <span data-ttu-id="569fa-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="569fa-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="569fa-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="569fa-155">NOTES</span></span>

## <span data-ttu-id="569fa-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="569fa-156">RELATED LINKS</span></span>

[<span data-ttu-id="569fa-157">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="569fa-157">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="569fa-158">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="569fa-158">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="569fa-159">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="569fa-159">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="569fa-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="569fa-160">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

