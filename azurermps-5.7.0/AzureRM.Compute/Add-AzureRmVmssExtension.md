---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586814"
---
# <span data-ttu-id="4d852-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="4d852-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="4d852-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d852-102">SYNOPSIS</span></span>
<span data-ttu-id="4d852-103">VMSUBNET 'e bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="4d852-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d852-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4d852-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d852-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4d852-105">DESCRIPTION</span></span>
<span data-ttu-id="4d852-106">**Add-Azurermvmssextenma** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="4d852-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4d852-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4d852-107">EXAMPLES</span></span>

### <span data-ttu-id="4d852-108">Örnek 1: VMSS 'ye uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="4d852-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="4d852-109">Bu komut VMMS 'ye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="4d852-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="4d852-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4d852-110">PARAMETERS</span></span>

### <span data-ttu-id="4d852-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4d852-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4d852-112">Uzantı sürümünün otomatik olarak yeni bir alt sürüme güncelleştirilip güncelleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d852-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d852-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4d852-113">-Name</span></span>
<span data-ttu-id="4d852-114">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d852-114">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="4d852-115">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="4d852-115">-ProtectedSetting</span></span>
<span data-ttu-id="4d852-116">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d852-116">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="4d852-117">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="4d852-117">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d852-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4d852-118">-Publisher</span></span>
<span data-ttu-id="4d852-119">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d852-119">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="4d852-120">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="4d852-120">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="4d852-121">Bu, yayımcıyı almak için [Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md) cmdlet 'ini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="4d852-121">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="4d852-122">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="4d852-122">-Setting</span></span>
<span data-ttu-id="4d852-123">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d852-123">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="4d852-124">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="4d852-124">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d852-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="4d852-125">-Type</span></span>
<span data-ttu-id="4d852-126">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d852-126">Specifies the extension type.</span></span>
<span data-ttu-id="4d852-127">Extension türünü almak için [Get-Azurermvmextensionımagetype](./Get-AzureRmVMExtensionImageType.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d852-127">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="4d852-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4d852-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="4d852-129">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4d852-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="4d852-130">Uzantının sürümünü almak için [Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d852-130">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="4d852-131">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d852-131">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4d852-132">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4d852-132">Specify the VMSS object.</span></span>
<span data-ttu-id="4d852-133">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4d852-133">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="4d852-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="4d852-134">-Confirm</span></span>
<span data-ttu-id="4d852-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4d852-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d852-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d852-136">-WhatIf</span></span>
<span data-ttu-id="4d852-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4d852-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d852-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4d852-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d852-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d852-139">CommonParameters</span></span>
<span data-ttu-id="4d852-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4d852-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d852-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d852-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d852-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4d852-142">INPUTS</span></span>

### <span data-ttu-id="4d852-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4d852-143">None</span></span>
<span data-ttu-id="4d852-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4d852-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d852-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4d852-145">OUTPUTS</span></span>

###  
<span data-ttu-id="4d852-146">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4d852-146">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4d852-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4d852-147">NOTES</span></span>

## <span data-ttu-id="4d852-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4d852-148">RELATED LINKS</span></span>

[<span data-ttu-id="4d852-149">Remove-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="4d852-149">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="4d852-150">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="4d852-150">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="4d852-151">Get-Azurermvmextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="4d852-151">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="4d852-152">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="4d852-152">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="4d852-153">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4d852-153">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
