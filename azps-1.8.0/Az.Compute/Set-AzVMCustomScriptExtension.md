---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 331850ff03feeaf1f49bd8e6a6c8486bd9b0e95a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761234"
---
# <span data-ttu-id="afa61-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="afa61-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="afa61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afa61-102">SYNOPSIS</span></span>
<span data-ttu-id="afa61-103">Sanal makineye özel bir komut dosyası uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="afa61-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="afa61-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="afa61-104">SYNTAX</span></span>

### <span data-ttu-id="afa61-105">ByNameWithContainerAndFileNamesParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="afa61-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa61-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa61-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa61-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa61-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa61-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa61-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa61-109">Byresourceıdwithcontainerand Filenamesparameterset</span><span class="sxs-lookup"><span data-stu-id="afa61-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa61-110">Byresourceıdwithfileuriparameterset</span><span class="sxs-lookup"><span data-stu-id="afa61-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa61-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa61-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afa61-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="afa61-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afa61-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="afa61-113">DESCRIPTION</span></span>
<span data-ttu-id="afa61-114">**Set-AzVMCustomScriptExtension** cmdlet 'i bir sanal makineye özel betik sanal makine uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="afa61-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="afa61-115">Bu uzantı, sanal makinede kendi komut dosyalarınızı çalıştırmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="afa61-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="afa61-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="afa61-116">EXAMPLES</span></span>

