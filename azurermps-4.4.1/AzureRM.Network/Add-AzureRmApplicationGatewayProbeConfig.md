---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593084"
---
# <span data-ttu-id="94501-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="94501-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="94501-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94501-102">SYNOPSIS</span></span>
<span data-ttu-id="94501-103">Uygulama ağ geçidine sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="94501-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94501-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="94501-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94501-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="94501-105">DESCRIPTION</span></span>
<span data-ttu-id="94501-106">Add-AzureRmApplicationGatewayProbeConfig cmdlet 'i uygulama ağ geçidine bir sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="94501-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="94501-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="94501-107">EXAMPLES</span></span>

### <span data-ttu-id="94501-108">Örnek 1: uygulama ağ geçidine sistem durumu araştırması ekleme</span><span class="sxs-lookup"><span data-stu-id="94501-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="94501-109">Bu komut ağ geçidi adlı uygulama ağ geçidi için Probe01 adlı bir sistem durumu araştırması ekler.</span><span class="sxs-lookup"><span data-stu-id="94501-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="94501-110">Komut ayrıca sağlıksız eşiğini 8 yeniden denemeden ve 120 saniyeden sonraki zaman aşımına uğruyor.</span><span class="sxs-lookup"><span data-stu-id="94501-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="94501-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="94501-111">PARAMETERS</span></span>

### <span data-ttu-id="94501-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94501-112">-ApplicationGateway</span></span>
<span data-ttu-id="94501-113">Bu cmdlet 'in yoklama eklediği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="94501-114">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="94501-114">-HostName</span></span>
<span data-ttu-id="94501-115">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="94501-116">-Aralık</span><span class="sxs-lookup"><span data-stu-id="94501-116">-Interval</span></span>
<span data-ttu-id="94501-117">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="94501-118">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="94501-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="94501-119">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="94501-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="94501-120">-Match</span><span class="sxs-lookup"><span data-stu-id="94501-120">-Match</span></span>
<span data-ttu-id="94501-121">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="94501-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="94501-122">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="94501-122">Default value is empty</span></span>

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

### <span data-ttu-id="94501-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="94501-123">-MinServers</span></span>
<span data-ttu-id="94501-124">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="94501-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="94501-125">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="94501-125">Default value is 0</span></span>

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

### <span data-ttu-id="94501-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="94501-126">-Name</span></span>
<span data-ttu-id="94501-127">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="94501-128">-Yol</span><span class="sxs-lookup"><span data-stu-id="94501-128">-Path</span></span>
<span data-ttu-id="94501-129">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="94501-130">Geçerli yol, eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="94501-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="94501-131">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="94501-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="94501-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="94501-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="94501-133">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="94501-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="94501-134">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="94501-134">Default value is false</span></span>

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

### <span data-ttu-id="94501-135">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="94501-135">-Protocol</span></span>
<span data-ttu-id="94501-136">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="94501-137">Bu cmdlet yalnızca HTTP 'yi destekler.</span><span class="sxs-lookup"><span data-stu-id="94501-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="94501-138">-Timeout</span><span class="sxs-lookup"><span data-stu-id="94501-138">-Timeout</span></span>
<span data-ttu-id="94501-139">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="94501-140">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="94501-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="94501-141">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="94501-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="94501-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="94501-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="94501-143">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="94501-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="94501-144">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="94501-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="94501-145">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="94501-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="94501-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94501-146">-DefaultProfile</span></span>
<span data-ttu-id="94501-147">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="94501-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94501-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94501-148">CommonParameters</span></span>
<span data-ttu-id="94501-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="94501-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94501-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94501-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94501-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="94501-151">INPUTS</span></span>

### <span data-ttu-id="94501-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94501-152">PSApplicationGateway</span></span>
<span data-ttu-id="94501-153">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="94501-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="94501-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="94501-154">OUTPUTS</span></span>

### <span data-ttu-id="94501-155">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="94501-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="94501-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="94501-156">NOTES</span></span>

## <span data-ttu-id="94501-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="94501-157">RELATED LINKS</span></span>

[<span data-ttu-id="94501-158">Var olan uygulama ağ geçidine araştırma ekleme</span><span class="sxs-lookup"><span data-stu-id="94501-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="94501-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="94501-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="94501-160">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="94501-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="94501-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="94501-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="94501-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="94501-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

