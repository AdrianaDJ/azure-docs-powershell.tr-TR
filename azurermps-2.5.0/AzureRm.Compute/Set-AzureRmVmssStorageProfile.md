---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
ms.openlocfilehash: c96ff571ef1b82e52a313c2044a41b97d46ffa0b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939403"
---
# <span data-ttu-id="5a7f7-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5a7f7-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="5a7f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7f7-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7f7-103">VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a7f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a7f7-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <DiskCreateOptionTypes>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-ManagedDisk <StorageAccountTypes>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a7f7-105">DESCRIPTION</span></span>
<span data-ttu-id="5a7f7-106">**Set-AzureRmVmssStorageProfile** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5a7f7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a7f7-107">EXAMPLES</span></span>

### <span data-ttu-id="5a7f7-108">Örnek 1: VMSS için depolama profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5a7f7-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="5a7f7-109">Bu komut, ContosoVMSS adlı VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="5a7f7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a7f7-110">PARAMETERS</span></span>

### <span data-ttu-id="5a7f7-111">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="5a7f7-111">-DataDisk</span></span>
<span data-ttu-id="5a7f7-112">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="5a7f7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7f7-113">-DefaultProfile</span></span>
<span data-ttu-id="5a7f7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7f7-115">-Image</span><span class="sxs-lookup"><span data-stu-id="5a7f7-115">-Image</span></span>
<span data-ttu-id="5a7f7-116">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-116">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="5a7f7-117">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-117">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="5a7f7-118">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="5a7f7-118">-ImageReferenceId</span></span>
<span data-ttu-id="5a7f7-119">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-119">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="5a7f7-120">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="5a7f7-120">-ImageReferenceOffer</span></span>
<span data-ttu-id="5a7f7-121">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-121">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="5a7f7-122">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-122">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="5a7f7-123">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="5a7f7-123">-ImageReferencePublisher</span></span>
<span data-ttu-id="5a7f7-124">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-124">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="5a7f7-125">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-125">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="5a7f7-126">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="5a7f7-126">-ImageReferenceSku</span></span>
<span data-ttu-id="5a7f7-127">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-127">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="5a7f7-128">STB 'ler almak için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-128">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="5a7f7-129">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="5a7f7-129">-ImageReferenceVersion</span></span>
<span data-ttu-id="5a7f7-130">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-130">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="5a7f7-131">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-131">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="5a7f7-132">-Manageddısk</span><span class="sxs-lookup"><span data-stu-id="5a7f7-132">-ManagedDisk</span></span>
<span data-ttu-id="5a7f7-133">Yönetilen diski belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-133">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="5a7f7-134">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="5a7f7-134">-OsDiskCaching</span></span>
<span data-ttu-id="5a7f7-135">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-135">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="5a7f7-136">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5a7f7-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a7f7-137">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="5a7f7-137">ReadOnly</span></span>
- <span data-ttu-id="5a7f7-138">Yazma</span><span class="sxs-lookup"><span data-stu-id="5a7f7-138">ReadWrite</span></span>

<span data-ttu-id="5a7f7-139">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-139">The default value is ReadWrite.</span></span>
<span data-ttu-id="5a7f7-140">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-140">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="5a7f7-141">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-141">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="5a7f7-142">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="5a7f7-142">-OsDiskCreateOption</span></span>
<span data-ttu-id="5a7f7-143">Bu cmdlet 'in VMSS sanal makinelerini nasıl oluşturduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-143">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>

<span data-ttu-id="5a7f7-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5a7f7-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5a7f7-145">Ekle: Bu değer, VMSS sanal makinesini oluşturmak için özel bir disk kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-145">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="5a7f7-146">FromImage: Bu değer, bir resim kullanarak VMSS sanal makinesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-146">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="5a7f7-147">Bir platform görüntüsü kullanıyorsanız, *ImageReference* parametresini de kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-147">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="5a7f7-148">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="5a7f7-148">-OsDiskName</span></span>
<span data-ttu-id="5a7f7-149">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-149">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7f7-150">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="5a7f7-150">-OsDiskOsType</span></span>
<span data-ttu-id="5a7f7-151">Diskteki işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-151">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="5a7f7-152">Bu yalnızca Kullanıcı görüntüsü senaryoları için gereklidir ve bir platform görüntüsü için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-152">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="5a7f7-153">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="5a7f7-153">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="5a7f7-154">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-154">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="5a7f7-155">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="5a7f7-155">-VhdContainer</span></span>
<span data-ttu-id="5a7f7-156">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-156">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="5a7f7-157">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a7f7-157">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5a7f7-158">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-158">Specifies the VMSS object.</span></span>
<span data-ttu-id="5a7f7-159">Nesneyi edinmek için New-AzureRmVmssConfig nesneyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-159">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7f7-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a7f7-160">-Confirm</span></span>
<span data-ttu-id="5a7f7-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7f7-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7f7-162">-WhatIf</span></span>
<span data-ttu-id="5a7f7-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-163">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a7f7-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7f7-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7f7-165">CommonParameters</span></span>
<span data-ttu-id="5a7f7-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7f7-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7f7-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7f7-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a7f7-168">INPUTS</span></span>

###  
<span data-ttu-id="5a7f7-169">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5a7f7-169">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5a7f7-170">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a7f7-170">OUTPUTS</span></span>

### <span data-ttu-id="5a7f7-171">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5a7f7-171">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5a7f7-172">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a7f7-172">NOTES</span></span>

## <span data-ttu-id="5a7f7-173">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a7f7-173">RELATED LINKS</span></span>

[<span data-ttu-id="5a7f7-174">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="5a7f7-174">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="5a7f7-175">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="5a7f7-175">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="5a7f7-176">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5a7f7-176">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="5a7f7-177">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5a7f7-177">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


