---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssStorageProfile.md
ms.openlocfilehash: dc2f8633b303d15f3fe53bfc0be7eda3420e611f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763888"
---
# <span data-ttu-id="5b228-101">Set-AzureRmVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="5b228-101">Set-AzureRmVmssStorageProfile</span></span>

## <span data-ttu-id="5b228-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b228-102">SYNOPSIS</span></span>
<span data-ttu-id="5b228-103">VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5b228-103">Sets the storage profile properties for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b228-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5b228-104">SYNTAX</span></span>

```
Set-AzureRmVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DataDisk <VirtualMachineScaleSetDataDisk[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b228-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5b228-105">DESCRIPTION</span></span>
<span data-ttu-id="5b228-106">**Set-AzureRmVmssStorageProfile** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5b228-106">The **Set-AzureRmVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5b228-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5b228-107">EXAMPLES</span></span>

### <span data-ttu-id="5b228-108">Örnek 1: VMSS için depolama profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5b228-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzureRmVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="5b228-109">Bu komut, ContosoVMSS adlı VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5b228-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="5b228-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5b228-110">PARAMETERS</span></span>

### <span data-ttu-id="5b228-111">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="5b228-111">-DataDisk</span></span>
<span data-ttu-id="5b228-112">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-112">Specifies the data disk object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b228-113">-DefaultProfile</span></span>
<span data-ttu-id="5b228-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5b228-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b228-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="5b228-115">-DiffDiskSetting</span></span>
<span data-ttu-id="5b228-116">İşletim sistemi diskinin fark kayıt diski ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="5b228-117">-Image</span><span class="sxs-lookup"><span data-stu-id="5b228-117">-Image</span></span>
<span data-ttu-id="5b228-118">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-118">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="5b228-119">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5b228-119">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-120">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="5b228-120">-ImageReferenceId</span></span>
<span data-ttu-id="5b228-121">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-121">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="5b228-122">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="5b228-122">-ImageReferenceOffer</span></span>
<span data-ttu-id="5b228-123">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-123">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="5b228-124">Resim teklifi edinmek için Get-AzureRmVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b228-124">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-125">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="5b228-125">-ImageReferencePublisher</span></span>
<span data-ttu-id="5b228-126">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-126">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="5b228-127">Yayımcı edinmek için Get-AzureRmVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b228-127">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-128">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="5b228-128">-ImageReferenceSku</span></span>
<span data-ttu-id="5b228-129">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-129">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="5b228-130">STB 'ler almak için Get-AzureRmVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b228-130">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="5b228-131">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="5b228-131">-ImageReferenceVersion</span></span>
<span data-ttu-id="5b228-132">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-132">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="5b228-133">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="5b228-133">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="5b228-134">-Manageddısk</span><span class="sxs-lookup"><span data-stu-id="5b228-134">-ManagedDisk</span></span>
<span data-ttu-id="5b228-135">Yönetilen diski belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-135">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="5b228-136">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="5b228-136">-OsDiskCaching</span></span>
<span data-ttu-id="5b228-137">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-137">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="5b228-138">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5b228-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b228-139">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="5b228-139">ReadOnly</span></span>
- <span data-ttu-id="5b228-140">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="5b228-140">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="5b228-141">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="5b228-141">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="5b228-142">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="5b228-142">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-143">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="5b228-143">-OsDiskCreateOption</span></span>
<span data-ttu-id="5b228-144">Bu cmdlet 'in VMSS sanal makinelerini nasıl oluşturduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-144">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="5b228-145">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5b228-145">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5b228-146">Ekle: Bu değer, VMSS sanal makinesini oluşturmak için özel bir disk kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b228-146">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="5b228-147">FromImage: Bu değer, bir resim kullanarak VMSS sanal makinesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="5b228-147">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="5b228-148">Bir platform görüntüsü kullanıyorsanız, *ImageReference* parametresini de kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="5b228-148">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="5b228-149">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="5b228-149">-OsDiskName</span></span>
<span data-ttu-id="5b228-150">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-150">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-151">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="5b228-151">-OsDiskOsType</span></span>
<span data-ttu-id="5b228-152">Diskteki işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-152">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="5b228-153">Bu yalnızca Kullanıcı görüntüsü senaryoları için gereklidir ve bir platform görüntüsü için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="5b228-153">This is only needed for user image scenarios and not for a platform image.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-154">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="5b228-154">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="5b228-155">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-155">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="5b228-156">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="5b228-156">-VhdContainer</span></span>
<span data-ttu-id="5b228-157">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-157">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-158">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5b228-158">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5b228-159">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5b228-159">Specifies the VMSS object.</span></span>
<span data-ttu-id="5b228-160">Nesneyi edinmek için New-AzureRmVmssConfig nesneyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="5b228-160">To obtain the object, use the New-AzureRmVmssConfig object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="5b228-161">-Confirm</span></span>
<span data-ttu-id="5b228-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5b228-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b228-163">-WhatIf</span></span>
<span data-ttu-id="5b228-164">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5b228-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b228-165">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5b228-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b228-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b228-166">CommonParameters</span></span>
<span data-ttu-id="5b228-167">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5b228-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b228-168">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b228-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b228-169">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5b228-169">INPUTS</span></span>

### <span data-ttu-id="5b228-170">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5b228-170">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="5b228-171">System. String</span><span class="sxs-lookup"><span data-stu-id="5b228-171">System.String</span></span>

### <span data-ttu-id="5b228-172">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5b228-172">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5b228-173">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="5b228-173">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="5b228-174">System. String []</span><span class="sxs-lookup"><span data-stu-id="5b228-174">System.String[]</span></span>

### <span data-ttu-id="5b228-175">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="5b228-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="5b228-176">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5b228-176">OUTPUTS</span></span>

### <span data-ttu-id="5b228-177">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5b228-177">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="5b228-178">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5b228-178">NOTES</span></span>

## <span data-ttu-id="5b228-179">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5b228-179">RELATED LINKS</span></span>

[<span data-ttu-id="5b228-180">Get-Azurermvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="5b228-180">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="5b228-181">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="5b228-181">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="5b228-182">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5b228-182">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="5b228-183">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5b228-183">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


