---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 6a14a8472ca33fe9dbb15aa2ddf58208764a5a6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937064"
---
# <span data-ttu-id="de5e8-101">Disable-AzVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="de5e8-101">Disable-AzVMDiskEncryption</span></span>

## <span data-ttu-id="de5e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="de5e8-103">IaaS sanal makinesindeki şifrelemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de5e8-103">Disables encryption on an IaaS virtual machine.</span></span>

## <span data-ttu-id="de5e8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de5e8-104">SYNTAX</span></span>

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de5e8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="de5e8-105">DESCRIPTION</span></span>
<span data-ttu-id="de5e8-106">**Disable-AzVMDiskEncryption** cmdlet 'i bir altyapıda hizmet (IaaS) sanal makinesi olarak şifrelemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de5e8-106">The **Disable-AzVMDiskEncryption** cmdlet disables encryption on an infrastructure as a service (IaaS) virtual machine.</span></span>
<span data-ttu-id="de5e8-107">Bu cmdlet yalnızca Windows sanal makinelerinde, Linux sanal makinelerde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="de5e8-107">This cmdlet is only supported on Windows virtual machines and not Linux virtual machines.</span></span>
<span data-ttu-id="de5e8-108">Bu cmdlet, şifrelemeyi devre dışı bırakmak için sanal makinede bir uzantı yükler.</span><span class="sxs-lookup"><span data-stu-id="de5e8-108">This cmdlet installs an extension on the virtual machine to disable encryption.</span></span>
<span data-ttu-id="de5e8-109">*Name* parametresi belirtilmezse, "Windows için AzureDiskEncryption" adındaki bir uzantı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="de5e8-109">If the *Name* parameter is not specified, an extension with the default name "AzureDiskEncryption for Windows VMs" is created.</span></span>
<span data-ttu-id="de5e8-110">Uyarı: Bu cmdlet sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="de5e8-110">Caution: This cmdlet reboots the virtual machine.</span></span>

## <span data-ttu-id="de5e8-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de5e8-111">EXAMPLES</span></span>

### <span data-ttu-id="de5e8-112">Örnek 1: Windows sanal makinesindeki tüm birimlerde şifrelemeyi devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="de5e8-112">Example 1: Disable encryption for all volumes on a Windows virtual machine</span></span>
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

<span data-ttu-id="de5e8-113">Bu komut, Group001 adındaki kaynak grubuna ait olan VM002 adındaki sanal makinede tümü için gereken birimleri şifrelemeyi devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de5e8-113">This command disables encryption for volumes of type all for the virtual machine named VM002 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="de5e8-114">*Volumetype* parametresi belirtilmediğinden cmdlet değeri tümü olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="de5e8-114">Since the *VolumeType* parameter is not specified, the cmdlet sets the value to All.</span></span>

### <span data-ttu-id="de5e8-115">Örnek 2: Windows sanal makinesindeki veri birimlerinin şifrelemesini devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="de5e8-115">Example 2: Disable encryption for data volumes on a Windows virtual machine</span></span>
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

<span data-ttu-id="de5e8-116">Bu komut, Group002 adındaki kaynak grubuna ait olan VM004 adındaki sanal makine için veri türleri şifrelemesini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="de5e8-116">This command disables encryption for volumes of type data for the virtual machine named VM004 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="de5e8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de5e8-117">PARAMETERS</span></span>

### <span data-ttu-id="de5e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de5e8-118">-DefaultProfile</span></span>
<span data-ttu-id="de5e8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de5e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de5e8-120">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="de5e8-120">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="de5e8-121">Bu cmdlet 'in, uzantının ara sürümünün otomatik yükseltmesini devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de5e8-121">Indicates that this cmdlet disables auto-upgrade of the minor version of the extension.</span></span>

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

