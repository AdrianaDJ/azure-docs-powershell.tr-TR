---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1BA472FB-E684-486C-8066-42C9215DBDEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 83d1afcae66af7e4548b1dbd4031392969f4d267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106057"
---
# <span data-ttu-id="9c0a4-101">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c0a4-101">Set-AzureEndpoint</span></span>

## <span data-ttu-id="9c0a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0a4-103">Bir sanal makineye atanan uç noktayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-103">Modifies an endpoint assigned to a virtual machine.</span></span>

## <span data-ttu-id="9c0a4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c0a4-104">SYNTAX</span></span>

```
Set-AzureEndpoint [-Name] <String> [[-Protocol] <String>] [[-LocalPort] <Int32>] [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9c0a4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c0a4-105">DESCRIPTION</span></span>
<span data-ttu-id="9c0a4-106">**Set-AzureEndpoint** cmdlet 'ı bir Azure sanal makinesine atanmış uç noktayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-106">The **Set-AzureEndpoint** cmdlet modifies an endpoint assigned to an Azure virtual machine.</span></span>
<span data-ttu-id="9c0a4-107">Yük dengeli olmayan bir son noktadaki değişikliklerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-107">You can specify changes to an endpoint that is not load balanced.</span></span>

## <span data-ttu-id="9c0a4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c0a4-108">EXAMPLES</span></span>

### <span data-ttu-id="9c0a4-109">Örnek 1: bir bağlantı noktasını dinlemek için uç noktayı değiştirme</span><span class="sxs-lookup"><span data-stu-id="9c0a4-109">Example 1: Modify an endpoint to listen on a port</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Set-AzureEndpoint -Name "Web" -PublicPort 443 -LocalPort 443 -Protocol tcp | Update-AzureVM
```

<span data-ttu-id="9c0a4-110">Bu komut, **Get-AzureVM** cmdlet 'Ini kullanarak VirtualMachine01 adındaki sanal makinenin yapılandırmasını alır.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-110">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="9c0a4-111">Komut, ardışık düzen işlecini kullanarak bunu geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-111">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9c0a4-112">Bu cmdlet, bağlantı noktası 443 ' i dinlemek için Web adındaki uç noktayı değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-112">This cmdlet modifies the endpoint named Web to listen on port 443.</span></span>
<span data-ttu-id="9c0a4-113">Komut, sanal makine nesnesini, değişikliklerinizi uygulayan **Update-AzureVM** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-113">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="9c0a4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c0a4-114">PARAMETERS</span></span>

### <span data-ttu-id="9c0a4-115">-ACL</span><span class="sxs-lookup"><span data-stu-id="9c0a4-115">-ACL</span></span>
<span data-ttu-id="9c0a4-116">Bu cmdlet 'in uç noktaya uyguladığı bir erişim denetim listesi (ACL) yapılandırma nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-116">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoint.</span></span>

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

### <span data-ttu-id="9c0a4-117">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="9c0a4-117">-DirectServerReturn</span></span>
<span data-ttu-id="9c0a4-118">Bu cmdlet 'in doğrudan sunucu döndürülmesini etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-118">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="9c0a4-119">Etkinleştirmek için $True veya devre dışı bırakmak için $False belirtin.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-119">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="9c0a4-120">-Idfaizzamansayısı</span><span class="sxs-lookup"><span data-stu-id="9c0a4-120">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="9c0a4-121">Uç noktanın TCP boşta kalma zaman aşımı süresini dakika olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-121">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="9c0a4-122">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9c0a4-122">-InformationAction</span></span>
<span data-ttu-id="9c0a4-123">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9c0a4-124">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9c0a4-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c0a4-125">'A</span><span class="sxs-lookup"><span data-stu-id="9c0a4-125">Continue</span></span>
- <span data-ttu-id="9c0a4-126">Manıza</span><span class="sxs-lookup"><span data-stu-id="9c0a4-126">Ignore</span></span>
- <span data-ttu-id="9c0a4-127">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="9c0a4-127">Inquire</span></span>
- <span data-ttu-id="9c0a4-128">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="9c0a4-128">SilentlyContinue</span></span>
- <span data-ttu-id="9c0a4-129">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="9c0a4-129">Stop</span></span>
- <span data-ttu-id="9c0a4-130">Biliriz</span><span class="sxs-lookup"><span data-stu-id="9c0a4-130">Suspend</span></span>

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

