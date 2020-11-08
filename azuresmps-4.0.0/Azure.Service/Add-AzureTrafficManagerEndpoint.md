---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106376"
---
# <span data-ttu-id="99282-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99282-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="99282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99282-102">SYNOPSIS</span></span>
<span data-ttu-id="99282-103">Traffic Manager profiline uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="99282-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="99282-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99282-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99282-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="99282-105">DESCRIPTION</span></span>
<span data-ttu-id="99282-106">**Add-AzureTrafficManagerEndpoint** cmdlet 'ı bir Microsoft Azure Traffic Manager profiline uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="99282-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="99282-107">Uç nokta ekledikten sonra, Pipeline işlecini kullanarak sonucu **set-AzureTrafficManagerProfile** cmdlet 'ine geçirin.</span><span class="sxs-lookup"><span data-stu-id="99282-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="99282-108">Bu cmdlet değişikliklerinizi kaydetmek için Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="99282-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="99282-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99282-109">EXAMPLES</span></span>

### <span data-ttu-id="99282-110">Örnek 1: profile uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="99282-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="99282-111">İlk komut, ContosoProfile adlı profili almak için **Get-AzureTrafficManagerProfile** cmdlet 'ini kullanır ve ardından $TrafficManagerProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99282-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="99282-112">İkinci komut $TrafficManagerProfile depolanan Traffic Manager profiline bir uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="99282-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="99282-113">Uç nokta, Contoso02App.couldapp.net etki alanı adını içerir.</span><span class="sxs-lookup"><span data-stu-id="99282-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="99282-114">Komut aynı zamanda etkinleştirilip etkinleştirilmediğini ve türünü de belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="99282-115">Komut, Azure 'a bağlanarak değişikliklerinizi kaydetmek için profil nesnesini **set-AzureTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="99282-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="99282-116">Örnek 2: belirtilen konum ve ağırlığa sahip bir uç nokta ekleme</span><span class="sxs-lookup"><span data-stu-id="99282-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="99282-117">Bu komut bir Traffic Manager profiline uç nokta ekler.</span><span class="sxs-lookup"><span data-stu-id="99282-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="99282-118">Uç nokta, Contoso02App.couldapp.net etki alanı adını içerir.</span><span class="sxs-lookup"><span data-stu-id="99282-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="99282-119">Komut aynı zamanda etkinleştirilip etkinleştirilmediğini ve türünü de belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="99282-120">Komut ayrıca uç noktanın kalınlığını ve konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="99282-121">Bu komut, **AzureTrafficManagerProfile 'ı ayarlamak** için profil nesnesini geçirir; değişikliklerinizi kaydetmek için Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="99282-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="99282-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99282-122">PARAMETERS</span></span>

### <span data-ttu-id="99282-123">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="99282-123">-DomainName</span></span>
<span data-ttu-id="99282-124">Eklenecek uç noktanın etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="99282-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="99282-125">-Location</span></span>
<span data-ttu-id="99282-126">Cmdlet 'in eklediği uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="99282-127">Bu bir Azure konumu olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99282-127">This must be an Azure location.</span></span>

<span data-ttu-id="99282-128">Bu parametre "Any" türünde veya "TrafficManager" türünde, yük dengeleme yönteminin "performans" olarak ayarlandığı bir profildeki uç noktalar için değer içermelidir.</span><span class="sxs-lookup"><span data-stu-id="99282-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="99282-129">Olası değerler, konumunda listelendiği gibi, Azure bölge adlarıdır https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="99282-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="99282-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="99282-130">-MinChildEndpoints</span></span>
<span data-ttu-id="99282-131">İç içe profilin bu uç nokta için çevrimiçi olması gereken en az uç nokta sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="99282-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="99282-132">-Profile</span></span>
<span data-ttu-id="99282-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="99282-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="99282-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99282-135">-Durum</span><span class="sxs-lookup"><span data-stu-id="99282-135">-Status</span></span>
<span data-ttu-id="99282-136">İzleme uç noktasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="99282-137">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="99282-137">Valid values are:</span></span> 

- <span data-ttu-id="99282-138">Etkin</span><span class="sxs-lookup"><span data-stu-id="99282-138">Enabled</span></span>
- <span data-ttu-id="99282-139">DISABLED</span><span class="sxs-lookup"><span data-stu-id="99282-139">Disabled</span></span>

<span data-ttu-id="99282-140">Etkin bir değer belirtirseniz, Traffic Manager uç noktayı izler ve yük dengeleme yöntemi trafiği yönetirken dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="99282-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="99282-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="99282-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="99282-142">Uç noktanın ekleneceği Traffic Manager profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

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

### <span data-ttu-id="99282-143">-Tür</span><span class="sxs-lookup"><span data-stu-id="99282-143">-Type</span></span>
<span data-ttu-id="99282-144">Uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="99282-145">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="99282-145">Valid values are:</span></span> 

- <span data-ttu-id="99282-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="99282-146">CloudService</span></span>
- <span data-ttu-id="99282-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="99282-147">AzureWebsite</span></span>
- <span data-ttu-id="99282-148">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="99282-148">TrafficManager</span></span>

- <span data-ttu-id="99282-149">Tüm</span><span class="sxs-lookup"><span data-stu-id="99282-149">Any</span></span> 

<span data-ttu-id="99282-150">Birden çok AzureWebsite uç noktası varsa uç noktalar farklı datacenters 'da olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="99282-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="99282-151">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="99282-151">-Weight</span></span>
<span data-ttu-id="99282-152">Cmdlet 'in eklediği uç noktanın kalınlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99282-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="99282-153">Bu parametre için geçerli değer aralığı \[ 1, 1000 ' dir \] .</span><span class="sxs-lookup"><span data-stu-id="99282-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="99282-154">Bu parametre yalnızca RoundRobin Yük Dengeleme ilkeleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="99282-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="99282-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99282-155">CommonParameters</span></span>
<span data-ttu-id="99282-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99282-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99282-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99282-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99282-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99282-158">INPUTS</span></span>

## <span data-ttu-id="99282-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99282-159">OUTPUTS</span></span>

### <span data-ttu-id="99282-160">Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition</span><span class="sxs-lookup"><span data-stu-id="99282-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="99282-161">Bu cmdlet, güncelleştirilmiş profil hakkında bilgi içeren bir Traffic Manager profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="99282-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="99282-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99282-162">NOTES</span></span>

## <span data-ttu-id="99282-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99282-163">RELATED LINKS</span></span>

[<span data-ttu-id="99282-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99282-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="99282-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99282-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="99282-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="99282-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="99282-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="99282-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


