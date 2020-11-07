---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 538020fa9ef55eedfdf7b181fca16f9499f46682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763159"
---
# <span data-ttu-id="5b9db-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b9db-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="5b9db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b9db-102">SYNOPSIS</span></span>
<span data-ttu-id="5b9db-103">Sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b9db-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b9db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b9db-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b9db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b9db-105">DESCRIPTION</span></span>
<span data-ttu-id="5b9db-106">New-AzureRmApplicationGatewayProbeConfig cmdlet 'i bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b9db-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="5b9db-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b9db-107">EXAMPLES</span></span>

### <span data-ttu-id="5b9db-108">Example1: sistem durumu araştırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b9db-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="5b9db-109">Bu komut HTTP protokolü, 30 saniyelik bir Aralık, 120 saniyelik zaman aşımı ve 8 denemeden iyi durumda bir eşik eşiği olan Probe03 adlı bir sistem durumu araştırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b9db-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="5b9db-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b9db-110">PARAMETERS</span></span>

### <span data-ttu-id="5b9db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b9db-111">-DefaultProfile</span></span>
<span data-ttu-id="5b9db-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b9db-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b9db-113">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="5b9db-113">-HostName</span></span>
<span data-ttu-id="5b9db-114">Bu cmdlet 'in araştırılmasını gönderdiği ana bilgisayar adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="5b9db-115">-Aralık</span><span class="sxs-lookup"><span data-stu-id="5b9db-115">-Interval</span></span>
<span data-ttu-id="5b9db-116">Yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="5b9db-117">Bu, art arda iki sondaya arasındaki zaman aralığıdır.</span><span class="sxs-lookup"><span data-stu-id="5b9db-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="5b9db-118">Bu değer 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="5b9db-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="5b9db-119">-Match</span><span class="sxs-lookup"><span data-stu-id="5b9db-119">-Match</span></span>
<span data-ttu-id="5b9db-120">Sağlık yanıtında yer almalıdır.</span><span class="sxs-lookup"><span data-stu-id="5b9db-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="5b9db-121">Varsayılan değer boştur</span><span class="sxs-lookup"><span data-stu-id="5b9db-121">Default value is empty</span></span>

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

### <span data-ttu-id="5b9db-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="5b9db-122">-MinServers</span></span>
<span data-ttu-id="5b9db-123">Her zaman sağlıklı olarak işaretlenen en az sunucu sayısı.</span><span class="sxs-lookup"><span data-stu-id="5b9db-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="5b9db-124">Varsayılan değer 0 ' dır</span><span class="sxs-lookup"><span data-stu-id="5b9db-124">Default value is 0</span></span>

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

### <span data-ttu-id="5b9db-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="5b9db-125">-Name</span></span>
<span data-ttu-id="5b9db-126">Araştırın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="5b9db-127">-Yol</span><span class="sxs-lookup"><span data-stu-id="5b9db-127">-Path</span></span>
<span data-ttu-id="5b9db-128">Göreli araştırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="5b9db-129">Geçerli yollar eğik çizgi karakteriyle (/) başlar.</span><span class="sxs-lookup"><span data-stu-id="5b9db-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="5b9db-130">%//: Araştırması \<Protocol\> \<host\> \<port\> \<path\></span><span class="sxs-lookup"><span data-stu-id="5b9db-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="5b9db-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5b9db-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="5b9db-132">Ana bilgisayar üst bilgisinin http ayarlarından çekilip çekilmeyeceği.</span><span class="sxs-lookup"><span data-stu-id="5b9db-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="5b9db-133">Varsayılan değer: false</span><span class="sxs-lookup"><span data-stu-id="5b9db-133">Default value is false</span></span>

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

### <span data-ttu-id="5b9db-134">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="5b9db-134">-Protocol</span></span>
<span data-ttu-id="5b9db-135">Araştırma göndermek için kullanılan protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="5b9db-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="5b9db-136">-Timeout</span></span>
<span data-ttu-id="5b9db-137">Yoklama zaman aşımını saniye olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="5b9db-138">Bu, zaman aşımı dönemiyle geçerli bir yanıt alınmadıysa, araştırın başarısız olarak işaretlerini işaretler.</span><span class="sxs-lookup"><span data-stu-id="5b9db-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="5b9db-139">Geçerli değerler 1 saniye ile 86400 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="5b9db-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="5b9db-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="5b9db-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="5b9db-141">Yoklama yeniden deneme sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="5b9db-142">Arka uç sunucusu, ardışık yoklama hatası sayısı sağlıksız eşiğe ulaştığında aşağı işaretlenir.</span><span class="sxs-lookup"><span data-stu-id="5b9db-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="5b9db-143">Geçerli değerler 1 saniye ile 20 saniye arasındadır.</span><span class="sxs-lookup"><span data-stu-id="5b9db-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="5b9db-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b9db-144">CommonParameters</span></span>
<span data-ttu-id="5b9db-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b9db-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b9db-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b9db-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b9db-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b9db-147">INPUTS</span></span>

### <span data-ttu-id="5b9db-148">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5b9db-148">None</span></span>

## <span data-ttu-id="5b9db-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b9db-149">OUTPUTS</span></span>

### <span data-ttu-id="5b9db-150">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="5b9db-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="5b9db-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b9db-151">NOTES</span></span>

## <span data-ttu-id="5b9db-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b9db-152">RELATED LINKS</span></span>

[<span data-ttu-id="5b9db-153">Azure Resource Manager için PowerShell kullanarak uygulama ağ geçidi için özel araştırma oluşturma</span><span class="sxs-lookup"><span data-stu-id="5b9db-153">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="5b9db-154">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b9db-154">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5b9db-155">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b9db-155">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5b9db-156">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b9db-156">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="5b9db-157">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5b9db-157">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

