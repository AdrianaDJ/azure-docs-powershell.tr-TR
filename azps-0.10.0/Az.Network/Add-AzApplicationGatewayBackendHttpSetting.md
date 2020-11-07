---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 4361d025026e3ff9c9a72a092a99a72b8b63c850
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935665"
---
# <span data-ttu-id="8ddcf-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8ddcf-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="8ddcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ddcf-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddcf-103">Uygulama ağ geçidine arka uç HTTP ayarları ekler.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="8ddcf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ddcf-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ddcf-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ddcf-105">DESCRIPTION</span></span>
<span data-ttu-id="8ddcf-106">Add-AzApplicationGatewayBackendHttpSetting cmdlet 'i uygulama ağ geçidine arka uç HTTP ayarları ekler.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="8ddcf-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="8ddcf-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ddcf-108">EXAMPLES</span></span>

### <span data-ttu-id="8ddcf-109">Örnek 1: uygulama ağ geçidine arka uç HTTP ayarları ekleme</span><span class="sxs-lookup"><span data-stu-id="8ddcf-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="8ddcf-110">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine arka uç HTTP ayarları ekler, bağlantı noktasını 88 olarak ve protokol HTTP olarak ayarlanarak ayarlar Setting02.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="8ddcf-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ddcf-111">PARAMETERS</span></span>

### <span data-ttu-id="8ddcf-112">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="8ddcf-112">-AffinityCookieName</span></span>
<span data-ttu-id="8ddcf-113">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="8ddcf-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="8ddcf-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ddcf-114">-ApplicationGateway</span></span>
<span data-ttu-id="8ddcf-115">Bu cmdlet 'in ayarları eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="8ddcf-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="8ddcf-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="8ddcf-117">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="8ddcf-118">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="8ddcf-118">-ConnectionDraining</span></span>
<span data-ttu-id="8ddcf-119">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-119">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="8ddcf-120">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="8ddcf-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="8ddcf-121">Temel sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="8ddcf-122">Bu parametre için kabul edilebilir değerler: devre dışı, etkin.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

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

### <span data-ttu-id="8ddcf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddcf-123">-DefaultProfile</span></span>
<span data-ttu-id="8ddcf-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ddcf-125">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="8ddcf-125">-HostName</span></span>
<span data-ttu-id="8ddcf-126">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="8ddcf-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ddcf-127">-Name</span></span>
<span data-ttu-id="8ddcf-128">Bu cmdlet 'in eklediği arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="8ddcf-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="8ddcf-129">-Path</span></span>
<span data-ttu-id="8ddcf-130">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="8ddcf-131">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="8ddcf-132">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="8ddcf-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="8ddcf-133">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-133">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="8ddcf-134">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8ddcf-134">-Port</span></span>
<span data-ttu-id="8ddcf-135">Arka uç sunucu havuzunun bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-135">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="8ddcf-136">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="8ddcf-136">-Probe</span></span>
<span data-ttu-id="8ddcf-137">Arka uç sunucusuyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-137">Specifies a probe to associate with a back-end server.</span></span>

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

### <span data-ttu-id="8ddcf-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="8ddcf-138">-ProbeEnabled</span></span>
<span data-ttu-id="8ddcf-139">Yoklama etkin olması gerekiyorsa bayrak.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-139">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="8ddcf-140">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="8ddcf-140">-ProbeId</span></span>
<span data-ttu-id="8ddcf-141">Arka uç sunucusuyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="8ddcf-142">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="8ddcf-142">-Protocol</span></span>
<span data-ttu-id="8ddcf-143">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde iletişim kuralını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="8ddcf-144">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-144">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="8ddcf-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="8ddcf-145">-RequestTimeout</span></span>
<span data-ttu-id="8ddcf-146">İstek zaman aşımı değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-146">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="8ddcf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddcf-147">CommonParameters</span></span>
<span data-ttu-id="8ddcf-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ddcf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddcf-149">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ddcf-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddcf-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ddcf-150">INPUTS</span></span>

### <span data-ttu-id="8ddcf-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8ddcf-151">System.String</span></span>

## <span data-ttu-id="8ddcf-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ddcf-152">OUTPUTS</span></span>

### <span data-ttu-id="8ddcf-153">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8ddcf-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="8ddcf-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ddcf-154">NOTES</span></span>

## <span data-ttu-id="8ddcf-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ddcf-155">RELATED LINKS</span></span>

[<span data-ttu-id="8ddcf-156">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8ddcf-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="8ddcf-157">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8ddcf-157">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="8ddcf-158">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8ddcf-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="8ddcf-159">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8ddcf-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

