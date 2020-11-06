---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: a41daa12a126e768a4cc7842a72b031d4ca7a759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593533"
---
# <span data-ttu-id="865e2-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="865e2-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="865e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="865e2-102">SYNOPSIS</span></span>
<span data-ttu-id="865e2-103">Sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="865e2-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="865e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="865e2-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="865e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="865e2-105">DESCRIPTION</span></span>
<span data-ttu-id="865e2-106">New-AzureRmApplicationGatewayProbeConfig cmdlet 'i bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="865e2-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="865e2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="865e2-107">EXAMPLES</span></span>

### <span data-ttu-id="865e2-108">Example1: sistem durumu araştırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="865e2-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="865e2-109">Bu komut HTTP protokolü, 30 saniyelik bir Aralık, 120 saniyelik zaman aşımı ve 8 denemeden iyi durumda bir eşik eşiği olan Probe03 adlı bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="865e2-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="865e2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="865e2-110">PARAMETERS</span></span>

### <span data-ttu-id="865e2-111">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="865e2-111">-HostName</span></span>
<span data-ttu-id="865e2-112">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="865e2-112">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="865e2-113">-Aralık</span><span class="sxs-lookup"><span data-stu-id="865e2-113">-Interval</span></span>
<span data-ttu-id="865e2-114">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="865e2-114">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="865e2-115">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="865e2-115">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="865e2-116">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="865e2-116">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="865e2-117">-Match</span><span class="sxs-lookup"><span data-stu-id="865e2-117">-Match</span></span>
<span data-ttu-id="865e2-118">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="865e2-118">Body that must be contained in the health response.</span></span>
<span data-ttu-id="865e2-119">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="865e2-119">Default value is empty</span></span>

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

### <span data-ttu-id="865e2-120">-MinServers</span><span class="sxs-lookup"><span data-stu-id="865e2-120">-MinServers</span></span>
<span data-ttu-id="865e2-121">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="865e2-121">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="865e2-122">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="865e2-122">Default value is 0</span></span>

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

### <span data-ttu-id="865e2-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="865e2-123">-Name</span></span>
<span data-ttu-id="865e2-124">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="865e2-124">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="865e2-125">-Yol</span><span class="sxs-lookup"><span data-stu-id="865e2-125">-Path</span></span>
<span data-ttu-id="865e2-126">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="865e2-126">Specifies the relative path of probe.</span></span>
<span data-ttu-id="865e2-127">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="865e2-127">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="865e2-128">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="865e2-128">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="865e2-129">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="865e2-129">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="865e2-130">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="865e2-130">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="865e2-131">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="865e2-131">Default value is false</span></span>

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

### <span data-ttu-id="865e2-132">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="865e2-132">-Protocol</span></span>
<span data-ttu-id="865e2-133">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="865e2-133">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="865e2-134">-Timeout</span><span class="sxs-lookup"><span data-stu-id="865e2-134">-Timeout</span></span>
<span data-ttu-id="865e2-135">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="865e2-135">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="865e2-136">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="865e2-136">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="865e2-137">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="865e2-137">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="865e2-138">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="865e2-138">-UnhealthyThreshold</span></span>
<span data-ttu-id="865e2-139">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="865e2-139">Specifies the probe retry count.</span></span>
<span data-ttu-id="865e2-140">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="865e2-140">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="865e2-141">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="865e2-141">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="865e2-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865e2-142">-DefaultProfile</span></span>
<span data-ttu-id="865e2-143">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="865e2-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865e2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865e2-144">CommonParameters</span></span>
<span data-ttu-id="865e2-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="865e2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865e2-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="865e2-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865e2-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="865e2-147">INPUTS</span></span>

## <span data-ttu-id="865e2-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="865e2-148">OUTPUTS</span></span>

### <span data-ttu-id="865e2-149">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="865e2-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="865e2-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="865e2-150">NOTES</span></span>

## <span data-ttu-id="865e2-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="865e2-151">RELATED LINKS</span></span>

[<span data-ttu-id="865e2-152">Azure Resource Manager için PowerShell kullanarak uygulama ağ geçidi için özel araştırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="865e2-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="865e2-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="865e2-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="865e2-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="865e2-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="865e2-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="865e2-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="865e2-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="865e2-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

