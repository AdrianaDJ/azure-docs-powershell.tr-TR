---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106202"
---
# <span data-ttu-id="f8f55-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8f55-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="f8f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8f55-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f55-103">Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8f55-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="f8f55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8f55-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f8f55-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8f55-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f55-106">**New-AzureTrafficManagerProfile** cmdlet 'ı bir Microsoft Azure Traffic Manager profili oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8f55-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="f8f55-107">*LoadBalancingMethod* değerini "yük devretme" olarak ayarladığınız bir profili oluşturduktan sonra, Add-AzureTrafficManagerEndpoint cmdlet 'i kullanarak profilinize eklediğiniz uç noktaların yük devretme sırasını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8f55-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="f8f55-108">Daha fazla bilgi için aşağıdaki örnek 2 bölümüne bakın.</span><span class="sxs-lookup"><span data-stu-id="f8f55-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="f8f55-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8f55-109">EXAMPLES</span></span>

### <span data-ttu-id="f8f55-110">Örnek 1: Traffic Manager profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="f8f55-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="f8f55-111">Bu komut, belirtilen Traffic Manager etki alanında Myprofıle adlı bir Traffic Manager profili, bir deneme yük dengelemesi yöntemi, 30 saniyelik TTL, HTTP izleme protokolü, izleme bağlantı noktası 80 ve belirtilen yol ile birlikte oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8f55-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="f8f55-112">Örnek 2: uç noktaları istenen yük devretme sırasına yeniden sıralama</span><span class="sxs-lookup"><span data-stu-id="f8f55-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="f8f55-113">Bu örnek MyProfile 'e eklenecek uç noktaları istenen yük devretme siparişine yeniden sıralar.</span><span class="sxs-lookup"><span data-stu-id="f8f55-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="f8f55-114">İlk komut Myprofıle adlı Traffic Manager profil nesnesini alır ve nesneyi $Profile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="f8f55-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="f8f55-115">İkinci komut uç noktaları dizisindeki uç noktaları, yerine çalışma yerine gerçekleşecek şekilde yeniden sıralar.</span><span class="sxs-lookup"><span data-stu-id="f8f55-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="f8f55-116">Son komut $Profile uygulamasında depolanan Traffic Manager profilini yeni son nokta siparişiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="f8f55-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8f55-117">PARAMETERS</span></span>

### <span data-ttu-id="f8f55-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="f8f55-118">-DomainName</span></span>
<span data-ttu-id="f8f55-119">Traffic Manager profilinin etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="f8f55-120">Trafficmanager.net 'in alt etki alanı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f8f55-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="f8f55-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="f8f55-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="f8f55-122">Bağlantıyı dağıtmak için kullanılacak yük dengeleme yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="f8f55-123">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f8f55-123">Valid values are:</span></span> 

- <span data-ttu-id="f8f55-124">Performans</span><span class="sxs-lookup"><span data-stu-id="f8f55-124">Performance</span></span>
- <span data-ttu-id="f8f55-125">Devretmesini</span><span class="sxs-lookup"><span data-stu-id="f8f55-125">Failover</span></span>
- <span data-ttu-id="f8f55-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="f8f55-126">RoundRobin</span></span>

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

### <span data-ttu-id="f8f55-127">-Monitorın bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="f8f55-127">-MonitorPort</span></span>
<span data-ttu-id="f8f55-128">Uç nokta durumunu izlemek için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="f8f55-129">Geçerli değerler, 0 ' dan büyük ve 65.535 'ten küçük tamsayı değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="f8f55-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="f8f55-130">-MonitorProtocol</span></span>
<span data-ttu-id="f8f55-131">Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="f8f55-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="f8f55-132">Valid values are:</span></span> 

- <span data-ttu-id="f8f55-133">Http</span><span class="sxs-lookup"><span data-stu-id="f8f55-133">Http</span></span>

- <span data-ttu-id="f8f55-134">Https</span><span class="sxs-lookup"><span data-stu-id="f8f55-134">Https</span></span>

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

### <span data-ttu-id="f8f55-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="f8f55-135">-MonitorRelativePath</span></span>
<span data-ttu-id="f8f55-136">Sistem durumu için araştırma yapılacak uç nokta etki alanı adına göre yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="f8f55-137">Yol aşağıdaki kısıtlamalara uymalıdır:</span><span class="sxs-lookup"><span data-stu-id="f8f55-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="f8f55-138">Yol 1 ila 1000 karakter arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f8f55-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="f8f55-139">Eğik çizgiyle başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="f8f55-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="f8f55-140">XML öğeleri içermemesi gerekir \<\> .</span><span class="sxs-lookup"><span data-stu-id="f8f55-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="f8f55-141">Çift eğik çizgi içermemelidir,//.</span><span class="sxs-lookup"><span data-stu-id="f8f55-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="f8f55-142">Geçersiz HTML kaçış karakterleri içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="f8f55-143">Örneğin,% XY.</span><span class="sxs-lookup"><span data-stu-id="f8f55-143">For example, %XY.</span></span>

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

### <span data-ttu-id="f8f55-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="f8f55-144">-Name</span></span>
<span data-ttu-id="f8f55-145">Oluşturulacak Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f55-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="f8f55-146">-Profile</span></span>
<span data-ttu-id="f8f55-147">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f8f55-148">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f8f55-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f8f55-149">-TTL</span><span class="sxs-lookup"><span data-stu-id="f8f55-149">-Ttl</span></span>
<span data-ttu-id="f8f55-150">Yerel DNS çözümleyicilerine DNS girişlerini önbelleğe alma süresini bildiren DNS yaşam süresini (TTL) belirtir.</span><span class="sxs-lookup"><span data-stu-id="f8f55-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="f8f55-151">Geçerli değerler 30 ile 999.999 arasındaki tamsayılardır.</span><span class="sxs-lookup"><span data-stu-id="f8f55-151">Valid values are integers from 30 through 999,999.</span></span>

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

### <span data-ttu-id="f8f55-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f55-152">CommonParameters</span></span>
<span data-ttu-id="f8f55-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8f55-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f55-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f55-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f55-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8f55-155">INPUTS</span></span>

## <span data-ttu-id="f8f55-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8f55-156">OUTPUTS</span></span>

### <span data-ttu-id="f8f55-157">Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition</span><span class="sxs-lookup"><span data-stu-id="f8f55-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="f8f55-158">Bu cmdlet, bir Traffic Manager profil nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8f55-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="f8f55-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8f55-159">NOTES</span></span>

## <span data-ttu-id="f8f55-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8f55-160">RELATED LINKS</span></span>

[<span data-ttu-id="f8f55-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8f55-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f8f55-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8f55-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f8f55-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8f55-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f8f55-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8f55-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f8f55-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8f55-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


