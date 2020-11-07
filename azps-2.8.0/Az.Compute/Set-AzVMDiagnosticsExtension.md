---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 13ED884A-6224-4BD4-9F12-F896932F7842
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDiagnosticsExtension.md
ms.openlocfilehash: ed3215d6ae5b4e6386dc1ee9fce951f8b036d39d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752692"
---
# <span data-ttu-id="2263b-101">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="2263b-101">Set-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="2263b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2263b-102">SYNOPSIS</span></span>
<span data-ttu-id="2263b-103">Sanal makinede Azure tanılama uzantısını yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="2263b-103">Configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="2263b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2263b-104">SYNTAX</span></span>

```
Set-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String>
 [-DiagnosticsConfigurationPath] <String> [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <IStorageContext>] [[-Location] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [[-AutoUpgradeMinorVersion] <Boolean>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2263b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2263b-105">DESCRIPTION</span></span>
<span data-ttu-id="2263b-106">**Set-Azvmdiagnosticsextenkomutçuğu** , Azure Diagnostics uzantısını bir sanal makinede yapılandırır.</span><span class="sxs-lookup"><span data-stu-id="2263b-106">The **Set-AzVMDiagnosticsExtension** cmdlet configures the Azure diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="2263b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2263b-107">EXAMPLES</span></span>

### <span data-ttu-id="2263b-108">Örnek 1: tanılama yapılandırma dosyasında belirtilen bir depolama hesabını kullanarak tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2263b-108">Example 1: Enable diagnostics using a storage account specified in a diagnostics configuration file</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml"
```

<span data-ttu-id="2263b-109">Bu komut, tanılamayı etkinleştirmek için bir tanılama yapılandırma dosyası kullanır.</span><span class="sxs-lookup"><span data-stu-id="2263b-109">This command uses a diagnostics configuration file to enable diagnostics.</span></span>
<span data-ttu-id="2263b-110">Dosya diagnostics_publicconfig.xml, tanılama uzantısının gönderileceği depolama hesabının adı da dahil olmak üzere, tanılama uzantısının genel XML yapılandırmasını içerir.</span><span class="sxs-lookup"><span data-stu-id="2263b-110">The file diagnostics_publicconfig.xml contains the public XML configuration for the diagnostics extension including the name of the storage account to which diagnostics data will be sent.</span></span>
<span data-ttu-id="2263b-111">Tanılama depolama hesabı sanal makineyle aynı abonelikte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2263b-111">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="2263b-112">Örnek 2: depolama hesabı adını kullanarak tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2263b-112">Example 2: Enable diagnostics using a storage account name</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup1" -VMName "VirtualMachine2" -DiagnosticsConfigurationPath diagnostics_publicconfig.xml -StorageAccountName "MyStorageAccount"
```

<span data-ttu-id="2263b-113">Bu komut, tanılamayı etkinleştirmek için depolama hesabı adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="2263b-113">This command uses the storage account name to enable diagnostics.</span></span>
<span data-ttu-id="2263b-114">Tanılama yapılandırması bir depolama hesabı adı belirtmezse veya yapılandırma dosyasında belirtilen tanılama depolama hesabı adını geçersiz kılmak istiyorsanız, *storageAccountName* parametresini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2263b-114">If the diagnostics configuration does not specify a storage account name or if you want to override the diagnostics storage account name specified in the configuration file, use the *StorageAccountName* parameter.</span></span>
<span data-ttu-id="2263b-115">Tanılama depolama hesabı sanal makineyle aynı abonelikte olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2263b-115">The diagnostics storage account must be in the same subscription as the virtual machine.</span></span>

### <span data-ttu-id="2263b-116">Örnek 3: depolama hesabı adı ve anahtarı kullanarak tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="2263b-116">Example 3: Enable diagnostics using storage account name and key</span></span>
```
PS C:\> Set-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup01" -VMName "VirtualMachine02" -DiagnosticsConfigurationPath "diagnostics_publicconfig.xml" -StorageAccountName "MyStorageAccount" -StorageAccountKey $storage_key
```

<span data-ttu-id="2263b-117">Bu komut, tanılama 'yı etkinleştirmek için depolama hesabı adını ve anahtarını kullanır.</span><span class="sxs-lookup"><span data-stu-id="2263b-117">This command uses the storage account name and key to enable diagnostics.</span></span>
<span data-ttu-id="2263b-118">Tanılama depolama hesabı sanal makineden farklı bir abonedeyken, adını ve anahtarını açıkça belirterek tanılama verilerini bu depolama hesabına göndermeyi etkinleştir.</span><span class="sxs-lookup"><span data-stu-id="2263b-118">If the diagnostics storage account is in a different subscription than the virtual machine then enable sending diagnostics data to that storage account by explicitly specifying its name and key.</span></span>

## <span data-ttu-id="2263b-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2263b-119">PARAMETERS</span></span>

### <span data-ttu-id="2263b-120">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2263b-120">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2263b-121">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesine izin verip vermediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="2263b-121">Indicates whether this cmdlet allows the Azure guest agent to automatically update the extension to a newer minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2263b-122">-DefaultProfile</span></span>
<span data-ttu-id="2263b-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2263b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2263b-124">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="2263b-124">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="2263b-125">Yapılandırma dosyasının yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-125">Specifies the path of the configuration file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-126">-Konum</span><span class="sxs-lookup"><span data-stu-id="2263b-126">-Location</span></span>
<span data-ttu-id="2263b-127">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-127">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="2263b-128">-Name</span></span>
<span data-ttu-id="2263b-129">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-129">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2263b-130">-NoWait</span></span>
<span data-ttu-id="2263b-131">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="2263b-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2263b-132">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="2263b-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2263b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2263b-133">-ResourceGroupName</span></span>
<span data-ttu-id="2263b-134">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-135">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="2263b-135">-StorageAccountEndpoint</span></span>
<span data-ttu-id="2263b-136">Depolama hesabı uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-136">Specifies the storage account endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-137">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2263b-137">-StorageAccountKey</span></span>
<span data-ttu-id="2263b-138">Depolama hesabı anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-138">Specifies the storage account key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2263b-139">-StorageAccountName</span></span>
<span data-ttu-id="2263b-140">Depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-140">Specifies the storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-141">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="2263b-141">-StorageContext</span></span>
<span data-ttu-id="2263b-142">Azure depolama bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-142">Specifies the Azure storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-143">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2263b-143">-TypeHandlerVersion</span></span>
<span data-ttu-id="2263b-144">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-144">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2263b-145">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2263b-145">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="2263b-146">-VMName</span></span>
<span data-ttu-id="2263b-147">Bu cmdlet 'in üzerinde çalıştırıldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2263b-147">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2263b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2263b-148">CommonParameters</span></span>
<span data-ttu-id="2263b-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2263b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2263b-150">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2263b-150">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2263b-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2263b-151">INPUTS</span></span>

### <span data-ttu-id="2263b-152">System. String</span><span class="sxs-lookup"><span data-stu-id="2263b-152">System.String</span></span>

### <span data-ttu-id="2263b-153">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="2263b-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="2263b-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2263b-154">System.Boolean</span></span>

## <span data-ttu-id="2263b-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2263b-155">OUTPUTS</span></span>

### <span data-ttu-id="2263b-156">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2263b-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2263b-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2263b-157">NOTES</span></span>

## <span data-ttu-id="2263b-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2263b-158">RELATED LINKS</span></span>

[<span data-ttu-id="2263b-159">Get-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="2263b-159">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="2263b-160">Get-Azvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="2263b-160">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="2263b-161">Remove-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="2263b-161">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)


