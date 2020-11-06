---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Disable-AzureRmVMDiskEncryption.md
ms.openlocfilehash: 087ae12961d6bd9faf844221772b92c79362d13d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590522"
---
# <span data-ttu-id="4ab33-101">Disable-AzureRmVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4ab33-101">Disable-AzureRmVMDiskEncryption</span></span>

## <span data-ttu-id="4ab33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ab33-102">SYNOPSIS</span></span>
<span data-ttu-id="4ab33-103">IaaS sanal makinesindeki şifrelemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4ab33-103">Disables encryption on an IaaS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ab33-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ab33-104">SYNTAX</span></span>

```
Disable-AzureRmVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ab33-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ab33-105">DESCRIPTION</span></span>
<span data-ttu-id="4ab33-106">**Disable-AzureRmVMDiskEncryption** cmdlet 'i bir altyapıda hizmet (IaaS) sanal makinesi olarak şifrelemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4ab33-106">The **Disable-AzureRmVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="4ab33-107">Bu cmdlet yalnızca Windows sanal makinelerinde, Linux sanal makinelerde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="4ab33-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="4ab33-108">Bu cmdlet, şifrelemeyi devre dışı bırakmak için sanal makinede bir uzantı yükler.</span><span class="sxs-lookup"><span data-stu-id="4ab33-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="4ab33-109">*Name* parametresi belirtilmezse, "Windows için AzureDiskEncryption" adındaki bir uzantı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="4ab33-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="4ab33-110">Uyarı: Bu cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="4ab33-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="4ab33-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ab33-111">EXAMPLES</span></span>

### <span data-ttu-id="4ab33-112">Örnek 1: Windows sanal makinesindeki tüm birimlerde şifrelemeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4ab33-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="4ab33-113">Bu komut, Group001 adındaki kaynak grubuna ait olan VM002 adındaki sanal makinede tümü için gereken birimleri şifrelemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4ab33-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="4ab33-114">*Volumetype* parametresi belirtilmediğinden cmdlet değeri tümü olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ab33-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="4ab33-115">Örnek 2: Windows sanal makinesindeki veri birimlerinin şifrelemesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="4ab33-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzureRMVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="4ab33-116">Bu komut, Group002 adındaki kaynak grubuna ait olan VM004 adındaki sanal makine için veri türleri şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="4ab33-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="4ab33-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ab33-117">PARAMETERS</span></span>

### <span data-ttu-id="4ab33-118">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="4ab33-118">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="4ab33-119">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ab33-119">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab33-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4ab33-120">-Force</span></span>
<span data-ttu-id="4ab33-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4ab33-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4ab33-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="4ab33-122">-Name</span></span>
<span data-ttu-id="4ab33-123">Uzantıyı temsil eden Azure Resource Manager (ARM) kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab33-123">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="4ab33-124">Bu parametre belirtilmezse, bu cmdlet "Windows için AzureDiskEncryption" olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="4ab33-124">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab33-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ab33-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ab33-126">Sanal makinenin kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab33-126">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="4ab33-127">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="4ab33-127">-TypeHandlerVersion</span></span>
<span data-ttu-id="4ab33-128">Şifreleme uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab33-128">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="4ab33-129">Bu parametre için bir değer belirtmezseniz, uzantının en son sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="4ab33-129">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab33-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="4ab33-130">-VMName</span></span>
<span data-ttu-id="4ab33-131">Bu cmdlet 'in şifrelemeyi devre dışı bırakacağını belirten sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab33-131">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="4ab33-132">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="4ab33-132">-VolumeType</span></span>
<span data-ttu-id="4ab33-133">Şifreleme işlemini gerçekleştirecek sanal makine birimlerinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ab33-133">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="4ab33-134">Windows sanal makineleri için geçerli değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4ab33-134">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="4ab33-135">Tüm</span><span class="sxs-lookup"><span data-stu-id="4ab33-135">All</span></span>
- <span data-ttu-id="4ab33-136">ÖNYÜKLEME</span><span class="sxs-lookup"><span data-stu-id="4ab33-136">OS</span></span>
- <span data-ttu-id="4ab33-137">Verisini.</span><span class="sxs-lookup"><span data-stu-id="4ab33-137">Data.</span></span>
<span data-ttu-id="4ab33-138">Bu parametre için bir değer belirtmezseniz, varsayılan değer tümü olur.</span><span class="sxs-lookup"><span data-stu-id="4ab33-138">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="4ab33-139">Şu anda Linux için şifrelemeyi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="4ab33-139">Disable encryption is not currently supported for Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ab33-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ab33-140">-Confirm</span></span>
<span data-ttu-id="4ab33-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ab33-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ab33-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ab33-142">-WhatIf</span></span>
<span data-ttu-id="4ab33-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ab33-143">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4ab33-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ab33-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ab33-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ab33-145">CommonParameters</span></span>
<span data-ttu-id="4ab33-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ab33-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ab33-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ab33-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ab33-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ab33-148">INPUTS</span></span>

### <span data-ttu-id="4ab33-149">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4ab33-149">None</span></span>
<span data-ttu-id="4ab33-150">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4ab33-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ab33-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ab33-151">OUTPUTS</span></span>

### <span data-ttu-id="4ab33-152">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4ab33-152">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4ab33-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ab33-153">NOTES</span></span>

## <span data-ttu-id="4ab33-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ab33-154">RELATED LINKS</span></span>

[<span data-ttu-id="4ab33-155">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="4ab33-155">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="4ab33-156">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4ab33-156">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="4ab33-157">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="4ab33-157">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


