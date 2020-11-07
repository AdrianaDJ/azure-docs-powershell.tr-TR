---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 6fe34ae33ed70cebe4c8f76beb235e6fa7445fee
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936840"
---
# <span data-ttu-id="a2405-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a2405-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="a2405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2405-102">SYNOPSIS</span></span>
<span data-ttu-id="a2405-103">Sanal makineye özel bir komut dosyası uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="a2405-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="a2405-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a2405-104">SYNTAX</span></span>

### <span data-ttu-id="a2405-105">Setcustomscrip/2 Sionbycontainervedosyaadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a2405-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzVMCustomScriptExtension -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>]
 [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2405-106">Setcustomscripist Sionbyurilmürekkepler</span><span class="sxs-lookup"><span data-stu-id="a2405-106">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzVMCustomScriptExtension [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2405-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a2405-107">DESCRIPTION</span></span>
<span data-ttu-id="a2405-108">**Set-AzVMCustomScriptExtension** cmdlet 'i bir sanal makineye özel betik sanal makine uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="a2405-108">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="a2405-109">Bu uzantı, sanal makinede kendi komut dosyalarınızı çalıştırmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="a2405-109">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="a2405-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a2405-110">EXAMPLES</span></span>

### <span data-ttu-id="a2405-111">Örnek 1: özel komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="a2405-111">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="a2405-112">Bu komut, VirtualMachine07 adındaki sanal makineye özel bir komut dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="a2405-112">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="a2405-113">Komut dosyası contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="a2405-113">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="a2405-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a2405-114">PARAMETERS</span></span>

### <span data-ttu-id="a2405-115">-Bağımsız değişken</span><span class="sxs-lookup"><span data-stu-id="a2405-115">-Argument</span></span>
<span data-ttu-id="a2405-116">Komut dosyası uzantısının komut dosyasına geçirdiği bağımsız değişkenleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-116">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="a2405-117">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="a2405-117">-ContainerName</span></span>
<span data-ttu-id="a2405-118">Bu cmdlet 'in betiği sakladığı Azure depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-118">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="a2405-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2405-119">-DefaultProfile</span></span>
<span data-ttu-id="a2405-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a2405-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2405-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a2405-121">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="a2405-122">-Dosya adı</span><span class="sxs-lookup"><span data-stu-id="a2405-122">-FileName</span></span>
<span data-ttu-id="a2405-123">Komut dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-123">Specifies the name of the script file.</span></span> <span data-ttu-id="a2405-124">Dosya Azure Blob depolama alanında depolanıyorsa, dosya adı büyük/küçük harf yapılır.</span><span class="sxs-lookup"><span data-stu-id="a2405-124">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="a2405-125">Azure dosya depolaması 'nda depolanan dosyaların dosya adları büyük/küçük harf değildir.</span><span class="sxs-lookup"><span data-stu-id="a2405-125">File names of files stored in Azure File storage are not case-senstive.</span></span>

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

### <span data-ttu-id="a2405-126">-FileUri</span><span class="sxs-lookup"><span data-stu-id="a2405-126">-FileUri</span></span>
<span data-ttu-id="a2405-127">Komut dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-127">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="a2405-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a2405-128">-ForceRerun</span></span>
<span data-ttu-id="a2405-129">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2405-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="a2405-130">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="a2405-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="a2405-131">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="a2405-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="a2405-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="a2405-132">-Location</span></span>
<span data-ttu-id="a2405-133">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a2405-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="a2405-134">-Name</span></span>
<span data-ttu-id="a2405-135">Özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-135">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="a2405-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2405-136">-ResourceGroupName</span></span>
<span data-ttu-id="a2405-137">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-137">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a2405-138">-Run</span><span class="sxs-lookup"><span data-stu-id="a2405-138">-Run</span></span>
<span data-ttu-id="a2405-139">Komut dosyanızı çalıştıran kullanılacak komutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-139">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="a2405-140">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="a2405-140">-SecureExecution</span></span>
<span data-ttu-id="a2405-141">Bu cmdlet 'in, *Run* parametresi değerinin sunucuda günlüğe kaydedilmediğini veya genişletme uzantısı kullanılarak kullanıcıya döndürüldüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-141">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="a2405-142">*Run* değeri, komut dosyası dosyasına güvenli bir şekilde geçirilecek parolalar veya parolalar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="a2405-142">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="a2405-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a2405-143">-StorageAccountKey</span></span>
<span data-ttu-id="a2405-144">Azure depolama kapsayıcısı için anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-144">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="a2405-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a2405-145">-StorageAccountName</span></span>
<span data-ttu-id="a2405-146">Bu cmdlet 'in betiği sakladığı Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-146">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="a2405-147">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a2405-147">-StorageEndpointSuffix</span></span>
<span data-ttu-id="a2405-148">Depolama uç noktası sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-148">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="a2405-149">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a2405-149">-TypeHandlerVersion</span></span>
<span data-ttu-id="a2405-150">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-150">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="a2405-151">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="a2405-151">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="a2405-152">-VMName</span><span class="sxs-lookup"><span data-stu-id="a2405-152">-VMName</span></span>
<span data-ttu-id="a2405-153">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a2405-153">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a2405-154">Bu cmdlet, bu parametrenin belirttiği sanal makinenin özel komut dosyası uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="a2405-154">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2405-155">-Onay</span><span class="sxs-lookup"><span data-stu-id="a2405-155">-Confirm</span></span>
<span data-ttu-id="a2405-156">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a2405-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2405-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2405-157">-WhatIf</span></span>
<span data-ttu-id="a2405-158">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a2405-158">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a2405-159">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a2405-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2405-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2405-160">CommonParameters</span></span>
<span data-ttu-id="a2405-161">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a2405-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2405-162">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2405-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2405-163">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a2405-163">INPUTS</span></span>

### <span data-ttu-id="a2405-164">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a2405-164">None</span></span>
<span data-ttu-id="a2405-165">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="a2405-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a2405-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a2405-166">OUTPUTS</span></span>

### <span data-ttu-id="a2405-167">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a2405-167">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a2405-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a2405-168">NOTES</span></span>

## <span data-ttu-id="a2405-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a2405-169">RELATED LINKS</span></span>

[<span data-ttu-id="a2405-170">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a2405-170">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="a2405-171">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="a2405-171">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


