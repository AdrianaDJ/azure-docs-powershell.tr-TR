---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278732"
---
# <span data-ttu-id="62c57-101">Set-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="62c57-101">Set-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="62c57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62c57-102">SYNOPSIS</span></span>
<span data-ttu-id="62c57-103">Uzantıyı oluşturma veya güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="62c57-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="62c57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="62c57-104">SYNTAX</span></span>

### <span data-ttu-id="62c57-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="62c57-105">UpdateExpanded (Default)</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="62c57-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="62c57-106">Update</span></span>
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62c57-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="62c57-107">DESCRIPTION</span></span>
<span data-ttu-id="62c57-108">Uzantıyı oluşturma veya güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="62c57-108">The operation to create or update the extension.</span></span>

## <span data-ttu-id="62c57-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="62c57-109">EXAMPLES</span></span>

### <span data-ttu-id="62c57-110">Örnek 1: makinede uzantı ayarlama</span><span class="sxs-lookup"><span data-stu-id="62c57-110">Example 1: Set an extension on a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="62c57-111">Bir makinede uzantı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62c57-111">Sets an extension on a machine.</span></span>

### <span data-ttu-id="62c57-112">Örnek 2: ardışık düzen aracılığıyla uzantı parametreleriyle bir uzantı ayarlama</span><span class="sxs-lookup"><span data-stu-id="62c57-112">Example 2: Set an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="62c57-113">Bu, ardışık düzen aracılığıyla geçirilen nesne tarafından sağlanan uzantı parametreleriyle uzantıyı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62c57-113">This sets an extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="62c57-114">Bu, bir makinenin parametrelerini almak ve başka bir makineye uygulamak istiyorlar.</span><span class="sxs-lookup"><span data-stu-id="62c57-114">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

## <span data-ttu-id="62c57-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="62c57-115">PARAMETERS</span></span>

### <span data-ttu-id="62c57-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="62c57-116">-AsJob</span></span>
<span data-ttu-id="62c57-117">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="62c57-117">Run the command as a job</span></span>

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

### <span data-ttu-id="62c57-118">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="62c57-118">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="62c57-119">Dağıtım zamanında uzantının kullanılabilir olması durumunda, uzantının daha yeni bir alt sürüm kullanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="62c57-119">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="62c57-120">Ancak dağıtıldıktan sonra, bu özellik doğru olarak dağıtılmadıkça, uzantı ikincil sürümleri yükseltmez.</span><span class="sxs-lookup"><span data-stu-id="62c57-120">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c57-121">-DefaultProfile</span></span>
<span data-ttu-id="62c57-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="62c57-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-123">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="62c57-123">-ExtensionParameter</span></span>
<span data-ttu-id="62c57-124">Bir makine uzantısını açıklar.</span><span class="sxs-lookup"><span data-stu-id="62c57-124">Describes a Machine Extension.</span></span>
<span data-ttu-id="62c57-125">Oluşturmak için, EXTENSIONPARAMETER özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="62c57-125">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-126">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="62c57-126">-ExtensionType</span></span>
<span data-ttu-id="62c57-127">Uzantının türünü belirtir; Örneğin, "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="62c57-127">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-128">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="62c57-128">-ForceRerun</span></span>
<span data-ttu-id="62c57-129">Uzantı yapılandırması değişmese de, uzantı işleyicisinin güncelleştirmeye zorlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="62c57-129">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-130">-Konum</span><span class="sxs-lookup"><span data-stu-id="62c57-130">-Location</span></span>
<span data-ttu-id="62c57-131">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="62c57-131">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-132">-MachineName</span><span class="sxs-lookup"><span data-stu-id="62c57-132">-MachineName</span></span>
<span data-ttu-id="62c57-133">Uzantının oluşturulduğu veya güncelleştirileceği makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="62c57-133">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-134">-Ad</span><span class="sxs-lookup"><span data-stu-id="62c57-134">-Name</span></span>
<span data-ttu-id="62c57-135">Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="62c57-135">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-136">-NoWait</span><span class="sxs-lookup"><span data-stu-id="62c57-136">-NoWait</span></span>
<span data-ttu-id="62c57-137">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="62c57-137">Run the command asynchronously</span></span>

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

