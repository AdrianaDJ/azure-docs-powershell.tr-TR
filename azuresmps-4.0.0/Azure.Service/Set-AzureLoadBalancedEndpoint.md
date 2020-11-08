---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105953"
---
# <span data-ttu-id="17ca2-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="17ca2-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="17ca2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="17ca2-103">Bir Azure hizmeti içinde ayarlanan bir yük dengeleyicinin tüm uç noktalarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="17ca2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17ca2-104">SYNTAX</span></span>

### <span data-ttu-id="17ca2-105">Defaultaraştırması (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17ca2-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="17ca2-106">Tcparaştırması</span><span class="sxs-lookup"><span data-stu-id="17ca2-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="17ca2-107">Httparaştırması</span><span class="sxs-lookup"><span data-stu-id="17ca2-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="17ca2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17ca2-108">DESCRIPTION</span></span>
<span data-ttu-id="17ca2-109">**Set-AzureLoadBalancedEndpoint** cmdlet 'i, bir Azure hizmetinde ayarlanan bir yük dengeleyicinin tüm uç noktalarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="17ca2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17ca2-110">EXAMPLES</span></span>

### <span data-ttu-id="17ca2-111">Örnek 1: yük dengeleyici kümesindeki uç noktaları değiştirme</span><span class="sxs-lookup"><span data-stu-id="17ca2-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="17ca2-112">Bu komut, LBSet01 adlı yük dengeleyici kümesindeki tüm uç noktaları, TCP protokolünü ve özel bağlantı noktası 80 kullanacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="17ca2-113">Komut yük dengeleyici araştırın bağlantı noktası 8080 ' te TCP protokolünü kullanacak şekilde ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="17ca2-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="17ca2-114">Örnek 2: farklı bir sanal IP belirtme</span><span class="sxs-lookup"><span data-stu-id="17ca2-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="17ca2-115">Bu komut, yük dengeleyici kümesi adı olan yük dengeleyicın Vip01 adlı sanal bir IP 'yi kullanacak şekilde değiştirir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="17ca2-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17ca2-116">PARAMETERS</span></span>

### <span data-ttu-id="17ca2-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="17ca2-117">-ACL</span></span>
<span data-ttu-id="17ca2-118">Bu cmdlet 'in uç noktalara uyguladığı erişim denetim listesi (ACL) yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="17ca2-119">-DirectServerReturn</span></span>
<span data-ttu-id="17ca2-120">Bu cmdlet 'in doğrudan sunucu döndürülmesini etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="17ca2-121">Etkinleştirmek için $True veya devre dışı bırakmak için $False belirtin.</span><span class="sxs-lookup"><span data-stu-id="17ca2-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-122">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="17ca2-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="17ca2-123">Uç noktalar için dakika cinsinden TCP boşta kalma zaman aşımı süresini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

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

### <span data-ttu-id="17ca2-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="17ca2-124">-InformationAction</span></span>
<span data-ttu-id="17ca2-125">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="17ca2-126">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="17ca2-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="17ca2-127">'A</span><span class="sxs-lookup"><span data-stu-id="17ca2-127">Continue</span></span>
- <span data-ttu-id="17ca2-128">Manıza</span><span class="sxs-lookup"><span data-stu-id="17ca2-128">Ignore</span></span>
- <span data-ttu-id="17ca2-129">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="17ca2-129">Inquire</span></span>
- <span data-ttu-id="17ca2-130">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="17ca2-130">SilentlyContinue</span></span>
- <span data-ttu-id="17ca2-131">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="17ca2-131">Stop</span></span>
- <span data-ttu-id="17ca2-132">Biliriz</span><span class="sxs-lookup"><span data-stu-id="17ca2-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-133">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="17ca2-133">-InformationVariable</span></span>
<span data-ttu-id="17ca2-134">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-135">-Internalloadbalancername</span><span class="sxs-lookup"><span data-stu-id="17ca2-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="17ca2-136">Bu cmdlet 'in yapılandırmada eklediği iç yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="17ca2-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="17ca2-137">-LBSetName</span></span>
<span data-ttu-id="17ca2-138">Bu cmdlet 'in güncelleştirdiği yük dengeleyici kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="17ca2-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="17ca2-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="17ca2-140">Yük dengeleyici dağıtım algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="17ca2-141">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="17ca2-141">Valid values are:</span></span> 

