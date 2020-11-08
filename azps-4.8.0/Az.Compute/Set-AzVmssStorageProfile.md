---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 230DAE05-C197-451F-A24C-F4A2DAE4AD04
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssstorageprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssStorageProfile.md
ms.openlocfilehash: 7bf5e6b765fee14ca9ba12a289d6445e063ff9df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267890"
---
# <span data-ttu-id="1c2e6-101">Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="1c2e6-101">Set-AzVmssStorageProfile</span></span>

## <span data-ttu-id="1c2e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c2e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2e6-103">VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-103">Sets the storage profile properties for the VMSS.</span></span>

## <span data-ttu-id="1c2e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1c2e6-104">SYNTAX</span></span>

```
Set-AzVmssStorageProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-ImageReferencePublisher] <String>] [[-ImageReferenceOffer] <String>] [[-ImageReferenceSku] <String>]
 [[-ImageReferenceVersion] <String>] [[-OsDiskName] <String>] [[-OsDiskCaching] <CachingTypes>]
 [[-OsDiskCreateOption] <String>] [[-OsDiskOsType] <OperatingSystemTypes>] [[-Image] <String>]
 [[-VhdContainer] <String[]>] [-ImageReferenceId <String>] [-OsDiskWriteAccelerator]
 [-DiffDiskSetting <String>] [-ManagedDisk <String>] [-DiskEncryptionSetId <String>]
 [-DataDisk <VirtualMachineScaleSetDataDisk[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c2e6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1c2e6-105">DESCRIPTION</span></span>
<span data-ttu-id="1c2e6-106">**Set-AzVmssStorageProfile** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-106">The **Set-AzVmssStorageProfile** cmdlet sets the storage profile properties for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1c2e6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1c2e6-107">EXAMPLES</span></span>

### <span data-ttu-id="1c2e6-108">Örnek 1: VMSS için depolama profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="1c2e6-108">Example 1: Set the storage profile properties for the VMSS</span></span>
```
PS C:\> Set-AzVmssStorageProfile -VirtualMachineScaleSet "ContosoVMSS" -Name "Test" -OsDiskCreateOption "FromImage" -OsDiskCaching "None" `
            -ImageReferenceOffer $ImgRef.Offer -ImageReferenceSku $ImgRef.Skus -ImageReferenceVersion $ImgRef.Version `
            -ImageReferencePublisher $ImgRef.PublisherName -VhdContainer $VhdContainer
