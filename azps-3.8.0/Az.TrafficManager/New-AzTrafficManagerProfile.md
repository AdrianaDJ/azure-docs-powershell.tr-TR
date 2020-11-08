---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098080"
---
# <span data-ttu-id="53228-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53228-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="53228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53228-102">SYNOPSIS</span></span>
<span data-ttu-id="53228-103">Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="53228-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="53228-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="53228-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53228-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="53228-105">DESCRIPTION</span></span>
<span data-ttu-id="53228-106">**New-AzTrafficManagerProfile** cmdlet 'ı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="53228-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="53228-107">*Ad* parametresini ve gerekli ayarları belirtin.</span><span class="sxs-lookup"><span data-stu-id="53228-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="53228-108">Bu cmdlet, yeni profili temsil eden yerel bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="53228-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="53228-109">Bu cmdlet, Traffic Manager uç noktalarını yapılandırmaz.</span><span class="sxs-lookup"><span data-stu-id="53228-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="53228-110">Yerel profil nesnesini, Add-AzTrafficManagerEndpointConfig cmdlet 'ini kullanarak güncelleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53228-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="53228-111">Ardından Set-AzTrafficManagerProfile cmdlet 'ini kullanarak değişiklikleri Traffic Manager 'a yükleyin.</span><span class="sxs-lookup"><span data-stu-id="53228-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="53228-112">Alternatif olarak, New-AzTrafficManagerEndpoint cmdlet 'ini kullanarak uç noktalar ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="53228-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="53228-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="53228-113">EXAMPLES</span></span>

### <span data-ttu-id="53228-114">Örnek 1: profil oluşturma</span><span class="sxs-lookup"><span data-stu-id="53228-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="53228-115">Bu komut, kaynak grubu ResourceGroup11 ContosoProfile adlı bir Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="53228-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="53228-116">DNS FQDN 'si contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="53228-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="53228-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="53228-117">PARAMETERS</span></span>

### <span data-ttu-id="53228-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="53228-118">-CustomHeader</span></span>
<span data-ttu-id="53228-119">Yoklama istekleri için özel üstbilgi adı ve değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="53228-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="53228-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53228-120">-DefaultProfile</span></span>
<span data-ttu-id="53228-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="53228-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53228-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="53228-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="53228-123">Yoklama istekleri için beklenen HTTP durum kodu aralıklarının listesi.</span><span class="sxs-lookup"><span data-stu-id="53228-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="53228-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="53228-124">-MaxReturn</span></span>
<span data-ttu-id="53228-125">Birden çok değerli yönlendirme yöntemiyle profillerin döndürdüğü en fazla yanıt sayısı.</span><span class="sxs-lookup"><span data-stu-id="53228-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="53228-126">-Monitorıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="53228-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="53228-127">Traffic Manager 'ın Bu profildeki her uç noktanın durumunu denetlemesi gereken zaman aralığı (saniye cinsinden).</span><span class="sxs-lookup"><span data-stu-id="53228-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="53228-128">Varsayılan değer 30 ' dır.</span><span class="sxs-lookup"><span data-stu-id="53228-128">The default is 30.</span></span>

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

### <span data-ttu-id="53228-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="53228-129">-MonitorPath</span></span>
<span data-ttu-id="53228-130">Uç nokta durumunu izlemek için kullanılan yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="53228-131">Uç nokta etki alanı adıyla ilişkili bir değer belirtin.</span><span class="sxs-lookup"><span data-stu-id="53228-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="53228-132">Bu değer eğik çizgiyle (/) başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="53228-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="53228-133">-Monitorın bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="53228-133">-MonitorPort</span></span>
<span data-ttu-id="53228-134">Uç nokta durumunu izlemek için kullanılan TCP bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="53228-135">Geçerli değerler 1 ile 65535 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="53228-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="53228-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="53228-136">-MonitorProtocol</span></span>
<span data-ttu-id="53228-137">Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="53228-138">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="53228-138">Valid values are:</span></span>

- <span data-ttu-id="53228-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="53228-139">HTTP</span></span>
- <span data-ttu-id="53228-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="53228-140">HTTPS</span></span>

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

