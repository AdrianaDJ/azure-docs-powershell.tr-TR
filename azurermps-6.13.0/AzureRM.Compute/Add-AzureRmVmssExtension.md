---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: ad87e4e556263889de23640abad391ee28d7b397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592320"
---
# <span data-ttu-id="a6686-101">Add-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="a6686-101">Add-AzureRmVmssExtension</span></span>

## <span data-ttu-id="a6686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6686-102">SYNOPSIS</span></span>
<span data-ttu-id="a6686-103">VMSUBNET 'e bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="a6686-103">Adds an extension to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6686-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6686-104">SYNTAX</span></span>

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a6686-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6686-105">DESCRIPTION</span></span>
<span data-ttu-id="a6686-106">**Add-Azurermvmssextenma** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="a6686-106">The **Add-AzureRmVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="a6686-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6686-107">EXAMPLES</span></span>

### <span data-ttu-id="a6686-108">Örnek 1: VMSS 'ye uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="a6686-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="a6686-109">Bu komut, VMSS 'ye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="a6686-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="a6686-110">Örnek 2: VMSS 'ye ayarlar ve korumalı ayarlarla bir uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="a6686-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="a6686-111">Bu komut, blob depolamada bir örnek Bash betiği ile VMSS 'ye bir uzantı ekler, korumalı ayarlar 'da, ayarlar ve güvenlik erişimi 'nde BLOB depolama ve yürütülebilir komutunun URL 'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a6686-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="a6686-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6686-112">PARAMETERS</span></span>

### <span data-ttu-id="a6686-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a6686-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a6686-114">Uzantı sürümünün otomatik olarak yeni bir alt sürüme güncelleştirilip güncelleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6686-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6686-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6686-115">-DefaultProfile</span></span>
<span data-ttu-id="a6686-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6686-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6686-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="a6686-117">-ForceUpdateTag</span></span>
<span data-ttu-id="a6686-118">Bir değer sağlanmışsa ve önceki değerden farklıysa, uzantı yapılandırması değişmemiş olsa bile, uzantı işleyicisi güncelleştirmeye zorlanır.</span><span class="sxs-lookup"><span data-stu-id="a6686-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="a6686-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6686-119">-Name</span></span>
<span data-ttu-id="a6686-120">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6686-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a6686-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a6686-121">-ProtectedSetting</span></span>
<span data-ttu-id="a6686-122">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6686-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="a6686-123">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="a6686-123">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6686-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a6686-124">-Publisher</span></span>
<span data-ttu-id="a6686-125">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6686-125">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="a6686-126">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="a6686-126">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="a6686-127">Bu, yayımcıyı almak için [Get-Azurermvmımagepublisher](./Get-AzureRmVMImagePublisher.md) cmdlet 'ini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="a6686-127">This can use the [Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="a6686-128">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="a6686-128">-Setting</span></span>
<span data-ttu-id="a6686-129">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6686-129">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="a6686-130">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="a6686-130">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6686-131">-Tür</span><span class="sxs-lookup"><span data-stu-id="a6686-131">-Type</span></span>
<span data-ttu-id="a6686-132">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6686-132">Specifies the extension type.</span></span>
<span data-ttu-id="a6686-133">Extension türünü almak için [Get-Azurermvmextensionımagetype](./Get-AzureRmVMExtensionImageType.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6686-133">You can use the [Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="a6686-134">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a6686-134">-TypeHandlerVersion</span></span>
<span data-ttu-id="a6686-135">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6686-135">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="a6686-136">Uzantının sürümünü almak için [Get-Azurermvmextensionımage](./Get-AzureRmVMExtensionImage.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6686-136">You can use the [Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="a6686-137">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6686-137">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a6686-138">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a6686-138">Specify the VMSS object.</span></span>
<span data-ttu-id="a6686-139">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a6686-139">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="a6686-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6686-140">-Confirm</span></span>
<span data-ttu-id="a6686-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6686-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6686-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6686-142">-WhatIf</span></span>
<span data-ttu-id="a6686-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6686-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6686-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6686-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6686-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6686-145">CommonParameters</span></span>
<span data-ttu-id="a6686-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6686-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6686-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6686-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6686-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6686-148">INPUTS</span></span>

### <span data-ttu-id="a6686-149">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6686-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a6686-150">System. String</span><span class="sxs-lookup"><span data-stu-id="a6686-150">System.String</span></span>

### <span data-ttu-id="a6686-151">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a6686-151">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a6686-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="a6686-152">System.Object</span></span>

## <span data-ttu-id="a6686-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6686-153">OUTPUTS</span></span>

### <span data-ttu-id="a6686-154">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a6686-154">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a6686-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6686-155">NOTES</span></span>

## <span data-ttu-id="a6686-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6686-156">RELATED LINKS</span></span>

[<span data-ttu-id="a6686-157">Remove-Azurermvmssextenma</span><span class="sxs-lookup"><span data-stu-id="a6686-157">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)

[<span data-ttu-id="a6686-158">Get-Azurermvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="a6686-158">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="a6686-159">Get-Azurermvmextensionımagetype</span><span class="sxs-lookup"><span data-stu-id="a6686-159">Get-AzureRmVMExtensionImageType</span></span>](./Get-AzureRmVMExtensionImageType.md)

[<span data-ttu-id="a6686-160">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="a6686-160">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)

[<span data-ttu-id="a6686-161">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a6686-161">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)