```

<span data-ttu-id="1c2e6-109">Bu komut, ContosoVMSS adlı VMSS için depolama profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-109">This command sets the storage profile properties for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="1c2e6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1c2e6-110">PARAMETERS</span></span>

### <span data-ttu-id="1c2e6-111">-Datadısk</span><span class="sxs-lookup"><span data-stu-id="1c2e6-111">-DataDisk</span></span>
<span data-ttu-id="1c2e6-112">Veri diski nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-112">Specifies the data disk object.</span></span>

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

### <span data-ttu-id="1c2e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2e6-113">-DefaultProfile</span></span>
<span data-ttu-id="1c2e6-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c2e6-115">-DiffDiskSetting</span><span class="sxs-lookup"><span data-stu-id="1c2e6-115">-DiffDiskSetting</span></span>
<span data-ttu-id="1c2e6-116">İşletim sistemi diskinin fark kayıt diski ayarlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-116">Specifies the differencing disk settings for operating system disk.</span></span>

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

### <span data-ttu-id="1c2e6-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="1c2e6-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="1c2e6-118">Müşterinin yönettiği disk şifrelemesi kümesinin kaynak kimliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="1c2e6-119">Bu yalnızca yönetilen disk için belirtilebilir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="1c2e6-120">-Image</span><span class="sxs-lookup"><span data-stu-id="1c2e6-120">-Image</span></span>
<span data-ttu-id="1c2e6-121">Kullanıcı görüntüsü için blob URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-121">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="1c2e6-122">VMSS, Kullanıcı görüntüsünün aynı kapsayıcısında bir işletim sistemi diski oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-122">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="1c2e6-123">-Imagereferenceıd</span><span class="sxs-lookup"><span data-stu-id="1c2e6-123">-ImageReferenceId</span></span>
<span data-ttu-id="1c2e6-124">Resim başvuru KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-124">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="1c2e6-125">-Imagereferenceteklif</span><span class="sxs-lookup"><span data-stu-id="1c2e6-125">-ImageReferenceOffer</span></span>
<span data-ttu-id="1c2e6-126">Sanal makine görüntüsünün (Vmımage) teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-126">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="1c2e6-127">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-127">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="1c2e6-128">-Imagereferencepublisher</span><span class="sxs-lookup"><span data-stu-id="1c2e6-128">-ImageReferencePublisher</span></span>
<span data-ttu-id="1c2e6-129">Vmımage yayımcısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-129">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="1c2e6-130">Yayımcı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-130">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="1c2e6-131">-Imagereferencesku</span><span class="sxs-lookup"><span data-stu-id="1c2e6-131">-ImageReferenceSku</span></span>
<span data-ttu-id="1c2e6-132">VMImage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-132">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="1c2e6-133">STB 'ler almak için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-133">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="1c2e6-134">-Imagereferenceversion</span><span class="sxs-lookup"><span data-stu-id="1c2e6-134">-ImageReferenceVersion</span></span>
<span data-ttu-id="1c2e6-135">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-135">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="1c2e6-136">En son sürümü kullanmak için belirli bir sürüm yerine en son sürümünü belirtin.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-136">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="1c2e6-137">-Manageddısk</span><span class="sxs-lookup"><span data-stu-id="1c2e6-137">-ManagedDisk</span></span>
<span data-ttu-id="1c2e6-138">Yönetilen diski belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-138">Specifies the managed disk.</span></span>

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

### <span data-ttu-id="1c2e6-139">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="1c2e6-139">-OsDiskCaching</span></span>
<span data-ttu-id="1c2e6-140">İşletim sistemi diskinin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-140">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="1c2e6-141">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1c2e6-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1c2e6-142">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="1c2e6-142">ReadOnly</span></span>
- <span data-ttu-id="1c2e6-143">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-143">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="1c2e6-144">Önbellek değerini değiştirirseniz cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-144">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="1c2e6-145">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-145">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="1c2e6-146">-OsDiskCreateOption</span><span class="sxs-lookup"><span data-stu-id="1c2e6-146">-OsDiskCreateOption</span></span>
<span data-ttu-id="1c2e6-147">Bu cmdlet 'in VMSS sanal makinelerini nasıl oluşturduğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-147">Specifies how this cmdlet creates the VMSS virtual machines.</span></span>
<span data-ttu-id="1c2e6-148">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="1c2e6-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1c2e6-149">Ekle: Bu değer, VMSS sanal makinesini oluşturmak için özel bir disk kullanırken kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-149">Attach : This value is used when you are using a specialized disk to create the VMSS virtual machine.</span></span> 
- <span data-ttu-id="1c2e6-150">FromImage: Bu değer, bir resim kullanarak VMSS sanal makinesini oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-150">FromImage : This value is used when you are using an image to create the VMSS virtual machine.</span></span>
<span data-ttu-id="1c2e6-151">Bir platform görüntüsü kullanıyorsanız, *ImageReference* parametresini de kullanacaksınız.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-151">If you are using a platform image, you will also use the *imageReference* parameter.</span></span>

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

### <span data-ttu-id="1c2e6-152">-OsDiskName</span><span class="sxs-lookup"><span data-stu-id="1c2e6-152">-OsDiskName</span></span>
<span data-ttu-id="1c2e6-153">İşletim sistemi diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-153">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="1c2e6-154">-OsDiskOsType</span><span class="sxs-lookup"><span data-stu-id="1c2e6-154">-OsDiskOsType</span></span>
<span data-ttu-id="1c2e6-155">Diskteki işletim sisteminin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-155">Specifies the type of operating system on the disk.</span></span>
<span data-ttu-id="1c2e6-156">Bu yalnızca Kullanıcı görüntüsü senaryoları için gereklidir ve bir platform görüntüsü için kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-156">This is only needed for user image scenarios and not for a platform image.</span></span>

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

### <span data-ttu-id="1c2e6-157">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1c2e6-157">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="1c2e6-158">İşletim sistemi diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-158">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="1c2e6-159">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="1c2e6-159">-VhdContainer</span></span>
<span data-ttu-id="1c2e6-160">VMSS işletim sistemi disklerini depolamak için kullanılan kapsayıcı URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-160">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="1c2e6-161">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1c2e6-161">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1c2e6-162">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-162">Specifies the VMSS object.</span></span>
<span data-ttu-id="1c2e6-163">Nesneyi edinmek için New-AzVmssConfig nesneyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-163">To obtain the object, use the New-AzVmssConfig object.</span></span>

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

### <span data-ttu-id="1c2e6-164">-Onay</span><span class="sxs-lookup"><span data-stu-id="1c2e6-164">-Confirm</span></span>
<span data-ttu-id="1c2e6-165">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c2e6-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c2e6-166">-WhatIf</span></span>
<span data-ttu-id="1c2e6-167">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-167">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c2e6-168">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c2e6-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2e6-169">CommonParameters</span></span>
<span data-ttu-id="1c2e6-170">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2e6-171">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1c2e6-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2e6-172">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1c2e6-172">INPUTS</span></span>

### <span data-ttu-id="1c2e6-173">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1c2e6-173">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="1c2e6-174">System. String</span><span class="sxs-lookup"><span data-stu-id="1c2e6-174">System.String</span></span>

### <span data-ttu-id="1c2e6-175">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1c2e6-175">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1c2e6-176">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. OperatingSystemTypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="1c2e6-176">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="1c2e6-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="1c2e6-177">System.String[]</span></span>

### <span data-ttu-id="1c2e6-178">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetDataDisk []</span><span class="sxs-lookup"><span data-stu-id="1c2e6-178">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetDataDisk[]</span></span>

## <span data-ttu-id="1c2e6-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1c2e6-179">OUTPUTS</span></span>

### <span data-ttu-id="1c2e6-180">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1c2e6-180">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1c2e6-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1c2e6-181">NOTES</span></span>

## <span data-ttu-id="1c2e6-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1c2e6-182">RELATED LINKS</span></span>

[<span data-ttu-id="1c2e6-183">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="1c2e6-183">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="1c2e6-184">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="1c2e6-184">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="1c2e6-185">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="1c2e6-185">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="1c2e6-186">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="1c2e6-186">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


