---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssDiskEncryptionExtension.md
ms.openlocfilehash: 8036eede968d4c5f5b183b0713094740cfe127d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917212"
---
# <span data-ttu-id="510d0-101">Set-AzVmssDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="510d0-101">Set-AzVmssDiskEncryptionExtension</span></span>

## <span data-ttu-id="510d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="510d0-102">SYNOPSIS</span></span>
<span data-ttu-id="510d0-103">VM ölçeklendirme kümesinde disk şifrelemesini etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="510d0-103">Enables disk encryption on a VM scale set.</span></span>

## <span data-ttu-id="510d0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="510d0-104">SYNTAX</span></span>

```
Set-AzVmssDiskEncryptionExtension [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DiskEncryptionKeyVaultUrl] <String> [-DiskEncryptionKeyVaultId] <String> [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionKeyVaultId <String>] [-KeyEncryptionAlgorithm <String>] [-VolumeType <String>] [-ForceUpdate]
 [-TypeHandlerVersion <String>] [-ExtensionName <String>] [-Passphrase <String>] [-Force]
 [-DisableAutoUpgradeMinorVersion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="510d0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="510d0-105">DESCRIPTION</span></span>
<span data-ttu-id="510d0-106">**Set-AzVmssDiskEncryptionExtension** CMDLET 'i VM ölçeklendirme kümesinde şifrelemeyi olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="510d0-106">The **Set-AzVmssDiskEncryptionExtension** cmdlet enables encryption on a VM scale set.</span></span>
<span data-ttu-id="510d0-107">Bu cmdlet, VM ölçeklendirme kümesine disk şifrelemesi uzantısını yükleyerek şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="510d0-107">This cmdlet enables encryption by installing the disk encryption extension on the VM scale set.</span></span>
<span data-ttu-id="510d0-108">*Ad* parametresi belirtilmezse, Windows işletim sistemini veya Linux sanal makineleri için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde varsayılan ad AzureDiskEncryption bir uzantı yüklenir.</span><span class="sxs-lookup"><span data-stu-id="510d0-108">If no *Name* parameter is specified, an extension with the default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux virtual machines are installed.</span></span>

## <span data-ttu-id="510d0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="510d0-109">EXAMPLES</span></span>

### <span data-ttu-id="510d0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="510d0-110">Example 1</span></span>
```
$RGName = "MyResourceGroup"
$VmssName = "MyTestVmss"
$VaultName= "MyKeyVault"
$KeyVault = Get-AzKeyVault -VaultName $VaultName -ResourceGroupName $RGName
$DiskEncryptionKeyVaultUrl = $KeyVault.VaultUri
$KeyVaultResourceId = $KeyVault.ResourceId
PS C:\> Set-AzVmssDiskEncryptionExtension -ResourceGroupName $RGName -VMScaleSetName $VmssName -DiskEncryptionKeyVaultUrl $DiskEncryptionKeyVaultUrl -DiskEncryptionKeyVaultId $KeyVaultResourceId
```

<span data-ttu-id="510d0-111">Bu komut, VM Ölçek kümesindeki tüm VM 'lerin tüm disklerinde şifrelemeyi mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="510d0-111">This command enables encryption on all disks of all VMs in the VM scale set.</span></span>

## <span data-ttu-id="510d0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="510d0-112">PARAMETERS</span></span>

### <span data-ttu-id="510d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="510d0-113">-DefaultProfile</span></span>
<span data-ttu-id="510d0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="510d0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="510d0-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="510d0-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="510d0-116">Alt sürümün otomatik yükseltmesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="510d0-116">Disable auto-upgrade of minor version</span></span>

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

### <span data-ttu-id="510d0-117">-DiskEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="510d0-117">-DiskEncryptionKeyVaultId</span></span>
<span data-ttu-id="510d0-118">Oluşturulan şifreleme anahtarının yerleştirileceği tuş Kasası RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="510d0-118">ResourceID of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="510d0-119">-DiskEncryptionKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="510d0-119">-DiskEncryptionKeyVaultUrl</span></span>
<span data-ttu-id="510d0-120">Oluşturulan şifreleme anahtarının yerleştirileceği tuş Kasası URL 'SI</span><span class="sxs-lookup"><span data-stu-id="510d0-120">URL of the KeyVault where generated encryption key will be placed to</span></span>

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

### <span data-ttu-id="510d0-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="510d0-121">-ExtensionName</span></span>
<span data-ttu-id="510d0-122">Uzantı adı.</span><span class="sxs-lookup"><span data-stu-id="510d0-122">The extension name.</span></span>
<span data-ttu-id="510d0-123">Bu parametre belirtilmezse, kullanılan varsayılan değerler Windows VM 'Ler için AzureDiskEncryption ve Linux VM 'Ler için AzureDiskEncryptionForLinux</span><span class="sxs-lookup"><span data-stu-id="510d0-123">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs</span></span>

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

### <span data-ttu-id="510d0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="510d0-124">-Force</span></span>
<span data-ttu-id="510d0-125">Sanal makine ölçeği kümesinde şifrelemeyi etkinleştirmeye zorlamak için.</span><span class="sxs-lookup"><span data-stu-id="510d0-125">To force enabling encryption on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="510d0-126">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="510d0-126">-ForceUpdate</span></span>
<span data-ttu-id="510d0-127">Zorla güncelleştirmesi için bir etiket oluşturun.</span><span class="sxs-lookup"><span data-stu-id="510d0-127">Generate a tag for force update.</span></span>  <span data-ttu-id="510d0-128">Bu, aynı VM 'de yinelenen şifreleme işlemleri gerçekleştirmek için verilmelidir.</span><span class="sxs-lookup"><span data-stu-id="510d0-128">This should be given to perform repeated encryption operations on the same VM.</span></span>

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

### <span data-ttu-id="510d0-129">-KeyEncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="510d0-129">-KeyEncryptionAlgorithm</span></span>
<span data-ttu-id="510d0-130">Birim şifreleme anahtarını şifrelemek için kullanılan KeyEncryption algoritması</span><span class="sxs-lookup"><span data-stu-id="510d0-130">KeyEncryption Algorithm used to encrypt the volume encryption key</span></span>

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

### <span data-ttu-id="510d0-131">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="510d0-131">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="510d0-132">Disk şifrelemesi anahtarını şifrelemek için kullanılan KeyEncryptionKey 'in sürümlenmiş tuş Kasası URL 'SI</span><span class="sxs-lookup"><span data-stu-id="510d0-132">Versioned KeyVault URL of the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="510d0-133">-KeyEncryptionKeyVaultId</span><span class="sxs-lookup"><span data-stu-id="510d0-133">-KeyEncryptionKeyVaultId</span></span>
<span data-ttu-id="510d0-134">Disk şifrelemesi anahtarını şifrelemede kullanılan KeyEncryptionKey içeren Anahtar Kasası RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="510d0-134">ResourceID of the KeyVault containing the KeyEncryptionKey used to encrypt the disk encryption key</span></span>

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

### <span data-ttu-id="510d0-135">-Parola</span><span class="sxs-lookup"><span data-stu-id="510d0-135">-Passphrase</span></span>
<span data-ttu-id="510d0-136">Parametrelerde belirtilen parola.</span><span class="sxs-lookup"><span data-stu-id="510d0-136">The passphrase specified in parameters.</span></span>
<span data-ttu-id="510d0-137">Bu parametre yalnızca Linux VM için çalışır.</span><span class="sxs-lookup"><span data-stu-id="510d0-137">This parameter only works for Linux VM.</span></span>

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

### <span data-ttu-id="510d0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="510d0-138">-ResourceGroupName</span></span>
<span data-ttu-id="510d0-139">VM ölçeklendirme kümesinin ait olduğu kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="510d0-139">The resource group name to which the VM Scale Set belongs to</span></span>

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

### <span data-ttu-id="510d0-140">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="510d0-140">-TypeHandlerVersion</span></span>
<span data-ttu-id="510d0-141">Tür işleyicisi sürümü.</span><span class="sxs-lookup"><span data-stu-id="510d0-141">The type handler version.</span></span>

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

### <span data-ttu-id="510d0-142">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="510d0-142">-VMScaleSetName</span></span>
<span data-ttu-id="510d0-143">Sanal makine ölçek kümesinin adı</span><span class="sxs-lookup"><span data-stu-id="510d0-143">Name of the virtual machine scale set</span></span>

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

### <span data-ttu-id="510d0-144">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="510d0-144">-VolumeType</span></span>
<span data-ttu-id="510d0-145">Şifreleme işlemi gerçekleştirmek için birimin türü (OS veya veri)</span><span class="sxs-lookup"><span data-stu-id="510d0-145">Type of the volume (OS or Data) to perform encryption operation</span></span>

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

### <span data-ttu-id="510d0-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="510d0-146">-Confirm</span></span>
<span data-ttu-id="510d0-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="510d0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="510d0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="510d0-148">-WhatIf</span></span>
<span data-ttu-id="510d0-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="510d0-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="510d0-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="510d0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="510d0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="510d0-151">CommonParameters</span></span>
<span data-ttu-id="510d0-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="510d0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="510d0-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="510d0-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="510d0-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="510d0-154">INPUTS</span></span>

### <span data-ttu-id="510d0-155">System. String</span><span class="sxs-lookup"><span data-stu-id="510d0-155">System.String</span></span>

### <span data-ttu-id="510d0-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="510d0-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="510d0-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="510d0-157">OUTPUTS</span></span>

### <span data-ttu-id="510d0-158">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineScaleSetExtension</span><span class="sxs-lookup"><span data-stu-id="510d0-158">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineScaleSetExtension</span></span>

## <span data-ttu-id="510d0-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="510d0-159">NOTES</span></span>

## <span data-ttu-id="510d0-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="510d0-160">RELATED LINKS</span></span>
