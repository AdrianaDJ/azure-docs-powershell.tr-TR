---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMExtension.md
ms.openlocfilehash: da46aa0e6518c9a9eb9ebea58962f3da593ad264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590755"
---
# <span data-ttu-id="170e5-101">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="170e5-101">Set-AzureRmVMExtension</span></span>

## <span data-ttu-id="170e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="170e5-102">SYNOPSIS</span></span>
<span data-ttu-id="170e5-103">Uzantı özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="170e5-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="170e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="170e5-104">SYNTAX</span></span>

### <span data-ttu-id="170e5-105">Ayarlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="170e5-105">Settings (Default)</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170e5-106">Ayar dizesi</span><span class="sxs-lookup"><span data-stu-id="170e5-106">SettingString</span></span>
```
Set-AzureRmVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170e5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="170e5-107">DESCRIPTION</span></span>
<span data-ttu-id="170e5-108">**Set-Azurermvmexter** cmdlet 'ı mevcut sanal makine uzantılarının özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="170e5-108">The **Set-AzureRmVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="170e5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="170e5-109">EXAMPLES</span></span>

### <span data-ttu-id="170e5-110">Örnek 1: karma tablolar kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="170e5-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="170e5-111">İlk iki komut, karma tablolar oluşturmak için standart Windows PowerShell söz dizimini kullanır ve sonra $Settings ve $ProtectedSettings değişkenlerinde bu karma tabloları depolar.</span><span class="sxs-lookup"><span data-stu-id="170e5-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="170e5-112">Daha fazla bilgi için yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="170e5-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="170e5-113">İkinci komutta, daha önce oluşturulan ve değişkenlerde depolanan iki değer vardır.</span><span class="sxs-lookup"><span data-stu-id="170e5-113">The second command includes two values previously created and stored in variables.</span></span>

<span data-ttu-id="170e5-114">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $Settings ve $ProtectedSettings içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="170e5-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="170e5-115">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="170e5-116">Örnek 2: dizeleri kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="170e5-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="170e5-117">İlk iki komut ayarlar içeren dizeler oluşturur ve bunları $SettingsString ve $ProtectedSettingsString değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="170e5-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>

<span data-ttu-id="170e5-118">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $SettingsString ve $ProtectedSettingsString içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="170e5-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="170e5-119">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="170e5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="170e5-120">PARAMETERS</span></span>

### <span data-ttu-id="170e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170e5-121">-DefaultProfile</span></span>
<span data-ttu-id="170e5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="170e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-123">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="170e5-123">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="170e5-124">Bu cmdlet 'in, Azure Konuk aracısının uzantıları daha yeni bir alt sürüme otomatik olarak güncelleştirmesini engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="170e5-124">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="170e5-125">Varsayılan olarak, bu cmdlet Konuk aracısının uzantıları güncelleştirmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="170e5-125">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="170e5-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="170e5-126">-ExtensionType</span></span>
<span data-ttu-id="170e5-127">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-127">Specifies the extension type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Type

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="170e5-128">-ForceRerun</span></span>
<span data-ttu-id="170e5-129">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="170e5-129">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="170e5-130">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="170e5-130">The value can be any string different from the current value.</span></span>

<span data-ttu-id="170e5-131">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="170e5-131">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="170e5-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="170e5-132">-Location</span></span>
<span data-ttu-id="170e5-133">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-133">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="170e5-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="170e5-134">-Name</span></span>
<span data-ttu-id="170e5-135">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-135">Specifies the name of an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-136">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="170e5-136">-ProtectedSettings</span></span>
<span data-ttu-id="170e5-137">Karma tablo olarak, uzantının özel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-137">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="170e5-138">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="170e5-138">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-139">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="170e5-139">-ProtectedSettingString</span></span>
<span data-ttu-id="170e5-140">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-140">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="170e5-141">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="170e5-141">This cmdlet encrypts the private configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-142">-Publisher</span><span class="sxs-lookup"><span data-stu-id="170e5-142">-Publisher</span></span>
<span data-ttu-id="170e5-143">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-143">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="170e5-144">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="170e5-144">The publisher provides a name when the publisher registers an extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170e5-145">-ResourceGroupName</span></span>
<span data-ttu-id="170e5-146">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-146">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="170e5-147">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="170e5-147">-Settings</span></span>
<span data-ttu-id="170e5-148">Karma tablo olarak uzantının genel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-148">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="170e5-149">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="170e5-149">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Settings
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-150">-Settingdize</span><span class="sxs-lookup"><span data-stu-id="170e5-150">-SettingString</span></span>
<span data-ttu-id="170e5-151">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-151">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="170e5-152">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="170e5-152">This cmdlet does not encrypt public configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SettingString
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="170e5-153">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="170e5-153">-TypeHandlerVersion</span></span>
<span data-ttu-id="170e5-154">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-154">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="170e5-155">-VMName</span><span class="sxs-lookup"><span data-stu-id="170e5-155">-VMName</span></span>
<span data-ttu-id="170e5-156">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="170e5-156">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="170e5-157">Bu cmdlet, bu parametrenin belirttiği sanal makine için uzantıları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="170e5-157">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="170e5-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="170e5-158">-Confirm</span></span>
<span data-ttu-id="170e5-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="170e5-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170e5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170e5-160">-WhatIf</span></span>
<span data-ttu-id="170e5-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="170e5-161">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="170e5-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="170e5-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170e5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170e5-163">CommonParameters</span></span>
<span data-ttu-id="170e5-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="170e5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170e5-165">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170e5-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170e5-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="170e5-166">INPUTS</span></span>

## <span data-ttu-id="170e5-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="170e5-167">OUTPUTS</span></span>

## <span data-ttu-id="170e5-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="170e5-168">NOTES</span></span>

## <span data-ttu-id="170e5-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="170e5-169">RELATED LINKS</span></span>

[<span data-ttu-id="170e5-170">Get-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="170e5-170">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="170e5-171">Remove-Azurermvmexgeri</span><span class="sxs-lookup"><span data-stu-id="170e5-171">Remove-AzureRmVMExtension</span></span>](./Remove-AzureRmVMExtension.md)


