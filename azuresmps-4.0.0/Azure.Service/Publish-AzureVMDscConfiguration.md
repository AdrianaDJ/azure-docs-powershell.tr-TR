---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105882"
---
# <span data-ttu-id="00647-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00647-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="00647-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00647-102">SYNOPSIS</span></span>
<span data-ttu-id="00647-103">Azure Blob depolaması için istenen bir durum yapılandırma betiği yayımlar.</span><span class="sxs-lookup"><span data-stu-id="00647-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="00647-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00647-104">SYNTAX</span></span>

### <span data-ttu-id="00647-105">UploadArchive (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00647-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00647-106">CreateArchive</span><span class="sxs-lookup"><span data-stu-id="00647-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00647-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="00647-107">DESCRIPTION</span></span>
<span data-ttu-id="00647-108">**Publish-AzureVMDscConfiguration** cmdlet 'i, daha sonra **set-AzureVMDscExtension** cmdlet 'i kullanılarak Azure sanal makinelerine uygulanabilecek, Azure Blob depolama alanına istenen bir durum yapılandırma betiği yayımlar.</span><span class="sxs-lookup"><span data-stu-id="00647-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="00647-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00647-109">EXAMPLES</span></span>

### <span data-ttu-id="00647-110">Örnek 1: blob depolaması için bir durum yapılandırma betiği yayımlama</span><span class="sxs-lookup"><span data-stu-id="00647-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="00647-111">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu Azure depolama birimine yükler.</span><span class="sxs-lookup"><span data-stu-id="00647-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="00647-112">Örnek 2: bir durum yapılandırma betiğini yerel bir dosyaya yayımlama</span><span class="sxs-lookup"><span data-stu-id="00647-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="00647-113">Bu komut, verilen komut dosyası ve tüm bağımlı kaynak modülleri için bir. zip paketi oluşturur ve bunu yerel dosya .\MyConfiguration.ps1.zip depolar.</span><span class="sxs-lookup"><span data-stu-id="00647-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="00647-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00647-114">PARAMETERS</span></span>

### <span data-ttu-id="00647-115">-Addiyolu</span><span class="sxs-lookup"><span data-stu-id="00647-115">-AdditionalPath</span></span>
<span data-ttu-id="00647-116">Ek yollar dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-116">Specifies an array of additional paths.</span></span>

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

### <span data-ttu-id="00647-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="00647-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="00647-118">Bu cmdlet 'in yapılandırma arşivini yazdığı yerel. zip dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="00647-119">Bu parametreyi kullanırsanız, yapılandırma betiği Azure Blob depolama 'ya yüklenmez.</span><span class="sxs-lookup"><span data-stu-id="00647-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00647-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="00647-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="00647-121">Yapılandırma veri yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="00647-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="00647-122">-ConfigurationPath</span></span>
<span data-ttu-id="00647-123">Bir veya daha fazla yapılandırma içeren dosyanın yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="00647-124">Dosya, bir Windows PowerShell komut dosyası (. ps1 dosyası), modül (. psm1 dosyası) veya bir Windows PowerShell modülü içeren bir arşiv (. zip dosyası) olabilir ve her modül ayrı bir dizinde yer alır.</span><span class="sxs-lookup"><span data-stu-id="00647-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00647-125">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="00647-125">-ContainerName</span></span>
<span data-ttu-id="00647-126">Yapılandırmanın karşıya yüklediği Azure depolama kapsayıcısı 'nın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="00647-127">-Force</span><span class="sxs-lookup"><span data-stu-id="00647-127">-Force</span></span>
<span data-ttu-id="00647-128">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="00647-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00647-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="00647-129">-InformationAction</span></span>
<span data-ttu-id="00647-130">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="00647-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="00647-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="00647-132">'A</span><span class="sxs-lookup"><span data-stu-id="00647-132">Continue</span></span>
- <span data-ttu-id="00647-133">Manıza</span><span class="sxs-lookup"><span data-stu-id="00647-133">Ignore</span></span>
- <span data-ttu-id="00647-134">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="00647-134">Inquire</span></span>
- <span data-ttu-id="00647-135">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="00647-135">SilentlyContinue</span></span>
- <span data-ttu-id="00647-136">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="00647-136">Stop</span></span>
- <span data-ttu-id="00647-137">Biliriz</span><span class="sxs-lookup"><span data-stu-id="00647-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00647-138">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="00647-138">-InformationVariable</span></span>
<span data-ttu-id="00647-139">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00647-140">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="00647-140">-PassThru</span></span>
<span data-ttu-id="00647-141">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="00647-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00647-142">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="00647-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="00647-143">-Profil</span><span class="sxs-lookup"><span data-stu-id="00647-143">-Profile</span></span>
<span data-ttu-id="00647-144">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00647-145">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="00647-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00647-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="00647-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="00647-147">Bu cmdlet 'in bağımlılık algılamasını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00647-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="00647-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="00647-148">-StorageContext</span></span>
<span data-ttu-id="00647-149">*ContainerName* parametresinde belirtilen kapsayıcıya yapılandırma betiğini yüklemek için kullanılan güvenlik ayarlarını sağlayan Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00647-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="00647-150">Bu bağlam, kapsayıcıya yazma erişimi sağlar.</span><span class="sxs-lookup"><span data-stu-id="00647-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00647-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="00647-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="00647-152">Depolama uç noktası için sonek belirtir; Örneğin, core.contoso.net</span><span class="sxs-lookup"><span data-stu-id="00647-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

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

### <span data-ttu-id="00647-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="00647-153">-Confirm</span></span>
<span data-ttu-id="00647-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00647-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00647-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00647-155">-WhatIf</span></span>
<span data-ttu-id="00647-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00647-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00647-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00647-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00647-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00647-158">CommonParameters</span></span>
<span data-ttu-id="00647-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00647-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00647-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00647-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00647-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00647-161">INPUTS</span></span>

## <span data-ttu-id="00647-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00647-162">OUTPUTS</span></span>

## <span data-ttu-id="00647-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00647-163">NOTES</span></span>

## <span data-ttu-id="00647-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00647-164">RELATED LINKS</span></span>

[<span data-ttu-id="00647-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="00647-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


