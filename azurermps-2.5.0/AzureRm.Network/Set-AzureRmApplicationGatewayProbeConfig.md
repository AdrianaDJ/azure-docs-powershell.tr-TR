---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 7fb8a30986c31659b49a08b261062e150ebe7e09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938776"
---
# <span data-ttu-id="870d5-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="870d5-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="870d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870d5-102">SYNOPSIS</span></span>
<span data-ttu-id="870d5-103">Var olan uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="870d5-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="870d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="870d5-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="870d5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="870d5-105">DESCRIPTION</span></span>
<span data-ttu-id="870d5-106">Set-AzureRmApplicationGatewayProbeConfig cmdlet, varolan bir uygulama ağ geçidinde sistem durumu araştırma yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="870d5-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="870d5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="870d5-107">EXAMPLES</span></span>

### <span data-ttu-id="870d5-108">Örnek 1: uygulama ağ geçidinde durum araştırın yapılandırmasını ayarlama</span><span class="sxs-lookup"><span data-stu-id="870d5-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="870d5-109">Bu komut ağ geçidi adındaki uygulama ağ geçidi için Probe05 adlı bir sistem durumu araştırması yapılandırmasını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="870d5-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="870d5-110">Komut ayrıca sağlıksız eşiğini 8 yeniden denemeden ve 120 saniyeden sonraki zaman aşımına uğruyor.</span><span class="sxs-lookup"><span data-stu-id="870d5-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="870d5-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="870d5-111">PARAMETERS</span></span>

### <span data-ttu-id="870d5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="870d5-112">-ApplicationGateway</span></span>
<span data-ttu-id="870d5-113">Bu cmdlet 'in yoklama gönderdiği uygulama ağ geçidini belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="870d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870d5-114">-DefaultProfile</span></span>
<span data-ttu-id="870d5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="870d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="870d5-116">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="870d5-116">-HostName</span></span>
<span data-ttu-id="870d5-117">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="870d5-118">-Aralık</span><span class="sxs-lookup"><span data-stu-id="870d5-118">-Interval</span></span>
<span data-ttu-id="870d5-119">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="870d5-120">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="870d5-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="870d5-121">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="870d5-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="870d5-122">-Match</span><span class="sxs-lookup"><span data-stu-id="870d5-122">-Match</span></span>
<span data-ttu-id="870d5-123">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="870d5-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="870d5-124">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="870d5-124">Default value is empty</span></span>

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

### <span data-ttu-id="870d5-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="870d5-125">-MinServers</span></span>
<span data-ttu-id="870d5-126">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="870d5-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="870d5-127">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="870d5-127">Default value is 0</span></span>

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

### <span data-ttu-id="870d5-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="870d5-128">-Name</span></span>
<span data-ttu-id="870d5-129">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="870d5-130">-Yol</span><span class="sxs-lookup"><span data-stu-id="870d5-130">-Path</span></span>
<span data-ttu-id="870d5-131">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="870d5-132">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="870d5-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="870d5-133">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="870d5-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="870d5-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="870d5-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="870d5-135">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="870d5-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="870d5-136">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="870d5-136">Default value is false</span></span>

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

### <span data-ttu-id="870d5-137">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="870d5-137">-Protocol</span></span>
<span data-ttu-id="870d5-138">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="870d5-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="870d5-139">-Timeout</span></span>
<span data-ttu-id="870d5-140">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="870d5-141">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="870d5-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="870d5-142">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="870d5-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="870d5-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="870d5-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="870d5-144">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="870d5-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="870d5-145">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="870d5-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="870d5-146">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="870d5-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="870d5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870d5-147">CommonParameters</span></span>
<span data-ttu-id="870d5-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="870d5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870d5-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870d5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870d5-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="870d5-150">INPUTS</span></span>

### <span data-ttu-id="870d5-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="870d5-151">PSApplicationGateway</span></span>
<span data-ttu-id="870d5-152">Parametre ' ApplicationGateway ', ardışık düzenin ' PSApplicationGateway ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="870d5-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="870d5-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="870d5-153">OUTPUTS</span></span>

### <span data-ttu-id="870d5-154">Microsoft. Azure. Commands. Network. modeller. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="870d5-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="870d5-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="870d5-155">NOTES</span></span>

## <span data-ttu-id="870d5-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="870d5-156">RELATED LINKS</span></span>

[<span data-ttu-id="870d5-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="870d5-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="870d5-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="870d5-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="870d5-159">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="870d5-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="870d5-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="870d5-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

