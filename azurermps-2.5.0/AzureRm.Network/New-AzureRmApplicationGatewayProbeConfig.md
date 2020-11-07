---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 0e3c0c9a3f1c47163a28dc1732ef488f87014c63
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938800"
---
# <span data-ttu-id="4df16-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4df16-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="4df16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4df16-102">SYNOPSIS</span></span>
<span data-ttu-id="4df16-103">Sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4df16-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4df16-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4df16-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4df16-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4df16-105">DESCRIPTION</span></span>
<span data-ttu-id="4df16-106">New-AzureRmApplicationGatewayProbeConfig cmdlet 'i bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4df16-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="4df16-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4df16-107">EXAMPLES</span></span>

### <span data-ttu-id="4df16-108">Example1: sistem durumu araştırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="4df16-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="4df16-109">Bu komut HTTP protokolü, 30 saniyelik bir Aralık, 120 saniyelik zaman aşımı ve 8 denemeden iyi durumda bir eşik eşiği olan Probe03 adlı bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4df16-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="4df16-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4df16-110">PARAMETERS</span></span>

### <span data-ttu-id="4df16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df16-111">-DefaultProfile</span></span>
<span data-ttu-id="4df16-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4df16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4df16-113">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="4df16-113">-HostName</span></span>
<span data-ttu-id="4df16-114">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df16-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="4df16-115">-Aralık</span><span class="sxs-lookup"><span data-stu-id="4df16-115">-Interval</span></span>
<span data-ttu-id="4df16-116">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df16-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="4df16-117">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="4df16-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="4df16-118">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="4df16-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4df16-119">-Match</span><span class="sxs-lookup"><span data-stu-id="4df16-119">-Match</span></span>
<span data-ttu-id="4df16-120">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="4df16-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="4df16-121">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="4df16-121">Default value is empty</span></span>

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

### <span data-ttu-id="4df16-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="4df16-122">-MinServers</span></span>
<span data-ttu-id="4df16-123">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="4df16-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="4df16-124">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="4df16-124">Default value is 0</span></span>

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

### <span data-ttu-id="4df16-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="4df16-125">-Name</span></span>
<span data-ttu-id="4df16-126">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df16-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="4df16-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="4df16-127">-Path</span></span>
<span data-ttu-id="4df16-128">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df16-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="4df16-129">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="4df16-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="4df16-130">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="4df16-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="4df16-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="4df16-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="4df16-132">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="4df16-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="4df16-133">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="4df16-133">Default value is false</span></span>

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

### <span data-ttu-id="4df16-134">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="4df16-134">-Protocol</span></span>
<span data-ttu-id="4df16-135">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df16-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="4df16-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="4df16-136">-Timeout</span></span>
<span data-ttu-id="4df16-137">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df16-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="4df16-138">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="4df16-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="4df16-139">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="4df16-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="4df16-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="4df16-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="4df16-141">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4df16-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="4df16-142">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="4df16-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="4df16-143">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="4df16-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="4df16-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df16-144">CommonParameters</span></span>
<span data-ttu-id="4df16-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4df16-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df16-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4df16-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df16-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4df16-147">INPUTS</span></span>

## <span data-ttu-id="4df16-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4df16-148">OUTPUTS</span></span>

### <span data-ttu-id="4df16-149">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="4df16-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="4df16-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4df16-150">NOTES</span></span>

## <span data-ttu-id="4df16-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4df16-151">RELATED LINKS</span></span>

[<span data-ttu-id="4df16-152">Azure Resource Manager için PowerShell kullanarak uygulama ağ geçidi için özel araştırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="4df16-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="4df16-153">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4df16-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4df16-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4df16-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4df16-155">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4df16-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="4df16-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4df16-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