### <span data-ttu-id="9c0a4-131">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="9c0a4-131">-InformationVariable</span></span>
<span data-ttu-id="9c0a4-132">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9c0a4-133">-Internalloadbalancername</span><span class="sxs-lookup"><span data-stu-id="9c0a4-133">-InternalLoadBalancerName</span></span>
<span data-ttu-id="9c0a4-134">İç yük dengeleyicinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-134">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="9c0a4-135">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="9c0a4-135">-LoadBalancerDistribution</span></span>
<span data-ttu-id="9c0a4-136">Yük dengeleyici dağıtım algoritmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-136">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="9c0a4-137">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9c0a4-137">Valid values are:</span></span> 

- <span data-ttu-id="9c0a4-138">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-138">sourceIP.</span></span>
<span data-ttu-id="9c0a4-139">İki demet benzeşim: kaynak IP, hedef IP</span><span class="sxs-lookup"><span data-stu-id="9c0a4-139">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="9c0a4-140">Sourceıpprotocol.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-140">sourceIPProtocol.</span></span>
<span data-ttu-id="9c0a4-141">Üç demet benzeşim: kaynak IP, hedef IP, protokol</span><span class="sxs-lookup"><span data-stu-id="9c0a4-141">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="9c0a4-142">yabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-142">none.</span></span>
<span data-ttu-id="9c0a4-143">Beş demet benzeşim: kaynak IP, kaynak bağlantı noktası, hedef IP, hedef bağlantı noktası Protokolü</span><span class="sxs-lookup"><span data-stu-id="9c0a4-143">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="9c0a4-144">Varsayılan değer yok 'tur.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-144">The default value is none.</span></span>

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

### <span data-ttu-id="9c0a4-145">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="9c0a4-145">-LocalPort</span></span>
<span data-ttu-id="9c0a4-146">Bu uç noktanın kullandığı yerel, özel bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-146">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="9c0a4-147">Sanal makinedeki uygulamalar bu bağlantı noktasında bu uç nokta için hizmet giriş isteklerini dinler.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-147">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c0a4-148">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c0a4-148">-Name</span></span>
<span data-ttu-id="9c0a4-149">Uç noktasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-149">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="9c0a4-150">-Profil</span><span class="sxs-lookup"><span data-stu-id="9c0a4-150">-Profile</span></span>
<span data-ttu-id="9c0a4-151">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c0a4-152">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c0a4-153">-İletişim kuralı</span><span class="sxs-lookup"><span data-stu-id="9c0a4-153">-Protocol</span></span>
<span data-ttu-id="9c0a4-154">Uç noktasının protokolünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-154">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="9c0a4-155">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="9c0a4-155">Valid values are:</span></span> 

- <span data-ttu-id="9c0a4-156">TC</span><span class="sxs-lookup"><span data-stu-id="9c0a4-156">tcp</span></span> 
- <span data-ttu-id="9c0a4-157">UDP</span><span class="sxs-lookup"><span data-stu-id="9c0a4-157">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c0a4-158">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="9c0a4-158">-PublicPort</span></span>
<span data-ttu-id="9c0a4-159">Uç noktanın kullandığı ortak bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-159">Specifies the public port that the endpoint uses.</span></span>

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

### <span data-ttu-id="9c0a4-160">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="9c0a4-160">-VirtualIPName</span></span>
<span data-ttu-id="9c0a4-161">Azure 'un uç noktayla ilişki kurduğu sanal IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-161">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="9c0a4-162">Hizmetiniz birden çok sanal IP 'ye sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-162">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="9c0a4-163">Sanal IP 'Ler oluşturmak için **Add-AzureVirtualIP** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-163">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="9c0a4-164">-VM</span><span class="sxs-lookup"><span data-stu-id="9c0a4-164">-VM</span></span>
<span data-ttu-id="9c0a4-165">Uç noktanın ait olduğu sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-165">Specifies the virtual machine to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="9c0a4-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0a4-166">CommonParameters</span></span>
<span data-ttu-id="9c0a4-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c0a4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0a4-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c0a4-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0a4-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c0a4-169">INPUTS</span></span>

## <span data-ttu-id="9c0a4-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c0a4-170">OUTPUTS</span></span>

### <span data-ttu-id="9c0a4-171">System. Object</span><span class="sxs-lookup"><span data-stu-id="9c0a4-171">System.Object</span></span>

## <span data-ttu-id="9c0a4-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c0a4-172">NOTES</span></span>

## <span data-ttu-id="9c0a4-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c0a4-173">RELATED LINKS</span></span>

[<span data-ttu-id="9c0a4-174">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c0a4-174">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="9c0a4-175">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="9c0a4-175">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="9c0a4-176">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c0a4-176">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="9c0a4-177">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9c0a4-177">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="9c0a4-178">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c0a4-178">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="9c0a4-179">Güncelleştirme-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9c0a4-179">Update-AzureVM</span></span>](./Update-AzureVM.md)


