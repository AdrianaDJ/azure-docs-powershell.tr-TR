---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 6183b3cd61380b139bd74d676c6ab5225bf338fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592177"
---
# <span data-ttu-id="0eb24-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0eb24-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0eb24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0eb24-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb24-103">Uygulama ağ geçidi için arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0eb24-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eb24-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0eb24-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eb24-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0eb24-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb24-106">New-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i uygulama ağ geçidi için arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0eb24-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="0eb24-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="0eb24-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="0eb24-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0eb24-108">EXAMPLES</span></span>

### <span data-ttu-id="0eb24-109">Örnek 1: arka uç HTTP ayarları oluşturma</span><span class="sxs-lookup"><span data-stu-id="0eb24-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="0eb24-110">Bu komut, Setting01 adlı bağlantı noktası 80, tanımlama bilgisi tabanlı benzeşim devre dışı olan HTTP protokolünü kullanarak arka uç HTTP ayarları oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0eb24-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="0eb24-111">Ayarlar $Setting değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="0eb24-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="0eb24-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0eb24-112">PARAMETERS</span></span>

### <span data-ttu-id="0eb24-113">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="0eb24-113">-AffinityCookieName</span></span>
<span data-ttu-id="0eb24-114">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="0eb24-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="0eb24-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="0eb24-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="0eb24-116">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="0eb24-117">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="0eb24-117">-ConnectionDraining</span></span>
<span data-ttu-id="0eb24-118">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="0eb24-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="0eb24-119">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="0eb24-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="0eb24-120">Arka uç sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="0eb24-121">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="0eb24-121">-HostName</span></span>
<span data-ttu-id="0eb24-122">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="0eb24-122">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="0eb24-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="0eb24-123">-Name</span></span>
<span data-ttu-id="0eb24-124">Bu cmdlet 'in oluşturduğu arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-124">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0eb24-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="0eb24-125">-Path</span></span>
<span data-ttu-id="0eb24-126">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="0eb24-126">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="0eb24-127">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="0eb24-127">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="0eb24-128">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="0eb24-128">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="0eb24-129">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="0eb24-129">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="0eb24-130">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="0eb24-130">-Port</span></span>
<span data-ttu-id="0eb24-131">Arka uç sunucu havuzunun bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-131">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="0eb24-132">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="0eb24-132">-Probe</span></span>
<span data-ttu-id="0eb24-133">Arka uç sunucu havuzuyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-133">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="0eb24-134">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="0eb24-134">-ProbeEnabled</span></span>
<span data-ttu-id="0eb24-135">Yoklama etkin olması gerekiyorsa bayrak.</span><span class="sxs-lookup"><span data-stu-id="0eb24-135">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="0eb24-136">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="0eb24-136">-ProbeId</span></span>
<span data-ttu-id="0eb24-137">Arka uç sunucu havuzuyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="0eb24-138">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0eb24-138">-Protocol</span></span>
<span data-ttu-id="0eb24-139">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="0eb24-140">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="0eb24-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="0eb24-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="0eb24-141">-RequestTimeout</span></span>
<span data-ttu-id="0eb24-142">İstek zaman aşımı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="0eb24-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="0eb24-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb24-143">-DefaultProfile</span></span>
<span data-ttu-id="0eb24-144">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0eb24-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb24-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb24-145">CommonParameters</span></span>
<span data-ttu-id="0eb24-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0eb24-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb24-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb24-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb24-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0eb24-148">INPUTS</span></span>

### <span data-ttu-id="0eb24-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb24-149">System.String</span></span>

## <span data-ttu-id="0eb24-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0eb24-150">OUTPUTS</span></span>

### <span data-ttu-id="0eb24-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0eb24-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="0eb24-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0eb24-152">NOTES</span></span>

## <span data-ttu-id="0eb24-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0eb24-153">RELATED LINKS</span></span>

[<span data-ttu-id="0eb24-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0eb24-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0eb24-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0eb24-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0eb24-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0eb24-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="0eb24-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0eb24-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

