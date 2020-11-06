---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: 6c24c01ebff1d0a74835b968640caea6b5d2b308
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586779"
---
# <span data-ttu-id="acb48-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="acb48-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="acb48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acb48-102">SYNOPSIS</span></span>
<span data-ttu-id="acb48-103">Sanal makineye VMAccess uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="acb48-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb48-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acb48-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acb48-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="acb48-105">DESCRIPTION</span></span>
<span data-ttu-id="acb48-106">**Set-Azurermvmaccessextenma** cmdlet 'i sanal makine erişimi (VMAccess) sanal makine VMAccess uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="acb48-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="acb48-107">VMAccess uzantısı geçici bir parola ayarlamak için kullanılabilir ve bu, makinede oturum açıldıktan sonra hemen değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="acb48-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="acb48-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acb48-108">EXAMPLES</span></span>

### <span data-ttu-id="acb48-109">Örnek 1: VMAccess uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="acb48-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="acb48-110">Bu komut, ResrouceGroup11 'da VirtualMachine07 adındaki sanal makine için bir VMAccess uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="acb48-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="acb48-111">Komut, VMAccess için ad ve tür işleyicisi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="acb48-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acb48-112">PARAMETERS</span></span>

### <span data-ttu-id="acb48-113">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="acb48-113">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="acb48-114">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="acb48-114">-ForceRerun</span></span>
<span data-ttu-id="acb48-115">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acb48-115">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="acb48-116">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="acb48-116">The value can be any string different from the current value.</span></span>

<span data-ttu-id="acb48-117">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="acb48-117">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="acb48-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="acb48-118">-Location</span></span>
<span data-ttu-id="acb48-119">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-119">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="acb48-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="acb48-120">-Name</span></span>
<span data-ttu-id="acb48-121">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-121">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="acb48-122">-Parola</span><span class="sxs-lookup"><span data-stu-id="acb48-122">-Password</span></span>
<span data-ttu-id="acb48-123">Sanal makinenin yeni parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-123">Specifies the new password of the virtual machine.</span></span>

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

### <span data-ttu-id="acb48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acb48-124">-ResourceGroupName</span></span>
<span data-ttu-id="acb48-125">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="acb48-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="acb48-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="acb48-127">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-127">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="acb48-128">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzureRmVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="acb48-128">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="acb48-129">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="acb48-129">-UserName</span></span>
<span data-ttu-id="acb48-130">Sanal makine için yeni kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-130">Specifies the new user name for the virtual machine.</span></span>

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

### <span data-ttu-id="acb48-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="acb48-131">-VMName</span></span>
<span data-ttu-id="acb48-132">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acb48-132">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="acb48-133">Bu cmdlet, bu parametrenin belirttiği sanal makine için VMAccess öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="acb48-133">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="acb48-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="acb48-134">-Confirm</span></span>
<span data-ttu-id="acb48-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="acb48-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acb48-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acb48-136">-WhatIf</span></span>
<span data-ttu-id="acb48-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acb48-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="acb48-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="acb48-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acb48-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb48-139">CommonParameters</span></span>
<span data-ttu-id="acb48-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acb48-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb48-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb48-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb48-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acb48-142">INPUTS</span></span>

### <span data-ttu-id="acb48-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="acb48-143">None</span></span>
<span data-ttu-id="acb48-144">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="acb48-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acb48-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acb48-145">OUTPUTS</span></span>

## <span data-ttu-id="acb48-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acb48-146">NOTES</span></span>

## <span data-ttu-id="acb48-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acb48-147">RELATED LINKS</span></span>

[<span data-ttu-id="acb48-148">Get-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="acb48-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="acb48-149">Remove-Azurermvmaccessextenma</span><span class="sxs-lookup"><span data-stu-id="acb48-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="acb48-150">Set-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="acb48-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="acb48-151">Get-Azurermvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="acb48-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


