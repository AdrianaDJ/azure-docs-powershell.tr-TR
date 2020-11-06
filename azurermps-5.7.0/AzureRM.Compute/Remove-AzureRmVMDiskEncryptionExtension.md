---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiskEncryptionExtension.md
ms.openlocfilehash: 9c9f7dca5bd698a0eda76637618fe946b723a576
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589850"
---
# <span data-ttu-id="19cff-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="19cff-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="19cff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19cff-102">SYNOPSIS</span></span>
<span data-ttu-id="19cff-103">Sanal makineden disk şifrelemesi uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19cff-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19cff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19cff-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19cff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19cff-105">DESCRIPTION</span></span>
<span data-ttu-id="19cff-106">**Remove-AzureRmVMDiskEncryptionExtension** cmdlet 'i sanal makineden disk şifrelemesi uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19cff-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="19cff-107">Uzantı adı belirtilmemişse, bu cmdlet, Windows işletim sistemini veya Linux tabanlı sanal makineler için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde varsayılan ad AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="19cff-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="19cff-108">Bu cmdlet sanal makinede şifrelemeyi devre dışı bırakmaz.</span><span class="sxs-lookup"><span data-stu-id="19cff-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="19cff-109">Uzantıyı ve ilişkili uzantı yapılandırmasını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19cff-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="19cff-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19cff-110">EXAMPLES</span></span>

### <span data-ttu-id="19cff-111">Örnek 1: sanal makineden disk şifrelemesi uzantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="19cff-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="19cff-112">Bu komut, Windows işletim sistemi veya AzureDiskEncryptionForLinux adlı Linux tabanlı sanal makinede çalışan bir sanal makine için varsayılan ad AzureDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="19cff-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="19cff-113">Örnek 2: sanal makineden belirli bir disk şifrelemesi uzantısını kaldırın.</span><span class="sxs-lookup"><span data-stu-id="19cff-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="19cff-114">Bu komut Mydiskencryptionextenmytestvm adlı sanal makineden MyDiskEncryptionExtension adlı şifreleme uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19cff-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="19cff-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19cff-115">PARAMETERS</span></span>

### <span data-ttu-id="19cff-116">-Force</span><span class="sxs-lookup"><span data-stu-id="19cff-116">-Force</span></span>
<span data-ttu-id="19cff-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="19cff-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cff-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="19cff-118">-Name</span></span>
<span data-ttu-id="19cff-119">Uzantıyı temsil eden Azure Resource Manager kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19cff-119">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="19cff-120">Set-AzureRmVMDiskEncryptionExtension cmdlet, Windows işletim sistemi ve Linux sanal makineler için AzureDiskEncryptionForLinux çalıştıran sanal makinelerde bu adı AzureDiskEncryption olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="19cff-120">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="19cff-121">Bu parametreyi yalnızca **set-AzureRmVMDiskEncryptionExtension** cmdlet 'inde varsayılan adı değiştirdiyseniz veya Kaynak Yöneticisi şablonunda farklı bir kaynak adı kullandıysanız belirtin.</span><span class="sxs-lookup"><span data-stu-id="19cff-121">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19cff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19cff-122">-ResourceGroupName</span></span>
<span data-ttu-id="19cff-123">Sanal makine için kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19cff-123">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="19cff-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="19cff-124">-VMName</span></span>
<span data-ttu-id="19cff-125">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="19cff-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="19cff-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="19cff-126">-Confirm</span></span>
<span data-ttu-id="19cff-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19cff-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19cff-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19cff-128">-WhatIf</span></span>
<span data-ttu-id="19cff-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19cff-129">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="19cff-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19cff-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19cff-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cff-131">CommonParameters</span></span>
<span data-ttu-id="19cff-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19cff-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cff-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cff-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cff-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19cff-134">INPUTS</span></span>

### <span data-ttu-id="19cff-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="19cff-135">None</span></span>
<span data-ttu-id="19cff-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="19cff-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19cff-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19cff-137">OUTPUTS</span></span>

## <span data-ttu-id="19cff-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19cff-138">NOTES</span></span>

## <span data-ttu-id="19cff-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19cff-139">RELATED LINKS</span></span>

[<span data-ttu-id="19cff-140">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="19cff-140">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="19cff-141">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="19cff-141">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