### <span data-ttu-id="62c57-138">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="62c57-138">-ProtectedSetting</span></span>
<span data-ttu-id="62c57-139">Uzantı, protectedSettings veya Protectedsettingsfromkeykasası içerebilir veya hiç korumalı ayar içermez.</span><span class="sxs-lookup"><span data-stu-id="62c57-139">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-140">-Publisher</span><span class="sxs-lookup"><span data-stu-id="62c57-140">-Publisher</span></span>
<span data-ttu-id="62c57-141">Uzantı işleyicisi yayımcısı adı.</span><span class="sxs-lookup"><span data-stu-id="62c57-141">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62c57-142">-ResourceGroupName</span></span>
<span data-ttu-id="62c57-143">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="62c57-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-144">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="62c57-144">-Setting</span></span>
<span data-ttu-id="62c57-145">Uzantı için JSON olarak biçimlendirilmiş genel ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62c57-145">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-146">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="62c57-146">-SubscriptionId</span></span>
<span data-ttu-id="62c57-147">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="62c57-147">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="62c57-148">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="62c57-148">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-149">Etiketli</span><span class="sxs-lookup"><span data-stu-id="62c57-149">-Tag</span></span>
<span data-ttu-id="62c57-150">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="62c57-150">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-151">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="62c57-151">-TypeHandlerVersion</span></span>
<span data-ttu-id="62c57-152">Komut dosyası işleyicisinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c57-152">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62c57-153">-Onay</span><span class="sxs-lookup"><span data-stu-id="62c57-153">-Confirm</span></span>
<span data-ttu-id="62c57-154">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="62c57-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62c57-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62c57-155">-WhatIf</span></span>
<span data-ttu-id="62c57-156">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="62c57-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62c57-157">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="62c57-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62c57-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c57-158">CommonParameters</span></span>
<span data-ttu-id="62c57-159">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="62c57-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c57-160">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="62c57-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c57-161">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="62c57-161">INPUTS</span></span>

### <span data-ttu-id="62c57-162">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="62c57-162">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="62c57-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="62c57-163">OUTPUTS</span></span>

### <span data-ttu-id="62c57-164">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="62c57-164">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="62c57-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="62c57-165">NOTES</span></span>

<span data-ttu-id="62c57-166">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="62c57-166">ALIASES</span></span>

<span data-ttu-id="62c57-167">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="62c57-167">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="62c57-168">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="62c57-168">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="62c57-169">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="62c57-169">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="62c57-170">EXTENSIONPARAMETER <IMachineExtension> : bir makine uzantısını açıklar.</span><span class="sxs-lookup"><span data-stu-id="62c57-170">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="62c57-171">`Location <String>`: Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="62c57-171">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="62c57-172">`[Tag <ITrackedResourceTags>]`: Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="62c57-172">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="62c57-173">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="62c57-173">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="62c57-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Dağıtım zamanında uzantının kullanılabiliyorsa, uzantının daha yeni bir alt sürüm kullanması gerekip gerekmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c57-174">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="62c57-175">Ancak dağıtıldıktan sonra, bu özellik doğru olarak dağıtılmadıkça, uzantı ikincil sürümleri yükseltmez.</span><span class="sxs-lookup"><span data-stu-id="62c57-175">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="62c57-176">`[ForceUpdateTag <String>]`: Uzantı yapılandırması değişmemiş olsa bile, uzantı işleyicisinin güncelleştirmeye zorlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="62c57-176">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="62c57-177">`[MachineExtensionType <String>]`: Uzantının türünü belirtir; Örneğin, "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="62c57-177">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="62c57-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Uzantı, protectedSettings veya Protectedsettingsfromkeykasası içerebilir veya hiç korumalı ayar içermez.</span><span class="sxs-lookup"><span data-stu-id="62c57-178">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="62c57-179">`[Publisher <String>]`: Uzantı işleyicisi yayımcısı adı.</span><span class="sxs-lookup"><span data-stu-id="62c57-179">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="62c57-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Uzantı için JSON olarak biçimlendirilmiş genel ayarlar.</span><span class="sxs-lookup"><span data-stu-id="62c57-180">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="62c57-181">`[TypeHandlerVersion <String>]`: Betik işleyicisinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="62c57-181">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

## <span data-ttu-id="62c57-182">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="62c57-182">RELATED LINKS</span></span>

