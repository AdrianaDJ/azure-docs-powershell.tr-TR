---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Publish-AzureRmVMDscConfiguration.md
ms.openlocfilehash: 49dc91288c955de10c3dbcb84da74ffd3d71f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572890"
---
# <span data-ttu-id="4a72d-101">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a72d-101">Publish-AzureRmVMDscConfiguration</span></span>

## <span data-ttu-id="4a72d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a72d-102">SYNOPSIS</span></span>
<span data-ttu-id="4a72d-103">DSC betiğini Azure Blob depolama alanına yükler.</span><span class="sxs-lookup"><span data-stu-id="4a72d-103">Uploads a DSC script to Azure blob storage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a72d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a72d-104">SYNTAX</span></span>

### <span data-ttu-id="4a72d-105">UploadArchive (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a72d-105">UploadArchive (Default)</span></span>
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4a72d-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="4a72d-106">CreateArchive</span></span>
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a72d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a72d-107">DESCRIPTION</span></span>
<span data-ttu-id="4a72d-108">**Publish-AzureRmVMDscConfiguration** cmdlet 'i, daha sonra Set-AzureRmVMDscExtension cmdlet kullanılarak Azure sanal makinelere uygulanabilecek Azure Blob depolama alanına Istenen bir durum YAPıLANDıRMASı (DSC) kodu yükler.</span><span class="sxs-lookup"><span data-stu-id="4a72d-108">The **Publish-AzureRmVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzureRmVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="4a72d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a72d-109">EXAMPLES</span></span>

### <span data-ttu-id="4a72d-110">Örnek 1:. zip paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="4a72d-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="4a72d-111">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu Azure depolama birimine yükler.</span><span class="sxs-lookup"><span data-stu-id="4a72d-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="4a72d-112">Örnek 2:. zip paketi oluşturma ve yerel dosyaya depolama</span><span class="sxs-lookup"><span data-stu-id="4a72d-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="4a72d-113">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu .\MyConfiguration.ps1.zip adlı yerel dosyada depolar.</span><span class="sxs-lookup"><span data-stu-id="4a72d-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="4a72d-114">Örnek 3: arşive yapılandırma ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="4a72d-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="4a72d-115">Bu Sample.ps1 komut, Azure depolama 'ya yüklemek ve bağımlı kaynak modüllerini atlar.</span><span class="sxs-lookup"><span data-stu-id="4a72d-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="4a72d-116">Örnek 4: arşive yapılandırma ve yapılandırma verileri ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="4a72d-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="4a72d-117">Bu komut, Azure depolama 'ya yüklemek için yapılandırma arşivine SampleData.psd1 adlı Sample.ps1 adlı yapılandırmayı ekler.</span><span class="sxs-lookup"><span data-stu-id="4a72d-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="4a72d-118">Örnek 5: arşive yapılandırma, yapılandırma verileri ve ek içerik ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="4a72d-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="4a72d-119">Bu komut Sample.ps1, yapılandırma verileri SampleData.psd1 adlı yapılandırmayı ve Azure depolama 'ya yüklenecek yapılandırma arşivine ek içeriği ekler.</span><span class="sxs-lookup"><span data-stu-id="4a72d-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="4a72d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a72d-120">PARAMETERS</span></span>

### <span data-ttu-id="4a72d-121">-Addiyolu</span><span class="sxs-lookup"><span data-stu-id="4a72d-121">-AdditionalPath</span></span>
<span data-ttu-id="4a72d-122">Yapılandırma arşivine eklenecek dosyanın veya dizinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="4a72d-123">Yapılandırmayla birlikte sanal makineye indirilir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="4a72d-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="4a72d-125">Yapılandırma verilerini belirten bir. psd1 dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="4a72d-126">Bu, yapılandırma arşivine eklenir ve ardından yapılandırma işlevine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="4a72d-127">Set-AzureRmVMDscExtension cmdlet ile sağlanan yapılandırma veri yolunun üzerine yazılır</span><span class="sxs-lookup"><span data-stu-id="4a72d-127">It gets overwritten by the configuration data path provided through the Set-AzureRmVMDscExtension cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="4a72d-128">-ConfigurationPath</span></span>
<span data-ttu-id="4a72d-129">Bir veya daha fazla yapılandırma içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="4a72d-130">Dosya bir Windows PowerShell betik (. ps1) dosyası veya Windows PowerShell modülü (. psm1) dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-131">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="4a72d-131">-ContainerName</span></span>
<span data-ttu-id="4a72d-132">Yapılandırmanın karşıya yüklediği Azure depolama kapsayıcısı 'nın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a72d-133">-DefaultProfile</span></span>
<span data-ttu-id="4a72d-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a72d-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-135">-Force</span><span class="sxs-lookup"><span data-stu-id="4a72d-135">-Force</span></span>
<span data-ttu-id="4a72d-136">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4a72d-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="4a72d-137">-OutputArchivePath</span></span>
<span data-ttu-id="4a72d-138">Yapılandırma Arşivi yazılacak yerel. zip dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="4a72d-139">Bu parametre kullanıldığında, yapılandırma betiği Azure Blob depolama alanına yüklenmez.</span><span class="sxs-lookup"><span data-stu-id="4a72d-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a72d-140">-ResourceGroupName</span></span>
<span data-ttu-id="4a72d-141">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="4a72d-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="4a72d-143">Bu cmdlet 'in DSC Kaynak bağımlılıklarını yapılandırma arşivinden dışarıda tutuyorsa gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4a72d-144">-StorageAccountName</span></span>
<span data-ttu-id="4a72d-145">*ContainerName* parametresinde belirtilen kapsayıcıya yapılandırma betiğini yüklemek Için kullanılan Azure depolama hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4a72d-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="4a72d-147">Depolama uç noktasının sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="4a72d-148">-Confirm</span></span>
<span data-ttu-id="4a72d-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4a72d-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a72d-150">-WhatIf</span></span>
<span data-ttu-id="4a72d-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4a72d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a72d-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4a72d-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a72d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a72d-153">CommonParameters</span></span>
<span data-ttu-id="4a72d-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a72d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a72d-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a72d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a72d-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a72d-156">INPUTS</span></span>

### <span data-ttu-id="4a72d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="4a72d-157">System.String</span></span>

### <span data-ttu-id="4a72d-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="4a72d-158">System.String[]</span></span>

## <span data-ttu-id="4a72d-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a72d-159">OUTPUTS</span></span>

### <span data-ttu-id="4a72d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="4a72d-160">System.String</span></span>

## <span data-ttu-id="4a72d-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a72d-161">NOTES</span></span>

## <span data-ttu-id="4a72d-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a72d-162">RELATED LINKS</span></span>

[<span data-ttu-id="4a72d-163">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4a72d-163">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="4a72d-164">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4a72d-164">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="4a72d-165">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="4a72d-165">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


