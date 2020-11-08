---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 64AB1BAE-A756-43A8-A40F-10B746EA0946
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMCustomScriptExtension.md
ms.openlocfilehash: 69b6dec11f0135803320bb7b58bdb8362aaee26e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108396"
---
# <span data-ttu-id="2fa17-101">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2fa17-101">Set-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="2fa17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa17-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa17-103">Sanal makineye özel bir komut dosyası uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="2fa17-103">Adds a custom script extension to a virtual machine.</span></span>

## <span data-ttu-id="2fa17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2fa17-104">SYNTAX</span></span>

### <span data-ttu-id="2fa17-105">ByNameWithContainerAndFileNamesParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2fa17-105">ByNameWithContainerAndFileNamesParameterSet (Default)</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 -ContainerName <String> -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa17-106">ByNameWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fa17-106">ByNameWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-FileUri <String[]>] [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>]
 [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa17-107">ByParentObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fa17-107">ByParentObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa17-108">ByParentObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fa17-108">ByParentObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -Name <String> -VMObject <PSVirtualMachine> [-FileUri <String[]>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa17-109">Byresourceıdwithcontainerand Filenamesparameterset</span><span class="sxs-lookup"><span data-stu-id="2fa17-109">ByResourceIdWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> -ContainerName <String> -FileName <String[]>
 [-StorageAccountName <String>] [-StorageEndpointSuffix <String>] [-StorageAccountKey <String>] [-Run <String>]
 [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa17-110">Byresourceıdwithfileuriparameterset</span><span class="sxs-lookup"><span data-stu-id="2fa17-110">ByResourceIdWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -ResourceId <String> [-FileUri <String[]>] [-Run <String>] [-Argument <String>]
 [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2fa17-111">ByInputObjectWithContainerAndFileNamesParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fa17-111">ByInputObjectWithContainerAndFileNamesParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> -ContainerName <String>
 -FileName <String[]> [-StorageAccountName <String>] [-StorageEndpointSuffix <String>]
 [-StorageAccountKey <String>] [-Run <String>] [-Argument <String>] [-SecureExecution]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fa17-112">ByInputObjectWithFileUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fa17-112">ByInputObjectWithFileUriParameterSet</span></span>
```
Set-AzVMCustomScriptExtension -InputObject <VirtualMachineCustomScriptExtensionContext> [-FileUri <String[]>]
 [-Run <String>] [-Argument <String>] [-SecureExecution] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa17-113">Tanım</span><span class="sxs-lookup"><span data-stu-id="2fa17-113">DESCRIPTION</span></span>
<span data-ttu-id="2fa17-114">**Set-AzVMCustomScriptExtension** cmdlet 'i bir sanal makineye özel betik sanal makine uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="2fa17-114">The **Set-AzVMCustomScriptExtension** cmdlet adds a custom script Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="2fa17-115">Bu uzantı, sanal makinede kendi komut dosyalarınızı çalıştırmanıza olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="2fa17-115">This extension lets you run your own scripts on the virtual machine.</span></span>

## <span data-ttu-id="2fa17-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2fa17-116">EXAMPLES</span></span>

### <span data-ttu-id="2fa17-117">Örnek 1: özel komut dosyası ekleme</span><span class="sxs-lookup"><span data-stu-id="2fa17-117">Example 1: Add a custom script</span></span>
```powershell
PS C:\> Set-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "1.1" -StorageAccountName "Contoso" -StorageAccountKey <StorageKey> -FileName "ContosoScript.exe" -ContainerName "Scripts"
```

<span data-ttu-id="2fa17-118">Bu komut, VirtualMachine07 adındaki sanal makineye özel bir komut dosyası ekler.</span><span class="sxs-lookup"><span data-stu-id="2fa17-118">This command adds a custom script to the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="2fa17-119">Komut dosyası contososcript.exe.</span><span class="sxs-lookup"><span data-stu-id="2fa17-119">The script file is contososcript.exe.</span></span>

### <span data-ttu-id="2fa17-120">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2fa17-120">Example 2</span></span>

<span data-ttu-id="2fa17-121">Sanal makineye özel bir komut dosyası uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="2fa17-121">Adds a custom script extension to a virtual machine.</span></span> <span data-ttu-id="2fa17-122">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="2fa17-122">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMCustomScriptExtension -Argument <String> -ContainerName 'Scripts' -DefaultProfile <IAzureContextContainer> -FileName 'ContosoScript.exe' -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -Run 'myScript.ps1' -SecureExecution -StorageAccountKey <String> -StorageAccountName 'Contoso' -TypeHandlerVersion '1.1' -VMName 'VirtualMachine07'
```

## <span data-ttu-id="2fa17-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2fa17-123">PARAMETERS</span></span>

### <span data-ttu-id="2fa17-124">-Bağımsız değişken</span><span class="sxs-lookup"><span data-stu-id="2fa17-124">-Argument</span></span>
<span data-ttu-id="2fa17-125">Komut dosyası uzantısının komut dosyasına geçirdiği bağımsız değişkenleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-125">Specifies arguments that the script extension passes to the script.</span></span>

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

### <span data-ttu-id="2fa17-126">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="2fa17-126">-ContainerName</span></span>
<span data-ttu-id="2fa17-127">Bu cmdlet 'in betiği sakladığı Azure depolama kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-127">Specifies the name of the Azure storage container where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="2fa17-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa17-128">-DefaultProfile</span></span>
<span data-ttu-id="2fa17-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2fa17-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa17-130">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2fa17-130">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="2fa17-131">-Dosya adı</span><span class="sxs-lookup"><span data-stu-id="2fa17-131">-FileName</span></span>
<span data-ttu-id="2fa17-132">Komut dosyasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-132">Specifies the name of the script file.</span></span> <span data-ttu-id="2fa17-133">Dosya Azure Blob depolamada depolanıyorsa, dosya adı büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="2fa17-133">If the file is stored in Azure Blob storage, the file name value is case-sensitive.</span></span> <span data-ttu-id="2fa17-134">Azure dosya depolaması 'nda depolanan dosyaların dosya adları büyük/küçük harfe duyarlı değildir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-134">File names of files stored in Azure File storage are not case-sensitive.</span></span>

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

### <span data-ttu-id="2fa17-135">-FileUri</span><span class="sxs-lookup"><span data-stu-id="2fa17-135">-FileUri</span></span>
<span data-ttu-id="2fa17-136">Komut dosyasının URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-136">Specifies the URI of the script file.</span></span>

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

### <span data-ttu-id="2fa17-137">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2fa17-137">-ForceRerun</span></span>
<span data-ttu-id="2fa17-138">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-138">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2fa17-139">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-139">The value can be any string different from the current value.</span></span>
<span data-ttu-id="2fa17-140">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2fa17-140">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2fa17-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2fa17-141">-InputObject</span></span>
<span data-ttu-id="2fa17-142">VM Uzantısı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2fa17-142">VM extension object.</span></span>

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

### <span data-ttu-id="2fa17-143">-Konum</span><span class="sxs-lookup"><span data-stu-id="2fa17-143">-Location</span></span>
<span data-ttu-id="2fa17-144">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-144">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2fa17-145">-Ad</span><span class="sxs-lookup"><span data-stu-id="2fa17-145">-Name</span></span>
<span data-ttu-id="2fa17-146">Özel komut dosyası uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-146">Specifies the name of the custom script extension.</span></span>

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

### <span data-ttu-id="2fa17-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2fa17-147">-NoWait</span></span>
<span data-ttu-id="2fa17-148">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="2fa17-148">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2fa17-149">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="2fa17-149">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2fa17-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fa17-150">-ResourceGroupName</span></span>
<span data-ttu-id="2fa17-151">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2fa17-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2fa17-152">-ResourceId</span></span>
<span data-ttu-id="2fa17-153">VM Uzantısı RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="2fa17-153">VM extension ResourceID.</span></span>

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

### <span data-ttu-id="2fa17-154">-Run</span><span class="sxs-lookup"><span data-stu-id="2fa17-154">-Run</span></span>
<span data-ttu-id="2fa17-155">Komut dosyanızı çalıştıran kullanılacak komutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-155">Specifies the command to use that runs your script.</span></span>

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

### <span data-ttu-id="2fa17-156">-SecureExecution</span><span class="sxs-lookup"><span data-stu-id="2fa17-156">-SecureExecution</span></span>
<span data-ttu-id="2fa17-157">Bu cmdlet 'in, *Run* parametresi değerinin sunucuda günlüğe kaydedilmediğini veya genişletme uzantısı kullanılarak kullanıcıya döndürüldüğünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-157">Indicates that this cmdlet makes sure that the value of the *Run* parameter is not logged on the server or returned to the user by using the GET extension API.</span></span>
<span data-ttu-id="2fa17-158">*Run* değeri, komut dosyası dosyasına güvenli bir şekilde geçirilecek parolalar veya parolalar içerebilir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-158">The value of *Run* might contain secrets or passwords to be passed to the script file securely.</span></span>

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

### <span data-ttu-id="2fa17-159">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2fa17-159">-StorageAccountKey</span></span>
<span data-ttu-id="2fa17-160">Azure depolama kapsayıcısı için anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-160">Specifies the key for the Azure storage container.</span></span>

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

### <span data-ttu-id="2fa17-161">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2fa17-161">-StorageAccountName</span></span>
<span data-ttu-id="2fa17-162">Bu cmdlet 'in betiği sakladığı Azure depolama hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-162">Specifies the name of the Azure storage account where this cmdlet stores the script.</span></span>

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

### <span data-ttu-id="2fa17-163">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2fa17-163">-StorageEndpointSuffix</span></span>
<span data-ttu-id="2fa17-164">Depolama uç noktası sonekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-164">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="2fa17-165">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2fa17-165">-TypeHandlerVersion</span></span>
<span data-ttu-id="2fa17-166">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-166">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2fa17-167">Sürümü edinmek için, Get-AzVMExtensionImage cmdlet 'i, *tür* parametresine yönelik *PublisherName* parametresi ve customscriptextension ile çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2fa17-167">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and CustomScriptExtension for the *Type* parameter.</span></span>

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

### <span data-ttu-id="2fa17-168">-VMName</span><span class="sxs-lookup"><span data-stu-id="2fa17-168">-VMName</span></span>
<span data-ttu-id="2fa17-169">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-169">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2fa17-170">Bu cmdlet, bu parametrenin belirttiği sanal makinenin özel komut dosyası uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="2fa17-170">This cmdlet adds the custom script extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2fa17-171">-VMObject</span><span class="sxs-lookup"><span data-stu-id="2fa17-171">-VMObject</span></span>
<span data-ttu-id="2fa17-172">VM nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2fa17-172">VM object.</span></span>

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

### <span data-ttu-id="2fa17-173">-Onay</span><span class="sxs-lookup"><span data-stu-id="2fa17-173">-Confirm</span></span>
<span data-ttu-id="2fa17-174">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2fa17-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa17-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa17-175">-WhatIf</span></span>
<span data-ttu-id="2fa17-176">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2fa17-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa17-177">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2fa17-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa17-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa17-178">CommonParameters</span></span>
<span data-ttu-id="2fa17-179">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2fa17-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa17-180">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2fa17-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa17-181">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2fa17-181">INPUTS</span></span>

### <span data-ttu-id="2fa17-182">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa17-182">System.String</span></span>

### <span data-ttu-id="2fa17-183">System. String []</span><span class="sxs-lookup"><span data-stu-id="2fa17-183">System.String[]</span></span>

### <span data-ttu-id="2fa17-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2fa17-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2fa17-185">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2fa17-185">OUTPUTS</span></span>

### <span data-ttu-id="2fa17-186">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2fa17-186">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2fa17-187">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2fa17-187">NOTES</span></span>

## <span data-ttu-id="2fa17-188">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2fa17-188">RELATED LINKS</span></span>

[<span data-ttu-id="2fa17-189">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2fa17-189">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="2fa17-190">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2fa17-190">Remove-AzVMCustomScriptExtension</span></span>](./Remove-AzVMCustomScriptExtension.md)