### <span data-ttu-id="53228-141">-Monitortimeout Inseconds</span><span class="sxs-lookup"><span data-stu-id="53228-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="53228-142">Traffic Manager 'ın Bu profildeki uç noktaların sistem durumu denetimini yanıtlamasını sağlayan süre (saniye).</span><span class="sxs-lookup"><span data-stu-id="53228-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="53228-143">Varsayılan 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="53228-143">The default is 10.</span></span>

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

### <span data-ttu-id="53228-144">-Monitortoleranda Başarısızlıksayısı</span><span class="sxs-lookup"><span data-stu-id="53228-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="53228-145">Sonraki ardışık başarısız durum denetiminin ardından, bu profildeki bir uç noktanın düşürülmeden önce, Trafik Yöneticisi toleransındaki ardışık başarısız durumu denetler.</span><span class="sxs-lookup"><span data-stu-id="53228-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="53228-146">Varsayılan 3 ' dir.</span><span class="sxs-lookup"><span data-stu-id="53228-146">The default is 3.</span></span>

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

### <span data-ttu-id="53228-147">-Ad</span><span class="sxs-lookup"><span data-stu-id="53228-147">-Name</span></span>
<span data-ttu-id="53228-148">Bu cmdlet 'in oluşturduğu Traffic Manager profili için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="53228-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="53228-149">-ProfileStatus</span></span>
<span data-ttu-id="53228-150">Profilin durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="53228-151">Geçerli değerler: etkin ve devre dışı.</span><span class="sxs-lookup"><span data-stu-id="53228-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="53228-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="53228-152">-RelativeDnsName</span></span>
<span data-ttu-id="53228-153">Bu Traffic Manager profilinin sağladığı göreli DNS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="53228-154">Traffic Manager bu değeri ve Azure Traffic Manager 'ın profilin tam etki alanı adını (FQDN) oluşturmak için kullandığı DNS etki alanı adını birleştirir.</span><span class="sxs-lookup"><span data-stu-id="53228-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="53228-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53228-155">-ResourceGroupName</span></span>
<span data-ttu-id="53228-156">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="53228-157">Bu cmdlet, bu parametrenin belirttiği grupta bir Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="53228-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="53228-158">Etiketli</span><span class="sxs-lookup"><span data-stu-id="53228-158">-Tag</span></span>
<span data-ttu-id="53228-159">Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="53228-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="53228-160">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="53228-160">For example:</span></span>

<span data-ttu-id="53228-161">@ {Key0 = "value0"; anahtar = $null; anahtar2 = "değer2"}</span><span class="sxs-lookup"><span data-stu-id="53228-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="53228-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="53228-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="53228-163">Trafik yönlendirme yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="53228-164">Bu yöntem, gelen DNS sorgularına yanıt olarak hangi Endpoint Traffic Manager 'ın geri döndüğü belirlenir.</span><span class="sxs-lookup"><span data-stu-id="53228-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="53228-165">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="53228-165">Valid values are:</span></span>

- <span data-ttu-id="53228-166">Performans</span><span class="sxs-lookup"><span data-stu-id="53228-166">Performance</span></span>
- <span data-ttu-id="53228-167">Ağırlıklı</span><span class="sxs-lookup"><span data-stu-id="53228-167">Weighted</span></span>
- <span data-ttu-id="53228-168">Öncelik</span><span class="sxs-lookup"><span data-stu-id="53228-168">Priority</span></span>
- <span data-ttu-id="53228-169">Coğrafya</span><span class="sxs-lookup"><span data-stu-id="53228-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53228-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="53228-170">-Ttl</span></span>
<span data-ttu-id="53228-171">Yaşam süresi (TTL) değerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="53228-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="53228-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53228-172">CommonParameters</span></span>
<span data-ttu-id="53228-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="53228-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53228-174">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53228-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53228-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="53228-175">INPUTS</span></span>

### <span data-ttu-id="53228-176">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="53228-176">None</span></span>

## <span data-ttu-id="53228-177">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="53228-177">OUTPUTS</span></span>

### <span data-ttu-id="53228-178">Microsoft. Azure. Commands. TrafficManager. modeller. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53228-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="53228-179">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="53228-179">NOTES</span></span>

## <span data-ttu-id="53228-180">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="53228-180">RELATED LINKS</span></span>

[<span data-ttu-id="53228-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="53228-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="53228-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53228-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="53228-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53228-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="53228-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53228-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="53228-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53228-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="53228-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="53228-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