- <span data-ttu-id="17ca2-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="17ca2-142">sourceIP.</span></span>
<span data-ttu-id="17ca2-143">İki demet benzeşim: kaynak IP, hedef IP</span><span class="sxs-lookup"><span data-stu-id="17ca2-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="17ca2-144">Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="17ca2-144">sourceIPProtocol.</span></span>
<span data-ttu-id="17ca2-145">Üç demet benzeşim: kaynak IP, hedef IP, protokol</span><span class="sxs-lookup"><span data-stu-id="17ca2-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="17ca2-146">yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17ca2-146">none.</span></span>
<span data-ttu-id="17ca2-147">Beş demet benzeşim: kaynak IP, kaynak bağlantı noktası, hedef IP, hedef bağlantı noktası Protokolü</span><span class="sxs-lookup"><span data-stu-id="17ca2-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="17ca2-148">Varsayılan değer yok 'tur.</span><span class="sxs-lookup"><span data-stu-id="17ca2-148">The default value is none.</span></span>

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

### <span data-ttu-id="17ca2-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="17ca2-149">-LocalPort</span></span>
<span data-ttu-id="17ca2-150">Bu uç noktaların kullandığı yerel, özel ve bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="17ca2-151">Sanal makinedeki uygulamalar bu uç noktada hizmet giriş isteklerini dinler.</span><span class="sxs-lookup"><span data-stu-id="17ca2-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

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

### <span data-ttu-id="17ca2-152">-Probeıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="17ca2-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="17ca2-153">Uç noktalar için saniye cinsinden yoklama yoklama aralığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="17ca2-154">-ProbePath</span></span>
<span data-ttu-id="17ca2-155">HTTP araştırın göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="17ca2-156">-ProbePort</span></span>
<span data-ttu-id="17ca2-157">Yük dengeleyici araştırın kullandığı bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="17ca2-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="17ca2-159">Yük dengeleyici uç noktalarının bir HTTP araştırması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="17ca2-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="17ca2-161">Yük dengeleyici uç noktalarının bir TCP araştırması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-162">-Probetimeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="17ca2-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="17ca2-163">Saniye cinsinden yoklama yoklama zaman aşımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-164">-Profil</span><span class="sxs-lookup"><span data-stu-id="17ca2-164">-Profile</span></span>
<span data-ttu-id="17ca2-165">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="17ca2-166">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="17ca2-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-167">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="17ca2-167">-Protocol</span></span>
<span data-ttu-id="17ca2-168">Uç noktaların protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="17ca2-169">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="17ca2-169">Valid values are:</span></span> 

- <span data-ttu-id="17ca2-170">TC</span><span class="sxs-lookup"><span data-stu-id="17ca2-170">TCP</span></span> 
- <span data-ttu-id="17ca2-171">UDP</span><span class="sxs-lookup"><span data-stu-id="17ca2-171">UDP</span></span>

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

### <span data-ttu-id="17ca2-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="17ca2-172">-PublicPort</span></span>
<span data-ttu-id="17ca2-173">Uç noktanın kullandığı ortak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="17ca2-174">Bir değer belirtmezseniz, Azure kullanılabilir bir bağlantı noktası atar.</span><span class="sxs-lookup"><span data-stu-id="17ca2-174">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="17ca2-175">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="17ca2-175">-ServiceName</span></span>
<span data-ttu-id="17ca2-176">Bu cmdlet 'in değiştirdiği uç noktaları içeren Azure hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ca2-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="17ca2-177">-VirtualIPName</span></span>
<span data-ttu-id="17ca2-178">Azure 'un uç noktalara ilişki kurduğu sanal IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17ca2-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="17ca2-179">Hizmetinize sanal IP 'Ler eklemek için **Add-AzureVirtualIP** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="17ca2-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="17ca2-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ca2-180">CommonParameters</span></span>
<span data-ttu-id="17ca2-181">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17ca2-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ca2-182">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17ca2-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ca2-183">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17ca2-183">INPUTS</span></span>

## <span data-ttu-id="17ca2-184">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17ca2-184">OUTPUTS</span></span>

## <span data-ttu-id="17ca2-185">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17ca2-185">NOTES</span></span>

## <span data-ttu-id="17ca2-186">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17ca2-186">RELATED LINKS</span></span>

[<span data-ttu-id="17ca2-187">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="17ca2-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="17ca2-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="17ca2-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


