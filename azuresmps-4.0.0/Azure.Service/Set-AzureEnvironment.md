---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105967"
---
# <span data-ttu-id="cfd62-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cfd62-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="cfd62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfd62-102">SYNOPSIS</span></span>
<span data-ttu-id="cfd62-103">Azure ortamının özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="cfd62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cfd62-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cfd62-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cfd62-105">DESCRIPTION</span></span>
<span data-ttu-id="cfd62-106">**Set-AzureEnvironment** cmdlet 'ı bir Azure ortamının özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="cfd62-107">Yeni özellik değerleriyle ortamı temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cfd62-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="cfd62-108">Ortam ve özellik değerlerini değiştirmek için diğer parametreleri belirlemek için **ad** parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="cfd62-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="cfd62-109">**Set-AzureEnvironment** ' i kullanarak Azure ortamının adını değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cfd62-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="cfd62-110">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="cfd62-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="cfd62-111">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cfd62-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="cfd62-112">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="cfd62-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="cfd62-113">Not: Azurecyüksek veya AzureChinaCloud ortamlarının özelliklerini değiştirmeyin.</span><span class="sxs-lookup"><span data-stu-id="cfd62-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="cfd62-114">Oluşturduğunuz özel ortamların değerlerini değiştirmek için bu cmdlet 'i kullanın.</span><span class="sxs-lookup"><span data-stu-id="cfd62-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="cfd62-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cfd62-115">EXAMPLES</span></span>

### <span data-ttu-id="cfd62-116">Örnek 1: ortam özelliklerini değiştirme</span><span class="sxs-lookup"><span data-stu-id="cfd62-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="cfd62-117">Bu komut, ContosoEnv ortamının **Publishsettingsfileurl** ve **storageendpoint** özelliklerinin değerlerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="cfd62-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cfd62-118">PARAMETERS</span></span>

### <span data-ttu-id="cfd62-119">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="cfd62-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="cfd62-120">Azure Active Directory kimlik doğrulaması uç noktasını belirtilen değerle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd62-121">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="cfd62-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="cfd62-122">Azure Active Directory tarafından yönetilen bir yönetim API 'sinin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="cfd62-123">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="cfd62-123">-AdTenant</span></span>
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

### <span data-ttu-id="cfd62-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="cfd62-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="cfd62-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="cfd62-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="cfd62-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="cfd62-126">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd62-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfd62-127">-GalleryEndpoint</span></span>
<span data-ttu-id="cfd62-128">Azure Resource Manager galerisinin uç noktasını belirtilen değerle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="cfd62-129">Galeri uç noktası, kaynak grubu Galeri şablonlarının konumudur.</span><span class="sxs-lookup"><span data-stu-id="cfd62-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="cfd62-130">Azure Kaynak grupları ve galeri şablonları hakkında daha fazla bilgi için [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052)yardım konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="cfd62-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd62-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfd62-131">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd62-132">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="cfd62-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="cfd62-133">Azure yönetim portalının URL 'sini belirtilen değerle değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="cfd62-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="cfd62-134">-Name</span></span>
<span data-ttu-id="cfd62-135">Değiştirilecek ortamı tanımlar.</span><span class="sxs-lookup"><span data-stu-id="cfd62-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="cfd62-136">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-136">This parameter is required.</span></span>
<span data-ttu-id="cfd62-137">Parametre değeri büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="cfd62-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="cfd62-138">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="cfd62-138">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="cfd62-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="cfd62-139">-Profile</span></span>
<span data-ttu-id="cfd62-140">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="cfd62-141">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="cfd62-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cfd62-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="cfd62-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="cfd62-143">Belirtilen ortamdaki yayımlama ayarları dosyalarının URL 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="cfd62-144">Azure yayımlama ayarları dosyası, hesabınızla ilgili bilgileri içeren bir XML dosyasıdır ve Windows PowerShell 'in sizin adınıza Azure hesabınızda oturum açmasını sağlayan bir yönetim sertifikasıdır.</span><span class="sxs-lookup"><span data-stu-id="cfd62-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="cfd62-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfd62-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="cfd62-146">Hesap ile ilişkili kaynak gruplarıyla ilgili veriler de içinde olmak üzere, Azure Resource Manager verilerinin uç noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="cfd62-147">Azure Resource Manager hakkında daha fazla bilgi için [Azure Resource Manager cmdlet 'lerinin](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) ve [Kaynak Yöneticisi ile Windows PowerShell](https://go.microsoft.com/fwlink/?LinkID=394767)  'in ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="cfd62-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd62-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfd62-148">-ServiceEndpoint</span></span>
<span data-ttu-id="cfd62-149">Belirtilen ortamdaki Azure hizmeti uç noktasının URL 'sini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="cfd62-150">Azure hizmeti uç noktası, uygulamanızın Genel Azure platformu tarafından yönetilip yönetilmediğini, Çin 'de 21Vianet tarafından sağlanan Azure 'u veya özel bir Azure yüklemesini belirler.</span><span class="sxs-lookup"><span data-stu-id="cfd62-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfd62-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="cfd62-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="cfd62-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfd62-152">-StorageEndpoint</span></span>
<span data-ttu-id="cfd62-153">Belirtilen ortamdaki depolama hizmetlerinin varsayılan uç noktasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="cfd62-153">Changes the default endpoint of storage services in the specified environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfd62-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="cfd62-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="cfd62-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfd62-155">CommonParameters</span></span>
<span data-ttu-id="cfd62-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cfd62-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfd62-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfd62-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfd62-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cfd62-158">INPUTS</span></span>

### <span data-ttu-id="cfd62-159">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cfd62-159">None</span></span>
<span data-ttu-id="cfd62-160">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cfd62-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="cfd62-161">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cfd62-161">OUTPUTS</span></span>

### <span data-ttu-id="cfd62-162">Microsoft. Windowsazme. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cfd62-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="cfd62-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cfd62-163">NOTES</span></span>

## <span data-ttu-id="cfd62-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cfd62-164">RELATED LINKS</span></span>

[<span data-ttu-id="cfd62-165">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cfd62-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="cfd62-166">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cfd62-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="cfd62-167">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="cfd62-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


