---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105733"
---
# <span data-ttu-id="ec1f5-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec1f5-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="ec1f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec1f5-103">Sanal makineye uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="ec1f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec1f5-104">SYNTAX</span></span>

### <span data-ttu-id="ec1f5-105">NoLB (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec1f5-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ec1f5-106">Lbnoaraştırması</span><span class="sxs-lookup"><span data-stu-id="ec1f5-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ec1f5-107">Lbdefaultaraştırması</span><span class="sxs-lookup"><span data-stu-id="ec1f5-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ec1f5-108">Lbcustomaraştırması</span><span class="sxs-lookup"><span data-stu-id="ec1f5-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ec1f5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec1f5-109">DESCRIPTION</span></span>
<span data-ttu-id="ec1f5-110">**Add-AzureEndpoint** cmdlet 'ı bir Azure sanal makine nesnesine uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="ec1f5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec1f5-111">EXAMPLES</span></span>

### <span data-ttu-id="ec1f5-112">Örnek 1: uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="ec1f5-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="ec1f5-113">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak VirtualMachine01 adındaki sanal makinenin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ec1f5-114">Komut, ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ec1f5-115">Bu cmdlet, HttpIn adlı bir uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="ec1f5-116">Uç noktada 80 ve yerel bağlantı noktası 8080 ortak bağlantı noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="ec1f5-117">Komut, sanal makine nesnesini, değişikliklerinizi uygulayan **Update-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="ec1f5-118">Örnek 2: yük dengeli bir gruba ait olan bir uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="ec1f5-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="ec1f5-119">Bu komut, VirtualMachine07 adındaki bir sanal makinenin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="ec1f5-120">Current cmdlet 'i HttpIn adlı bir uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="ec1f5-121">Uç noktada 80 ve yerel bağlantı noktası 8080 ortak bağlantı noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="ec1f5-122">Uç nokta, Web grubu adlı paylaşılan yük dengeli grubuna aittir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="ec1f5-123">'/' Yolunun bulunduğu bağlantı noktası 80 üzerinde bir HTTP araştırması uç noktanın kullanılabilirliğini izler.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="ec1f5-124">Komut değişikliklerinizi uygular.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-124">The command implements your changes.</span></span>

### <span data-ttu-id="ec1f5-125">Örnek 3: sanal IP 'yi uç noktayla Ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="ec1f5-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="ec1f5-126">Bu komut, VirtualMachine25 adındaki bir sanal makinenin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="ec1f5-127">Current cmdlet 'i HttpIn adlı bir uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="ec1f5-128">Uç noktada 80 ve yerel bağlantı noktası 8080 ortak bağlantı noktası vardır.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="ec1f5-129">Bu komut sanal IP 'yi uç noktayla ilişkilendirir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="ec1f5-130">Komut değişikliklerinizi uygular.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-130">The command implements your changes.</span></span>

## <span data-ttu-id="ec1f5-131">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec1f5-131">PARAMETERS</span></span>

### <span data-ttu-id="ec1f5-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="ec1f5-132">-ACL</span></span>
<span data-ttu-id="ec1f5-133">Uç nokta için bir erişim denetim listesi (ACL) yapılandırma nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="ec1f5-134">-Defaultaraştırması</span><span class="sxs-lookup"><span data-stu-id="ec1f5-134">-DefaultProbe</span></span>
<span data-ttu-id="ec1f5-135">Bu cmdlet 'in varsayılan yoklama ayarını kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="ec1f5-136">-DirectServerReturn</span></span>
<span data-ttu-id="ec1f5-137">Bu cmdlet 'in doğrudan sunucu döndürülmesini etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="ec1f5-138">Etkinleştirmek için $True veya devre dışı bırakmak için $False belirtin.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="ec1f5-139">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="ec1f5-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ec1f5-140">Uç noktanın TCP boşta kalma zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="ec1f5-141">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ec1f5-141">-InformationAction</span></span>
<span data-ttu-id="ec1f5-142">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ec1f5-143">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="ec1f5-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ec1f5-144">'A</span><span class="sxs-lookup"><span data-stu-id="ec1f5-144">Continue</span></span>
- <span data-ttu-id="ec1f5-145">Manıza</span><span class="sxs-lookup"><span data-stu-id="ec1f5-145">Ignore</span></span>
- <span data-ttu-id="ec1f5-146">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="ec1f5-146">Inquire</span></span>
- <span data-ttu-id="ec1f5-147">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="ec1f5-147">SilentlyContinue</span></span>
- <span data-ttu-id="ec1f5-148">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="ec1f5-148">Stop</span></span>
- <span data-ttu-id="ec1f5-149">Biliriz</span><span class="sxs-lookup"><span data-stu-id="ec1f5-149">Suspend</span></span>

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

### <span data-ttu-id="ec1f5-150">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="ec1f5-150">-InformationVariable</span></span>
<span data-ttu-id="ec1f5-151">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ec1f5-152">-Internalloadbalancername</span><span class="sxs-lookup"><span data-stu-id="ec1f5-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="ec1f5-153">İç yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="ec1f5-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="ec1f5-154">-LBSetName</span></span>
<span data-ttu-id="ec1f5-155">Uç nokta için ayarlanan yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="ec1f5-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="ec1f5-157">Yük dengeleyici dağıtım algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="ec1f5-158">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ec1f5-158">Valid values are:</span></span> 

