---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107714"
---
# <span data-ttu-id="ffeb0-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ffeb0-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ffeb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffeb0-102">SYNOPSIS</span></span>
<span data-ttu-id="ffeb0-103">Uygulama ağ geçidine sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ffeb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffeb0-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffeb0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffeb0-105">DESCRIPTION</span></span>
<span data-ttu-id="ffeb0-106">Add-AzApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidine bir sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ffeb0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffeb0-107">EXAMPLES</span></span>

### <span data-ttu-id="ffeb0-108">Örnek 1: uygulama ağ geçidine sistem durumu araştırması ekleme</span><span class="sxs-lookup"><span data-stu-id="ffeb0-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ffeb0-109">Bu komut ağ geçidi adlı uygulama ağ geçidi için Probe01 adlı bir sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="ffeb0-110">Komut ayrıca sağlıksız eşiğini 8 yeniden denemeden ve 120 saniyeden sonraki zaman aşımına uğruyor.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="ffeb0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffeb0-111">PARAMETERS</span></span>

### <span data-ttu-id="ffeb0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffeb0-112">-ApplicationGateway</span></span>
<span data-ttu-id="ffeb0-113">Bu cmdlet 'in yoklama eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="ffeb0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffeb0-114">-DefaultProfile</span></span>
<span data-ttu-id="ffeb0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffeb0-116">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="ffeb0-116">-HostName</span></span>
<span data-ttu-id="ffeb0-117">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="ffeb0-118">-Aralık</span><span class="sxs-lookup"><span data-stu-id="ffeb0-118">-Interval</span></span>
<span data-ttu-id="ffeb0-119">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ffeb0-120">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ffeb0-121">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ffeb0-122">-Match</span><span class="sxs-lookup"><span data-stu-id="ffeb0-122">-Match</span></span>
<span data-ttu-id="ffeb0-123">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ffeb0-124">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="ffeb0-124">Default value is empty</span></span>

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

### <span data-ttu-id="ffeb0-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ffeb0-125">-MinServers</span></span>
<span data-ttu-id="ffeb0-126">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ffeb0-127">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="ffeb0-127">Default value is 0</span></span>

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

### <span data-ttu-id="ffeb0-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="ffeb0-128">-Name</span></span>
<span data-ttu-id="ffeb0-129">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="ffeb0-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="ffeb0-130">-Path</span></span>
<span data-ttu-id="ffeb0-131">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ffeb0-132">Geçerli yol, eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="ffeb0-133">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="ffeb0-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="ffeb0-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ffeb0-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ffeb0-135">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ffeb0-136">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="ffeb0-136">Default value is false</span></span>

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

### <span data-ttu-id="ffeb0-137">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ffeb0-137">-Protocol</span></span>
<span data-ttu-id="ffeb0-138">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="ffeb0-139">Bu cmdlet yalnızca HTTP 'yi destekler.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="ffeb0-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="ffeb0-140">-Timeout</span></span>
<span data-ttu-id="ffeb0-141">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ffeb0-142">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ffeb0-143">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ffeb0-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ffeb0-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="ffeb0-145">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="ffeb0-146">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ffeb0-147">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="ffeb0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffeb0-148">CommonParameters</span></span>
<span data-ttu-id="ffeb0-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffeb0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffeb0-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffeb0-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffeb0-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffeb0-151">INPUTS</span></span>

### <span data-ttu-id="ffeb0-152">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffeb0-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ffeb0-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffeb0-153">OUTPUTS</span></span>

### <span data-ttu-id="ffeb0-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ffeb0-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ffeb0-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffeb0-155">NOTES</span></span>

## <span data-ttu-id="ffeb0-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffeb0-156">RELATED LINKS</span></span>

[<span data-ttu-id="ffeb0-157">Var olan uygulama ağ geçidine araştırma ekleme</span><span class="sxs-lookup"><span data-stu-id="ffeb0-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="ffeb0-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ffeb0-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ffeb0-159">Yeni-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ffeb0-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ffeb0-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ffeb0-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ffeb0-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ffeb0-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

