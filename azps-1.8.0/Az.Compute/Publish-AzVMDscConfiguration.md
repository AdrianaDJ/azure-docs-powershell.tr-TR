---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 7b8e770a37b7f196878d1650f20d08ee382f6008
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761295"
---
# <span data-ttu-id="e8f6e-101">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8f6e-101">Publish-AzVMDscConfiguration</span></span>

## <span data-ttu-id="e8f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f6e-103">DSC betiğini Azure Blob depolama alanına yükler.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-103">Uploads a DSC script to Azure blob storage.</span></span>

## <span data-ttu-id="e8f6e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8f6e-104">SYNTAX</span></span>

### <span data-ttu-id="e8f6e-105">UploadArchive (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8f6e-105">UploadArchive (Default)</span></span>
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f6e-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="e8f6e-106">CreateArchive</span></span>
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f6e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8f6e-107">DESCRIPTION</span></span>
<span data-ttu-id="e8f6e-108">**Publish-AzVMDscConfiguration** cmdlet 'i Azure Blob depolama 'ya, daha sonra Set-AzVMDscExtension cmdlet kullanılarak Azure sanal makinelere uygulanabilecek bir Istenen durum YAPıLANDıRMASı (DSC) kodu yükler.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-108">The **Publish-AzVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="e8f6e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8f6e-109">EXAMPLES</span></span>

### <span data-ttu-id="e8f6e-110">Örnek 1:. zip paketi oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8f6e-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="e8f6e-111">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu Azure depolama birimine yükler.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="e8f6e-112">Örnek 2:. zip paketi oluşturma ve yerel dosyaya depolama</span><span class="sxs-lookup"><span data-stu-id="e8f6e-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="e8f6e-113">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu .\MyConfiguration.ps1.zip adlı yerel dosyada depolar.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="e8f6e-114">Örnek 3: arşive yapılandırma ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="e8f6e-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="e8f6e-115">Bu Sample.ps1 komut, Azure depolama 'ya yüklemek ve bağımlı kaynak modüllerini atlar.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="e8f6e-116">Örnek 4: arşive yapılandırma ve yapılandırma verileri ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="e8f6e-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="e8f6e-117">Bu komut, Azure depolama 'ya yüklemek için yapılandırma arşivine SampleData.psd1 adlı Sample.ps1 adlı yapılandırmayı ekler.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="e8f6e-118">Örnek 5: arşive yapılandırma, yapılandırma verileri ve ek içerik ekleme ve ardından depolama birimine yükleme</span><span class="sxs-lookup"><span data-stu-id="e8f6e-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="e8f6e-119">Bu komut Sample.ps1, yapılandırma verileri SampleData.psd1 adlı yapılandırmayı ve Azure depolama 'ya yüklenecek yapılandırma arşivine ek içeriği ekler.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="e8f6e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8f6e-120">PARAMETERS</span></span>

### <span data-ttu-id="e8f6e-121">-Addiyolu</span><span class="sxs-lookup"><span data-stu-id="e8f6e-121">-AdditionalPath</span></span>
<span data-ttu-id="e8f6e-122">Yapılandırma arşivine eklenecek dosyanın veya dizinin yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="e8f6e-123">Yapılandırmayla birlikte sanal makineye indirilir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

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

### <span data-ttu-id="e8f6e-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="e8f6e-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="e8f6e-125">Yapılandırma verilerini belirten bir. psd1 dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="e8f6e-126">Bu, yapılandırma arşivine eklenir ve ardından yapılandırma işlevine geçirilir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="e8f6e-127">Set-AzVMDscExtension cmdlet ile sağlanan yapılandırma veri yolunun üzerine yazılır</span><span class="sxs-lookup"><span data-stu-id="e8f6e-127">It gets overwritten by the configuration data path provided through the Set-AzVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="e8f6e-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="e8f6e-128">-ConfigurationPath</span></span>
<span data-ttu-id="e8f6e-129">Bir veya daha fazla yapılandırma içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="e8f6e-130">Dosya bir Windows PowerShell betik (. ps1) dosyası veya Windows PowerShell modülü (. psm1) dosyası olabilir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

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

### <span data-ttu-id="e8f6e-131">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="e8f6e-131">-ContainerName</span></span>
<span data-ttu-id="e8f6e-132">Yapılandırmanın karşıya yüklediği Azure depolama kapsayıcısı 'nın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="e8f6e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f6e-133">-DefaultProfile</span></span>
<span data-ttu-id="e8f6e-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f6e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="e8f6e-135">-Force</span></span>
<span data-ttu-id="e8f6e-136">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e8f6e-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="e8f6e-137">-OutputArchivePath</span></span>
<span data-ttu-id="e8f6e-138">Yapılandırma Arşivi yazılacak yerel. zip dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="e8f6e-139">Bu parametre kullanıldığında, yapılandırma betiği Azure Blob depolama alanına yüklenmez.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

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

### <span data-ttu-id="e8f6e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f6e-140">-ResourceGroupName</span></span>
<span data-ttu-id="e8f6e-141">Depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-141">Specifies the name of the resource group that contains the storage account.</span></span>

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

### <span data-ttu-id="e8f6e-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="e8f6e-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="e8f6e-143">Bu cmdlet 'in DSC Kaynak bağımlılıklarını yapılandırma arşivinden dışarıda tutuyorsa gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="e8f6e-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e8f6e-144">-StorageAccountName</span></span>
<span data-ttu-id="e8f6e-145">*ContainerName* parametresinde belirtilen kapsayıcıya yapılandırma betiğini yüklemek Için kullanılan Azure depolama hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

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

### <span data-ttu-id="e8f6e-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e8f6e-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="e8f6e-147">Depolama uç noktasının sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-147">Specifies the suffix for the storage end point.</span></span>

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

### <span data-ttu-id="e8f6e-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8f6e-148">-Confirm</span></span>
<span data-ttu-id="e8f6e-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f6e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f6e-150">-WhatIf</span></span>
<span data-ttu-id="e8f6e-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f6e-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f6e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f6e-153">CommonParameters</span></span>
<span data-ttu-id="e8f6e-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8f6e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f6e-155">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f6e-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f6e-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8f6e-156">INPUTS</span></span>

### <span data-ttu-id="e8f6e-157">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f6e-157">System.String</span></span>

### <span data-ttu-id="e8f6e-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="e8f6e-158">System.String[]</span></span>

## <span data-ttu-id="e8f6e-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8f6e-159">OUTPUTS</span></span>

### <span data-ttu-id="e8f6e-160">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f6e-160">System.String</span></span>

## <span data-ttu-id="e8f6e-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8f6e-161">NOTES</span></span>

## <span data-ttu-id="e8f6e-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8f6e-162">RELATED LINKS</span></span>

[<span data-ttu-id="e8f6e-163">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e8f6e-163">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="e8f6e-164">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e8f6e-164">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="e8f6e-165">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e8f6e-165">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


