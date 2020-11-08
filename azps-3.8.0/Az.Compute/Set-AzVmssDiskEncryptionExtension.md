---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: a18e91a147e60ddc54caacccd8c63f3568bfe2eb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104619"
---
# <span data-ttu-id="e7219-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="e7219-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="e7219-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7219-102">SYNOPSIS</span></span>
<span data-ttu-id="e7219-103">VM ölçeklendirme kümesinde disk şifrelemesini etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="e7219-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="e7219-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7219-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7219-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7219-105">DESCRIPTION</span></span>
<span data-ttu-id="e7219-106">**Set-AzVmssDiskEncryptionExtension** CMDLET 'i VM ölçeklendirme kümesinde şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="e7219-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span> <span data-ttu-id="e7219-107">Bu cmdlet, VM ölçeklendirme kümesine disk şifrelemesi uzantısını yükleyerek şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="e7219-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>

<span data-ttu-id="e7219-108">Linux sanal makinelerde, *Birimtürü* parametresi olmalıdır ve "veriler" olarak ayarlanmalıdır</span><span class="sxs-lookup"><span data-stu-id="e7219-108">For Linux virtual machines, the *VolumeType* parameter must be present and must be set to "Data"</span></span>

## <span data-ttu-id="e7219-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7219-109">EXAMPLES</span></span>

### <span data-ttu-id="e7219-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7219-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="e7219-111">Bu komut, bir VM Ölçek kümesindeki tüm Windows VM 'Lerde şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="e7219-111">This command enables encryption on all disks of all Windows VMs in a VM scale set.</span></span>

### <span data-ttu-id="e7219-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e7219-112">Example 2</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
$VolumeType = "Data"

PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
 -VolumeType $volumeType
```

<span data-ttu-id="e7219-113">Bu komut, bir VM Ölçek kümesindeki tüm Linux VM 'lerin veri disklerinde şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="e7219-113">This command enables encryption on the data disks of all Linux VMs in a VM scale set.</span></span>

## <span data-ttu-id="e7219-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7219-114">PARAMETERS</span></span>

### <span data-ttu-id="e7219-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7219-115">-DefaultProfile</span></span>
<span data-ttu-id="e7219-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7219-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7219-117">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="e7219-117">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="e7219-118">Alt sürümün otomatik yükseltmesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e7219-118">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="e7219-119">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e7219-119">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="e7219-120">Oluşturulan şifreleme anahtarının yerleştirileceği tuş Kasası RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e7219-120">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7219-121">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e7219-121">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="e7219-122">Oluşturulan şifreleme anahtarının yerleştirileceği tuş Kasası URL 'SI</span><span class="sxs-lookup"><span data-stu-id="e7219-122">URL of the KeyVault where generated encryption key will be placed to</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7219-123">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e7219-123">-ExtensionName</span></span>
<span data-ttu-id="e7219-124">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="e7219-124">The extension name.</span></span>
<span data-ttu-id="e7219-125">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'Ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="e7219-125">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="e7219-126">-Force</span><span class="sxs-lookup"><span data-stu-id="e7219-126">-Force</span></span>
<span data-ttu-id="e7219-127">Sanal makine ölçeği kümesinde şifrelemeyi etkinleştirmeye zorlamak için.</span><span class="sxs-lookup"><span data-stu-id="e7219-127">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e7219-128">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="e7219-128">-ForceUpdate</span></span>
<span data-ttu-id="e7219-129">Zorla güncelleştirmesi için bir etiket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e7219-129">Generate a tag for force update.</span></span>  <span data-ttu-id="e7219-130">Bu, aynı VM 'de yinelenen şifreleme işlemleri gerçekleştirmek için verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="e7219-130">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="e7219-131">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e7219-131">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="e7219-132">Birim şifreleme anahtarını şifrelemek için kullanılan KeyEncryption algoritması</span><span class="sxs-lookup"><span data-stu-id="e7219-132">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7219-133">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="e7219-133">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="e7219-134">Disk şifrelemesi anahtarını şifrelemek için kullanılan KeyEncryptionKey 'in sürümlenmiş tuş Kasası URL 'SI</span><span class="sxs-lookup"><span data-stu-id="e7219-134">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="e7219-135">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e7219-135">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="e7219-136">Disk şifrelemesi anahtarını şifrelemede kullanılan KeyEncryptionKey içeren Anahtar Kasası RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e7219-136">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="e7219-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="e7219-137">-Passphrase</span></span>
<span data-ttu-id="e7219-138">Parametrelerde belirtilen parola.</span><span class="sxs-lookup"><span data-stu-id="e7219-138">The passphrase specified in parameters.</span></span>
<span data-ttu-id="e7219-139">Bu parametre yalnızca Linux VM için çalışır.</span><span class="sxs-lookup"><span data-stu-id="e7219-139">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="e7219-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7219-140">-ResourceGroupName</span></span>
<span data-ttu-id="e7219-141">VM ölçeklendirme kümesinin ait olduğu kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e7219-141">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="e7219-142">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="e7219-142">-TypeHandlerVersion</span></span>
<span data-ttu-id="e7219-143">Tür işleyicisi sürümü.</span><span class="sxs-lookup"><span data-stu-id="e7219-143">The type handler version.</span></span>

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

### <span data-ttu-id="e7219-144">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e7219-144">-VMScaleSetName</span></span>
<span data-ttu-id="e7219-145">Sanal makine ölçek kümesinin adı</span><span class="sxs-lookup"><span data-stu-id="e7219-145">Name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7219-146">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="e7219-146">-VolumeType</span></span>
<span data-ttu-id="e7219-147">Şifreleme işleminin gerçekleştirileceği sanal makine birimlerinin türünü belirtir: işletim sistemi, veri veya tümü.</span><span class="sxs-lookup"><span data-stu-id="e7219-147">Specifies the type of virtual machine volumes on which to perform encryption operation: OS, Data, or All.</span></span> 

<span data-ttu-id="e7219-148">Linux: **Birimtürü** parametresi bulunmalıdır ve veri olarak ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e7219-148">Linux: The **VolumeType** parameter must be present and must be set to Data.</span></span> 

<span data-ttu-id="e7219-149">Windows: varsa, **Birimtürü** parametresi Tümü veya işletim sistemine ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e7219-149">Windows: The **VolumeType** parameter, if present, must be set to either All or OS.</span></span> <span data-ttu-id="e7219-150">**Birimtürü** parametresi atlanırsa, varsayılan olarak "tümü" olur.</span><span class="sxs-lookup"><span data-stu-id="e7219-150">If the **VolumeType** parameter is omitted it defaults to "All".</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7219-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="e7219-151">-Confirm</span></span>
<span data-ttu-id="e7219-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e7219-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7219-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7219-153">-WhatIf</span></span>
<span data-ttu-id="e7219-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e7219-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7219-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e7219-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7219-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7219-156">CommonParameters</span></span>
<span data-ttu-id="e7219-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7219-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7219-158">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e7219-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7219-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7219-159">INPUTS</span></span>

### <span data-ttu-id="e7219-160">System. String</span><span class="sxs-lookup"><span data-stu-id="e7219-160">System.String</span></span>

### <span data-ttu-id="e7219-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7219-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7219-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7219-162">OUTPUTS</span></span>

### <span data-ttu-id="e7219-163">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="e7219-163">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="e7219-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7219-164">NOTES</span></span>

## <span data-ttu-id="e7219-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7219-165">RELATED LINKS</span></span>
