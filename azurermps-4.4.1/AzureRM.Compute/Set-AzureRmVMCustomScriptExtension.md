---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: a9d03bd7f506c7210eeee90c379f90dd0833818e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586930"
---
# <span data-ttu-id="5a785-101">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5a785-101">Set-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="5a785-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a785-102">SYNOPSIS</span></span>
<span data-ttu-id="5a785-103">Sanal makineye özel bir komut dosyası uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="5a785-103">Adds a custom script extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a785-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a785-104">SYNTAX</span></span>

### <span data-ttu-id="5a785-105">Setcustomscrip/2 Sionbycontainervedosyaadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5a785-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureRmVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a785-106">Setcustomscripist Sionbyurilmürekkepler</span><span class="sxs-lookup"><span data-stu-id="5a785-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureRmVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a785-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a785-107">DESCRIPTION</span></span>
<span data-ttu-id="5a785-108">**Set-AzureRmVMCustomScriptExtension** cmdlet 'i bir sanal makineye özel betik sanal makine uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="5a785-108">The **Set-AzureRmVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="5a785-109">Bu uzantı, sanal makinede kendi komut dosyalarınızı çalıştırmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5a785-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="5a785-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a785-110">EXAMPLES</span></span>

### <span data-ttu-id="5a785-111">Örnek 1: özel komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="5a785-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzureRmVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="5a785-112">Bu komut, VirtualMachine07 adındaki sanal makineye özel bir komut dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="5a785-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="5a785-113">Komut dosyası contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="5a785-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="5a785-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a785-114">PARAMETERS</span></span>

### <span data-ttu-id="5a785-115">-Bağımsız değişken</span><span class="sxs-lookup"><span data-stu-id="5a785-115">-Argument</span></span>
<span data-ttu-id="5a785-116">Komut dosyası uzantısının komut dosyasına geçirdiği bağımsız değişkenleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="5a785-117">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="5a785-117">-ContainerName</span></span>
<span data-ttu-id="5a785-118">Bu cmdlet 'in betiği sakladığı Azure depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a785-119">-DefaultProfile</span></span>
<span data-ttu-id="5a785-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a785-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a785-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="5a785-121">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-122">-Dosya adı</span><span class="sxs-lookup"><span data-stu-id="5a785-122">-FileName</span></span>
<span data-ttu-id="5a785-123">Komut dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-123">Specifies the name of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-124">-FileUri</span><span class="sxs-lookup"><span data-stu-id="5a785-124">-FileUri</span></span>
<span data-ttu-id="5a785-125">Komut dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-125">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="5a785-126">-ForceRerun</span></span>
<span data-ttu-id="5a785-127">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a785-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="5a785-128">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5a785-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="5a785-129">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="5a785-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="5a785-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="5a785-130">-Location</span></span>
<span data-ttu-id="5a785-131">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5a785-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a785-132">-Name</span></span>
<span data-ttu-id="5a785-133">Özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-133">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a785-134">-ResourceGroupName</span></span>
<span data-ttu-id="5a785-135">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-135">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5a785-136">-Run</span><span class="sxs-lookup"><span data-stu-id="5a785-136">-Run</span></span>
<span data-ttu-id="5a785-137">Komut dosyanızı çalıştıran kullanılacak komutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-137">Specifies the command to use that runs your script.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunFile, Command

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-138">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="5a785-138">-SecureExecution</span></span>
<span data-ttu-id="5a785-139">Bu cmdlet 'in, *Run* parametresi değerinin sunucuda günlüğe kaydedilmediğini veya genişletme uzantısı kullanılarak kullanıcıya döndürüldüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-139">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="5a785-140">*Run* değeri, komut dosyası dosyasına güvenli bir şekilde geçirilecek parolalar veya parolalar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="5a785-140">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-141">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5a785-141">-StorageAccountKey</span></span>
<span data-ttu-id="5a785-142">Azure depolama kapsayıcısı için anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-142">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-143">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5a785-143">-StorageAccountName</span></span>
<span data-ttu-id="5a785-144">Bu cmdlet 'in betiği sakladığı Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-144">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-145">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="5a785-145">-StorageEndpointSuffix</span></span>
<span data-ttu-id="5a785-146">Depolama uç noktası sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-146">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-147">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="5a785-147">-TypeHandlerVersion</span></span>
<span data-ttu-id="5a785-148">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-148">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="5a785-149">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzureRmVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="5a785-149">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-150">-VMName</span><span class="sxs-lookup"><span data-stu-id="5a785-150">-VMName</span></span>
<span data-ttu-id="5a785-151">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a785-151">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="5a785-152">Bu cmdlet, bu parametrenin belirttiği sanal makinenin özel komut dosyası uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="5a785-152">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="5a785-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a785-153">-Confirm</span></span>
<span data-ttu-id="5a785-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a785-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a785-155">-WhatIf</span></span>
<span data-ttu-id="5a785-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a785-156">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5a785-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a785-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a785-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a785-158">CommonParameters</span></span>
<span data-ttu-id="5a785-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a785-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a785-160">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a785-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a785-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a785-161">INPUTS</span></span>

## <span data-ttu-id="5a785-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a785-162">OUTPUTS</span></span>

## <span data-ttu-id="5a785-163">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a785-163">NOTES</span></span>

## <span data-ttu-id="5a785-164">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a785-164">RELATED LINKS</span></span>

[<span data-ttu-id="5a785-165">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5a785-165">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="5a785-166">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="5a785-166">Remove-AzureRmVMCustomScriptExtension</span></span>](./Remove-AzureRmVMCustomScriptExtension.md)


