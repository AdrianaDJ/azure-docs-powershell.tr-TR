---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105794"
---
# <span data-ttu-id="526ab-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="526ab-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="526ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="526ab-102">SYNOPSIS</span></span>
<span data-ttu-id="526ab-103">Traffic Manager profilinin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="526ab-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="526ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="526ab-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="526ab-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="526ab-105">DESCRIPTION</span></span>
<span data-ttu-id="526ab-106">**Set-AzureTrafficManagerProfile** cmdlet 'ı Microsoft Azure Traffic Manager profilinin özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="526ab-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="526ab-107">*LoadBalancingMethod* değerini "yük devretme" olarak ayarlamış olduğunuz profillerde, Add-AzureTrafficManagerEndpoint cmdlet 'ine sahip profilinize eklediğiniz uç noktaların yük devretme sırasını belirleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="526ab-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="526ab-108">Daha fazla bilgi için aşağıdaki örnek 3 konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="526ab-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="526ab-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="526ab-109">EXAMPLES</span></span>

### <span data-ttu-id="526ab-110">Örnek 1: Traffic Manager profili için TTL 'yi ayarlama</span><span class="sxs-lookup"><span data-stu-id="526ab-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="526ab-111">Bu komut, MyTrafficManagerProfile Traffic Manager profil nesnesi için TTL değerini 60 saniye olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="526ab-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="526ab-112">Örnek 2: bir profil için birkaç değer ayarlama</span><span class="sxs-lookup"><span data-stu-id="526ab-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="526ab-113">Bu komut, **Get-AzureTrafficManagerProfile** cmdlet 'Ini kullanarak myprofıle adlı bir Traffic Manager profili alır.</span><span class="sxs-lookup"><span data-stu-id="526ab-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="526ab-114">Profil, bir Traffic Manager profili için RoundRobin Yük Dengeleme yöntemi, 30 saniye TTL, izleme Protokolü HTTP, izleyici bağlantı noktası ve göreli yol kullanır.</span><span class="sxs-lookup"><span data-stu-id="526ab-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="526ab-115">Örnek 3: uç noktaları istenen yük devretme sırasına yeniden sıralama</span><span class="sxs-lookup"><span data-stu-id="526ab-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="526ab-116">Bu örnek MyProfile 'e eklenecek uç noktaları istenen yük devretme siparişine yeniden sıralar.</span><span class="sxs-lookup"><span data-stu-id="526ab-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="526ab-117">İlk komut Myprofıle adlı Traffic Manager profil nesnesini alır ve nesneyi $Profile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="526ab-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="526ab-118">İkinci komut uç noktaları dizisindeki uç noktaları, yerine çalışma yerine gerçekleşecek şekilde yeniden sıralar.</span><span class="sxs-lookup"><span data-stu-id="526ab-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="526ab-119">Son komut $Profile uygulamasında depolanan Traffic Manager profilini yeni son nokta siparişiyle güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="526ab-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="526ab-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="526ab-120">PARAMETERS</span></span>

### <span data-ttu-id="526ab-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="526ab-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="526ab-122">Bağlantıyı dağıtmak için kullanılacak yük dengeleme yöntemini belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="526ab-123">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="526ab-123">Valid values are:</span></span> 

- <span data-ttu-id="526ab-124">Performans</span><span class="sxs-lookup"><span data-stu-id="526ab-124">Performance</span></span>
- <span data-ttu-id="526ab-125">Devretmesini</span><span class="sxs-lookup"><span data-stu-id="526ab-125">Failover</span></span>
- <span data-ttu-id="526ab-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="526ab-126">RoundRobin</span></span>

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

