---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105434"
---
# <span data-ttu-id="c257d-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c257d-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="c257d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c257d-102">SYNOPSIS</span></span>
<span data-ttu-id="c257d-103">Traffic Manager profilindeki uç noktasının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c257d-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="c257d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c257d-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c257d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c257d-105">DESCRIPTION</span></span>
<span data-ttu-id="c257d-106">**Set-AzureTrafficManagerEndpoint** cmdlet 'ı, Microsoft Azure Traffic Manager profilinde uç noktanın özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c257d-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="c257d-107">Uç nokta geçerli profilde yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c257d-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="c257d-108">Uç nokta ekledikten sonra, Pipeline işlecini kullanarak sonucu **set-AzureTrafficManagerProfile** cmdlet 'ine geçirin.</span><span class="sxs-lookup"><span data-stu-id="c257d-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c257d-109">Bu cmdlet değişikliklerinizi kaydetmek için Azure 'a bağlanır.</span><span class="sxs-lookup"><span data-stu-id="c257d-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="c257d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c257d-110">EXAMPLES</span></span>

### <span data-ttu-id="c257d-111">Örnek 1: bir profilin uç noktasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c257d-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="c257d-112">İlk komut, ContosoProfile adlı profili almak için **Get-AzureTrafficManagerProfile** cmdlet 'ini kullanır ve ardından $TrafficManagerProfile değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c257d-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="c257d-113">İkinci komut $TrafficManagerProfile depolanan Traffic Manager profilindeki uç noktayı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c257d-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="c257d-114">Uç nokta, ContosoApp02.cloudapp.net etki alanı adını içerir.</span><span class="sxs-lookup"><span data-stu-id="c257d-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="c257d-115">Komut ayrıca uç noktanın durumunu, türünü, ağırlığını ve konumunu da belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="c257d-116">Bu komut, değişiklikleri kaydetmek üzere Azure 'a bağlanmak için değiştirilmiş profili **set-AzureTrafficManagerProfile** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="c257d-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="c257d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c257d-117">PARAMETERS</span></span>

### <span data-ttu-id="c257d-118">-EtkiAlanıAdı</span><span class="sxs-lookup"><span data-stu-id="c257d-118">-DomainName</span></span>
<span data-ttu-id="c257d-119">Değiştirilecek uç noktanın etki alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="c257d-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="c257d-120">-Location</span></span>
<span data-ttu-id="c257d-121">Cmdlet 'in eklediği uç noktasının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="c257d-122">Bu bir Azure konumu olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c257d-122">This must be an Azure location.</span></span>

<span data-ttu-id="c257d-123">Bu parametre "Any" türünde veya "TrafficManager" türünde, yük dengeleme yönteminin "performans" olarak ayarlandığı bir profildeki uç noktalar için değer içermelidir.</span><span class="sxs-lookup"><span data-stu-id="c257d-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="c257d-124">Olası değerler, konumunda listelendiği gibi, Azure bölge adlarıdır  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="c257d-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="c257d-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="c257d-125">-MinChildEndpoints</span></span>
<span data-ttu-id="c257d-126">İç içe profilin bu uç nokta için çevrimiçi olması gereken en az uç nokta sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="c257d-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="c257d-127">-Profile</span></span>
<span data-ttu-id="c257d-128">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="c257d-129">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="c257d-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c257d-130">-Durum</span><span class="sxs-lookup"><span data-stu-id="c257d-130">-Status</span></span>
<span data-ttu-id="c257d-131">İzleme uç noktasının durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="c257d-132">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c257d-132">Valid values are:</span></span> 

- <span data-ttu-id="c257d-133">Etkin</span><span class="sxs-lookup"><span data-stu-id="c257d-133">Enabled</span></span>
- <span data-ttu-id="c257d-134">DISABLED</span><span class="sxs-lookup"><span data-stu-id="c257d-134">Disabled</span></span>

<span data-ttu-id="c257d-135">Etkin bir değer belirtirseniz, Traffic Manager uç noktayı izler ve yük dengeleme yöntemi trafiği yönetirken dikkate alır.</span><span class="sxs-lookup"><span data-stu-id="c257d-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="c257d-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c257d-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="c257d-137">Uç noktanın değiştirileceği Traffic Manager profili nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="c257d-138">-Tür</span><span class="sxs-lookup"><span data-stu-id="c257d-138">-Type</span></span>
<span data-ttu-id="c257d-139">Uç nokta türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="c257d-140">Geçerli değerler:</span><span class="sxs-lookup"><span data-stu-id="c257d-140">Valid values are:</span></span> 

- <span data-ttu-id="c257d-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="c257d-141">CloudService</span></span>
- <span data-ttu-id="c257d-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c257d-142">AzureWebsite</span></span>
- <span data-ttu-id="c257d-143">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c257d-143">TrafficManager</span></span>

- <span data-ttu-id="c257d-144">Tüm</span><span class="sxs-lookup"><span data-stu-id="c257d-144">Any</span></span> 

<span data-ttu-id="c257d-145">Birden çok AzureWebsite uç noktası varsa uç noktalar farklı datacenters 'da olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c257d-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="c257d-146">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="c257d-146">-Weight</span></span>
<span data-ttu-id="c257d-147">Cmdlet 'in eklediği uç noktanın kalınlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c257d-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="c257d-148">Bu parametre için geçerli değer aralığı \[ 1, 1000 ' dir \] .</span><span class="sxs-lookup"><span data-stu-id="c257d-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="c257d-149">Bu parametre yalnızca RoundRobin Yük Dengeleme ilkeleri için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="c257d-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="c257d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c257d-150">CommonParameters</span></span>
<span data-ttu-id="c257d-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c257d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c257d-152">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c257d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c257d-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c257d-153">INPUTS</span></span>

## <span data-ttu-id="c257d-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c257d-154">OUTPUTS</span></span>

### <span data-ttu-id="c257d-155">Microsoft. Windowsaziy. Commands. Utilities. TrafficManager. modeller. ıprofilewithdefinition</span><span class="sxs-lookup"><span data-stu-id="c257d-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="c257d-156">Bu cmdlet, güncelleştirilmiş profil hakkında bilgi içeren bir Traffic Manager profili nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c257d-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="c257d-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c257d-157">NOTES</span></span>

## <span data-ttu-id="c257d-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c257d-158">RELATED LINKS</span></span>

[<span data-ttu-id="c257d-159">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c257d-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="c257d-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c257d-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="c257d-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c257d-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="c257d-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c257d-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


