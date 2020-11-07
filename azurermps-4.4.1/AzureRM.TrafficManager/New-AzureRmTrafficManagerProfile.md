---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 8b88ee761ab9ee136777fb29e7726a2f72110553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764748"
---
# <span data-ttu-id="fc6d1-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="fc6d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc6d1-103">Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc6d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc6d1-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc6d1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc6d1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc6d1-106">**New-AzureRmTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="fc6d1-107">*Ad* parametresini ve gerekli ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="fc6d1-108">Bu cmdlet, yeni profili temsil eden yerel bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="fc6d1-109">Bu cmdlet, Traffic Manager uç noktalarını yapılandırmaz.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="fc6d1-110">Yerel profil nesnesini, Add-AzureRmTrafficManagerEndpointConfig cmdlet 'ini kullanarak güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="fc6d1-111">Ardından Set-AzureRmTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri Traffic Manager 'a yükleyin.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="fc6d1-112">Alternatif olarak, New-AzureRmTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktalar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="fc6d1-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc6d1-113">EXAMPLES</span></span>

### <span data-ttu-id="fc6d1-114">Örnek 1: profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="fc6d1-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="fc6d1-115">Bu komut, kaynak grubu ResourceGroup11 ContosoProfile adlı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="fc6d1-116">DNS FQDN 'si contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="fc6d1-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc6d1-117">PARAMETERS</span></span>

### <span data-ttu-id="fc6d1-118">-Monitorıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="fc6d1-118">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="fc6d1-119">Traffic Manager 'ın Bu profildeki her uç noktanın durumunu denetlemesi gereken zaman aralığı (saniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="fc6d1-119">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="fc6d1-120">Varsayılan değer 30 ' dır.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-120">The default is 30.</span></span>

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

### <span data-ttu-id="fc6d1-121">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="fc6d1-121">-MonitorPath</span></span>
<span data-ttu-id="fc6d1-122">Uç nokta durumunu izlemek için kullanılan yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-122">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="fc6d1-123">Uç nokta etki alanı adıyla ilişkili bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-123">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="fc6d1-124">Bu değer eğik çizgiyle (/) başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-124">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="fc6d1-125">-Monitorın bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="fc6d1-125">-MonitorPort</span></span>
<span data-ttu-id="fc6d1-126">Uç nokta durumunu izlemek için kullanılan TCP bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-126">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="fc6d1-127">Geçerli değerler 1 ile 65535 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-127">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="fc6d1-128">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="fc6d1-128">-MonitorProtocol</span></span>
<span data-ttu-id="fc6d1-129">Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-129">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="fc6d1-130">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="fc6d1-130">Valid values are:</span></span>

- <span data-ttu-id="fc6d1-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="fc6d1-131">HTTP</span></span>
- <span data-ttu-id="fc6d1-132">HTTPS</span><span class="sxs-lookup"><span data-stu-id="fc6d1-132">HTTPS</span></span>

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

### <span data-ttu-id="fc6d1-133">-Monitortimeout Inseconds</span><span class="sxs-lookup"><span data-stu-id="fc6d1-133">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="fc6d1-134">Traffic Manager 'ın Bu profildeki uç noktaların sistem durumu denetimini yanıtlamasını sağlayan süre (saniye).</span><span class="sxs-lookup"><span data-stu-id="fc6d1-134">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="fc6d1-135">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-135">The default is 10.</span></span>

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

### <span data-ttu-id="fc6d1-136">-Monitortoleranda Başarısızlıksayısı</span><span class="sxs-lookup"><span data-stu-id="fc6d1-136">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="fc6d1-137">Sonraki ardışık başarısız durum denetiminin ardından, bu profildeki bir uç noktanın düşürülmeden önce, Trafik Yöneticisi toleransındaki ardışık başarısız durumu denetler.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-137">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="fc6d1-138">Varsayılan 3 ' dir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-138">The default is 3.</span></span>

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

### <span data-ttu-id="fc6d1-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="fc6d1-139">-Name</span></span>
<span data-ttu-id="fc6d1-140">Bu cmdlet 'in oluşturduğu Traffic Manager profili için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-140">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fc6d1-141">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="fc6d1-141">-ProfileStatus</span></span>
<span data-ttu-id="fc6d1-142">Profilin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-142">Specifies the status of the profile.</span></span>
<span data-ttu-id="fc6d1-143">Geçerli değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-143">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="fc6d1-144">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="fc6d1-144">-RelativeDnsName</span></span>
<span data-ttu-id="fc6d1-145">Bu Traffic Manager profilinin sağladığı göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-145">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="fc6d1-146">Traffic Manager bu değeri ve Azure Traffic Manager 'ın profilin tam etki alanı adını (FQDN) oluşturmak için kullandığı DNS etki alanı adını birleştirir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-146">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="fc6d1-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc6d1-147">-ResourceGroupName</span></span>
<span data-ttu-id="fc6d1-148">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="fc6d1-149">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-149">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fc6d1-150">Etiketli</span><span class="sxs-lookup"><span data-stu-id="fc6d1-150">-Tag</span></span>
<span data-ttu-id="fc6d1-151">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-151">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="fc6d1-152">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="fc6d1-152">For example:</span></span>

<span data-ttu-id="fc6d1-153">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="fc6d1-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fc6d1-154">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="fc6d1-154">-TrafficRoutingMethod</span></span>
<span data-ttu-id="fc6d1-155">Trafik yönlendirme yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-155">Specifies the traffic routing method.</span></span>
<span data-ttu-id="fc6d1-156">Bu yöntem, gelen DNS sorgularına yanıt olarak hangi Endpoint Traffic Manager 'ın geri döndüğü belirlenir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-156">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="fc6d1-157">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="fc6d1-157">Valid values are:</span></span>

- <span data-ttu-id="fc6d1-158">Performans</span><span class="sxs-lookup"><span data-stu-id="fc6d1-158">Performance</span></span>
- <span data-ttu-id="fc6d1-159">Ağırlıklı</span><span class="sxs-lookup"><span data-stu-id="fc6d1-159">Weighted</span></span>
- <span data-ttu-id="fc6d1-160">Öncelik</span><span class="sxs-lookup"><span data-stu-id="fc6d1-160">Priority</span></span>

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

### <span data-ttu-id="fc6d1-161">-TTL</span><span class="sxs-lookup"><span data-stu-id="fc6d1-161">-Ttl</span></span>
<span data-ttu-id="fc6d1-162">Yaşam süresi (TTL) değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-162">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="fc6d1-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-163">-DefaultProfile</span></span>
<span data-ttu-id="fc6d1-164">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc6d1-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc6d1-165">CommonParameters</span></span>
<span data-ttu-id="fc6d1-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc6d1-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc6d1-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc6d1-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc6d1-168">INPUTS</span></span>

## <span data-ttu-id="fc6d1-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc6d1-169">OUTPUTS</span></span>

### <span data-ttu-id="fc6d1-170">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-170">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="fc6d1-171">Bu cmdlet yeni bir TrafficManagerProfile nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc6d1-171">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="fc6d1-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc6d1-172">NOTES</span></span>

## <span data-ttu-id="fc6d1-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc6d1-173">RELATED LINKS</span></span>

[<span data-ttu-id="fc6d1-174">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="fc6d1-174">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="fc6d1-175">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-175">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fc6d1-176">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-176">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fc6d1-177">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-177">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fc6d1-178">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-178">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="fc6d1-179">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fc6d1-179">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


