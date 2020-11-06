---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: d93fd01fb178f093b6ed5527cca0c018cebe4f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591712"
---
# <span data-ttu-id="6ad9c-101">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6ad9c-101">Set-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="6ad9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad9c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad9c-103">Sanal makinede Azure tanılama uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ad9c-104">SYNTAX</span></span>

```
Set-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ad9c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ad9c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ad9c-106">**Set-Azurermvmdiagnosticsextenma** cmdlet 'i sanal makinede Azure tanılama uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-106">The **Set-AzureRmVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="6ad9c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ad9c-107">EXAMPLES</span></span>

### <span data-ttu-id="6ad9c-108">Örnek 1: tanılama yapılandırma dosyasında belirtilen bir depolama hesabını kullanarak tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6ad9c-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="6ad9c-109">Bu komut, tanılamayı etkinleştirmek için bir tanılama yapılandırma dosyası kullanır.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="6ad9c-110">Dosya diagnostics_publicconfig.xml, tanılama uzantısının gönderileceği depolama hesabının adı da dahil olmak üzere, tanılama uzantısının genel XML yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="6ad9c-111">Tanılama depolama hesabı sanal makineyle aynı abonelikte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="6ad9c-112">Örnek 2: depolama hesabı adını kullanarak tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6ad9c-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="6ad9c-113">Bu komut, tanılamayı etkinleştirmek için depolama hesabı adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="6ad9c-114">Tanılama yapılandırması bir depolama hesabı adı belirtmezse veya yapılandırma dosyasında belirtilen tanılama depolama hesabı adını geçersiz kılmak istiyorsanız, *storageAccountName* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="6ad9c-115">Tanılama depolama hesabı sanal makineyle aynı abonelikte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="6ad9c-116">Örnek 3: depolama hesabı adı ve anahtarı kullanarak tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="6ad9c-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="6ad9c-117">Bu komut, tanılama 'yı etkinleştirmek için depolama hesabı adını ve anahtarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="6ad9c-118">Tanılama depolama hesabı sanal makineden farklı bir abonedeyken, adını ve anahtarını açıkça belirterek tanılama verilerini bu depolama hesabına göndermeyi etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="6ad9c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ad9c-119">PARAMETERS</span></span>

### <span data-ttu-id="6ad9c-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6ad9c-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6ad9c-121">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesine izin verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="6ad9c-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="6ad9c-123">Yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-123">Specifies the path of the configuration file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="6ad9c-124">-Location</span></span>
<span data-ttu-id="6ad9c-125">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-125">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ad9c-126">-Name</span></span>
<span data-ttu-id="6ad9c-127">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-127">Specifies the name of an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad9c-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ad9c-129">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-130">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="6ad9c-130">-StorageAccountEndpoint</span></span>
<span data-ttu-id="6ad9c-131">Depolama hesabı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-131">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6ad9c-132">-StorageAccountKey</span></span>
<span data-ttu-id="6ad9c-133">Depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-133">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6ad9c-134">-StorageAccountName</span></span>
<span data-ttu-id="6ad9c-135">Depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-135">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-136">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="6ad9c-136">-StorageContext</span></span>
<span data-ttu-id="6ad9c-137">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-137">Specifies the Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-138">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6ad9c-138">-TypeHandlerVersion</span></span>
<span data-ttu-id="6ad9c-139">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-139">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="6ad9c-140">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzureRmVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-140">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="6ad9c-141">-VMName</span></span>
<span data-ttu-id="6ad9c-142">Bu cmdlet 'in üzerinde çalıştırıldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-142">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ad9c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad9c-143">CommonParameters</span></span>
<span data-ttu-id="6ad9c-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad9c-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad9c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad9c-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ad9c-146">INPUTS</span></span>

### <span data-ttu-id="6ad9c-147">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ad9c-147">None</span></span>
<span data-ttu-id="6ad9c-148">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6ad9c-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ad9c-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ad9c-149">OUTPUTS</span></span>

## <span data-ttu-id="6ad9c-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ad9c-150">NOTES</span></span>

## <span data-ttu-id="6ad9c-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ad9c-151">RELATED LINKS</span></span>

[<span data-ttu-id="6ad9c-152">Get-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="6ad9c-152">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="6ad9c-153">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="6ad9c-153">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="6ad9c-154">Remove-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="6ad9c-154">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)


