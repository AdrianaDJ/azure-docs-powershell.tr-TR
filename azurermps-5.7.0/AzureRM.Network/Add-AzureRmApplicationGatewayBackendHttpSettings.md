---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: e88614de1f61cb976937759b6962e682ee6bb0ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592109"
---
# <span data-ttu-id="a5b34-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5b34-101">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="a5b34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b34-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b34-103">Uygulama ağ geçidine arka uç HTTP ayarları ekler.</span><span class="sxs-lookup"><span data-stu-id="a5b34-103">Adds back-end HTTP settings to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5b34-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5b34-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5b34-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5b34-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b34-106">Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet 'i uygulama ağ geçidine arka uç HTTP ayarları ekler.</span><span class="sxs-lookup"><span data-stu-id="a5b34-106">The Add-AzureRmApplicationGatewayBackendHttpSettings cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="a5b34-107">Arka uç HTTP ayarları havuzdaki tüm arka uç sunucularına uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a5b34-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="a5b34-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5b34-108">EXAMPLES</span></span>

### <span data-ttu-id="a5b34-109">Örnek 1: uygulama ağ geçidine arka uç HTTP ayarları ekleme</span><span class="sxs-lookup"><span data-stu-id="a5b34-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="a5b34-110">İlk komut, ApplicationGateway01 adındaki kaynak grubuna ait olan ResourceGroup01 adındaki uygulama ağ geçidini alır ve $AppGw değişkeninde depolar. İkinci komut, uygulama ağ geçidine arka uç HTTP ayarları ekler, bağlantı noktasını 88 olarak ve protokol HTTP olarak ayarlanarak ayarlar Setting02.</span><span class="sxs-lookup"><span data-stu-id="a5b34-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="a5b34-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5b34-111">PARAMETERS</span></span>

### <span data-ttu-id="a5b34-112">-Affinitybir ENAME adı</span><span class="sxs-lookup"><span data-stu-id="a5b34-112">-AffinityCookieName</span></span>
<span data-ttu-id="a5b34-113">Benzeşim tanımlama bilgisi için kullanılacak tanımlama bilgisi adı</span><span class="sxs-lookup"><span data-stu-id="a5b34-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="a5b34-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5b34-114">-ApplicationGateway</span></span>
<span data-ttu-id="a5b34-115">Bu cmdlet 'in ayarları eklediği uygulama ağ geçidi adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="a5b34-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="a5b34-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="a5b34-117">Uygulama ağ geçidi için kimlik doğrulama sertifikalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-117">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="a5b34-118">-Connectionboşaltma</span><span class="sxs-lookup"><span data-stu-id="a5b34-118">-ConnectionDraining</span></span>
<span data-ttu-id="a5b34-119">Arka uç http ayarları kaynağının bağlantı boşaltma.</span><span class="sxs-lookup"><span data-stu-id="a5b34-119">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="a5b34-120">-Pişirme</span><span class="sxs-lookup"><span data-stu-id="a5b34-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="a5b34-121">Temel sunucu havuzu için tanımlama bilgisi tabanlı benzeşim 'in etkinleştirilip etkinleştirilmeyeceğini veya devre dışı bırakılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="a5b34-122">Bu parametre için kabul edilebilir değerler: devre dışı, etkin.</span><span class="sxs-lookup"><span data-stu-id="a5b34-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

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

### <span data-ttu-id="a5b34-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b34-123">-DefaultProfile</span></span>
<span data-ttu-id="a5b34-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a5b34-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5b34-125">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="a5b34-125">-HostName</span></span>
<span data-ttu-id="a5b34-126">Ana bilgisayar üstbilgisini arka uç sunucularına göndermek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a5b34-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="a5b34-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="a5b34-127">-Name</span></span>
<span data-ttu-id="a5b34-128">Bu cmdlet 'in eklediği arka uç HTTP ayarlarının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="a5b34-129">-Yol</span><span class="sxs-lookup"><span data-stu-id="a5b34-129">-Path</span></span>
<span data-ttu-id="a5b34-130">Tüm HTTP istekleri için önek olarak kullanılması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="a5b34-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="a5b34-131">Bu parametre için bir değer sağlanmadıysa, hiçbir yol önekli.</span><span class="sxs-lookup"><span data-stu-id="a5b34-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="a5b34-132">-Sözcükanabilgisayaradı</span><span class="sxs-lookup"><span data-stu-id="a5b34-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="a5b34-133">Ana bilgisayar üst bilgisinin ana bilgisayar adından çekilmelidir bayrağı.</span><span class="sxs-lookup"><span data-stu-id="a5b34-133">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="a5b34-134">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="a5b34-134">-Port</span></span>
<span data-ttu-id="a5b34-135">Arka uç sunucu havuzunun bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-135">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="a5b34-136">-Araştırma</span><span class="sxs-lookup"><span data-stu-id="a5b34-136">-Probe</span></span>
<span data-ttu-id="a5b34-137">Arka uç sunucusuyla ilişkilendirilecek bir yoklama belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-137">Specifies a probe to associate with a back-end server.</span></span>

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

### <span data-ttu-id="a5b34-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="a5b34-138">-ProbeEnabled</span></span>
<span data-ttu-id="a5b34-139">Yoklama etkin olması gerekiyorsa bayrak.</span><span class="sxs-lookup"><span data-stu-id="a5b34-139">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="a5b34-140">-Probeıd</span><span class="sxs-lookup"><span data-stu-id="a5b34-140">-ProbeId</span></span>
<span data-ttu-id="a5b34-141">Arka uç sunucusuyla ilişkilendirilecek araştırın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="a5b34-142">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="a5b34-142">-Protocol</span></span>
<span data-ttu-id="a5b34-143">Uygulama ağ geçidi ve arka uç sunucuları arasındaki iletişimde iletişim kuralını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="a5b34-144">Bu parametre için kabul edilebilir değerler: http ve https.</span><span class="sxs-lookup"><span data-stu-id="a5b34-144">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="a5b34-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="a5b34-145">-RequestTimeout</span></span>
<span data-ttu-id="a5b34-146">İstek zaman aşımı değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5b34-146">Specifies the request time-out value.</span></span>

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

### <span data-ttu-id="a5b34-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b34-147">CommonParameters</span></span>
<span data-ttu-id="a5b34-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5b34-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b34-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b34-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b34-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5b34-150">INPUTS</span></span>

### <span data-ttu-id="a5b34-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b34-151">System.String</span></span>

## <span data-ttu-id="a5b34-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5b34-152">OUTPUTS</span></span>

### <span data-ttu-id="a5b34-153">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a5b34-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a5b34-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5b34-154">NOTES</span></span>

## <span data-ttu-id="a5b34-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5b34-155">RELATED LINKS</span></span>

[<span data-ttu-id="a5b34-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5b34-156">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="a5b34-157">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5b34-157">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="a5b34-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5b34-158">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="a5b34-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a5b34-159">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

