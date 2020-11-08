---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 16499dfb72f973169769c35cd1ba427eba52fd0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104797"
---
# <span data-ttu-id="b8587-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="b8587-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="b8587-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8587-102">SYNOPSIS</span></span>
<span data-ttu-id="b8587-103">Sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8587-103">Creates a health probe.</span></span>

## <span data-ttu-id="b8587-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b8587-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-Port <Int32>]
```

## <span data-ttu-id="b8587-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b8587-105">DESCRIPTION</span></span>
<span data-ttu-id="b8587-106">New-AzApplicationGatewayProbeConfig cmdlet 'i bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8587-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="b8587-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b8587-107">EXAMPLES</span></span>

### <span data-ttu-id="b8587-108">Example1: sistem durumu araştırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="b8587-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="b8587-109">Bu komut HTTP protokolü, 30 saniyelik bir Aralık, 120 saniyelik zaman aşımı ve 8 denemeden iyi durumda bir eşik eşiği olan Probe03 adlı bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b8587-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="b8587-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b8587-110">PARAMETERS</span></span>

### <span data-ttu-id="b8587-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8587-111">-DefaultProfile</span></span>
<span data-ttu-id="b8587-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b8587-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8587-113">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="b8587-113">-HostName</span></span>
<span data-ttu-id="b8587-114">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="b8587-115">-Aralık</span><span class="sxs-lookup"><span data-stu-id="b8587-115">-Interval</span></span>
<span data-ttu-id="b8587-116">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="b8587-117">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="b8587-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="b8587-118">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="b8587-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="b8587-119">-Match</span><span class="sxs-lookup"><span data-stu-id="b8587-119">-Match</span></span>
<span data-ttu-id="b8587-120">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="b8587-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="b8587-121">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="b8587-121">Default value is empty</span></span>

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

### <span data-ttu-id="b8587-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="b8587-122">-MinServers</span></span>
<span data-ttu-id="b8587-123">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="b8587-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="b8587-124">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="b8587-124">Default value is 0</span></span>

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

### <span data-ttu-id="b8587-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b8587-125">-Name</span></span>
<span data-ttu-id="b8587-126">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="b8587-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="b8587-127">-Path</span></span>
<span data-ttu-id="b8587-128">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="b8587-129">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="b8587-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="b8587-130">Araştırma \< iletişim kuralı \> :// \< ana bilgisayar \> : \< bağlantı noktası \> \< yoluna gönderilir \> .</span><span class="sxs-lookup"><span data-stu-id="b8587-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="b8587-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b8587-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="b8587-132">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="b8587-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="b8587-133">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="b8587-133">Default value is false</span></span>

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

### <span data-ttu-id="b8587-134">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="b8587-134">-Protocol</span></span>
<span data-ttu-id="b8587-135">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="b8587-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="b8587-136">-Timeout</span></span>
<span data-ttu-id="b8587-137">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="b8587-138">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="b8587-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="b8587-139">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="b8587-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="b8587-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="b8587-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="b8587-141">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="b8587-142">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="b8587-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="b8587-143">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="b8587-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="b8587-144">-Bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="b8587-144">-Port</span></span>
<span data-ttu-id="b8587-145">Arka uç sunucularını yoklama için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b8587-145">Specifies the port used for probing backend servers.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe

## NOTES

## RELATED LINKS

[Create custom probe for Application Gateway using PowerShell for Azure Resource Manager](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

[Set-AzApplicationGatewayProbeConfig](./Set-AzApplicationGatewayProbeConfig.md)