### <span data-ttu-id="de5e8-122">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="de5e8-122">-ExtensionPublisherName</span></span>
<span data-ttu-id="de5e8-123">Dahili yayımcı adı.</span><span class="sxs-lookup"><span data-stu-id="de5e8-123">The extension publisher name.</span></span> <span data-ttu-id="de5e8-124">Bu parametreyi yalnızca "Microsoft. Azure. Security" varsayılan değerini geçersiz kılmak için belirtin.</span><span class="sxs-lookup"><span data-stu-id="de5e8-124">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="de5e8-125">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="de5e8-125">-ExtensionType</span></span>
<span data-ttu-id="de5e8-126">Uzantı türü.</span><span class="sxs-lookup"><span data-stu-id="de5e8-126">The extension type.</span></span> <span data-ttu-id="de5e8-127">Windows VM 'ler için "AzureDiskEncryption" varsayılan değerini (Linux VM 'Ler için "AzureDiskEncryptionForLinux" olarak geçersiz kılmak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="de5e8-127">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="de5e8-128">-Force</span><span class="sxs-lookup"><span data-stu-id="de5e8-128">-Force</span></span>
<span data-ttu-id="de5e8-129">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="de5e8-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de5e8-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="de5e8-130">-Name</span></span>
<span data-ttu-id="de5e8-131">Uzantıyı temsil eden Azure Resource Manager (ARM) kaynağının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5e8-131">Specifes the name of the Azure Resource Manager (ARM) resource that represents the extension.</span></span>
<span data-ttu-id="de5e8-132">Bu parametre belirtilmezse, bu cmdlet "Windows için AzureDiskEncryption" olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="de5e8-132">If this parameter is not specified, this cmdlet defaults to "AzureDiskEncryption for Windows VMs".</span></span>

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

### <span data-ttu-id="de5e8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de5e8-133">-ResourceGroupName</span></span>
<span data-ttu-id="de5e8-134">Sanal makinenin kaynak grubu adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5e8-134">Specifies the resource group name of the virtual machine.</span></span>

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

### <span data-ttu-id="de5e8-135">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="de5e8-135">-TypeHandlerVersion</span></span>
<span data-ttu-id="de5e8-136">Şifreleme uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5e8-136">Specifies the version of the encryption extension.</span></span>
<span data-ttu-id="de5e8-137">Bu parametre için bir değer belirtmezseniz, uzantının en son sürümü kullanılır.</span><span class="sxs-lookup"><span data-stu-id="de5e8-137">If you do not specify a value for this parameter, the latest version of the extension is used.</span></span>

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

### <span data-ttu-id="de5e8-138">-VMName</span><span class="sxs-lookup"><span data-stu-id="de5e8-138">-VMName</span></span>
<span data-ttu-id="de5e8-139">Bu cmdlet 'in şifrelemeyi devre dışı bırakacağını belirten sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5e8-139">Specifies the name of the virtual machine that this cmdlet disables encryption on.</span></span>

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

### <span data-ttu-id="de5e8-140">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="de5e8-140">-VolumeType</span></span>
<span data-ttu-id="de5e8-141">Şifreleme işlemini gerçekleştirecek sanal makine birimlerinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="de5e8-141">Specifies the type of virtual machine volumes to perform the encryption operation.</span></span>
<span data-ttu-id="de5e8-142">Windows sanal makineleri için geçerli değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="de5e8-142">For Windows virtual machines, valid values are:</span></span> 

- <span data-ttu-id="de5e8-143">Tüm</span><span class="sxs-lookup"><span data-stu-id="de5e8-143">All</span></span>
- <span data-ttu-id="de5e8-144">ÖNYÜKLEME</span><span class="sxs-lookup"><span data-stu-id="de5e8-144">OS</span></span>
- <span data-ttu-id="de5e8-145">Verisini.</span><span class="sxs-lookup"><span data-stu-id="de5e8-145">Data.</span></span>
<span data-ttu-id="de5e8-146">Bu parametre için bir değer belirtmezseniz, varsayılan değer tümü olur.</span><span class="sxs-lookup"><span data-stu-id="de5e8-146">If you do not specify a value for this parameter, the default value is All.</span></span>
<span data-ttu-id="de5e8-147">Şu anda Linux için şifrelemeyi devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="de5e8-147">Disable encryption is not currently supported for Linux.</span></span>

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

### <span data-ttu-id="de5e8-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="de5e8-148">-Confirm</span></span>
<span data-ttu-id="de5e8-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de5e8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de5e8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de5e8-150">-WhatIf</span></span>
<span data-ttu-id="de5e8-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de5e8-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="de5e8-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de5e8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de5e8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de5e8-153">CommonParameters</span></span>
<span data-ttu-id="de5e8-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de5e8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de5e8-155">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de5e8-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de5e8-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de5e8-156">INPUTS</span></span>

### <span data-ttu-id="de5e8-157">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="de5e8-157">None</span></span>
<span data-ttu-id="de5e8-158">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="de5e8-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de5e8-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de5e8-159">OUTPUTS</span></span>

### <span data-ttu-id="de5e8-160">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="de5e8-160">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="de5e8-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de5e8-161">NOTES</span></span>

## <span data-ttu-id="de5e8-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de5e8-162">RELATED LINKS</span></span>

[<span data-ttu-id="de5e8-163">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="de5e8-163">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="de5e8-164">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="de5e8-164">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="de5e8-165">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="de5e8-165">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


