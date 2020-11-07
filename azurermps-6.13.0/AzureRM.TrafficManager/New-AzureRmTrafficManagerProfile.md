---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: bc59e5b317588317ae9dc428db76c924847895da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764096"
---
# <span data-ttu-id="8be78-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="8be78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be78-102">SYNOPSIS</span></span>
<span data-ttu-id="8be78-103">Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8be78-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8be78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8be78-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8be78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8be78-105">DESCRIPTION</span></span>
<span data-ttu-id="8be78-106">**New-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8be78-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="8be78-107">*Ad* parametresini ve gerekli ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="8be78-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="8be78-108">Bu cmdlet, yeni profili temsil eden yerel bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8be78-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="8be78-109">Bu cmdlet, Traffic Manager uç noktalarını yapılandırmaz.</span><span class="sxs-lookup"><span data-stu-id="8be78-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="8be78-110">Yerel profil nesnesini, Add-AzureRmTrafficManagerEndpointConfig cmdlet 'ini kullanarak güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be78-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="8be78-111">Ardından Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri Traffic Manager 'a yükleyin.</span><span class="sxs-lookup"><span data-stu-id="8be78-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="8be78-112">Alternatif olarak, New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktalar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="8be78-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="8be78-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8be78-113">EXAMPLES</span></span>

### <span data-ttu-id="8be78-114">Örnek 1: profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="8be78-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="8be78-115">Bu komut, kaynak grubu ResourceGroup11 ContosoProfile adlı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8be78-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="8be78-116">DNS FQDN 'si contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="8be78-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="8be78-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8be78-117">PARAMETERS</span></span>

### <span data-ttu-id="8be78-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="8be78-118">-CustomHeader</span></span>
<span data-ttu-id="8be78-119">Yoklama istekleri için özel üstbilgi adı ve değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="8be78-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-120">-DefaultProfile</span></span>
<span data-ttu-id="8be78-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8be78-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8be78-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="8be78-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="8be78-123">Yoklama istekleri için beklenen HTTP durum kodu aralıklarının listesi.</span><span class="sxs-lookup"><span data-stu-id="8be78-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="8be78-124">-MaxReturn</span></span>
<span data-ttu-id="8be78-125">Birden çok değerli yönlendirme yöntemiyle profillerin döndürdüğü en fazla yanıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="8be78-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-126">-Monitorıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="8be78-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="8be78-127">Traffic Manager 'ın Bu profildeki her uç noktanın durumunu denetlemesi gereken zaman aralığı (saniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="8be78-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="8be78-128">Varsayılan değer 30 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8be78-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="8be78-129">-MonitorPath</span></span>
<span data-ttu-id="8be78-130">Uç nokta durumunu izlemek için kullanılan yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="8be78-131">Uç nokta etki alanı adıyla ilişkili bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="8be78-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="8be78-132">Bu değer eğik çizgiyle (/) başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="8be78-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-133">-Monitorın bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="8be78-133">-MonitorPort</span></span>
<span data-ttu-id="8be78-134">Uç nokta durumunu izlemek için kullanılan TCP bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="8be78-135">Geçerli değerler 1 ile 65535 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="8be78-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="8be78-136">-MonitorProtocol</span></span>
<span data-ttu-id="8be78-137">Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="8be78-138">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8be78-138">Valid values are:</span></span>

- <span data-ttu-id="8be78-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="8be78-139">HTTP</span></span>
- <span data-ttu-id="8be78-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="8be78-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-141">-Monitortimeout Inseconds</span><span class="sxs-lookup"><span data-stu-id="8be78-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="8be78-142">Traffic Manager 'ın Bu profildeki uç noktaların sistem durumu denetimini yanıtlamasını sağlayan süre (saniye).</span><span class="sxs-lookup"><span data-stu-id="8be78-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="8be78-143">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="8be78-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-144">-Monitortoleranda Başarısızlıksayısı</span><span class="sxs-lookup"><span data-stu-id="8be78-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="8be78-145">Sonraki ardışık başarısız durum denetiminin ardından, bu profildeki bir uç noktanın düşürülmeden önce, Trafik Yöneticisi toleransındaki ardışık başarısız durumu denetler.</span><span class="sxs-lookup"><span data-stu-id="8be78-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="8be78-146">Varsayılan 3 ' dir.</span><span class="sxs-lookup"><span data-stu-id="8be78-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="8be78-147">-Name</span></span>
<span data-ttu-id="8be78-148">Bu cmdlet 'in oluşturduğu Traffic Manager profili için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8be78-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="8be78-149">-ProfileStatus</span></span>
<span data-ttu-id="8be78-150">Profilin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="8be78-151">Geçerli değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="8be78-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="8be78-152">-RelativeDnsName</span></span>
<span data-ttu-id="8be78-153">Bu Traffic Manager profilinin sağladığı göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="8be78-154">Traffic Manager bu değeri ve Azure Traffic Manager 'ın profilin tam etki alanı adını (FQDN) oluşturmak için kullandığı DNS etki alanı adını birleştirir.</span><span class="sxs-lookup"><span data-stu-id="8be78-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="8be78-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be78-155">-ResourceGroupName</span></span>
<span data-ttu-id="8be78-156">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8be78-157">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8be78-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8be78-158">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8be78-158">-Tag</span></span>
<span data-ttu-id="8be78-159">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="8be78-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="8be78-160">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="8be78-160">For example:</span></span>

<span data-ttu-id="8be78-161">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="8be78-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="8be78-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="8be78-163">Trafik yönlendirme yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="8be78-164">Bu yöntem, gelen DNS sorgularına yanıt olarak hangi Endpoint Traffic Manager 'ın geri döndüğü belirlenir.</span><span class="sxs-lookup"><span data-stu-id="8be78-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="8be78-165">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="8be78-165">Valid values are:</span></span>

- <span data-ttu-id="8be78-166">Performans</span><span class="sxs-lookup"><span data-stu-id="8be78-166">Performance</span></span>
- <span data-ttu-id="8be78-167">Ağırlıklı</span><span class="sxs-lookup"><span data-stu-id="8be78-167">Weighted</span></span>
- <span data-ttu-id="8be78-168">Öncelik</span><span class="sxs-lookup"><span data-stu-id="8be78-168">Priority</span></span>
- <span data-ttu-id="8be78-169">Coğrafya</span><span class="sxs-lookup"><span data-stu-id="8be78-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="8be78-170">-Ttl</span></span>
<span data-ttu-id="8be78-171">Yaşam süresi (TTL) değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8be78-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8be78-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be78-172">CommonParameters</span></span>
<span data-ttu-id="8be78-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8be78-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be78-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be78-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be78-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8be78-175">INPUTS</span></span>

### <span data-ttu-id="8be78-176">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8be78-176">None</span></span>
<span data-ttu-id="8be78-177">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="8be78-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8be78-178">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8be78-178">OUTPUTS</span></span>

### <span data-ttu-id="8be78-179">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-179">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="8be78-180">Bu cmdlet yeni bir TrafficManagerProfile nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="8be78-180">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="8be78-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8be78-181">NOTES</span></span>

## <span data-ttu-id="8be78-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8be78-182">RELATED LINKS</span></span>

[<span data-ttu-id="8be78-183">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8be78-183">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="8be78-184">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-184">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8be78-185">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-185">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8be78-186">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-186">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8be78-187">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-187">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="8be78-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8be78-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


