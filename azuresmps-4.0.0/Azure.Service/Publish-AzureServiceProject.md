---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105883"
---
# <span data-ttu-id="65c64-101">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="65c64-101">Publish-AzureServiceProject</span></span>

## <span data-ttu-id="65c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65c64-102">SYNOPSIS</span></span>
<span data-ttu-id="65c64-103">Geçerli hizmeti Windows Azure 'a yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="65c64-103">Publish the current service to Windows Azure.</span></span>

## <span data-ttu-id="65c64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65c64-104">SYNTAX</span></span>

### <span data-ttu-id="65c64-105">PublishFromServiceDefinition (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65c64-105">PublishFromServiceDefinition (Default)</span></span>
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="65c64-106">PublishFromPackage</span><span class="sxs-lookup"><span data-stu-id="65c64-106">PublishFromPackage</span></span>
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65c64-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="65c64-107">DESCRIPTION</span></span>
<span data-ttu-id="65c64-108">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="65c64-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="65c64-109">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="65c64-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="65c64-110">**Publish-AzureServiceProject** cmdlet 'i geçerli hizmeti buluta yayımlar.</span><span class="sxs-lookup"><span data-stu-id="65c64-110">The **Publish-AzureServiceProject** cmdlet publishes the current service to the cloud.</span></span>
<span data-ttu-id="65c64-111">Komut satırında yayımlama yapılandırması ( **abonelik** , **storageAccountName** , **konum** , **yuva** ) veya **set-AzureServiceProject** cmdlet aracılığıyla yerel ayarlarda belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65c64-111">You can specify publishing configuration (such as **Subscription** , **StorageAccountName** , **Location** , **Slot** ) on the command line, or in local settings through the **Set-AzureServiceProject** cmdlet.</span></span>

## <span data-ttu-id="65c64-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65c64-112">EXAMPLES</span></span>

### <span data-ttu-id="65c64-113">Örnek 1: varsayılan değerlerle bir hizmet projesi yayımlama</span><span class="sxs-lookup"><span data-stu-id="65c64-113">Example 1: Publish a service project with default values</span></span>
```
PS C:\> Publish-AzureServiceProject
```

<span data-ttu-id="65c64-114">Bu örnek geçerli hizmeti, geçerli hizmet ayarlarını ve geçerli Azure yayımlama profilini kullanarak yayımlar.</span><span class="sxs-lookup"><span data-stu-id="65c64-114">This example publishes the current service, using the current service settings and the current Azure publish profile.</span></span>

### <span data-ttu-id="65c64-115">Örnek 2: dağıtım paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="65c64-115">Example 2: Create a deployment package</span></span>
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

<span data-ttu-id="65c64-116">Bu örnekte, hizmet dizininde dağıtım paketi (. cspkg) dosyası oluşturulur ve Windows Azure 'da yayınlanmaz.</span><span class="sxs-lookup"><span data-stu-id="65c64-116">This example creates a deployment package (.cspkg) file in the service directory and does not publish to Windows Azure.</span></span>

## <span data-ttu-id="65c64-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65c64-117">PARAMETERS</span></span>

### <span data-ttu-id="65c64-118">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="65c64-118">-AffinityGroup</span></span>
<span data-ttu-id="65c64-119">Hizmetin kullanmasını istediğiniz benzeşim grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="65c64-119">Specifies the affinity group that you want the service to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-120">-Yapılandırma</span><span class="sxs-lookup"><span data-stu-id="65c64-120">-Configuration</span></span>
<span data-ttu-id="65c64-121">Hizmet yapılandırma dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65c64-121">Specifies the service configuration file.</span></span>
<span data-ttu-id="65c64-122">Bu parametreyi belirtirseniz, *paket* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="65c64-122">If you specify this parameter, specify the *Package* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-123">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="65c64-123">-DeploymentName</span></span>
<span data-ttu-id="65c64-124">Dağıtım adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65c64-124">Specifies the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-125">-ForceUpgrade</span><span class="sxs-lookup"><span data-stu-id="65c64-125">-ForceUpgrade</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-126">-Başlat</span><span class="sxs-lookup"><span data-stu-id="65c64-126">-Launch</span></span>
<span data-ttu-id="65c64-127">Uygulamayı dağıtıldıktan sonra bir tarayıcı penceresi açar.</span><span class="sxs-lookup"><span data-stu-id="65c64-127">Opens a browser window so you can view the application after it is deployed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="65c64-128">-Location</span></span>
<span data-ttu-id="65c64-129">Uygulamanın barındırıldığı bölge.</span><span class="sxs-lookup"><span data-stu-id="65c64-129">The region in which the application will be hosted.</span></span>
<span data-ttu-id="65c64-130">Olası değerler:</span><span class="sxs-lookup"><span data-stu-id="65c64-130">Possible values are:</span></span> 
  
