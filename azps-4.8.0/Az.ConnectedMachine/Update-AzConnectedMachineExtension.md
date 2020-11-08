---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109084"
---
# <span data-ttu-id="3b9d3-101">Update-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3b9d3-101">Update-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="3b9d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b9d3-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9d3-103">Uzantıyı oluşturma veya güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="3b9d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b9d3-104">SYNTAX</span></span>

### <span data-ttu-id="3b9d3-105">Updategenişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b9d3-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3b9d3-106">Güncelleştiremedi</span><span class="sxs-lookup"><span data-stu-id="3b9d3-106">Update</span></span>
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b9d3-107">Updateviaıdentity</span><span class="sxs-lookup"><span data-stu-id="3b9d3-107">UpdateViaIdentity</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b9d3-108">Updateviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="3b9d3-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b9d3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b9d3-109">DESCRIPTION</span></span>
<span data-ttu-id="3b9d3-110">Uzantıyı oluşturma veya güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="3b9d3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b9d3-111">EXAMPLES</span></span>

### <span data-ttu-id="3b9d3-112">Örnek 1: uzantıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3b9d3-112">Example 1: Update an extension</span></span>
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="3b9d3-113">Belirli bir makinedeki uzantıyı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-113">Updates an extension on a specific machine.</span></span>

### <span data-ttu-id="3b9d3-114">Örnek 2: ardışık düzen aracılığıyla belirtilen konumdaki uzantıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3b9d3-114">Example 2: Update an extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="3b9d3-115">Ardışık düzen aracılığıyla geçirilen belirli bir uzantıyı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-115">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="3b9d3-116">Burada, hangi uzantıyı kullanmak istediğimizi ve normal parametreler aracılığıyla neyi değiştirmek istediğimizi belirtmemize yardımcı olmak için ardışık düzen aracılığıyla geçirilen uzantıyı kullanıyoruz. `-Settings`</span><span class="sxs-lookup"><span data-stu-id="3b9d3-116">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on and are specifying what we want to change via the normal parameters (like `-Settings`)</span></span>

### <span data-ttu-id="3b9d3-117">Örnek 3: ardışık düzen aracılığıyla uzantı parametreleriyle uzantıyı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3b9d3-117">Example 3: Update an extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="3b9d3-118">Ardışık düzen aracılığıyla geçirilen belirli bir uzantıyı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-118">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="3b9d3-119">Burada, uzantıda yapmak istediğimiz değişiklikleri sağlamak için ardışık düzene geçilen uzantıyı kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-119">Here we are using the extension passed in via the pipeline to provide the changes we want to make on the extension.</span></span>
<span data-ttu-id="3b9d3-120">Uzantının konumu ardışık düzen aracılığıyla alınmadı, ancak normalde belirtilen parametreler aracılığıyla (Splat parametresine göre).</span><span class="sxs-lookup"><span data-stu-id="3b9d3-120">The location of the extension is not retrieved via the pipeline but rather via the parameters specified normally (by the splat parameter).</span></span>

### <span data-ttu-id="3b9d3-121">Örnek 4: bir uzantı nesnesini güncelleme için hem konum hem de parametre olarak kullanma</span><span class="sxs-lookup"><span data-stu-id="3b9d3-121">Example 4: Using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

<span data-ttu-id="3b9d3-122">Ardışık düzen aracılığıyla geçirilen belirli bir uzantıyı güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-122">Updates a specific extension passed in via the pipeline.</span></span>
<span data-ttu-id="3b9d3-123">Burada, hangi uzantının üzerinde çalışmak istediğimizi belirlememıza yardımcı olmak için ardışık düzen aracılığıyla geçirilen uzantıyı kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-123">Here we are using the extension passed in via the pipeline to help us identify which extension we want to operate on.</span></span>
<span data-ttu-id="3b9d3-124">Bunun yanı sıra, nelerin güncelleştirileceğini belirtmek için Extension nesnesinin parametrelerini de kullanıyoruz.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-124">In addition to that, we are using the parameters of the extension object to specify what to update.</span></span>

## <span data-ttu-id="3b9d3-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b9d3-125">PARAMETERS</span></span>

### <span data-ttu-id="3b9d3-126">-Iş</span><span class="sxs-lookup"><span data-stu-id="3b9d3-126">-AsJob</span></span>
<span data-ttu-id="3b9d3-127">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="3b9d3-127">Run the command as a job</span></span>

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

