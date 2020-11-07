---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: f69b8901b2bc2c07bdf158da4c92deba0330109d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938893"
---
# <span data-ttu-id="15f45-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="15f45-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="15f45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15f45-102">SYNOPSIS</span></span>
<span data-ttu-id="15f45-103">VMSUBNET 'e bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="15f45-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15f45-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15f45-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15f45-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15f45-105">DESCRIPTION</span></span>
<span data-ttu-id="15f45-106">**Add-Azurermvmssextenma** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="15f45-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="15f45-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15f45-107">EXAMPLES</span></span>

### <span data-ttu-id="15f45-108">Örnek 1: VMSS 'ye uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="15f45-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="15f45-109">Bu komut VMMS 'ye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="15f45-109">This command adds an extension to the VMMS.</span></span>

## <span data-ttu-id="15f45-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15f45-110">PARAMETERS</span></span>

### <span data-ttu-id="15f45-111">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="15f45-111">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="15f45-112">Uzantı sürümünün otomatik olarak yeni bir alt sürüme güncelleştirilip güncelleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15f45-112">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="15f45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f45-113">-DefaultProfile</span></span>
<span data-ttu-id="15f45-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15f45-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15f45-115">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="15f45-115">-ForceUpdateTag</span></span>
<span data-ttu-id="15f45-116">Bir değer sağlanmışsa ve önceki değerden farklıysa, uzantı yapılandırması değişmemiş olsa bile, uzantı işleyicisi güncelleştirmeye zorlanır.</span><span class="sxs-lookup"><span data-stu-id="15f45-116">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="15f45-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="15f45-117">-Name</span></span>
<span data-ttu-id="15f45-118">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15f45-118">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="15f45-119">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="15f45-119">-ProtectedSetting</span></span>
<span data-ttu-id="15f45-120">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="15f45-120">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="15f45-121">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="15f45-121">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="15f45-122">-Publisher</span><span class="sxs-lookup"><span data-stu-id="15f45-122">-Publisher</span></span>
<span data-ttu-id="15f45-123">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15f45-123">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="15f45-124">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="15f45-124">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="15f45-125">Bu, yayımcıyı almak için [Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md) cmdlet 'ini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="15f45-125">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="15f45-126">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="15f45-126">-Setting</span></span>
<span data-ttu-id="15f45-127">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="15f45-127">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="15f45-128">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="15f45-128">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="15f45-129">-Tür</span><span class="sxs-lookup"><span data-stu-id="15f45-129">-Type</span></span>
<span data-ttu-id="15f45-130">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="15f45-130">Specifies the extension type.</span></span>
<span data-ttu-id="15f45-131">Extension türünü almak için [Get-Azurermvmextensionımagetype](./Get-AzureRmVMExtensionImageType.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15f45-131">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="15f45-132">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="15f45-132">-TypeHandlerVersion</span></span>
<span data-ttu-id="15f45-133">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="15f45-133">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="15f45-134">Uzantının sürümünü almak için [Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15f45-134">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="15f45-135">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15f45-135">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="15f45-136">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="15f45-136">Specify the VMSS object.</span></span>
<span data-ttu-id="15f45-137">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="15f45-137">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="15f45-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="15f45-138">-Confirm</span></span>
<span data-ttu-id="15f45-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15f45-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15f45-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15f45-140">-WhatIf</span></span>
<span data-ttu-id="15f45-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15f45-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15f45-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15f45-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15f45-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f45-143">CommonParameters</span></span>
<span data-ttu-id="15f45-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15f45-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f45-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15f45-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f45-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15f45-146">INPUTS</span></span>

### <span data-ttu-id="15f45-147">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="15f45-147">VirtualMachineScaleSet</span></span>
<span data-ttu-id="15f45-148">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="15f45-148">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="15f45-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15f45-149">OUTPUTS</span></span>

###  
<span data-ttu-id="15f45-150">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="15f45-150">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="15f45-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15f45-151">NOTES</span></span>

## <span data-ttu-id="15f45-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15f45-152">RELATED LINKS</span></span>

[<span data-ttu-id="15f45-153">Remove-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="15f45-153">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="15f45-154">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="15f45-154">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="15f45-155">Get-Azurermvmextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="15f45-155">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="15f45-156">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="15f45-156">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="15f45-157">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="15f45-157">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
