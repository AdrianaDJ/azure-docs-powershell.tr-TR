---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276240"
---
# <span data-ttu-id="9d1a3-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9d1a3-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="9d1a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="9d1a3-103">Sanal makineden disk şifrelemesi uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="9d1a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9d1a3-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d1a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9d1a3-105">DESCRIPTION</span></span>
<span data-ttu-id="9d1a3-106">**Remove-AzVMDiskEncryptionExtension** cmdlet 'i, disk şifrelemesi uzantısını ve ilişkili uzantı yapılandırmasını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="9d1a3-107">Uzantı adı belirtilmemişse, bu cmdlet, Windows işletim sistemini veya Linux tabanlı sanal makineler için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde varsayılan ad AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="9d1a3-108">Sanal makinede şifreleme ilk kez devre dışı bırakılmışsa, bu cmdlet başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="9d1a3-109">Bir sanal makinede şifrelemeyi devre dışı bırakmak için [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md)'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="9d1a3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9d1a3-110">EXAMPLES</span></span>

### <span data-ttu-id="9d1a3-111">Örnek 1: sanal makineden disk şifrelemesi uzantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="9d1a3-112">Bu komut, Windows işletim sistemi veya AzureDiskEncryptionForLinux adlı Linux tabanlı sanal makinede çalışan bir sanal makine için varsayılan ad AzureDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9d1a3-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="9d1a3-113">Örnek 2: sanal makineden belirli bir disk şifrelemesi uzantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="9d1a3-114">Bu komut Mydiskencryptionextenmytestvm adlı sanal makineden MyDiskEncryptionExtension adlı şifreleme uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="9d1a3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9d1a3-115">PARAMETERS</span></span>

### <span data-ttu-id="9d1a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d1a3-116">-DefaultProfile</span></span>
<span data-ttu-id="9d1a3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d1a3-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9d1a3-118">-Force</span></span>
<span data-ttu-id="9d1a3-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9d1a3-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="9d1a3-120">-Name</span></span>
<span data-ttu-id="9d1a3-121">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="9d1a3-122">Set-AzVMDiskEncryptionExtension cmdlet, Windows işletim sistemi ve Linux sanal makineler için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde bu adı AzureDiskEncryption olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="9d1a3-123">Bu parametreyi yalnızca **set-AzVMDiskEncryptionExtension** cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d1a3-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9d1a3-124">-NoWait</span></span>
<span data-ttu-id="9d1a3-125">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9d1a3-126">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9d1a3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d1a3-127">-ResourceGroupName</span></span>
<span data-ttu-id="9d1a3-128">Sanal makine için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="9d1a3-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="9d1a3-129">-VMName</span></span>
<span data-ttu-id="9d1a3-130">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="9d1a3-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="9d1a3-131">-Confirm</span></span>
<span data-ttu-id="9d1a3-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d1a3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d1a3-133">-WhatIf</span></span>
<span data-ttu-id="9d1a3-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d1a3-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d1a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d1a3-136">CommonParameters</span></span>
<span data-ttu-id="9d1a3-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d1a3-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9d1a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d1a3-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9d1a3-139">INPUTS</span></span>

### <span data-ttu-id="9d1a3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9d1a3-140">System.String</span></span>

## <span data-ttu-id="9d1a3-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9d1a3-141">OUTPUTS</span></span>

### <span data-ttu-id="9d1a3-142">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d1a3-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9d1a3-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9d1a3-143">NOTES</span></span>

## <span data-ttu-id="9d1a3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9d1a3-144">RELATED LINKS</span></span>

[<span data-ttu-id="9d1a3-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="9d1a3-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="9d1a3-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="9d1a3-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


