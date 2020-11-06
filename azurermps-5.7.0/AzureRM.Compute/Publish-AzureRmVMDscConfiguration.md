---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
ms.openlocfilehash: ed65956b777ca760be3034f656c25d6c86e5aa3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586798"
---
# <span data-ttu-id="6df22-101">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6df22-101">Publish-AzureRmVMDscConfiguration</span></span>

## <span data-ttu-id="6df22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6df22-102">SYNOPSIS</span></span>
<span data-ttu-id="6df22-103">DSC betiğini Azure Blob depolama alanına yükler.</span><span class="sxs-lookup"><span data-stu-id="6df22-103">Uploads a DSC script to Azure blob storage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6df22-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6df22-104">SYNTAX</span></span>

### <span data-ttu-id="6df22-105">UploadArchive (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6df22-105">UploadArchive (Default)</span></span>
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6df22-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="6df22-106">CreateArchive</span></span>
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6df22-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6df22-107">DESCRIPTION</span></span>
<span data-ttu-id="6df22-108">**Publish-AzureRmVMDscConfiguration** cmdlet 'i, daha sonra Set-AzureRmVMDscExtension cmdlet kullanılarak Azure sanal makinelere uygulanabilecek Azure Blob depolama alanına Istenen bir durum YAPıLANDıRMASı (DSC) kodu yükler.</span><span class="sxs-lookup"><span data-stu-id="6df22-108">The **Publish-AzureRmVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzureRmVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="6df22-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6df22-109">EXAMPLES</span></span>

### <span data-ttu-id="6df22-110">Örnek 1:. zip paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="6df22-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="6df22-111">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu Azure depolama birimine yükler.</span><span class="sxs-lookup"><span data-stu-id="6df22-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="6df22-112">Örnek 2:. zip paketi oluşturma ve yerel dosyaya depolama</span><span class="sxs-lookup"><span data-stu-id="6df22-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="6df22-113">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu .\MyConfiguration.ps1.zip adlı yerel dosyada depolar.</span><span class="sxs-lookup"><span data-stu-id="6df22-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="6df22-114">Örnek 3: arşive yapılandırma ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="6df22-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="6df22-115">Bu Sample.ps1 komut, Azure depolama 'ya yüklemek ve bağımlı kaynak modüllerini atlar.</span><span class="sxs-lookup"><span data-stu-id="6df22-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="6df22-116">Örnek 4: arşive yapılandırma ve yapılandırma verileri ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="6df22-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="6df22-117">Bu komut, Azure depolama 'ya yüklemek için yapılandırma arşivine SampleData.psd1 adlı Sample.ps1 adlı yapılandırmayı ekler.</span><span class="sxs-lookup"><span data-stu-id="6df22-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="6df22-118">Örnek 5: arşive yapılandırma, yapılandırma verileri ve ek içerik ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="6df22-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="6df22-119">Bu komut Sample.ps1, yapılandırma verileri SampleData.psd1 adlı yapılandırmayı ve Azure depolama 'ya yüklenecek yapılandırma arşivine ek içeriği ekler.</span><span class="sxs-lookup"><span data-stu-id="6df22-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="6df22-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6df22-120">PARAMETERS</span></span>

### <span data-ttu-id="6df22-121">-Addiyolu</span><span class="sxs-lookup"><span data-stu-id="6df22-121">-AdditionalPath</span></span>
<span data-ttu-id="6df22-122">Yapılandırma arşivine eklenecek dosyanın veya dizinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="6df22-123">Yapılandırmayla birlikte sanal makineye indirilir.</span><span class="sxs-lookup"><span data-stu-id="6df22-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="6df22-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="6df22-125">Yapılandırma verilerini belirten bir. psd1 dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="6df22-126">Bu, yapılandırma arşivine eklenir ve ardından yapılandırma işlevine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="6df22-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="6df22-127">Set-AzureRmVMDscExtension cmdlet ile sağlanan yapılandırma veri yolunun üzerine yazılır</span><span class="sxs-lookup"><span data-stu-id="6df22-127">It gets overwritten by the configuration data path provided through the Set-AzureRmVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="6df22-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="6df22-128">-ConfigurationPath</span></span>
<span data-ttu-id="6df22-129">Bir veya daha fazla yapılandırma içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="6df22-130">Dosya bir Windows PowerShell betik (. ps1) dosyası veya Windows PowerShell modülü (. psm1) dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="6df22-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-131">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="6df22-131">-ContainerName</span></span>
<span data-ttu-id="6df22-132">Yapılandırmanın karşıya yüklediği Azure depolama kapsayıcısı 'nın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-133">-Force</span><span class="sxs-lookup"><span data-stu-id="6df22-133">-Force</span></span>
<span data-ttu-id="6df22-134">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="6df22-134">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-135">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="6df22-135">-OutputArchivePath</span></span>
<span data-ttu-id="6df22-136">Yapılandırma Arşivi yazılacak yerel. zip dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-136">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="6df22-137">Bu parametre kullanıldığında, yapılandırma betiği Azure Blob depolama alanına yüklenmez.</span><span class="sxs-lookup"><span data-stu-id="6df22-137">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6df22-138">-ResourceGroupName</span></span>
<span data-ttu-id="6df22-139">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-139">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-140">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="6df22-140">-SkipDependencyDetection</span></span>
<span data-ttu-id="6df22-141">Bu cmdlet 'in DSC Kaynak bağımlılıklarını yapılandırma arşivinden dışarıda tutuyorsa gösterir.</span><span class="sxs-lookup"><span data-stu-id="6df22-141">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-142">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6df22-142">-StorageAccountName</span></span>
<span data-ttu-id="6df22-143">*ContainerName* parametresinde belirtilen kapsayıcıya yapılandırma betiğini yüklemek Için kullanılan Azure depolama hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-143">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-144">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="6df22-144">-StorageEndpointSuffix</span></span>
<span data-ttu-id="6df22-145">Depolama uç noktasının sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6df22-145">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="6df22-146">-Confirm</span></span>
<span data-ttu-id="6df22-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6df22-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6df22-148">-WhatIf</span></span>
<span data-ttu-id="6df22-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6df22-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6df22-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6df22-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6df22-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6df22-151">CommonParameters</span></span>
<span data-ttu-id="6df22-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6df22-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6df22-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6df22-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6df22-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6df22-154">INPUTS</span></span>

### <span data-ttu-id="6df22-155">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6df22-155">None</span></span>
<span data-ttu-id="6df22-156">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6df22-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6df22-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6df22-157">OUTPUTS</span></span>

## <span data-ttu-id="6df22-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6df22-158">NOTES</span></span>

## <span data-ttu-id="6df22-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6df22-159">RELATED LINKS</span></span>

[<span data-ttu-id="6df22-160">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6df22-160">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="6df22-161">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6df22-161">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="6df22-162">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="6df22-162">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


