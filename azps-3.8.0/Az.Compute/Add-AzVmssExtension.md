---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 87ea9af1980948f28477a9f483b3c6429df98d12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104898"
---
# <span data-ttu-id="c68fb-101">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c68fb-101">Add-AzVmssExtension</span></span>

## <span data-ttu-id="c68fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c68fb-103">VMSUBNET 'e bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="c68fb-103">Adds an extension to the VMSS.</span></span>

## <span data-ttu-id="c68fb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c68fb-104">SYNTAX</span></span>

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c68fb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c68fb-105">DESCRIPTION</span></span>
<span data-ttu-id="c68fb-106">**Add-AzVmssExtension** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="c68fb-106">The **Add-AzVmssExtension** cmdlet adds an extension to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="c68fb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c68fb-107">EXAMPLES</span></span>

### <span data-ttu-id="c68fb-108">Örnek 1: VMSS 'ye uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="c68fb-108">Example 1: Add an extension to the VMSS</span></span>
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

<span data-ttu-id="c68fb-109">Bu komut, VMSS 'ye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="c68fb-109">This command adds an extension to the VMSS.</span></span>

### <span data-ttu-id="c68fb-110">Örnek 2: VMSS 'ye ayarlar ve korumalı ayarlarla bir uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="c68fb-110">Example 2: Add an extension to the VMSS with settings and protected settings</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

<span data-ttu-id="c68fb-111">Bu komut, blob depolamada bir örnek Bash betiği ile VMSS 'ye bir uzantı ekler, korumalı ayarlar 'da, ayarlar ve güvenlik erişimi 'nde BLOB depolama ve yürütülebilir komutunun URL 'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="c68fb-111">This command adds an extension to the VMSS with a sample bash script on a blob storage, specify the url of blob storage and executable command in settings and security access in protected settings.</span></span> 

## <span data-ttu-id="c68fb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c68fb-112">PARAMETERS</span></span>

### <span data-ttu-id="c68fb-113">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c68fb-113">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c68fb-114">Uzantı sürümünün otomatik olarak yeni bir alt sürüme güncelleştirilip güncelleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-114">Indicates whether the extension version should be automatically updated to a newer minor version.</span></span>

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

### <span data-ttu-id="c68fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68fb-115">-DefaultProfile</span></span>
<span data-ttu-id="c68fb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c68fb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c68fb-117">-ForceUpdateTag</span><span class="sxs-lookup"><span data-stu-id="c68fb-117">-ForceUpdateTag</span></span>
<span data-ttu-id="c68fb-118">Bir değer sağlanmışsa ve önceki değerden farklıysa, uzantı yapılandırması değişmemiş olsa bile, uzantı işleyicisi güncelleştirmeye zorlanır.</span><span class="sxs-lookup"><span data-stu-id="c68fb-118">If a value is provided and is different from the previous value, the extension handler will be forced to update even if the extension configuration has not changed.</span></span>

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

### <span data-ttu-id="c68fb-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c68fb-119">-Name</span></span>
<span data-ttu-id="c68fb-120">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-120">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="c68fb-121">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="c68fb-121">-ProtectedSetting</span></span>
<span data-ttu-id="c68fb-122">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-122">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="c68fb-123">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="c68fb-123">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="c68fb-124">-ProvisionAfterExtension</span><span class="sxs-lookup"><span data-stu-id="c68fb-124">-ProvisionAfterExtension</span></span>
<span data-ttu-id="c68fb-125">Bu uzantının sağlanması gereken uzantı adları koleksiyonu.</span><span class="sxs-lookup"><span data-stu-id="c68fb-125">Collection of extension names after which this extension needs to be provisioned.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68fb-126">-Publisher</span><span class="sxs-lookup"><span data-stu-id="c68fb-126">-Publisher</span></span>
<span data-ttu-id="c68fb-127">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-127">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="c68fb-128">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="c68fb-128">The publisher provides a name when the publisher registers an extension.</span></span>
<span data-ttu-id="c68fb-129">Bu, yayımcıyı almak için [Get-Azvmımagepublisher](./Get-AzVMImagePublisher.md) cmdlet 'ini kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-129">This can use the [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) cmdlet to get the publisher.</span></span>

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

### <span data-ttu-id="c68fb-130">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="c68fb-130">-Setting</span></span>
<span data-ttu-id="c68fb-131">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-131">Specifies the public configuration, as a string, for the extension.</span></span>
<span data-ttu-id="c68fb-132">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="c68fb-132">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="c68fb-133">-Tür</span><span class="sxs-lookup"><span data-stu-id="c68fb-133">-Type</span></span>
<span data-ttu-id="c68fb-134">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-134">Specifies the extension type.</span></span>
<span data-ttu-id="c68fb-135">Extension türünü almak için [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c68fb-135">You can use the [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) cmdlet to get the extension type.</span></span>

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

### <span data-ttu-id="c68fb-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c68fb-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="c68fb-137">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="c68fb-138">Uzantının sürümünü almak için [Get-Azvmextensionımage](./Get-AzVMExtensionImage.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c68fb-138">You can use the [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) cmdlet to get the version of the extension.</span></span>

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

### <span data-ttu-id="c68fb-139">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c68fb-139">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c68fb-140">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="c68fb-140">Specify the VMSS object.</span></span>
<span data-ttu-id="c68fb-141">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c68fb-141">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) to create the object.</span></span>

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

### <span data-ttu-id="c68fb-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="c68fb-142">-Confirm</span></span>
<span data-ttu-id="c68fb-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c68fb-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c68fb-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c68fb-144">-WhatIf</span></span>
<span data-ttu-id="c68fb-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c68fb-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c68fb-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c68fb-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c68fb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68fb-147">CommonParameters</span></span>
<span data-ttu-id="c68fb-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c68fb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68fb-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c68fb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68fb-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c68fb-150">INPUTS</span></span>

### <span data-ttu-id="c68fb-151">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c68fb-151">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="c68fb-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c68fb-152">System.String</span></span>

### <span data-ttu-id="c68fb-153">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="c68fb-153">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c68fb-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="c68fb-154">System.Object</span></span>

## <span data-ttu-id="c68fb-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c68fb-155">OUTPUTS</span></span>

### <span data-ttu-id="c68fb-156">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c68fb-156">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="c68fb-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c68fb-157">NOTES</span></span>

## <span data-ttu-id="c68fb-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c68fb-158">RELATED LINKS</span></span>

[<span data-ttu-id="c68fb-159">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="c68fb-159">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)

[<span data-ttu-id="c68fb-160">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="c68fb-160">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="c68fb-161">Get-AzVMExtensionImageType</span><span class="sxs-lookup"><span data-stu-id="c68fb-161">Get-AzVMExtensionImageType</span></span>](./Get-AzVMExtensionImageType.md)

[<span data-ttu-id="c68fb-162">Get-Azvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="c68fb-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)

[<span data-ttu-id="c68fb-163">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c68fb-163">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
