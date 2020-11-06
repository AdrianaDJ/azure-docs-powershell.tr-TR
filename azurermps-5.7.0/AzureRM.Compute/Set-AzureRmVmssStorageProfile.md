---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: 26f61261bd8fd1c2d5fc2bbdacec71f73db91fb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591698"
---
# <span data-ttu-id="f52f2-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="f52f2-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="f52f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f52f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f52f2-103">VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f52f2-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f52f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f52f2-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [-OsDiskName <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-ManagedDisk <StorageAccountTypes>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f52f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f52f2-105">DESCRIPTION</span></span>
<span data-ttu-id="f52f2-106">**Set-AzureRmVmssStorageProfile** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f52f2-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f52f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f52f2-107">EXAMPLES</span></span>

### <span data-ttu-id="f52f2-108">Örnek 1: VMSS için depolama profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="f52f2-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="f52f2-109">Bu komut, ContosoVMSS adlı VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f52f2-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="f52f2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f52f2-110">PARAMETERS</span></span>

### <span data-ttu-id="f52f2-111">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="f52f2-111">-DataDisk</span></span>
<span data-ttu-id="f52f2-112">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-112">Specifies the data disk object.</span></span>

```yaml
Type: VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-113">-Image</span><span class="sxs-lookup"><span data-stu-id="f52f2-113">-Image</span></span>
<span data-ttu-id="f52f2-114">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-114">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="f52f2-115">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f52f2-115">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-116">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="f52f2-116">-ImageReferenceId</span></span>
<span data-ttu-id="f52f2-117">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-117">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="f52f2-118">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="f52f2-118">-ImageReferenceOffer</span></span>
<span data-ttu-id="f52f2-119">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-119">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="f52f2-120">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f52f2-120">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-121">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="f52f2-121">-ImageReferencePublisher</span></span>
<span data-ttu-id="f52f2-122">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-122">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="f52f2-123">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f52f2-123">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-124">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="f52f2-124">-ImageReferenceSku</span></span>
<span data-ttu-id="f52f2-125">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-125">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="f52f2-126">STB 'ler almak için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f52f2-126">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="f52f2-127">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="f52f2-127">-ImageReferenceVersion</span></span>
<span data-ttu-id="f52f2-128">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-128">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="f52f2-129">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="f52f2-129">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="f52f2-130">-Manageddısk</span><span class="sxs-lookup"><span data-stu-id="f52f2-130">-ManagedDisk</span></span>
<span data-ttu-id="f52f2-131">Yönetilen diski belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-131">Specifies the managed disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-132">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="f52f2-132">-OsDiskCaching</span></span>
<span data-ttu-id="f52f2-133">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-133">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="f52f2-134">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f52f2-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f52f2-135">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="f52f2-135">ReadOnly</span></span>
- <span data-ttu-id="f52f2-136">Yazma</span><span class="sxs-lookup"><span data-stu-id="f52f2-136">ReadWrite</span></span>

<span data-ttu-id="f52f2-137">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-137">The default value is ReadWrite.</span></span>
<span data-ttu-id="f52f2-138">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="f52f2-138">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="f52f2-139">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="f52f2-139">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-140">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="f52f2-140">-OsDiskCreateOption</span></span>
<span data-ttu-id="f52f2-141">Bu cmdlet 'in VMSS sanal makinelerini nasıl oluşturduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-141">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="f52f2-142">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="f52f2-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f52f2-143">Ekle: Bu değer, VMSS sanal makinesini oluşturmak için özel bir disk kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f52f2-143">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="f52f2-144">FromImage: Bu değer, bir resim kullanarak VMSS sanal makinesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="f52f2-144">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="f52f2-145">Bir platform görüntüsü kullanıyorsanız, *ImageReference* parametresini de kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="f52f2-145">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-146">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="f52f2-146">-OsDiskName</span></span>
<span data-ttu-id="f52f2-147">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-147">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-148">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="f52f2-148">-OsDiskOsType</span></span>
<span data-ttu-id="f52f2-149">Diskteki işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-149">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="f52f2-150">Bu yalnızca Kullanıcı görüntüsü senaryoları için gereklidir ve bir platform görüntüsü için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="f52f2-150">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: OperatingSystemTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-151">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="f52f2-151">-VhdContainer</span></span>
<span data-ttu-id="f52f2-152">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-152">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-153">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f52f2-153">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f52f2-154">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-154">Specifies the VMSS object.</span></span>
<span data-ttu-id="f52f2-155">Nesneyi edinmek için New-AzureRmVmssConfig nesneyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="f52f2-155">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="f52f2-156">-Confirm</span></span>
<span data-ttu-id="f52f2-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f52f2-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f52f2-158">-WhatIf</span></span>
<span data-ttu-id="f52f2-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f52f2-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f52f2-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f52f2-160">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f52f2-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f52f2-161">CommonParameters</span></span>
<span data-ttu-id="f52f2-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f52f2-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f52f2-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f52f2-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f52f2-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f52f2-164">INPUTS</span></span>

###  
<span data-ttu-id="f52f2-165">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="f52f2-165">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f52f2-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f52f2-166">OUTPUTS</span></span>

## <span data-ttu-id="f52f2-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f52f2-167">NOTES</span></span>

## <span data-ttu-id="f52f2-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f52f2-168">RELATED LINKS</span></span>

[<span data-ttu-id="f52f2-169">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="f52f2-169">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="f52f2-170">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="f52f2-170">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="f52f2-171">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="f52f2-171">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="f52f2-172">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f52f2-172">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


