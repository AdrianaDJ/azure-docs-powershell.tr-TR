---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 955f5179340351dd662979385ca3d3dc2a39b9f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592452"
---
# <span data-ttu-id="e7400-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e7400-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e7400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7400-102">SYNOPSIS</span></span>
<span data-ttu-id="e7400-103">Sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7400-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7400-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7400-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7400-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7400-105">DESCRIPTION</span></span>
<span data-ttu-id="e7400-106">New-AzureRmApplicationGatewayProbeConfig cmdlet 'i bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7400-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="e7400-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7400-107">EXAMPLES</span></span>

### <span data-ttu-id="e7400-108">Example1: sistem durumu araştırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="e7400-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="e7400-109">Bu komut HTTP protokolü, 30 saniyelik bir Aralık, 120 saniyelik zaman aşımı ve 8 denemeden iyi durumda bir eşik eşiği olan Probe03 adlı bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7400-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="e7400-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7400-110">PARAMETERS</span></span>

### <span data-ttu-id="e7400-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7400-111">-DefaultProfile</span></span>
<span data-ttu-id="e7400-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7400-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7400-113">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="e7400-113">-HostName</span></span>
<span data-ttu-id="e7400-114">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7400-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="e7400-115">-Aralık</span><span class="sxs-lookup"><span data-stu-id="e7400-115">-Interval</span></span>
<span data-ttu-id="e7400-116">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7400-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="e7400-117">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="e7400-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="e7400-118">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="e7400-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e7400-119">-Match</span><span class="sxs-lookup"><span data-stu-id="e7400-119">-Match</span></span>
<span data-ttu-id="e7400-120">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="e7400-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="e7400-121">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="e7400-121">Default value is empty</span></span>

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

### <span data-ttu-id="e7400-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="e7400-122">-MinServers</span></span>
<span data-ttu-id="e7400-123">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="e7400-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="e7400-124">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="e7400-124">Default value is 0</span></span>

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

### <span data-ttu-id="e7400-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7400-125">-Name</span></span>
<span data-ttu-id="e7400-126">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7400-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e7400-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="e7400-127">-Path</span></span>
<span data-ttu-id="e7400-128">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7400-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="e7400-129">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="e7400-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="e7400-130">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="e7400-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="e7400-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e7400-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="e7400-132">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="e7400-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="e7400-133">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="e7400-133">Default value is false</span></span>

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

### <span data-ttu-id="e7400-134">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="e7400-134">-Protocol</span></span>
<span data-ttu-id="e7400-135">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7400-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="e7400-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="e7400-136">-Timeout</span></span>
<span data-ttu-id="e7400-137">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7400-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="e7400-138">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="e7400-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="e7400-139">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="e7400-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e7400-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="e7400-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="e7400-141">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e7400-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="e7400-142">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="e7400-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="e7400-143">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="e7400-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="e7400-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7400-144">CommonParameters</span></span>
<span data-ttu-id="e7400-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7400-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7400-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7400-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7400-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7400-147">INPUTS</span></span>

### <span data-ttu-id="e7400-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e7400-148">None</span></span>
<span data-ttu-id="e7400-149">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e7400-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e7400-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7400-150">OUTPUTS</span></span>

### <span data-ttu-id="e7400-151">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="e7400-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="e7400-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7400-152">NOTES</span></span>

## <span data-ttu-id="e7400-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7400-153">RELATED LINKS</span></span>

[<span data-ttu-id="e7400-154">Azure Resource Manager için PowerShell kullanarak uygulama ağ geçidi için özel araştırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="e7400-154">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="e7400-155">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e7400-155">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e7400-156">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e7400-156">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e7400-157">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e7400-157">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e7400-158">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e7400-158">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

