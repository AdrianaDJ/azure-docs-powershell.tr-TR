---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 16463a44017c52b9dbaffc0042a7f0fa60823a94
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935653"
---
# <span data-ttu-id="b18ad-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b18ad-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="b18ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b18ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b18ad-103">Uygulama ağ geçidine sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b18ad-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="b18ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b18ad-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b18ad-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b18ad-105">DESCRIPTION</span></span>
<span data-ttu-id="b18ad-106">Add-AzApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidine bir sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b18ad-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="b18ad-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b18ad-107">EXAMPLES</span></span>

### <span data-ttu-id="b18ad-108">Örnek 1: uygulama ağ geçidine sistem durumu araştırması ekleme</span><span class="sxs-lookup"><span data-stu-id="b18ad-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="b18ad-109">Bu komut ağ geçidi adlı uygulama ağ geçidi için Probe01 adlı bir sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="b18ad-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="b18ad-110">Komut ayrıca sağlıksız eşiğini 8 yeniden denemeden ve 120 saniyeden sonraki zaman aşımına uğruyor.</span><span class="sxs-lookup"><span data-stu-id="b18ad-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="b18ad-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b18ad-111">PARAMETERS</span></span>

### <span data-ttu-id="b18ad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b18ad-112">-ApplicationGateway</span></span>
<span data-ttu-id="b18ad-113">Bu cmdlet 'in yoklama eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="b18ad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b18ad-114">-DefaultProfile</span></span>
<span data-ttu-id="b18ad-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b18ad-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b18ad-116">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="b18ad-116">-HostName</span></span>
<span data-ttu-id="b18ad-117">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="b18ad-118">-Aralık</span><span class="sxs-lookup"><span data-stu-id="b18ad-118">-Interval</span></span>
<span data-ttu-id="b18ad-119">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="b18ad-120">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="b18ad-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="b18ad-121">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="b18ad-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="b18ad-122">-Match</span><span class="sxs-lookup"><span data-stu-id="b18ad-122">-Match</span></span>
<span data-ttu-id="b18ad-123">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="b18ad-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="b18ad-124">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="b18ad-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b18ad-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="b18ad-125">-MinServers</span></span>
<span data-ttu-id="b18ad-126">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="b18ad-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="b18ad-127">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="b18ad-127">Default value is 0</span></span>

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

### <span data-ttu-id="b18ad-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="b18ad-128">-Name</span></span>
<span data-ttu-id="b18ad-129">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="b18ad-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="b18ad-130">-Path</span></span>
<span data-ttu-id="b18ad-131">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="b18ad-132">Geçerli yol, eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="b18ad-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="b18ad-133">Araştırma \< iletişim kuralı \> :// \< ana bilgisayar \> : \< bağlantı noktası \> \< yoluna gönderilir \> .</span><span class="sxs-lookup"><span data-stu-id="b18ad-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="b18ad-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b18ad-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="b18ad-135">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="b18ad-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="b18ad-136">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="b18ad-136">Default value is false</span></span>

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

### <span data-ttu-id="b18ad-137">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b18ad-137">-Protocol</span></span>
<span data-ttu-id="b18ad-138">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="b18ad-139">Bu cmdlet yalnızca HTTP 'yi destekler.</span><span class="sxs-lookup"><span data-stu-id="b18ad-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="b18ad-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="b18ad-140">-Timeout</span></span>
<span data-ttu-id="b18ad-141">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="b18ad-142">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="b18ad-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="b18ad-143">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="b18ad-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="b18ad-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="b18ad-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="b18ad-145">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="b18ad-146">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="b18ad-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="b18ad-147">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="b18ad-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="b18ad-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18ad-148">CommonParameters</span></span>
<span data-ttu-id="b18ad-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b18ad-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18ad-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b18ad-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18ad-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b18ad-151">INPUTS</span></span>

### <span data-ttu-id="b18ad-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b18ad-152">PSApplicationGateway</span></span>
<span data-ttu-id="b18ad-153">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="b18ad-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="b18ad-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b18ad-154">OUTPUTS</span></span>

### <span data-ttu-id="b18ad-155">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b18ad-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b18ad-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b18ad-156">NOTES</span></span>

## <span data-ttu-id="b18ad-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b18ad-157">RELATED LINKS</span></span>

[<span data-ttu-id="b18ad-158">Var olan uygulama ağ geçidine araştırma ekleme</span><span class="sxs-lookup"><span data-stu-id="b18ad-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="b18ad-159">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b18ad-159">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b18ad-160">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b18ad-160">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b18ad-161">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b18ad-161">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="b18ad-162">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b18ad-162">Set-AzApplicationGatewayProbeConfig</span></span>]()
