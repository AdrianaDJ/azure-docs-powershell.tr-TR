---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589644"
---
# <span data-ttu-id="17e36-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="17e36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17e36-102">SYNOPSIS</span></span>
<span data-ttu-id="17e36-103">Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17e36-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17e36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17e36-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17e36-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17e36-105">DESCRIPTION</span></span>
<span data-ttu-id="17e36-106">**New-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17e36-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="17e36-107">*Ad* parametresini ve gerekli ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="17e36-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="17e36-108">Bu cmdlet, yeni profili temsil eden yerel bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="17e36-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="17e36-109">Bu cmdlet, Traffic Manager uç noktalarını yapılandırmaz.</span><span class="sxs-lookup"><span data-stu-id="17e36-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="17e36-110">Yerel profil nesnesini, Add-AzureRmTrafficManagerEndpointConfig cmdlet 'ini kullanarak güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17e36-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="17e36-111">Ardından Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri Traffic Manager 'a yükleyin.</span><span class="sxs-lookup"><span data-stu-id="17e36-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="17e36-112">Alternatif olarak, New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktalar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17e36-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="17e36-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17e36-113">EXAMPLES</span></span>

### <span data-ttu-id="17e36-114">Örnek 1: profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="17e36-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="17e36-115">Bu komut, kaynak grubu ResourceGroup11 ContosoProfile adlı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17e36-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="17e36-116">DNS FQDN 'si contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="17e36-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="17e36-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17e36-117">PARAMETERS</span></span>

### <span data-ttu-id="17e36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-118">-DefaultProfile</span></span>
<span data-ttu-id="17e36-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17e36-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17e36-120">-Monitorıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="17e36-120">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="17e36-121">Traffic Manager 'ın Bu profildeki her uç noktanın durumunu denetlemesi gereken zaman aralığı (saniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="17e36-121">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="17e36-122">Varsayılan değer 30 ' dır.</span><span class="sxs-lookup"><span data-stu-id="17e36-122">The default is 30.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-123">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="17e36-123">-MonitorPath</span></span>
<span data-ttu-id="17e36-124">Uç nokta durumunu izlemek için kullanılan yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-124">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="17e36-125">Uç nokta etki alanı adıyla ilişkili bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="17e36-125">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="17e36-126">Bu değer eğik çizgiyle (/) başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="17e36-126">This value must begin with a slash (/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-127">-Monitorın bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="17e36-127">-MonitorPort</span></span>
<span data-ttu-id="17e36-128">Uç nokta durumunu izlemek için kullanılan TCP bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-128">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="17e36-129">Geçerli değerler 1 ile 65535 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="17e36-129">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="17e36-130">-MonitorProtocol</span></span>
<span data-ttu-id="17e36-131">Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="17e36-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="17e36-132">Valid values are:</span></span>

- <span data-ttu-id="17e36-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="17e36-133">HTTP</span></span>
- <span data-ttu-id="17e36-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="17e36-134">HTTPS</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-135">-Monitortimeout Inseconds</span><span class="sxs-lookup"><span data-stu-id="17e36-135">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="17e36-136">Traffic Manager 'ın Bu profildeki uç noktaların sistem durumu denetimini yanıtlamasını sağlayan süre (saniye).</span><span class="sxs-lookup"><span data-stu-id="17e36-136">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="17e36-137">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="17e36-137">The default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-138">-Monitortoleranda Başarısızlıksayısı</span><span class="sxs-lookup"><span data-stu-id="17e36-138">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="17e36-139">Sonraki ardışık başarısız durum denetiminin ardından, bu profildeki bir uç noktanın düşürülmeden önce, Trafik Yöneticisi toleransındaki ardışık başarısız durumu denetler.</span><span class="sxs-lookup"><span data-stu-id="17e36-139">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="17e36-140">Varsayılan 3 ' dir.</span><span class="sxs-lookup"><span data-stu-id="17e36-140">The default is 3.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="17e36-141">-Name</span></span>
<span data-ttu-id="17e36-142">Bu cmdlet 'in oluşturduğu Traffic Manager profili için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-142">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="17e36-143">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="17e36-143">-ProfileStatus</span></span>
<span data-ttu-id="17e36-144">Profilin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-144">Specifies the status of the profile.</span></span>
<span data-ttu-id="17e36-145">Geçerli değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="17e36-145">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-146">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="17e36-146">-RelativeDnsName</span></span>
<span data-ttu-id="17e36-147">Bu Traffic Manager profilinin sağladığı göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-147">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="17e36-148">Traffic Manager bu değeri ve Azure Traffic Manager 'ın profilin tam etki alanı adını (FQDN) oluşturmak için kullandığı DNS etki alanı adını birleştirir.</span><span class="sxs-lookup"><span data-stu-id="17e36-148">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="17e36-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e36-149">-ResourceGroupName</span></span>
<span data-ttu-id="17e36-150">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="17e36-151">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="17e36-151">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="17e36-152">Etiketli</span><span class="sxs-lookup"><span data-stu-id="17e36-152">-Tag</span></span>
<span data-ttu-id="17e36-153">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="17e36-153">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="17e36-154">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="17e36-154">For example:</span></span>

<span data-ttu-id="17e36-155">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="17e36-155">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-156">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="17e36-156">-TrafficRoutingMethod</span></span>
<span data-ttu-id="17e36-157">Trafik yönlendirme yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-157">Specifies the traffic routing method.</span></span>
<span data-ttu-id="17e36-158">Bu yöntem, gelen DNS sorgularına yanıt olarak hangi Endpoint Traffic Manager 'ın geri döndüğü belirlenir.</span><span class="sxs-lookup"><span data-stu-id="17e36-158">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="17e36-159">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="17e36-159">Valid values are:</span></span>

- <span data-ttu-id="17e36-160">Performans</span><span class="sxs-lookup"><span data-stu-id="17e36-160">Performance</span></span>
- <span data-ttu-id="17e36-161">Ağırlıklı</span><span class="sxs-lookup"><span data-stu-id="17e36-161">Weighted</span></span>
- <span data-ttu-id="17e36-162">Öncelik</span><span class="sxs-lookup"><span data-stu-id="17e36-162">Priority</span></span>
- <span data-ttu-id="17e36-163">Coğrafya</span><span class="sxs-lookup"><span data-stu-id="17e36-163">Geographic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-164">-TTL</span><span class="sxs-lookup"><span data-stu-id="17e36-164">-Ttl</span></span>
<span data-ttu-id="17e36-165">Yaşam süresi (TTL) değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17e36-165">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e36-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e36-166">CommonParameters</span></span>
<span data-ttu-id="17e36-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17e36-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e36-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17e36-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e36-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17e36-169">INPUTS</span></span>

### <span data-ttu-id="17e36-170">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="17e36-170">None</span></span>
<span data-ttu-id="17e36-171">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="17e36-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17e36-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17e36-172">OUTPUTS</span></span>

### <span data-ttu-id="17e36-173">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-173">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="17e36-174">Bu cmdlet yeni bir TrafficManagerProfile nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="17e36-174">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="17e36-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17e36-175">NOTES</span></span>

## <span data-ttu-id="17e36-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17e36-176">RELATED LINKS</span></span>

[<span data-ttu-id="17e36-177">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="17e36-177">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="17e36-178">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-178">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="17e36-179">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-179">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="17e36-180">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-180">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="17e36-181">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-181">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="17e36-182">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="17e36-182">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