- <span data-ttu-id="65c64-131">Her yerde Asya</span><span class="sxs-lookup"><span data-stu-id="65c64-131">Anywhere Asia</span></span>
- <span data-ttu-id="65c64-132">Her yerde</span><span class="sxs-lookup"><span data-stu-id="65c64-132">Anywhere Europe</span></span>
- <span data-ttu-id="65c64-133">Her yerde</span><span class="sxs-lookup"><span data-stu-id="65c64-133">Anywhere US</span></span>
- <span data-ttu-id="65c64-134">Doğu Asya</span><span class="sxs-lookup"><span data-stu-id="65c64-134">East Asia</span></span>
- <span data-ttu-id="65c64-135">Doğu ABD</span><span class="sxs-lookup"><span data-stu-id="65c64-135">East US</span></span>
- <span data-ttu-id="65c64-136">Kuzey Orta ABD</span><span class="sxs-lookup"><span data-stu-id="65c64-136">North Central US</span></span>
- <span data-ttu-id="65c64-137">Kuzey Avrupa</span><span class="sxs-lookup"><span data-stu-id="65c64-137">North Europe</span></span>
- <span data-ttu-id="65c64-138">Güney Orta ABD</span><span class="sxs-lookup"><span data-stu-id="65c64-138">South Central US</span></span>
- <span data-ttu-id="65c64-139">Güneydoğu Asya</span><span class="sxs-lookup"><span data-stu-id="65c64-139">Southeast Asia</span></span>
- <span data-ttu-id="65c64-140">Batı Avrupa</span><span class="sxs-lookup"><span data-stu-id="65c64-140">West Europe</span></span>
- <span data-ttu-id="65c64-141">Batı ABD</span><span class="sxs-lookup"><span data-stu-id="65c64-141">West US</span></span>
 
