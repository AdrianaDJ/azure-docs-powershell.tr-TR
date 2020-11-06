---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMDscExtension.md
ms.openlocfilehash: a7bffb3b1387c084ef3b29ad6feb3962c724278f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588969"
---
# <span data-ttu-id="62c64-101">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62c64-101">Set-AzureRmVMDscExtension</span></span>

## <span data-ttu-id="62c64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62c64-102">SYNOPSIS</span></span>
<span data-ttu-id="62c64-103">Bir sanal makinede DSC uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="62c64-103">Configures the DSC extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62c64-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62c64-104">SYNTAX</span></span>

```
Set-AzureRmVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62c64-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="62c64-105">DESCRIPTION</span></span>
<span data-ttu-id="62c64-106">**Set-AzureRmVMDscExtension** cmdlet 'i, kaynak grubundaki bir sanal makinede Windows PowerShell Istenen durum YAPıLANDıRMASı (DSC) uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="62c64-106">The **Set-AzureRmVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="62c64-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62c64-107">EXAMPLES</span></span>

### <span data-ttu-id="62c64-108">Örnek 1: DSC uzantısını ayarlama</span><span class="sxs-lookup"><span data-stu-id="62c64-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="62c64-109">Bu komut, Sample.ps1.zip VM07 adındaki sanal makinede, STG adlı depolama hesabından ve varsayılan kapsayıcıdaki DSC uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62c64-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="62c64-110">Komut ConfigName adındaki yapılandırmayı çağırır.</span><span class="sxs-lookup"><span data-stu-id="62c64-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="62c64-111">Sample.ps1.zip dosyası daha önce **Publish-AzureRmVMDscConfiguration** kullanılarak karşıya yüklendi.</span><span class="sxs-lookup"><span data-stu-id="62c64-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="62c64-112">Örnek 2: yapılandırma verileriyle bir DSC Uzantısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="62c64-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="62c64-113">Bu komut, VM13 adındaki sanal makinede, STG adlı depolama hesabından ve WindowsPowerShellDSC adlı kapsayıcıdaki Sample.ps1.zip indileceği uzantıyı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62c64-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="62c64-114">Komut ConfigName adlı yapılandırma ve yapılandırma verilerini ve bağımsız değişkenleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="62c64-115">Sample.ps1.zip dosyası daha önce **Publish-AzureRmVMDscConfiguration** kullanılarak karşıya yüklendi.</span><span class="sxs-lookup"><span data-stu-id="62c64-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

### <span data-ttu-id="62c64-116">Örnek 3: otomatik güncellemeli yapılandırma verileriyle DSC Uzantısı ayarlama</span><span class="sxs-lookup"><span data-stu-id="62c64-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzureRmVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="62c64-117">Bu komut, VM22 adındaki sanal makinede, STG adlı depolama hesabından ve WindowsPowerShellDSC adlı kapsayıcıdaki Sample.ps1.zip indileceği uzantıyı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62c64-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="62c64-118">Komut ConfigName adındaki yapılandırmayı başlatır ve yapılandırma verilerini ve bağımsız değişkenleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="62c64-119">Bu komut, otomatik genişletme işleyicisinin en son sürüme güncelleştirilmesini de olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="62c64-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="62c64-120">Sample.ps1.zip daha önce **Publish-AzureRmVMDscConfiguration** kullanılarak karşıya yüklendi.</span><span class="sxs-lookup"><span data-stu-id="62c64-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzureRmVMDscConfiguration**.</span></span>

## <span data-ttu-id="62c64-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62c64-121">PARAMETERS</span></span>

### <span data-ttu-id="62c64-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="62c64-122">-ArchiveBlobName</span></span>
<span data-ttu-id="62c64-123">Daha önce Publish-AzureRmVMDscConfiguration cmdlet 'i tarafından yüklenmiş olan yapılandırma dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzureRmVMDscConfiguration cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="62c64-124">-ArchiveContainerName</span></span>
<span data-ttu-id="62c64-125">Yapılandırma Arşivi bulunan Azure depolama kapsayıcısı türleri adı.</span><span class="sxs-lookup"><span data-stu-id="62c64-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c64-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="62c64-127">Yapılandırma arşivini içeren depolama hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="62c64-128">Depolama hesabı ve sanal makine aynı kaynak grubunda yer alıyorsa bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="62c64-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="62c64-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62c64-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="62c64-130">ArchiveBlobName indirmek için kullanılan Azure depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="62c64-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="62c64-132">Depolama uç noktası sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-133">-Otomatik güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="62c64-133">-AutoUpdate</span></span>
<span data-ttu-id="62c64-134">*Sürüm* parametresi tarafından belirtilen uzantı işleyicisi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="62c64-135">Varsayılan olarak uzantı işleyicisi otomatik güncelleştirme değildir.</span><span class="sxs-lookup"><span data-stu-id="62c64-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="62c64-136">Otomatik güncelleştirme *parametresini kullanarak, uzantı* işleyicisinin en son sürüme ve kullanılabilir olduğunda otomatik güncelleştirilmesini sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="62c64-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="62c64-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="62c64-137">-ConfigurationArgument</span></span>
<span data-ttu-id="62c64-138">Yapılandırma işlevinin bağımsız değişkenlerini içeren karma tabloyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="62c64-139">-ConfigurationData</span></span>
<span data-ttu-id="62c64-140">Yapılandırma verilerini belirten bir. psd1 dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="62c64-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="62c64-141">-ConfigurationName</span></span>
<span data-ttu-id="62c64-142">DSC uzantısının çağırkullandığı yapılandırmanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="62c64-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="62c64-143">-DataCollection</span></span>
<span data-ttu-id="62c64-144">Veri toplama türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-144">Specifies the data collection type.</span></span>
<span data-ttu-id="62c64-145">Bu parametre için kabul edilebilir değerler şunlardır: etkinleştir ve devre dışı bırak.</span><span class="sxs-lookup"><span data-stu-id="62c64-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-146">-Force</span><span class="sxs-lookup"><span data-stu-id="62c64-146">-Force</span></span>
<span data-ttu-id="62c64-147">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="62c64-147">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="62c64-148">-Konum</span><span class="sxs-lookup"><span data-stu-id="62c64-148">-Location</span></span>
<span data-ttu-id="62c64-149">Kaynak uzantısının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-149">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="62c64-150">-Ad</span><span class="sxs-lookup"><span data-stu-id="62c64-150">-Name</span></span>
<span data-ttu-id="62c64-151">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-151">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="62c64-152">Varsayılan değer Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="62c64-152">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="62c64-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c64-153">-ResourceGroupName</span></span>
<span data-ttu-id="62c64-154">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-154">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-155">-Version</span><span class="sxs-lookup"><span data-stu-id="62c64-155">-Version</span></span>
<span data-ttu-id="62c64-156">Set-AzureRmVMDscExtension ayarların uygulandığı DSC uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-156">Specifies the version of the DSC extension that Set-AzureRmVMDscExtension applies the settings to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="62c64-157">-VMName</span></span>
<span data-ttu-id="62c64-158">DSC genişletme işleyicisinin yüklü olduğu sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-158">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-159">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="62c64-159">-WmfVersion</span></span>
<span data-ttu-id="62c64-160">WMF sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c64-160">Specifies the WMF version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c64-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="62c64-161">-Confirm</span></span>
<span data-ttu-id="62c64-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62c64-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c64-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c64-163">-WhatIf</span></span>
<span data-ttu-id="62c64-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62c64-164">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="62c64-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62c64-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c64-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c64-166">CommonParameters</span></span>
<span data-ttu-id="62c64-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62c64-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c64-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c64-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c64-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62c64-169">INPUTS</span></span>

### <span data-ttu-id="62c64-170">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="62c64-170">None</span></span>
<span data-ttu-id="62c64-171">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="62c64-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62c64-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62c64-172">OUTPUTS</span></span>

## <span data-ttu-id="62c64-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62c64-173">NOTES</span></span>

## <span data-ttu-id="62c64-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62c64-174">RELATED LINKS</span></span>

[<span data-ttu-id="62c64-175">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62c64-175">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="62c64-176">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="62c64-176">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="62c64-177">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="62c64-177">Publish-AzureRmVMDscConfiguration</span></span>](./Publish-AzureRmVMDscConfiguration.md)


