---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 50f54d258e6b5575983d8cd35f487783ea922eb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936564"
---
# <span data-ttu-id="57cba-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57cba-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="57cba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57cba-102">SYNOPSIS</span></span>
<span data-ttu-id="57cba-103">Var olan uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="57cba-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="57cba-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="57cba-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57cba-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="57cba-105">DESCRIPTION</span></span>
<span data-ttu-id="57cba-106">Set-AzApplicationGatewayProbeConfig cmdlet, varolan bir uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="57cba-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="57cba-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="57cba-107">EXAMPLES</span></span>

### <span data-ttu-id="57cba-108">Örnek 1: uygulama ağ geçidinde durum araştırın yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="57cba-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="57cba-109">Bu komut ağ geçidi adındaki uygulama ağ geçidi için Probe05 adlı bir sistem durumu araştırması yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="57cba-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="57cba-110">Komut ayrıca sağlıksız eşiğini 8 yeniden denemeden ve 120 saniyeden sonraki zaman aşımına uğruyor.</span><span class="sxs-lookup"><span data-stu-id="57cba-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="57cba-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="57cba-111">PARAMETERS</span></span>

### <span data-ttu-id="57cba-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57cba-112">-ApplicationGateway</span></span>
<span data-ttu-id="57cba-113">Bu cmdlet 'in yoklama gönderdiği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="57cba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57cba-114">-DefaultProfile</span></span>
<span data-ttu-id="57cba-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="57cba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57cba-116">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="57cba-116">-HostName</span></span>
<span data-ttu-id="57cba-117">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="57cba-118">-Aralık</span><span class="sxs-lookup"><span data-stu-id="57cba-118">-Interval</span></span>
<span data-ttu-id="57cba-119">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="57cba-120">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="57cba-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="57cba-121">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="57cba-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="57cba-122">-Match</span><span class="sxs-lookup"><span data-stu-id="57cba-122">-Match</span></span>
<span data-ttu-id="57cba-123">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="57cba-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="57cba-124">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="57cba-124">Default value is empty</span></span>

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

### <span data-ttu-id="57cba-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="57cba-125">-MinServers</span></span>
<span data-ttu-id="57cba-126">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="57cba-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="57cba-127">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="57cba-127">Default value is 0</span></span>

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

### <span data-ttu-id="57cba-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="57cba-128">-Name</span></span>
<span data-ttu-id="57cba-129">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="57cba-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="57cba-130">-Path</span></span>
<span data-ttu-id="57cba-131">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="57cba-132">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="57cba-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="57cba-133">Araştırma \< iletişim kuralı \> :// \< ana bilgisayar \> : \< bağlantı noktası \> \< yoluna gönderilir \> .</span><span class="sxs-lookup"><span data-stu-id="57cba-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="57cba-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="57cba-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="57cba-135">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="57cba-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="57cba-136">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="57cba-136">Default value is false</span></span>

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

### <span data-ttu-id="57cba-137">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="57cba-137">-Protocol</span></span>
<span data-ttu-id="57cba-138">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="57cba-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="57cba-139">-Timeout</span></span>
<span data-ttu-id="57cba-140">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="57cba-141">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="57cba-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="57cba-142">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="57cba-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="57cba-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="57cba-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="57cba-144">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="57cba-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="57cba-145">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="57cba-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="57cba-146">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="57cba-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="57cba-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cba-147">CommonParameters</span></span>
<span data-ttu-id="57cba-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="57cba-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cba-149">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57cba-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cba-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="57cba-150">INPUTS</span></span>

### <span data-ttu-id="57cba-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57cba-151">PSApplicationGateway</span></span>
<span data-ttu-id="57cba-152">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="57cba-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="57cba-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="57cba-153">OUTPUTS</span></span>

### <span data-ttu-id="57cba-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="57cba-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="57cba-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="57cba-155">NOTES</span></span>

## <span data-ttu-id="57cba-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="57cba-156">RELATED LINKS</span></span>

[<span data-ttu-id="57cba-157">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57cba-157">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="57cba-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57cba-158">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="57cba-159">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57cba-159">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="57cba-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="57cba-160">Remove-AzApplicationGatewayProbeConfig</span></span>]()

