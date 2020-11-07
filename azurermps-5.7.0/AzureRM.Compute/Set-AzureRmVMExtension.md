---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: 1f758f77fc7162f8110f0e2d5887eadb55d7f7c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762030"
---
# <span data-ttu-id="f09da-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="f09da-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="f09da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f09da-102">SYNOPSIS</span></span>
<span data-ttu-id="f09da-103">Uzantı özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="f09da-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f09da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f09da-104">SYNTAX</span></span>

### <span data-ttu-id="f09da-105">Ayarlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f09da-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f09da-106">Ayar dizesi</span><span class="sxs-lookup"><span data-stu-id="f09da-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f09da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f09da-107">DESCRIPTION</span></span>
<span data-ttu-id="f09da-108">**Set-Azurermvmexter** cmdlet 'ı mevcut sanal makine uzantılarının özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="f09da-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="f09da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f09da-109">EXAMPLES</span></span>

### <span data-ttu-id="f09da-110">Örnek 1: karma tablolar kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="f09da-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="f09da-111">İlk iki komut, karma tablolar oluşturmak için standart Windows PowerShell söz dizimini kullanır ve sonra $Settings ve $ProtectedSettings değişkenlerinde bu karma tabloları depolar.</span><span class="sxs-lookup"><span data-stu-id="f09da-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="f09da-112">Daha fazla bilgi için yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="f09da-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="f09da-113">İkinci komutta, daha önce oluşturulan ve değişkenlerde depolanan iki değer vardır.</span><span class="sxs-lookup"><span data-stu-id="f09da-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="f09da-114">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $Settings ve $ProtectedSettings içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f09da-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="f09da-115">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="f09da-116">Örnek 2: dizeleri kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="f09da-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="f09da-117">İlk iki komut ayarlar içeren dizeler oluşturur ve bunları $SettingsString ve $ProtectedSettingsString değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="f09da-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="f09da-118">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $SettingsString ve $ProtectedSettingsString içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f09da-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="f09da-119">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="f09da-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f09da-120">PARAMETERS</span></span>

### <span data-ttu-id="f09da-121">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f09da-121">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f09da-122">Bu cmdlet 'in, Azure Konuk aracısının uzantıları daha yeni bir alt sürüme otomatik olarak güncelleştirmesini engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f09da-122">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="f09da-123">Varsayılan olarak, bu cmdlet Konuk aracısının uzantıları güncelleştirmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="f09da-123">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="f09da-124">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f09da-124">-ExtensionType</span></span>
<span data-ttu-id="f09da-125">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-125">Specifies the extension type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09da-126">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f09da-126">-ForceRerun</span></span>
<span data-ttu-id="f09da-127">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f09da-127">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="f09da-128">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f09da-128">The value can be any string different from the current value.</span></span>

<span data-ttu-id="f09da-129">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f09da-129">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f09da-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="f09da-130">-Location</span></span>
<span data-ttu-id="f09da-131">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-131">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f09da-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="f09da-132">-Name</span></span>
<span data-ttu-id="f09da-133">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-133">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="f09da-134">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="f09da-134">-ProtectedSettings</span></span>
<span data-ttu-id="f09da-135">Karma tablo olarak, uzantının özel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-135">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f09da-136">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="f09da-136">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09da-137">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="f09da-137">-ProtectedSettingString</span></span>
<span data-ttu-id="f09da-138">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-138">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="f09da-139">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="f09da-139">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09da-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f09da-140">-Publisher</span></span>
<span data-ttu-id="f09da-141">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-141">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="f09da-142">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="f09da-142">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09da-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f09da-143">-ResourceGroupName</span></span>
<span data-ttu-id="f09da-144">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-144">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f09da-145">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="f09da-145">-Settings</span></span>
<span data-ttu-id="f09da-146">Karma tablo olarak uzantının genel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-146">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="f09da-147">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="f09da-147">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09da-148">-Settingdize</span><span class="sxs-lookup"><span data-stu-id="f09da-148">-SettingString</span></span>
<span data-ttu-id="f09da-149">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-149">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="f09da-150">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="f09da-150">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f09da-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f09da-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="f09da-152">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-152">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="f09da-153">-VMName</span><span class="sxs-lookup"><span data-stu-id="f09da-153">-VMName</span></span>
<span data-ttu-id="f09da-154">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f09da-154">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="f09da-155">Bu cmdlet, bu parametrenin belirttiği sanal makine için uzantıları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="f09da-155">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="f09da-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="f09da-156">-Confirm</span></span>
<span data-ttu-id="f09da-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f09da-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09da-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09da-158">-WhatIf</span></span>
<span data-ttu-id="f09da-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f09da-159">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f09da-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f09da-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09da-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09da-161">CommonParameters</span></span>
<span data-ttu-id="f09da-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f09da-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09da-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09da-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09da-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f09da-164">INPUTS</span></span>

### <span data-ttu-id="f09da-165">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f09da-165">None</span></span>
<span data-ttu-id="f09da-166">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="f09da-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f09da-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f09da-167">OUTPUTS</span></span>

## <span data-ttu-id="f09da-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f09da-168">NOTES</span></span>

## <span data-ttu-id="f09da-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f09da-169">RELATED LINKS</span></span>

[<span data-ttu-id="f09da-170">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="f09da-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="f09da-171">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="f09da-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


