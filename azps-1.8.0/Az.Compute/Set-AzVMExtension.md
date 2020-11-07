---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: c3637ade50258370c37e559ba5e4befbb677d0b6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917228"
---
# <span data-ttu-id="1ab29-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1ab29-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="1ab29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ab29-102">SYNOPSIS</span></span>
<span data-ttu-id="1ab29-103">Uzantı özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="1ab29-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="1ab29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ab29-104">SYNTAX</span></span>

### <span data-ttu-id="1ab29-105">Ayarlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ab29-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ab29-106">Ayar dizesi</span><span class="sxs-lookup"><span data-stu-id="1ab29-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ab29-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ab29-107">DESCRIPTION</span></span>
<span data-ttu-id="1ab29-108">**Set-Azvmexter** cmdlet 'ı mevcut sanal makine uzantılarının özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="1ab29-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="1ab29-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ab29-109">EXAMPLES</span></span>

### <span data-ttu-id="1ab29-110">Örnek 1: karma tablolar kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="1ab29-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="1ab29-111">İlk iki komut, karma tablolar oluşturmak için standart Windows PowerShell söz dizimini kullanır ve sonra $Settings ve $ProtectedSettings değişkenlerinde bu karma tabloları depolar.</span><span class="sxs-lookup"><span data-stu-id="1ab29-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="1ab29-112">Daha fazla bilgi için yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="1ab29-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="1ab29-113">İkinci komutta, daha önce oluşturulan ve değişkenlerde depolanan iki değer vardır.</span><span class="sxs-lookup"><span data-stu-id="1ab29-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="1ab29-114">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $Settings ve $ProtectedSettings içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="1ab29-115">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="1ab29-116">Örnek 2: dizeleri kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="1ab29-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="1ab29-117">İlk iki komut ayarlar içeren dizeler oluşturur ve bunları $SettingsString ve $ProtectedSettingsString değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="1ab29-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="1ab29-118">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $SettingsString ve $ProtectedSettingsString içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="1ab29-119">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="1ab29-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ab29-120">PARAMETERS</span></span>

### <span data-ttu-id="1ab29-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="1ab29-121">-AsJob</span></span>
<span data-ttu-id="1ab29-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="1ab29-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ab29-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ab29-123">-DefaultProfile</span></span>
<span data-ttu-id="1ab29-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ab29-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ab29-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1ab29-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1ab29-126">Bu cmdlet 'in, Azure Konuk aracısının uzantıları daha yeni bir alt sürüme otomatik olarak güncelleştirmesini engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="1ab29-127">Varsayılan olarak, bu cmdlet Konuk aracısının uzantıları güncelleştirmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="1ab29-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="1ab29-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="1ab29-128">-ExtensionType</span></span>
<span data-ttu-id="1ab29-129">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="1ab29-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1ab29-130">-ForceRerun</span></span>
<span data-ttu-id="1ab29-131">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="1ab29-132">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1ab29-133">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="1ab29-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="1ab29-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="1ab29-134">-Location</span></span>
<span data-ttu-id="1ab29-135">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="1ab29-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ab29-136">-Name</span></span>
<span data-ttu-id="1ab29-137">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="1ab29-138">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="1ab29-138">-ProtectedSettings</span></span>
<span data-ttu-id="1ab29-139">Karma tablo olarak, uzantının özel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-139">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="1ab29-140">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="1ab29-140">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="1ab29-141">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="1ab29-141">-ProtectedSettingString</span></span>
<span data-ttu-id="1ab29-142">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-142">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="1ab29-143">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="1ab29-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="1ab29-144">-Publisher</span><span class="sxs-lookup"><span data-stu-id="1ab29-144">-Publisher</span></span>
<span data-ttu-id="1ab29-145">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-145">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="1ab29-146">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="1ab29-146">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="1ab29-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ab29-147">-ResourceGroupName</span></span>
<span data-ttu-id="1ab29-148">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-148">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1ab29-149">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="1ab29-149">-Settings</span></span>
<span data-ttu-id="1ab29-150">Karma tablo olarak uzantının genel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-150">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="1ab29-151">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="1ab29-151">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="1ab29-152">-Settingdize</span><span class="sxs-lookup"><span data-stu-id="1ab29-152">-SettingString</span></span>
<span data-ttu-id="1ab29-153">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-153">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="1ab29-154">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="1ab29-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="1ab29-155">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1ab29-155">-TypeHandlerVersion</span></span>
<span data-ttu-id="1ab29-156">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-156">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="1ab29-157">-VMName</span><span class="sxs-lookup"><span data-stu-id="1ab29-157">-VMName</span></span>
<span data-ttu-id="1ab29-158">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-158">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1ab29-159">Bu cmdlet, bu parametrenin belirttiği sanal makine için uzantıları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-159">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ab29-160">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ab29-160">-Confirm</span></span>
<span data-ttu-id="1ab29-161">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ab29-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ab29-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ab29-162">-WhatIf</span></span>
<span data-ttu-id="1ab29-163">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ab29-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ab29-164">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ab29-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ab29-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ab29-165">CommonParameters</span></span>
<span data-ttu-id="1ab29-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ab29-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ab29-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ab29-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ab29-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ab29-168">INPUTS</span></span>

### <span data-ttu-id="1ab29-169">System. String</span><span class="sxs-lookup"><span data-stu-id="1ab29-169">System.String</span></span>

### <span data-ttu-id="1ab29-170">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1ab29-170">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1ab29-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1ab29-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1ab29-172">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ab29-172">OUTPUTS</span></span>

### <span data-ttu-id="1ab29-173">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1ab29-173">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1ab29-174">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ab29-174">NOTES</span></span>

## <span data-ttu-id="1ab29-175">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ab29-175">RELATED LINKS</span></span>

[<span data-ttu-id="1ab29-176">Get-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="1ab29-176">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="1ab29-177">Remove-Azvmexgergeri</span><span class="sxs-lookup"><span data-stu-id="1ab29-177">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