### <span data-ttu-id="3b9d3-128">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="3b9d3-128">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="3b9d3-129">Dağıtım zamanında uzantının kullanılabilir olması durumunda, uzantının daha yeni bir alt sürüm kullanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-129">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="3b9d3-130">Ancak dağıtıldıktan sonra, bu özellik doğru olarak dağıtılmadıkça, uzantı ikincil sürümleri yükseltmez.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-130">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9d3-131">-DefaultProfile</span></span>
<span data-ttu-id="3b9d3-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9d3-133">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="3b9d3-133">-ExtensionParameter</span></span>
<span data-ttu-id="3b9d3-134">Makine uzantısı güncelleştirmesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-134">Describes a Machine Extension Update.</span></span>
<span data-ttu-id="3b9d3-135">Oluşturmak için, EXTENSIONPARAMETER özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-135">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="3b9d3-136">-ForceRerun</span></span>
<span data-ttu-id="3b9d3-137">Uzantı yapılandırması değişmese de, uzantı işleyicisinin güncelleştirmeye zorlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b9d3-138">-InputObject</span></span>
<span data-ttu-id="3b9d3-139">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-140">-MachineName</span><span class="sxs-lookup"><span data-stu-id="3b9d3-140">-MachineName</span></span>
<span data-ttu-id="3b9d3-141">Uzantının oluşturulduğu veya güncelleştirileceği makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-141">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-142">-Ad</span><span class="sxs-lookup"><span data-stu-id="3b9d3-142">-Name</span></span>
<span data-ttu-id="3b9d3-143">Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-143">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-144">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3b9d3-144">-NoWait</span></span>
<span data-ttu-id="3b9d3-145">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="3b9d3-145">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b9d3-146">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="3b9d3-146">-ProtectedSetting</span></span>
<span data-ttu-id="3b9d3-147">Uzantı, protectedSettings veya Protectedsettingsfromkeykasası içerebilir veya hiç korumalı ayar içermez.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-147">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-148">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3b9d3-148">-Publisher</span></span>
<span data-ttu-id="3b9d3-149">Uzantı işleyicisi yayımcısı adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-149">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b9d3-150">-ResourceGroupName</span></span>
<span data-ttu-id="3b9d3-151">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-152">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="3b9d3-152">-Setting</span></span>
<span data-ttu-id="3b9d3-153">Uzantı için JSON olarak biçimlendirilmiş genel ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-153">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-154">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="3b9d3-154">-SubscriptionId</span></span>
<span data-ttu-id="3b9d3-155">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-155">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b9d3-156">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-156">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-157">Etiketli</span><span class="sxs-lookup"><span data-stu-id="3b9d3-157">-Tag</span></span>
<span data-ttu-id="3b9d3-158">Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="3b9d3-158">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-159">-Tür</span><span class="sxs-lookup"><span data-stu-id="3b9d3-159">-Type</span></span>
<span data-ttu-id="3b9d3-160">Uzantının türünü belirtir; Örneğin, "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="3b9d3-160">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="3b9d3-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="3b9d3-162">Komut dosyası işleyicisinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d3-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b9d3-163">-Confirm</span></span>
<span data-ttu-id="3b9d3-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b9d3-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b9d3-165">-WhatIf</span></span>
<span data-ttu-id="3b9d3-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b9d3-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b9d3-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9d3-168">CommonParameters</span></span>
<span data-ttu-id="3b9d3-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9d3-170">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9d3-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b9d3-171">INPUTS</span></span>

### <span data-ttu-id="3b9d3-172">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. ımachineextensionupdate</span><span class="sxs-lookup"><span data-stu-id="3b9d3-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate</span></span>

### <span data-ttu-id="3b9d3-173">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Iconnectedmachineıdentity</span><span class="sxs-lookup"><span data-stu-id="3b9d3-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="3b9d3-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b9d3-174">OUTPUTS</span></span>

### <span data-ttu-id="3b9d3-175">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3b9d3-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="3b9d3-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b9d3-176">NOTES</span></span>

<span data-ttu-id="3b9d3-177">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="3b9d3-177">ALIASES</span></span>

<span data-ttu-id="3b9d3-178">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="3b9d3-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3b9d3-179">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b9d3-180">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3b9d3-181">EXTENSIONPARAMETER <IMachineExtensionUpdate> : bir makine uzantısı güncelleştirmesini açıklar.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-181">EXTENSIONPARAMETER <IMachineExtensionUpdate>: Describes a Machine Extension Update.</span></span>
  - <span data-ttu-id="3b9d3-182">`[Tag <IUpdateResourceTags>]`: Kaynak etiketleri</span><span class="sxs-lookup"><span data-stu-id="3b9d3-182">`[Tag <IUpdateResourceTags>]`: Resource tags</span></span>
    - <span data-ttu-id="3b9d3-183">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-183">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="3b9d3-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Dağıtım zamanında uzantının kullanılabiliyorsa, uzantının daha yeni bir alt sürüm kullanması gerekip gerekmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-184">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="3b9d3-185">Ancak dağıtıldıktan sonra, bu özellik doğru olarak dağıtılmadıkça, uzantı ikincil sürümleri yükseltmez.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-185">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="3b9d3-186">`[ForceUpdateTag <String>]`: Uzantı yapılandırması değişmemiş olsa bile, uzantı işleyicisinin güncelleştirmeye zorlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-186">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="3b9d3-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Uzantı, protectedSettings veya Protectedsettingsfromkeykasası içerebilir veya hiç korumalı ayar içermez.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-187">`[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="3b9d3-188">`[Publisher <String>]`: Uzantı işleyicisi yayımcısı adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-188">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="3b9d3-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Uzantı için JSON olarak biçimlendirilmiş genel ayarlar.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-189">`[Setting <IMachineExtensionUpdatePropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="3b9d3-190">`[Type <String>]`: Uzantının türünü belirtir; Örneğin, "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="3b9d3-190">`[Type <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="3b9d3-191">`[TypeHandlerVersion <String>]`: Betik işleyicisinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-191">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="3b9d3-192">INPUTOBJECT <IConnectedMachineIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="3b9d3-192">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b9d3-193">`[ExtensionName <String>]`: Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-193">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="3b9d3-194">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="3b9d3-194">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b9d3-195">`[Name <String>]`: Karma makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-195">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="3b9d3-196">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-196">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3b9d3-197">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-197">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3b9d3-198">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="3b9d3-198">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3b9d3-199">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b9d3-199">RELATED LINKS</span></span>

