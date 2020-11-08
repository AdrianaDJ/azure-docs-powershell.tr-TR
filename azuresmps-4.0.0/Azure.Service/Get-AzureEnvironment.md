---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106352"
---
# <span data-ttu-id="bf4c0-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4c0-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="bf4c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="bf4c0-103">Azure ortamlarını alır</span><span class="sxs-lookup"><span data-stu-id="bf4c0-103">Gets Azure environments</span></span>

## <span data-ttu-id="bf4c0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf4c0-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bf4c0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf4c0-105">DESCRIPTION</span></span>
<span data-ttu-id="bf4c0-106">**Get-AzureEnvironment** cmdlet 'ı Windows PowerShell 'In kullanabildiği Azure ortamlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="bf4c0-107">Bir Azure ortamında, Çin 'de 21Vianet tarafından sağlanan, genel Azure ve Azure için AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="bf4c0-108">Ayrıca, Azure paketini ve WAPack cmdlet 'lerini kullanarak şirket içi Azure ortamları oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="bf4c0-109">Daha fazla bilgi için bkz: [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="bf4c0-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="bf4c0-110">**Get-AzureEnvironment** cmdlet 'i Azure 'dan değil, abonelik veri dosyanızdaki ortamları alır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="bf4c0-111">Abonelik verileri dosyası güncel değilse, bunu yenilemek için **Add-AzureAccount** veya **Import-publishsettingsfile** cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="bf4c0-112">Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bf4c0-113">Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bf4c0-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="bf4c0-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf4c0-114">EXAMPLES</span></span>

### <span data-ttu-id="bf4c0-115">Örnek 1: tüm ortamları alma</span><span class="sxs-lookup"><span data-stu-id="bf4c0-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="bf4c0-116">Bu komut Windows PowerShell 'in kullanabildiği tüm ortamları alır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="bf4c0-117">Örnek 2: ada göre ortam alma</span><span class="sxs-lookup"><span data-stu-id="bf4c0-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="bf4c0-118">Bu örnekte, Azurecyüksek ortamı alınır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="bf4c0-119">Örnek 3: tüm ortamlardaki tüm özellikleri alma</span><span class="sxs-lookup"><span data-stu-id="bf4c0-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="bf4c0-120">Bu komut, tüm ortamların tüm özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="bf4c0-121">Komut **Get-AzureEnvironment** cmdlet 'ini kullanarak bu hesabın tüm Azure ortamlarını alır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="bf4c0-122">Ardından, her ortamdaki **Name** parametresiyle **Get-AzureEnvironment** komutunu çalıştırmak için **ForEach-Object** cmdlet 'ini kullanır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="bf4c0-123">**Name** parametresinin değeri, her ortamın **environmentname** özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="bf4c0-124">Parametresiz, **Get-AzureEnvironment** , bir ortamın yalnızca seçili özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="bf4c0-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf4c0-125">PARAMETERS</span></span>

### <span data-ttu-id="bf4c0-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf4c0-126">-Name</span></span>
<span data-ttu-id="bf4c0-127">Yalnızca belirtilen ortamı alır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-127">Gets only the specified environment.</span></span>
<span data-ttu-id="bf4c0-128">Ortam adını yazın.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-128">Type the environment name.</span></span>
<span data-ttu-id="bf4c0-129">Parametre değeri büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="bf4c0-130">Joker karakterler kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="bf4c0-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="bf4c0-131">-Profile</span></span>
<span data-ttu-id="bf4c0-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bf4c0-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf4c0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf4c0-134">CommonParameters</span></span>
<span data-ttu-id="bf4c0-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf4c0-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf4c0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf4c0-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf4c0-137">INPUTS</span></span>

### <span data-ttu-id="bf4c0-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bf4c0-138">None</span></span>
<span data-ttu-id="bf4c0-139">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="bf4c0-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf4c0-140">OUTPUTS</span></span>

### <span data-ttu-id="bf4c0-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="bf4c0-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="bf4c0-142">Varsayılan olarak **Get-AzureEnvironment** , özel bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="bf4c0-143">Microsoft. Windowsazme. Commands. Utilities. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4c0-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="bf4c0-144">**Name** parametresiyle **Get-AzureEnvironment** 'ı çalıştırdığınızda, bir **windowsazureenvironment** nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="bf4c0-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="bf4c0-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf4c0-145">NOTES</span></span>

## <span data-ttu-id="bf4c0-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf4c0-146">RELATED LINKS</span></span>

[<span data-ttu-id="bf4c0-147">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="bf4c0-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="bf4c0-148">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4c0-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="bf4c0-149">Get-Azuikinci dosyayı</span><span class="sxs-lookup"><span data-stu-id="bf4c0-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="bf4c0-150">Import-Azuyeniden yayımlayan ayarları dosyası</span><span class="sxs-lookup"><span data-stu-id="bf4c0-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="bf4c0-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4c0-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="bf4c0-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="bf4c0-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


