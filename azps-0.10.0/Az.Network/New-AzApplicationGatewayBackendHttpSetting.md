---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 8815813e12c249eebbdc825b75b05d9796a5d01c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935443"
---
# <span data-ttu-id="0ca0e-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0ca0e-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="0ca0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ca0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca0e-103">Uygulama ağ geçidi için arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-103">Creates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="0ca0e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0ca0e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ca0e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0ca0e-105">DESCRIPTION</span></span>
<span data-ttu-id="0ca0e-106">New-AzApplicationGatewayBackendHttpSetting cmdlet 'i uygulama ağ geçidi için arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="0ca0e-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="0ca0e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0ca0e-108">EXAMPLES</span></span>

### <span data-ttu-id="0ca0e-109">Örnek 1: arka uç HTTP ayarları oluşturma</span><span class="sxs-lookup"><span data-stu-id="0ca0e-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="0ca0e-110">Bu komut, Setting01 adlı bağlantı noktası 80, tanımlama bilgisi tabanlı benzeşim devre dışı olan HTTP protokolünü kullanarak arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="0ca0e-111">Ayarlar $Setting değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="0ca0e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0ca0e-112">PARAMETERS</span></span>

### <span data-ttu-id="0ca0e-113">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="0ca0e-113">-AffinityCookieName</span></span>
<span data-ttu-id="0ca0e-114">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="0ca0e-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="0ca0e-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="0ca0e-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="0ca0e-116">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="0ca0e-117">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="0ca0e-117">-ConnectionDraining</span></span>
<span data-ttu-id="0ca0e-118">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="0ca0e-119">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="0ca0e-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="0ca0e-120">Arka uç sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="0ca0e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca0e-121">-DefaultProfile</span></span>
<span data-ttu-id="0ca0e-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ca0e-123">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="0ca0e-123">-HostName</span></span>
<span data-ttu-id="0ca0e-124">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="0ca0e-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0ca0e-125">-Name</span></span>
<span data-ttu-id="0ca0e-126">Bu cmdlet 'in oluşturduğu arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0ca0e-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="0ca0e-127">-Path</span></span>
<span data-ttu-id="0ca0e-128">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="0ca0e-129">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="0ca0e-130">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="0ca0e-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="0ca0e-131">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="0ca0e-132">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="0ca0e-132">-Port</span></span>
<span data-ttu-id="0ca0e-133">Arka uç sunucu havuzunun bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="0ca0e-134">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="0ca0e-134">-Probe</span></span>
<span data-ttu-id="0ca0e-135">Arka uç sunucu havuzuyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="0ca0e-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="0ca0e-136">-ProbeEnabled</span></span>
<span data-ttu-id="0ca0e-137">Yoklama etkin olması gerekiyorsa bayrak.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-137">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="0ca0e-138">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="0ca0e-138">-ProbeId</span></span>
<span data-ttu-id="0ca0e-139">Arka uç sunucu havuzuyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-139">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="0ca0e-140">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0ca0e-140">-Protocol</span></span>
<span data-ttu-id="0ca0e-141">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-141">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="0ca0e-142">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="0ca0e-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="0ca0e-143">-RequestTimeout</span></span>
<span data-ttu-id="0ca0e-144">İstek zaman aşımı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-144">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="0ca0e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca0e-145">CommonParameters</span></span>
<span data-ttu-id="0ca0e-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0ca0e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca0e-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ca0e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca0e-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0ca0e-148">INPUTS</span></span>

### <span data-ttu-id="0ca0e-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0ca0e-149">System.String</span></span>

## <span data-ttu-id="0ca0e-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0ca0e-150">OUTPUTS</span></span>

### <span data-ttu-id="0ca0e-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0ca0e-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0ca0e-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0ca0e-152">NOTES</span></span>

## <span data-ttu-id="0ca0e-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0ca0e-153">RELATED LINKS</span></span>

[<span data-ttu-id="0ca0e-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0ca0e-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="0ca0e-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0ca0e-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="0ca0e-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0ca0e-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="0ca0e-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0ca0e-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