### <span data-ttu-id="526ab-127">-Monitorın bağlantı noktası</span><span class="sxs-lookup"><span data-stu-id="526ab-127">-MonitorPort</span></span>
<span data-ttu-id="526ab-128">Uç nokta durumunu izlemek için kullanılan bağlantı noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="526ab-129">Geçerli değerler, 0 ' dan büyük ve 65.535 'ten küçük tamsayı değerlerdir.</span><span class="sxs-lookup"><span data-stu-id="526ab-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="526ab-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="526ab-130">-MonitorProtocol</span></span>
<span data-ttu-id="526ab-131">Uç nokta durumunu izlemek için kullanılacak protokolü belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="526ab-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="526ab-132">Valid values are:</span></span> 

- <span data-ttu-id="526ab-133">Http</span><span class="sxs-lookup"><span data-stu-id="526ab-133">Http</span></span>
- <span data-ttu-id="526ab-134">Https</span><span class="sxs-lookup"><span data-stu-id="526ab-134">Https</span></span>

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

### <span data-ttu-id="526ab-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="526ab-135">-MonitorRelativePath</span></span>
<span data-ttu-id="526ab-136">Sistem durumu için araştırma yapılacak uç nokta etki alanı adına göre yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="526ab-137">Yol aşağıdaki kısıtlamalara uymalıdır:</span><span class="sxs-lookup"><span data-stu-id="526ab-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="526ab-138">Yol 1 ila 1000 karakter arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="526ab-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="526ab-139">Eğik çizgiyle başlamalıdır.</span><span class="sxs-lookup"><span data-stu-id="526ab-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="526ab-140">XML öğeleri içermemesi gerekir \<\> .</span><span class="sxs-lookup"><span data-stu-id="526ab-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="526ab-141">Çift eğik çizgi içermemelidir,//.</span><span class="sxs-lookup"><span data-stu-id="526ab-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="526ab-142">Geçersiz HTML kaçış karakterleri içermemelidir.</span><span class="sxs-lookup"><span data-stu-id="526ab-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="526ab-143">Örneğin,% XY.</span><span class="sxs-lookup"><span data-stu-id="526ab-143">For example, %XY.</span></span>

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

### <span data-ttu-id="526ab-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="526ab-144">-Name</span></span>
<span data-ttu-id="526ab-145">Güncelleştirilecek Traffic Manager profilinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="526ab-146">-Profil</span><span class="sxs-lookup"><span data-stu-id="526ab-146">-Profile</span></span>
<span data-ttu-id="526ab-147">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="526ab-148">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="526ab-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="526ab-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="526ab-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="526ab-150">Profili ayarlamak için kullandığınız Traffic Manager profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="526ab-151">-TTL</span><span class="sxs-lookup"><span data-stu-id="526ab-151">-Ttl</span></span>
<span data-ttu-id="526ab-152">Yerel DNS çözümleyicilerine DNS girişlerini önbelleğe alma süresini bildiren DNS yaşam süresini (TTL) belirtir.</span><span class="sxs-lookup"><span data-stu-id="526ab-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="526ab-153">Geçerli değerler 30 ile 999.999 arasında bir tamsayıdır.</span><span class="sxs-lookup"><span data-stu-id="526ab-153">Valid values are an integer from 30 through 999,999.</span></span>

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

### <span data-ttu-id="526ab-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="526ab-154">CommonParameters</span></span>
<span data-ttu-id="526ab-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="526ab-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="526ab-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="526ab-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="526ab-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="526ab-157">INPUTS</span></span>

## <span data-ttu-id="526ab-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="526ab-158">OUTPUTS</span></span>

### <span data-ttu-id="526ab-159">Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition</span><span class="sxs-lookup"><span data-stu-id="526ab-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="526ab-160">Bu cmdlet, bir Traffic Manager profil nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="526ab-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="526ab-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="526ab-161">NOTES</span></span>

## <span data-ttu-id="526ab-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="526ab-162">RELATED LINKS</span></span>

[<span data-ttu-id="526ab-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="526ab-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="526ab-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="526ab-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="526ab-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="526ab-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="526ab-166">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="526ab-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="526ab-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="526ab-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