<span data-ttu-id="65c64-142">Konum belirtilmezse, ayarlanacak son çağrıda belirtilen konum **-AzureServiceProject** kullanılır.</span><span class="sxs-lookup"><span data-stu-id="65c64-142">If no Location is specified, the location specified in the last call to **Set-AzureServiceProject** will be used.</span></span> <span data-ttu-id="65c64-143">Hiçbir konum belirtilmemişse, konum, ' Kuzey Merkezi ABD ' ve ' Güney Merkezi ' konumlarından rastgele seçilir.</span><span class="sxs-lookup"><span data-stu-id="65c64-143">If no Location was ever specified, the Location will be randomly chosen from 'North Central US' and 'South Central US' locations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-144">-Package</span><span class="sxs-lookup"><span data-stu-id="65c64-144">-Package</span></span>
<span data-ttu-id="65c64-145">Dağıtılacak paket dosyasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65c64-145">Specifies the package file to deploy.</span></span>
<span data-ttu-id="65c64-146">. Cspkg dosya adı uzantısına sahip yerel bir dosya veya paketi içeren bir blob URI 'SI belirtin.</span><span class="sxs-lookup"><span data-stu-id="65c64-146">Specify either a local file that has the .cspkg file name extension or a URI of a blob that contains the package.</span></span>
<span data-ttu-id="65c64-147">Bu parametreyi belirtirseniz, *ServiceName* parametresini belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="65c64-147">If you specify this parameter, do not specify the *ServiceName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-148">-Profil</span><span class="sxs-lookup"><span data-stu-id="65c64-148">-Profile</span></span>
<span data-ttu-id="65c64-149">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="65c64-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65c64-150">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="65c64-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65c64-151">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="65c64-151">-ServiceName</span></span>
<span data-ttu-id="65c64-152">Windows Azure 'a yayımlarken hizmet için kullanılacak adı belirtir.</span><span class="sxs-lookup"><span data-stu-id="65c64-152">Specifies the name to be used for the service when publishing to Windows Azure.</span></span>
<span data-ttu-id="65c64-153">Bu ad, Windows Azure 'da ( **ad**. cloudapp.net) barındırılan hizmeti adresleyip hizmeti adresleyebilir.</span><span class="sxs-lookup"><span data-stu-id="65c64-153">The name determines part of the label in the cloudapp.net subdomain that is used to address the service when hosted in Windows Azure (that is, **name**.cloudapp.net).</span></span>
<span data-ttu-id="65c64-154">Hizmet yayımlandığında belirtilen ad, hizmet oluşturulduğunda verilen adı geçersiz kılar.</span><span class="sxs-lookup"><span data-stu-id="65c64-154">Any name specified while publishing the service overrides the name given when the service was created.</span></span>
<span data-ttu-id="65c64-155">( **New-AzureServiceProject** cmdlet 'ine bakın).</span><span class="sxs-lookup"><span data-stu-id="65c64-155">(See the **New-AzureServiceProject** cmdlet).</span></span>

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-156">Yuvalı</span><span class="sxs-lookup"><span data-stu-id="65c64-156">-Slot</span></span>
<span data-ttu-id="65c64-157">Bu hizmet için kullanılacak dağıtım yuvası.</span><span class="sxs-lookup"><span data-stu-id="65c64-157">The deployment slot to be used for this service.</span></span>
<span data-ttu-id="65c64-158">Olası değerler ' hazırlama ' ve ' üretim '.</span><span class="sxs-lookup"><span data-stu-id="65c64-158">Possible values are 'Staging' and 'Production'.</span></span>
<span data-ttu-id="65c64-159">Bir yuva belirtilmemişse, Set-AzureDeploymentSlot son çağrıda sağlanan yuva kullanılır.</span><span class="sxs-lookup"><span data-stu-id="65c64-159">If no slot is specified, the slot provided in the last call to Set-AzureDeploymentSlot is used.</span></span>
<span data-ttu-id="65c64-160">Hiçbir yuva belirtilmemişse ' üretim ' yuvası kullanılır.</span><span class="sxs-lookup"><span data-stu-id="65c64-160">If no slot has ever been specified, the 'Production' slot is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="65c64-161">-StorageAccountName</span></span>
<span data-ttu-id="65c64-162">Hizmet yayımlanırken kullanılacak Windows Azure depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="65c64-162">Specifies the Windows Azure storage account name to be used while publishing the service.</span></span>
<span data-ttu-id="65c64-163">Bu değer, hizmet yayımlanana kadar kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="65c64-163">This value is not used until the service is published.</span></span>
<span data-ttu-id="65c64-164">Bu parametre belirtilmediğinde, değer son **set-AzureServiceProject** komutundan alınır.</span><span class="sxs-lookup"><span data-stu-id="65c64-164">When this parameter is not specified, the value is obtained from the last **Set-AzureServiceProject** command.</span></span>
<span data-ttu-id="65c64-165">Hiçbir depolama hesabı belirtilmemişse, hizmetin adıyla eşleşen bir depolama hesabı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="65c64-165">If no storage account was ever specified, a storage account matching the name of the service will be used.</span></span>
<span data-ttu-id="65c64-166">Böyle bir depolama hesabı yoksa cmdlet, yenisini oluşturmaya çalışır.</span><span class="sxs-lookup"><span data-stu-id="65c64-166">If no such storage account exists, the cmdlet attempts to create a new one.</span></span>
<span data-ttu-id="65c64-167">Ancak, başka bir abonelikte hizmet adıyla eşleşen bir depolama hesabı varsa, deneme başarısız olabilir.</span><span class="sxs-lookup"><span data-stu-id="65c64-167">However, the attempt may fail if a storage account matching the service name exists in another subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c64-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c64-168">CommonParameters</span></span>
<span data-ttu-id="65c64-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65c64-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c64-170">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c64-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c64-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65c64-171">INPUTS</span></span>

## <span data-ttu-id="65c64-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65c64-172">OUTPUTS</span></span>

## <span data-ttu-id="65c64-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65c64-173">NOTES</span></span>

## <span data-ttu-id="65c64-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65c64-174">RELATED LINKS</span></span>

[<span data-ttu-id="65c64-175">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="65c64-175">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="65c64-176">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="65c64-176">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)