### <span data-ttu-id="afa61-117">Örnek 1: özel komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="afa61-117">Example 1: Add a custom script</span></span>
```
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="afa61-118">Bu komut, VirtualMachine07 adındaki sanal makineye özel bir komut dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="afa61-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="afa61-119">Komut dosyası contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="afa61-119">The script file is contososcript.exe.</span></span>

## <span data-ttu-id="afa61-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="afa61-120">PARAMETERS</span></span>

### <span data-ttu-id="afa61-121">-Bağımsız değişken</span><span class="sxs-lookup"><span data-stu-id="afa61-121">-Argument</span></span>
<span data-ttu-id="afa61-122">Komut dosyası uzantısının komut dosyasına geçirdiği bağımsız değişkenleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-122">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="afa61-123">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="afa61-123">-ContainerName</span></span>
<span data-ttu-id="afa61-124">Bu cmdlet 'in betiği sakladığı Azure depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-124">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afa61-125">-DefaultProfile</span></span>
<span data-ttu-id="afa61-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="afa61-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afa61-127">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="afa61-127">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="afa61-128">-Dosya adı</span><span class="sxs-lookup"><span data-stu-id="afa61-128">-FileName</span></span>
<span data-ttu-id="afa61-129">Komut dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-129">Specifies the name of the script file.</span></span> <span data-ttu-id="afa61-130">Dosya Azure Blob depolama alanında depolanıyorsa, dosya adı büyük/küçük harf yapılır.</span><span class="sxs-lookup"><span data-stu-id="afa61-130">If the file is stored in Azure Blob storage, the file name value is case-senstive.</span></span> <span data-ttu-id="afa61-131">Azure dosya depolaması 'nda depolanan dosyaların dosya adları büyük/küçük harf değildir.</span><span class="sxs-lookup"><span data-stu-id="afa61-131">File names of files stored in Azure File storage are not case-senstive.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-132">-FileUri</span><span class="sxs-lookup"><span data-stu-id="afa61-132">-FileUri</span></span>
<span data-ttu-id="afa61-133">Komut dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-133">Specifies the URI of the script file.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByNameWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: ByParentObjectWithFileUriParameterSet, ByResourceIdWithFileUriParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-134">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="afa61-134">-ForceRerun</span></span>
<span data-ttu-id="afa61-135">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afa61-135">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="afa61-136">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="afa61-136">The value can be any string different from the current value.</span></span>
<span data-ttu-id="afa61-137">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="afa61-137">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="afa61-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afa61-138">-InputObject</span></span>
<span data-ttu-id="afa61-139">VM Uzantısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="afa61-139">VM extension object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext
Parameter Sets: ByInputObjectWithContainerAndFileNamesParameterSet, ByInputObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="afa61-140">-Location</span></span>
<span data-ttu-id="afa61-141">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-141">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="afa61-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="afa61-142">-Name</span></span>
<span data-ttu-id="afa61-143">Özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-143">Specifies the name of the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases: ExtensionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afa61-144">-ResourceGroupName</span></span>
<span data-ttu-id="afa61-145">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-145">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-146">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="afa61-146">-ResourceId</span></span>
<span data-ttu-id="afa61-147">VM Uzantısı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="afa61-147">VM extension ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdWithContainerAndFileNamesParameterSet, ByResourceIdWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-148">-Run</span><span class="sxs-lookup"><span data-stu-id="afa61-148">-Run</span></span>
<span data-ttu-id="afa61-149">Komut dosyanızı çalıştıran kullanılacak komutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-149">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="afa61-150">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="afa61-150">-SecureExecution</span></span>
<span data-ttu-id="afa61-151">Bu cmdlet 'in, *Run* parametresi değerinin sunucuda günlüğe kaydedilmediğini veya genişletme uzantısı kullanılarak kullanıcıya döndürüldüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-151">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="afa61-152">*Run* değeri, komut dosyası dosyasına güvenli bir şekilde geçirilecek parolalar veya parolalar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="afa61-152">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="afa61-153">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="afa61-153">-StorageAccountKey</span></span>
<span data-ttu-id="afa61-154">Azure depolama kapsayıcısı için anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-154">Specifies the key for the Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-155">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="afa61-155">-StorageAccountName</span></span>
<span data-ttu-id="afa61-156">Bu cmdlet 'in betiği sakladığı Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-156">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-157">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="afa61-157">-StorageEndpointSuffix</span></span>
<span data-ttu-id="afa61-158">Depolama uç noktası sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-158">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByResourceIdWithContainerAndFileNamesParameterSet, ByInputObjectWithContainerAndFileNamesParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-159">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="afa61-159">-TypeHandlerVersion</span></span>
<span data-ttu-id="afa61-160">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-160">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="afa61-161">Sürümü edinmek için, Get-AzVMExtensionImage cmdlet 'i, *tür* parametresine yönelik *PublisherName* parametresi ve customscriptextension ile çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="afa61-161">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="afa61-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="afa61-162">-VMName</span></span>
<span data-ttu-id="afa61-163">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="afa61-163">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="afa61-164">Bu cmdlet, bu parametrenin belirttiği sanal makinenin özel komut dosyası uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="afa61-164">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameWithContainerAndFileNamesParameterSet, ByNameWithFileUriParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-165">-VMObject</span><span class="sxs-lookup"><span data-stu-id="afa61-165">-VMObject</span></span>
<span data-ttu-id="afa61-166">VM nesnesi.</span><span class="sxs-lookup"><span data-stu-id="afa61-166">VM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: ByParentObjectWithContainerAndFileNamesParameterSet, ByParentObjectWithFileUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afa61-167">-Onay</span><span class="sxs-lookup"><span data-stu-id="afa61-167">-Confirm</span></span>
<span data-ttu-id="afa61-168">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="afa61-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afa61-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afa61-169">-WhatIf</span></span>
<span data-ttu-id="afa61-170">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="afa61-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afa61-171">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="afa61-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afa61-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afa61-172">CommonParameters</span></span>
<span data-ttu-id="afa61-173">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="afa61-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afa61-174">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afa61-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afa61-175">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="afa61-175">INPUTS</span></span>

### <span data-ttu-id="afa61-176">System. String</span><span class="sxs-lookup"><span data-stu-id="afa61-176">System.String</span></span>

### <span data-ttu-id="afa61-177">System. String []</span><span class="sxs-lookup"><span data-stu-id="afa61-177">System.String[]</span></span>

### <span data-ttu-id="afa61-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="afa61-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="afa61-179">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="afa61-179">OUTPUTS</span></span>

### <span data-ttu-id="afa61-180">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="afa61-180">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="afa61-181">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="afa61-181">NOTES</span></span>

## <span data-ttu-id="afa61-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="afa61-182">RELATED LINKS</span></span>

[<span data-ttu-id="afa61-183">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="afa61-183">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="afa61-184">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="afa61-184">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


