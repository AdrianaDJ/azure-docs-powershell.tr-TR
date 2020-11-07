---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 43c74d2edd2cfd07f65b7d5437bf1cf5c0dfca9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935426"
---
# <span data-ttu-id="0bc98-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0bc98-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0bc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bc98-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc98-103">Sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bc98-103">Creates a health probe.</span></span>

## <span data-ttu-id="0bc98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0bc98-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bc98-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0bc98-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc98-106">New-AzApplicationGatewayProbeConfig cmdlet 'i bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bc98-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="0bc98-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0bc98-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc98-108">Example1: sistem durumu araştırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="0bc98-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="0bc98-109">Bu komut HTTP protokolü, 30 saniyelik bir Aralık, 120 saniyelik zaman aşımı ve 8 denemeden iyi durumda bir eşik eşiği olan Probe03 adlı bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0bc98-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="0bc98-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0bc98-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc98-111">-DefaultProfile</span></span>
<span data-ttu-id="0bc98-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0bc98-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bc98-113">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="0bc98-113">-HostName</span></span>
<span data-ttu-id="0bc98-114">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="0bc98-115">-Aralık</span><span class="sxs-lookup"><span data-stu-id="0bc98-115">-Interval</span></span>
<span data-ttu-id="0bc98-116">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="0bc98-117">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="0bc98-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="0bc98-118">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="0bc98-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0bc98-119">-Match</span><span class="sxs-lookup"><span data-stu-id="0bc98-119">-Match</span></span>
<span data-ttu-id="0bc98-120">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="0bc98-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="0bc98-121">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="0bc98-121">Default value is empty</span></span>

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

### <span data-ttu-id="0bc98-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="0bc98-122">-MinServers</span></span>
<span data-ttu-id="0bc98-123">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="0bc98-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="0bc98-124">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="0bc98-124">Default value is 0</span></span>

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

### <span data-ttu-id="0bc98-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0bc98-125">-Name</span></span>
<span data-ttu-id="0bc98-126">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0bc98-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="0bc98-127">-Path</span></span>
<span data-ttu-id="0bc98-128">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="0bc98-129">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="0bc98-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="0bc98-130">Araştırma \< iletişim kuralı \> :// \< ana bilgisayar \> : \< bağlantı noktası \> \< yoluna gönderilir \> .</span><span class="sxs-lookup"><span data-stu-id="0bc98-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="0bc98-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0bc98-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="0bc98-132">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="0bc98-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="0bc98-133">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="0bc98-133">Default value is false</span></span>

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

### <span data-ttu-id="0bc98-134">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="0bc98-134">-Protocol</span></span>
<span data-ttu-id="0bc98-135">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="0bc98-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="0bc98-136">-Timeout</span></span>
<span data-ttu-id="0bc98-137">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="0bc98-138">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="0bc98-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="0bc98-139">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="0bc98-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="0bc98-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="0bc98-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="0bc98-141">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="0bc98-142">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="0bc98-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="0bc98-143">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="0bc98-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="0bc98-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc98-144">CommonParameters</span></span>
<span data-ttu-id="0bc98-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0bc98-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc98-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc98-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc98-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0bc98-147">INPUTS</span></span>

## <span data-ttu-id="0bc98-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0bc98-148">OUTPUTS</span></span>

### <span data-ttu-id="0bc98-149">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="0bc98-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="0bc98-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0bc98-150">NOTES</span></span>

## <span data-ttu-id="0bc98-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0bc98-151">RELATED LINKS</span></span>

[<span data-ttu-id="0bc98-152">Azure Resource Manager için PowerShell kullanarak uygulama ağ geçidi için özel araştırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="0bc98-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="0bc98-153">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0bc98-153">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0bc98-154">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0bc98-154">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0bc98-155">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0bc98-155">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0bc98-156">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0bc98-156">Set-AzApplicationGatewayProbeConfig</span></span>]()

