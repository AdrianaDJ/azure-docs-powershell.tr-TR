---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 693809e46823cbcb8331eade7b8cd38c83238be2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588970"
---
# <span data-ttu-id="7f20f-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7f20f-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="7f20f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f20f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f20f-103">Sanal makineye özel bir komut dosyası uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="7f20f-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f20f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f20f-104">SYNTAX</span></span>

### <span data-ttu-id="7f20f-105">Setcustomscrip/2 Sionbycontainervedosyaadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f20f-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f20f-106">Setcustomscripist Sionbyurilmürekkepler</span><span class="sxs-lookup"><span data-stu-id="7f20f-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f20f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f20f-107">DESCRIPTION</span></span>
<span data-ttu-id="7f20f-108">**Set-AzureRmVMCustomScriptExtension** cmdlet 'i bir sanal makineye özel betik sanal makine uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="7f20f-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="7f20f-109">Bu uzantı, sanal makinede kendi komut dosyalarınızı çalıştırmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="7f20f-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="7f20f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f20f-110">EXAMPLES</span></span>

### <span data-ttu-id="7f20f-111">Örnek 1: özel komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="7f20f-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="7f20f-112">Bu komut, VirtualMachine07 adındaki sanal makineye özel bir komut dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="7f20f-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="7f20f-113">Komut dosyası contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="7f20f-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="7f20f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f20f-114">PARAMETERS</span></span>

### <span data-ttu-id="7f20f-115">-Bağımsız değişken</span><span class="sxs-lookup"><span data-stu-id="7f20f-115">-Argument</span></span>
<span data-ttu-id="7f20f-116">Komut dosyası uzantısının komut dosyasına geçirdiği bağımsız değişkenleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="7f20f-117">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="7f20f-117">-ContainerName</span></span>
<span data-ttu-id="7f20f-118">Bu cmdlet 'in betiği sakladığı Azure depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-119">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="7f20f-119">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-120">-Dosya adı</span><span class="sxs-lookup"><span data-stu-id="7f20f-120">-FileName</span></span>
<span data-ttu-id="7f20f-121">Komut dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-121">Specifies the name of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-122">-FileUri</span><span class="sxs-lookup"><span data-stu-id="7f20f-122">-FileUri</span></span>
<span data-ttu-id="7f20f-123">Komut dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-123">Specifies the URI of the script file.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-124">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="7f20f-124">-ForceRerun</span></span>
<span data-ttu-id="7f20f-125">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-125">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="7f20f-126">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-126">The value can be any string different from the current value.</span></span>

<span data-ttu-id="7f20f-127">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="7f20f-127">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="7f20f-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="7f20f-128">-Location</span></span>
<span data-ttu-id="7f20f-129">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-129">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="7f20f-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f20f-130">-Name</span></span>
<span data-ttu-id="7f20f-131">Özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-131">Specifies the name of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f20f-132">-ResourceGroupName</span></span>
<span data-ttu-id="7f20f-133">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-133">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7f20f-134">-Run</span><span class="sxs-lookup"><span data-stu-id="7f20f-134">-Run</span></span>
<span data-ttu-id="7f20f-135">Komut dosyanızı çalıştıran kullanılacak komutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-135">Specifies the command to use that runs your script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-136">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="7f20f-136">-SecureExecution</span></span>
<span data-ttu-id="7f20f-137">Bu cmdlet 'in, *Run* parametresi değerinin sunucuda günlüğe kaydedilmediğini veya genişletme uzantısı kullanılarak kullanıcıya döndürüldüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-137">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="7f20f-138">*Run* değeri, komut dosyası dosyasına güvenli bir şekilde geçirilecek parolalar veya parolalar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-138">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-139">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7f20f-139">-StorageAccountKey</span></span>
<span data-ttu-id="7f20f-140">Azure depolama kapsayıcısı için anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-140">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7f20f-141">-StorageAccountName</span></span>
<span data-ttu-id="7f20f-142">Bu cmdlet 'in betiği sakladığı Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-142">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-143">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="7f20f-143">-StorageEndpointSuffix</span></span>
<span data-ttu-id="7f20f-144">Depolama uç noktası sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-144">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-145">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="7f20f-145">-TypeHandlerVersion</span></span>
<span data-ttu-id="7f20f-146">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-146">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="7f20f-147">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzureRmVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="7f20f-147">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-148">-VMName</span><span class="sxs-lookup"><span data-stu-id="7f20f-148">-VMName</span></span>
<span data-ttu-id="7f20f-149">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-149">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7f20f-150">Bu cmdlet, bu parametrenin belirttiği sanal makinenin özel komut dosyası uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="7f20f-150">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="7f20f-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f20f-151">-Confirm</span></span>
<span data-ttu-id="7f20f-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f20f-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f20f-153">-WhatIf</span></span>
<span data-ttu-id="7f20f-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f20f-154">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7f20f-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f20f-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f20f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f20f-156">CommonParameters</span></span>
<span data-ttu-id="7f20f-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f20f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f20f-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f20f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f20f-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f20f-159">INPUTS</span></span>

### <span data-ttu-id="7f20f-160">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7f20f-160">None</span></span>
<span data-ttu-id="7f20f-161">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7f20f-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f20f-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f20f-162">OUTPUTS</span></span>

## <span data-ttu-id="7f20f-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f20f-163">NOTES</span></span>

## <span data-ttu-id="7f20f-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f20f-164">RELATED LINKS</span></span>

[<span data-ttu-id="7f20f-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7f20f-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="7f20f-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="7f20f-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


