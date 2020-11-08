---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105730"
---
# <span data-ttu-id="6a7c7-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a7c7-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="6a7c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7c7-103">Azure ortamı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="6a7c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6a7c7-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6a7c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6a7c7-105">DESCRIPTION</span></span>
<span data-ttu-id="6a7c7-106">**Add-AzureEnvironment** cmdlet 'i, yeni bir özel Azure hesap ortamı oluşturur ve bunu dolaşım kullanıcı profilinize kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="6a7c7-107">Cmdlet, yeni ortamı temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="6a7c7-108">Komut tamamlandığında, ortamı Windows PowerShell 'de kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="6a7c7-109">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="6a7c7-110">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="6a7c7-111">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="6a7c7-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="6a7c7-112">Bu cmdlet 'in yalnızca **Name** parametresi zorunludur.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="6a7c7-113">Bir parametreyi atlarsanız, değeri null ($Null) ve bu uç noktayı kullanan hizmet düzgün çalışmayabilir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="6a7c7-114">Bir ortam özelliğinin değerini eklemek veya değiştirmek için **set-AzureEnvironment** cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="6a7c7-115">Not: ortamınızı değiştirmek hesabınızın başarısız olmasına neden olabilir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="6a7c7-116">Genellikle, ortamlar yalnızca sınama veya sorun giderme için eklenir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="6a7c7-117">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6a7c7-118">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="6a7c7-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="6a7c7-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6a7c7-119">EXAMPLES</span></span>

### <span data-ttu-id="6a7c7-120">Örnek 1: Azure ortamı ekleme</span><span class="sxs-lookup"><span data-stu-id="6a7c7-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="6a7c7-121">Bu komut, ContosoEnv Azure ortamını oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="6a7c7-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6a7c7-122">PARAMETERS</span></span>

### <span data-ttu-id="6a7c7-123">-Activedirectoryenvseçnokta</span><span class="sxs-lookup"><span data-stu-id="6a7c7-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="6a7c7-124">Yeni ortamdaki Azure Active Directory kimlik doğrulaması uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

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

### <span data-ttu-id="6a7c7-125">-Activedirectoryserviceendpointresourceıd</span><span class="sxs-lookup"><span data-stu-id="6a7c7-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="6a7c7-126">Azure Active Directory tarafından yönetilen bir yönetim API 'sinin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="6a7c7-127">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="6a7c7-127">-AdTenant</span></span>
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

### <span data-ttu-id="6a7c7-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="6a7c7-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="6a7c7-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="6a7c7-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="6a7c7-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="6a7c7-130">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="6a7c7-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a7c7-131">-GalleryEndpoint</span></span>
<span data-ttu-id="6a7c7-132">Kaynak grubu Galeri şablonlarını depolayan Azure Resource Manager galerisinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="6a7c7-133">Azure Kaynak grupları ve galeri şablonları hakkında daha fazla bilgi için Get-AzureResourceGroupGalleryTemplate yardım konusuna bakın https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="6a7c7-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

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

### <span data-ttu-id="6a7c7-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a7c7-134">-GraphEndpoint</span></span>
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

### <span data-ttu-id="6a7c7-135">-ManagementPortalUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="6a7c7-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="6a7c7-136">Yeni ortamdaki Azure yönetim portalının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="6a7c7-137">-Ad</span><span class="sxs-lookup"><span data-stu-id="6a7c7-137">-Name</span></span>
<span data-ttu-id="6a7c7-138">Ortamın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="6a7c7-139">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-139">This parameter is required.</span></span>
<span data-ttu-id="6a7c7-140">Varsayılan ortamların adlarını, Azurecsesli ve AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="6a7c7-141">-Profil</span><span class="sxs-lookup"><span data-stu-id="6a7c7-141">-Profile</span></span>
<span data-ttu-id="6a7c7-142">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="6a7c7-143">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6a7c7-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="6a7c7-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="6a7c7-145">Hesabınız için yayımlama ayarları dosyalarının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="6a7c7-146">Azure yayımlama ayarları dosyası, hesabınızla ilgili bilgileri içeren bir XML dosyasıdır ve Windows PowerShell 'in sizin adınıza Azure hesabınızda oturum açmasını sağlayan bir yönetim sertifikasıdır.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="6a7c7-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a7c7-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="6a7c7-148">Hesap ile ilişkili kaynak gruplarıyla ilgili veriler de içinde olmak üzere, Azure Resource Manager verilerinin uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="6a7c7-149">Azure Resource Manager hakkında daha fazla bilgi için [Azure Resource Manager cmdlet 'lerinin](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) ve [Kaynak Yöneticisi ile Windows PowerShell](https://go.microsoft.com/fwlink/?LinkID=394767)  'in ( https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="6a7c7-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="6a7c7-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a7c7-150">-ServiceEndpoint</span></span>
<span data-ttu-id="6a7c7-151">Azure hizmeti uç noktasının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="6a7c7-152">Azure hizmeti uç noktası, uygulamanızın Genel Azure platformu tarafından yönetilip yönetilmediğini, Çin 'de 21Vianet tarafından sağlanan Azure 'u veya özel bir Azure yüklemesini belirler.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="6a7c7-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="6a7c7-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="6a7c7-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="6a7c7-154">-StorageEndpoint</span></span>
<span data-ttu-id="6a7c7-155">Yeni ortamdaki depolama hizmetleri 'nin varsayılan uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-155">Specifies the default endpoint of storage services in the new environment.</span></span>

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

### <span data-ttu-id="6a7c7-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="6a7c7-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="6a7c7-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7c7-157">CommonParameters</span></span>
<span data-ttu-id="6a7c7-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7c7-159">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a7c7-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7c7-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6a7c7-160">INPUTS</span></span>

### <span data-ttu-id="6a7c7-161">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6a7c7-161">None</span></span>
<span data-ttu-id="6a7c7-162">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6a7c7-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="6a7c7-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6a7c7-163">OUTPUTS</span></span>

### <span data-ttu-id="6a7c7-164">Microsoft. Windowsazme. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a7c7-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="6a7c7-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6a7c7-165">NOTES</span></span>

## <span data-ttu-id="6a7c7-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6a7c7-166">RELATED LINKS</span></span>

[<span data-ttu-id="6a7c7-167">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a7c7-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="6a7c7-168">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a7c7-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="6a7c7-169">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="6a7c7-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


