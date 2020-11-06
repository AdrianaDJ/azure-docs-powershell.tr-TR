---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 212e418c3fdaf8ba7f67ebdae0565d5d230daa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590722"
---
# <span data-ttu-id="afd20-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="afd20-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="afd20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd20-102">SYNOPSIS</span></span>
<span data-ttu-id="afd20-103">Var olan uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="afd20-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd20-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afd20-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afd20-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="afd20-105">DESCRIPTION</span></span>
<span data-ttu-id="afd20-106">Set-AzureRmApplicationGatewayProbeConfig cmdlet, varolan bir uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="afd20-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="afd20-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afd20-107">EXAMPLES</span></span>

### <span data-ttu-id="afd20-108">Örnek 1: uygulama ağ geçidinde durum araştırın yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="afd20-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="afd20-109">Bu komut ağ geçidi adındaki uygulama ağ geçidi için Probe05 adlı bir sistem durumu araştırması yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="afd20-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="afd20-110">Komut ayrıca sağlıksız eşiğini 8 yeniden denemeden ve 120 saniyeden sonraki zaman aşımına uğruyor.</span><span class="sxs-lookup"><span data-stu-id="afd20-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="afd20-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afd20-111">PARAMETERS</span></span>

### <span data-ttu-id="afd20-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afd20-112">-ApplicationGateway</span></span>
<span data-ttu-id="afd20-113">Bu cmdlet 'in yoklama gönderdiği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="afd20-114">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="afd20-114">-HostName</span></span>
<span data-ttu-id="afd20-115">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="afd20-116">-Aralık</span><span class="sxs-lookup"><span data-stu-id="afd20-116">-Interval</span></span>
<span data-ttu-id="afd20-117">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="afd20-118">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="afd20-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="afd20-119">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="afd20-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="afd20-120">-Match</span><span class="sxs-lookup"><span data-stu-id="afd20-120">-Match</span></span>
<span data-ttu-id="afd20-121">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="afd20-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="afd20-122">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="afd20-122">Default value is empty</span></span>

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

### <span data-ttu-id="afd20-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="afd20-123">-MinServers</span></span>
<span data-ttu-id="afd20-124">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="afd20-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="afd20-125">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="afd20-125">Default value is 0</span></span>

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

### <span data-ttu-id="afd20-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="afd20-126">-Name</span></span>
<span data-ttu-id="afd20-127">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="afd20-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="afd20-128">-Path</span></span>
<span data-ttu-id="afd20-129">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="afd20-130">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="afd20-130">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="afd20-131">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="afd20-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="afd20-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="afd20-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="afd20-133">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="afd20-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="afd20-134">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="afd20-134">Default value is false</span></span>

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

### <span data-ttu-id="afd20-135">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="afd20-135">-Protocol</span></span>
<span data-ttu-id="afd20-136">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-136">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="afd20-137">-Timeout</span><span class="sxs-lookup"><span data-stu-id="afd20-137">-Timeout</span></span>
<span data-ttu-id="afd20-138">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-138">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="afd20-139">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="afd20-139">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="afd20-140">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="afd20-140">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="afd20-141">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="afd20-141">-UnhealthyThreshold</span></span>
<span data-ttu-id="afd20-142">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afd20-142">Specifies the probe retry count.</span></span>
<span data-ttu-id="afd20-143">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="afd20-143">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="afd20-144">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="afd20-144">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="afd20-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd20-145">-DefaultProfile</span></span>
<span data-ttu-id="afd20-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afd20-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afd20-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd20-147">CommonParameters</span></span>
<span data-ttu-id="afd20-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afd20-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd20-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd20-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd20-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afd20-150">INPUTS</span></span>

### <span data-ttu-id="afd20-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afd20-151">PSApplicationGateway</span></span>
<span data-ttu-id="afd20-152">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="afd20-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="afd20-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afd20-153">OUTPUTS</span></span>

### <span data-ttu-id="afd20-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="afd20-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="afd20-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afd20-155">NOTES</span></span>

## <span data-ttu-id="afd20-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afd20-156">RELATED LINKS</span></span>

[<span data-ttu-id="afd20-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="afd20-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="afd20-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="afd20-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="afd20-159">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="afd20-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="afd20-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="afd20-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