- <span data-ttu-id="ec1f5-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-159">sourceIP.</span></span>
<span data-ttu-id="ec1f5-160">İki demet benzeşim: kaynak IP, hedef IP</span><span class="sxs-lookup"><span data-stu-id="ec1f5-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="ec1f5-161">Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-161">sourceIPProtocol.</span></span>
<span data-ttu-id="ec1f5-162">Üç demet benzeşim: kaynak IP, hedef IP, protokol</span><span class="sxs-lookup"><span data-stu-id="ec1f5-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="ec1f5-163">yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-163">none.</span></span>
<span data-ttu-id="ec1f5-164">Beş demet benzeşim: kaynak IP, kaynak bağlantı noktası, hedef IP, hedef bağlantı noktası Protokolü</span><span class="sxs-lookup"><span data-stu-id="ec1f5-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="ec1f5-165">Varsayılan değer yok 'tur.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-165">The default value is none.</span></span>

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

### <span data-ttu-id="ec1f5-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="ec1f5-166">-LocalPort</span></span>
<span data-ttu-id="ec1f5-167">Bu uç noktanın kullandığı yerel, özel bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="ec1f5-168">Sanal makinedeki uygulamalar bu bağlantı noktasında bu uç nokta için hizmet giriş isteklerini dinler.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-169">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec1f5-169">-Name</span></span>
<span data-ttu-id="ec1f5-170">Uç nokta için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-171">-Noaraştırması</span><span class="sxs-lookup"><span data-stu-id="ec1f5-171">-NoProbe</span></span>
<span data-ttu-id="ec1f5-172">Bu cmdlet 'in yoklama ayarını kullanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-173">-Probeıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="ec1f5-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="ec1f5-174">Uç nokta için yoklama yoklama aralığını saniye cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="ec1f5-175">-ProbePath</span></span>
<span data-ttu-id="ec1f5-176">HTTP araştırmasının göreli yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="ec1f5-177">-ProbePort</span></span>
<span data-ttu-id="ec1f5-178">Uç noktanın kullandığı bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="ec1f5-179">-ProbeProtocol</span></span>
<span data-ttu-id="ec1f5-180">Bağlantı noktası protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-180">Specifies the port protocol.</span></span>
<span data-ttu-id="ec1f5-181">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ec1f5-181">Valid values are:</span></span> 

- <span data-ttu-id="ec1f5-182">TC</span><span class="sxs-lookup"><span data-stu-id="ec1f5-182">tcp</span></span> 
- <span data-ttu-id="ec1f5-183">http</span><span class="sxs-lookup"><span data-stu-id="ec1f5-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-184">-Probetimeoutınseconds</span><span class="sxs-lookup"><span data-stu-id="ec1f5-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="ec1f5-185">Saniye cinsinden yoklama yoklama zaman aşımını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-186">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec1f5-186">-Profile</span></span>
<span data-ttu-id="ec1f5-187">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec1f5-188">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec1f5-189">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="ec1f5-189">-Protocol</span></span>
<span data-ttu-id="ec1f5-190">Uç noktasının protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="ec1f5-191">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="ec1f5-191">Valid values are:</span></span> 

- <span data-ttu-id="ec1f5-192">TC</span><span class="sxs-lookup"><span data-stu-id="ec1f5-192">tcp</span></span> 
- <span data-ttu-id="ec1f5-193">UDP</span><span class="sxs-lookup"><span data-stu-id="ec1f5-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="ec1f5-194">-PublicPort</span></span>
<span data-ttu-id="ec1f5-195">Uç noktanın kullandığı ortak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="ec1f5-196">Bir değer belirtmezseniz, Azure kullanılabilir bir bağlantı noktası atar.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="ec1f5-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="ec1f5-197">-VirtualIPName</span></span>
<span data-ttu-id="ec1f5-198">Azure 'un uç noktayla ilişki kurduğu sanal IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="ec1f5-199">Hizmetiniz birden çok sanal IP 'ye sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="ec1f5-200">Sanal IP 'Ler oluşturmak için **Add-AzureVirtualIP** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="ec1f5-201">-VM</span><span class="sxs-lookup"><span data-stu-id="ec1f5-201">-VM</span></span>
<span data-ttu-id="ec1f5-202">Uç noktanın ait olduğu sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec1f5-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec1f5-203">CommonParameters</span></span>
<span data-ttu-id="ec1f5-204">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec1f5-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec1f5-205">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec1f5-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec1f5-206">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec1f5-206">INPUTS</span></span>

## <span data-ttu-id="ec1f5-207">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec1f5-207">OUTPUTS</span></span>

### <span data-ttu-id="ec1f5-208">System. Object</span><span class="sxs-lookup"><span data-stu-id="ec1f5-208">System.Object</span></span>

## <span data-ttu-id="ec1f5-209">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec1f5-209">NOTES</span></span>

## <span data-ttu-id="ec1f5-210">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec1f5-210">RELATED LINKS</span></span>

[<span data-ttu-id="ec1f5-211">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="ec1f5-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="ec1f5-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec1f5-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="ec1f5-213">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ec1f5-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ec1f5-214">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec1f5-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="ec1f5-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="ec1f5-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="ec1f5-216">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ec1f5-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


