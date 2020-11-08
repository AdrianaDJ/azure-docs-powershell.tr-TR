---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: e7da21709215b4ab185a573e32c8d15de901b33f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104826"
---
# <span data-ttu-id="98dc6-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98dc6-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="98dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="98dc6-103">Var olan uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="98dc6-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="98dc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98dc6-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98dc6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98dc6-105">DESCRIPTION</span></span>
<span data-ttu-id="98dc6-106">Set-AzApplicationGatewayProbeConfig cmdlet, varolan bir uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="98dc6-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="98dc6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98dc6-107">EXAMPLES</span></span>

### <span data-ttu-id="98dc6-108">Örnek 1: uygulama ağ geçidinde durum araştırın yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="98dc6-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="98dc6-109">Bu komut ağ geçidi adındaki uygulama ağ geçidi için Probe05 adlı bir sistem durumu araştırması yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="98dc6-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="98dc6-110">Komut ayrıca sağlıksız eşiğini 8 yeniden denemeden ve 120 saniyeden sonraki zaman aşımına uğruyor.</span><span class="sxs-lookup"><span data-stu-id="98dc6-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="98dc6-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98dc6-111">PARAMETERS</span></span>

### <span data-ttu-id="98dc6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98dc6-112">-ApplicationGateway</span></span>
<span data-ttu-id="98dc6-113">Bu cmdlet 'in yoklama gönderdiği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="98dc6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98dc6-114">-DefaultProfile</span></span>
<span data-ttu-id="98dc6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98dc6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98dc6-116">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="98dc6-116">-HostName</span></span>
<span data-ttu-id="98dc6-117">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="98dc6-118">-Aralık</span><span class="sxs-lookup"><span data-stu-id="98dc6-118">-Interval</span></span>
<span data-ttu-id="98dc6-119">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="98dc6-120">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="98dc6-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="98dc6-121">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="98dc6-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="98dc6-122">-Match</span><span class="sxs-lookup"><span data-stu-id="98dc6-122">-Match</span></span>
<span data-ttu-id="98dc6-123">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="98dc6-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="98dc6-124">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="98dc6-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98dc6-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="98dc6-125">-MinServers</span></span>
<span data-ttu-id="98dc6-126">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="98dc6-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="98dc6-127">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="98dc6-127">Default value is 0</span></span>

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

### <span data-ttu-id="98dc6-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="98dc6-128">-Name</span></span>
<span data-ttu-id="98dc6-129">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="98dc6-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="98dc6-130">-Path</span></span>
<span data-ttu-id="98dc6-131">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="98dc6-132">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="98dc6-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="98dc6-133">Araştırma \< iletişim kuralı \> :// \< ana bilgisayar \> : \< bağlantı noktası \> \< yoluna gönderilir \> .</span><span class="sxs-lookup"><span data-stu-id="98dc6-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="98dc6-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="98dc6-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="98dc6-135">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="98dc6-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="98dc6-136">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="98dc6-136">Default value is false</span></span>

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

### <span data-ttu-id="98dc6-137">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="98dc6-137">-Protocol</span></span>
<span data-ttu-id="98dc6-138">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="98dc6-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="98dc6-139">-Timeout</span></span>
<span data-ttu-id="98dc6-140">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="98dc6-141">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="98dc6-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="98dc6-142">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="98dc6-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="98dc6-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="98dc6-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="98dc6-144">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="98dc6-145">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="98dc6-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="98dc6-146">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="98dc6-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="98dc6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98dc6-147">CommonParameters</span></span>
<span data-ttu-id="98dc6-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98dc6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98dc6-149">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98dc6-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98dc6-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98dc6-150">INPUTS</span></span>

### <span data-ttu-id="98dc6-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98dc6-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98dc6-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98dc6-152">OUTPUTS</span></span>

### <span data-ttu-id="98dc6-153">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="98dc6-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="98dc6-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98dc6-154">NOTES</span></span>

## <span data-ttu-id="98dc6-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98dc6-155">RELATED LINKS</span></span>

[<span data-ttu-id="98dc6-156">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98dc6-156">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="98dc6-157">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98dc6-157">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="98dc6-158">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98dc6-158">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="98dc6-159">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="98dc6-159">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

