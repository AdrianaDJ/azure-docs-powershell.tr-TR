---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 064196C3-ABF3-4F3A-A4AB-EB0D27098C70
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMExtension.md
ms.openlocfilehash: babe273e97d2b1b9a1e09959ba252557e2a7e7d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104628"
---
# <span data-ttu-id="8ce9c-101">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="8ce9c-101">Set-AzVMExtension</span></span>

## <span data-ttu-id="8ce9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ce9c-102">SYNOPSIS</span></span>
<span data-ttu-id="8ce9c-103">Uzantı özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-103">Updates extension properties or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="8ce9c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ce9c-104">SYNTAX</span></span>

### <span data-ttu-id="8ce9c-105">Ayarlar (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8ce9c-105">Settings (Default)</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-Settings <Hashtable>]
 [-ProtectedSettings <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ce9c-106">Ayar dizesi</span><span class="sxs-lookup"><span data-stu-id="8ce9c-106">SettingString</span></span>
```
Set-AzVMExtension -Publisher <String> -ExtensionType <String> [-SettingString <String>]
 [-ProtectedSettingString <String>] [-AsJob] [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ce9c-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ce9c-107">DESCRIPTION</span></span>
<span data-ttu-id="8ce9c-108">**Set-Azvmexter** cmdlet 'ı mevcut sanal makine uzantılarının özelliklerini güncelleştirir veya sanal makineye bir uzantı ekler.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-108">The **Set-AzVMExtension** cmdlet updates properties for existing Virtual Machine Extensions or adds an extension to a virtual machine.</span></span>

## <span data-ttu-id="8ce9c-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ce9c-109">EXAMPLES</span></span>

### <span data-ttu-id="8ce9c-110">Örnek 1: karma tablolar kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="8ce9c-110">Example 1: Modify settings by using hash tables</span></span>
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "ContosoTest" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -Settings $Settings -ProtectedSettings $ProtectedSettings;
```

<span data-ttu-id="8ce9c-111">İlk iki komut, karma tablolar oluşturmak için standart Windows PowerShell söz dizimini kullanır ve sonra $Settings ve $ProtectedSettings değişkenlerinde bu karma tabloları depolar.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-111">The first two commands use standard Windows PowerShell syntax to create hash tables, and then stores those hash tables in the $Settings and $ProtectedSettings variables.</span></span>
<span data-ttu-id="8ce9c-112">Daha fazla bilgi için yazın `Get-Help about_Hash_Tables` .</span><span class="sxs-lookup"><span data-stu-id="8ce9c-112">For more information, type `Get-Help about_Hash_Tables`.</span></span>
<span data-ttu-id="8ce9c-113">İkinci komutta, daha önce oluşturulan ve değişkenlerde depolanan iki değer vardır.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-113">The second command includes two values previously created and stored in variables.</span></span>
<span data-ttu-id="8ce9c-114">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $Settings ve $ProtectedSettings içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-114">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $Settings and $ProtectedSettings.</span></span>
<span data-ttu-id="8ce9c-115">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-115">The command specifies other required information that includes the publisher and the extension type.</span></span>

### <span data-ttu-id="8ce9c-116">Örnek 2: dizeleri kullanarak ayarları değiştirme</span><span class="sxs-lookup"><span data-stu-id="8ce9c-116">Example 2: Modify settings by using strings</span></span>
```
PS C:\> $SettingsString = '{"fileUris":[],"commandToExecute":""}';
PS C:\> $ProtectedSettingsString = '{"storageAccountName":"' + $stoname + '","storageAccountKey":"' + $stokey + '"}';
PS C:\> Set-AzVMExtension -ResourceGroupName "ResourceGroup11" -Location "West US" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Publisher "Contoso.Compute" -Type "CustomScriptExtension" -TypeHandlerVersion "1.1" -SettingString $SettingsString -ProtectedSettingString $ProtectedSettingsString ;
```

<span data-ttu-id="8ce9c-117">İlk iki komut ayarlar içeren dizeler oluşturur ve bunları $SettingsString ve $ProtectedSettingsString değişkenlerinde depolar.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-117">The first two commands create strings that contain settings, and then stores them in the $SettingsString and $ProtectedSettingsString variables.</span></span>
<span data-ttu-id="8ce9c-118">Son komutu, VirtualMachine22 adındaki adındaki sanal makinenin, $SettingsString ve $ProtectedSettingsString içeriğine göre değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-118">The final command modifies an extension of the virtual machine named VirtualMachine22 in ResourceGroup11 according to the contents of $SettingsString and $ProtectedSettingsString.</span></span>
<span data-ttu-id="8ce9c-119">Komut, yayımcıyı ve uzantı türünü içeren diğer zorunlu bilgileri belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-119">The command specifies other required information that includes the publisher and the extension type.</span></span>

## <span data-ttu-id="8ce9c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ce9c-120">PARAMETERS</span></span>

### <span data-ttu-id="8ce9c-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="8ce9c-121">-AsJob</span></span>
<span data-ttu-id="8ce9c-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="8ce9c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ce9c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ce9c-123">-DefaultProfile</span></span>
<span data-ttu-id="8ce9c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ce9c-125">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="8ce9c-125">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="8ce9c-126">Bu cmdlet 'in, Azure Konuk aracısının uzantıları daha yeni bir alt sürüme otomatik olarak güncelleştirmesini engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-126">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extensions to a newer minor version.</span></span>
<span data-ttu-id="8ce9c-127">Varsayılan olarak, bu cmdlet Konuk aracısının uzantıları güncelleştirmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-127">By default, this cmdlet enables the guest agent to update the extensions.</span></span>

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

### <span data-ttu-id="8ce9c-128">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="8ce9c-128">-ExtensionType</span></span>
<span data-ttu-id="8ce9c-129">Uzantı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-129">Specifies the extension type.</span></span>

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

### <span data-ttu-id="8ce9c-130">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="8ce9c-130">-ForceRerun</span></span>
<span data-ttu-id="8ce9c-131">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-131">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="8ce9c-132">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-132">The value can be any string different from the current value.</span></span>
<span data-ttu-id="8ce9c-133">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-133">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="8ce9c-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="8ce9c-134">-Location</span></span>
<span data-ttu-id="8ce9c-135">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-135">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="8ce9c-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ce9c-136">-Name</span></span>
<span data-ttu-id="8ce9c-137">Bir uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-137">Specifies the name of an extension.</span></span>

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

### <span data-ttu-id="8ce9c-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8ce9c-138">-NoWait</span></span>
<span data-ttu-id="8ce9c-139">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-139">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8ce9c-140">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-140">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8ce9c-141">-ProtectedSettings</span><span class="sxs-lookup"><span data-stu-id="8ce9c-141">-ProtectedSettings</span></span>
<span data-ttu-id="8ce9c-142">Karma tablo olarak, uzantının özel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-142">Specifies private configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="8ce9c-143">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-143">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="8ce9c-144">-ProtectedSettingString</span><span class="sxs-lookup"><span data-stu-id="8ce9c-144">-ProtectedSettingString</span></span>
<span data-ttu-id="8ce9c-145">Uzantı için özel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-145">Specifies private configuration for the extension, as a string.</span></span>
<span data-ttu-id="8ce9c-146">Bu cmdlet özel yapılandırmayı şifreler.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-146">This cmdlet encrypts the private configuration.</span></span>

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

### <span data-ttu-id="8ce9c-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8ce9c-147">-Publisher</span></span>
<span data-ttu-id="8ce9c-148">Uzantı yayıncısı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-148">Specifies the name of the extension publisher.</span></span>
<span data-ttu-id="8ce9c-149">Publisher bir uzantıyı kaydettiğinde yayımcı bir ad sağlar.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-149">The publisher provides a name when the publisher registers an extension.</span></span>

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

### <span data-ttu-id="8ce9c-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ce9c-150">-ResourceGroupName</span></span>
<span data-ttu-id="8ce9c-151">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-151">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8ce9c-152">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="8ce9c-152">-Settings</span></span>
<span data-ttu-id="8ce9c-153">Karma tablo olarak uzantının genel yapılandırmasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-153">Specifies public configuration for the extension, as a hash table.</span></span>
<span data-ttu-id="8ce9c-154">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-154">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="8ce9c-155">-Settingdize</span><span class="sxs-lookup"><span data-stu-id="8ce9c-155">-SettingString</span></span>
<span data-ttu-id="8ce9c-156">Uzantı için genel yapılandırmayı bir dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-156">Specifies public configuration for the extension, as a string.</span></span>
<span data-ttu-id="8ce9c-157">Bu cmdlet ortak yapılandırmayı şifrelemez.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-157">This cmdlet does not encrypt public configuration.</span></span>

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

### <span data-ttu-id="8ce9c-158">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="8ce9c-158">-TypeHandlerVersion</span></span>
<span data-ttu-id="8ce9c-159">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-159">Specifies the version of the extension to use for this virtual machine.</span></span>

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

### <span data-ttu-id="8ce9c-160">-VMName</span><span class="sxs-lookup"><span data-stu-id="8ce9c-160">-VMName</span></span>
<span data-ttu-id="8ce9c-161">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-161">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8ce9c-162">Bu cmdlet, bu parametrenin belirttiği sanal makine için uzantıları değiştirir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-162">This cmdlet modifies extensions for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="8ce9c-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ce9c-163">-Confirm</span></span>
<span data-ttu-id="8ce9c-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ce9c-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ce9c-165">-WhatIf</span></span>
<span data-ttu-id="8ce9c-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ce9c-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ce9c-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ce9c-168">CommonParameters</span></span>
<span data-ttu-id="8ce9c-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ce9c-170">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8ce9c-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ce9c-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ce9c-171">INPUTS</span></span>

### <span data-ttu-id="8ce9c-172">System. String</span><span class="sxs-lookup"><span data-stu-id="8ce9c-172">System.String</span></span>

### <span data-ttu-id="8ce9c-173">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8ce9c-173">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8ce9c-174">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8ce9c-174">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8ce9c-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ce9c-175">OUTPUTS</span></span>

### <span data-ttu-id="8ce9c-176">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8ce9c-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8ce9c-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ce9c-177">NOTES</span></span>

## <span data-ttu-id="8ce9c-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ce9c-178">RELATED LINKS</span></span>

[<span data-ttu-id="8ce9c-179">Get-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="8ce9c-179">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="8ce9c-180">Remove-Azvmexgergeri</span><span class="sxs-lookup"><span data-stu-id="8ce9c-180">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)


