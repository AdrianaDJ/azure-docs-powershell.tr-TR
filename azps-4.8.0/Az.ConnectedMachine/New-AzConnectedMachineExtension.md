---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/new-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/New-AzConnectedMachineExtension.md
ms.openlocfilehash: 13095d24bd095e27bac788d0d578bdcdf3e1a0f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275096"
---
# <span data-ttu-id="a6cf4-101">New-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a6cf4-101">New-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="a6cf4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="a6cf4-103">Uzantıyı oluşturma veya güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-103">The operation to create or update the extension.</span></span>

## <span data-ttu-id="a6cf4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6cf4-104">SYNTAX</span></span>

### <span data-ttu-id="a6cf4-105">Genişletilmiş (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6cf4-105">CreateExpanded (Default)</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a6cf4-106">Oluturmak</span><span class="sxs-lookup"><span data-stu-id="a6cf4-106">Create</span></span>
```
New-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a6cf4-107">Createviaıdentity</span><span class="sxs-lookup"><span data-stu-id="a6cf4-107">CreateViaIdentity</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtension> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a6cf4-108">Createviaıdentitygenişletilmiş</span><span class="sxs-lookup"><span data-stu-id="a6cf4-108">CreateViaIdentityExpanded</span></span>
```
New-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> -Location <String>
 [-AutoUpgradeMinorVersion] [-ExtensionType <String>] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>] [-TypeHandlerVersion <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a6cf4-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6cf4-109">DESCRIPTION</span></span>
<span data-ttu-id="a6cf4-110">Uzantıyı oluşturma veya güncelleştirme işlemi.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-110">The operation to create or update the extension.</span></span>

## <span data-ttu-id="a6cf4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6cf4-111">EXAMPLES</span></span>

### <span data-ttu-id="a6cf4-112">Örnek 1: makineye yeni uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="a6cf4-112">Example 1: Add a new extension to a machine</span></span>
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="a6cf4-113">Bir makinede uzantı ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-113">Sets an extension on a machine.</span></span>

### <span data-ttu-id="a6cf4-114">Örnek 2: ardışık düzen aracılığıyla belirtilen uzantı parametreleriyle yeni bir uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="a6cf4-114">Example 2: Add a new extension with extension parameters specified via the pipeline</span></span>
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | New-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="a6cf4-115">Bu, ardışık düzen aracılığıyla geçirilen nesne tarafından sağlanan uzantı parametreleriyle yeni bir uzantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-115">This creates a new extension with the extension parameters provided by the object passed in via the pipeline.</span></span>
<span data-ttu-id="a6cf4-116">Bu, bir makinenin parametrelerini almak ve başka bir makineye uygulamak istiyorlar.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-116">This is great if you want to grab the parameters of one machine and apply it to another machine.</span></span>

### <span data-ttu-id="a6cf4-117">Örnek 3: ardışık düzen aracılığıyla belirtilen konuma sahip yeni bir uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="a6cf4-117">Example 3: Add a new extension with location specified via the pipeline</span></span>
```powershell
PS C:\> $identity = [Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.ConnectedMachineIdentity]@{
    Id = "/subscriptions/$($SubscriptionId)/resourceGroups/$($ResourceGroupName)/providers/Microsoft.HybridCompute/machines/$MachineName/extensions/$ExtensionName"
}
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> $identity | New-AzConnectedMachineExtension -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

<span data-ttu-id="a6cf4-118">Bu, ardışık düzen aracılığıyla sağlanan kimliği kullanan yeni bir makine uzantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-118">This creates a new machine extension using the identity provided via the pipeline.</span></span>
<span data-ttu-id="a6cf4-119">Bunu yapmanız mümkün değildir ama olasıdır.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-119">You likely won't do this, but it's possible.</span></span>

### <span data-ttu-id="a6cf4-120">Örnek 4: Uzantı nesnesini kullanarak, güncelleştirme için hem konum hem de parametre olarak yeni bir uzantı ekleme</span><span class="sxs-lookup"><span data-stu-id="a6cf4-120">Example 4: Add a new extension using an extension object as both the location and parameters for updating</span></span>
```powershell
PS C:\> $ext = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $ext | New-AzConnectedMachineExtension -ExtensionParameter $ext
```

<span data-ttu-id="a6cf4-121">Bu işlem ardışık düzen ve geçirilen uzantı nesnesinin sağladığı uzantı ayrıntıları ile sağlanan kimliği kullanan yeni bir makine uzantısı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-121">This creates a new machine extension using the identity provided via the pipeline and the extension details provided by the passed in extension object.</span></span>
<span data-ttu-id="a6cf4-122">Bunu yapmanız mümkün değildir ama olasıdır.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-122">You likely won't do this, but it's possible.</span></span>

## <span data-ttu-id="a6cf4-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6cf4-123">PARAMETERS</span></span>

### <span data-ttu-id="a6cf4-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="a6cf4-124">-AsJob</span></span>
<span data-ttu-id="a6cf4-125">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="a6cf4-125">Run the command as a job</span></span>

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

### <span data-ttu-id="a6cf4-126">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="a6cf4-126">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="a6cf4-127">Dağıtım zamanında uzantının kullanılabilir olması durumunda, uzantının daha yeni bir alt sürüm kullanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-127">Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span>
<span data-ttu-id="a6cf4-128">Ancak dağıtıldıktan sonra, bu özellik doğru olarak dağıtılmadıkça, uzantı ikincil sürümleri yükseltmez.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-128">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6cf4-129">-DefaultProfile</span></span>
<span data-ttu-id="a6cf4-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6cf4-131">-ExtensionParameter</span><span class="sxs-lookup"><span data-stu-id="a6cf4-131">-ExtensionParameter</span></span>
<span data-ttu-id="a6cf4-132">Bir makine uzantısını açıklar.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-132">Describes a Machine Extension.</span></span>
<span data-ttu-id="a6cf4-133">Oluşturmak için, EXTENSIONPARAMETER özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-133">To construct, see NOTES section for EXTENSIONPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-134">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="a6cf4-134">-ExtensionType</span></span>
<span data-ttu-id="a6cf4-135">Uzantının türünü belirtir; Örneğin, "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="a6cf4-135">Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-136">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="a6cf4-136">-ForceRerun</span></span>
<span data-ttu-id="a6cf4-137">Uzantı yapılandırması değişmese de, uzantı işleyicisinin güncelleştirmeye zorlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-137">How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6cf4-138">-InputObject</span></span>
<span data-ttu-id="a6cf4-139">Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-139">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-140">-Konum</span><span class="sxs-lookup"><span data-stu-id="a6cf4-140">-Location</span></span>
<span data-ttu-id="a6cf4-141">Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="a6cf4-141">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-142">-MachineName</span><span class="sxs-lookup"><span data-stu-id="a6cf4-142">-MachineName</span></span>
<span data-ttu-id="a6cf4-143">Uzantının oluşturulduğu veya güncelleştirileceği makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-143">The name of the machine where the extension should be created or updated.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6cf4-144">-Name</span></span>
<span data-ttu-id="a6cf4-145">Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-145">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-146">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6cf4-146">-NoWait</span></span>
<span data-ttu-id="a6cf4-147">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="a6cf4-147">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6cf4-148">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="a6cf4-148">-ProtectedSetting</span></span>
<span data-ttu-id="a6cf4-149">Uzantı, protectedSettings veya Protectedsettingsfromkeykasası içerebilir veya hiç korumalı ayar içermez.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-149">The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-150">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a6cf4-150">-Publisher</span></span>
<span data-ttu-id="a6cf4-151">Uzantı işleyicisi yayımcısı adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-151">The name of the extension handler publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6cf4-152">-ResourceGroupName</span></span>
<span data-ttu-id="a6cf4-153">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-154">-Ayarlar</span><span class="sxs-lookup"><span data-stu-id="a6cf4-154">-Setting</span></span>
<span data-ttu-id="a6cf4-155">Uzantı için JSON olarak biçimlendirilmiş genel ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-155">Json formatted public settings for the extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-156">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a6cf4-156">-SubscriptionId</span></span>
<span data-ttu-id="a6cf4-157">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-157">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a6cf4-158">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-158">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-159">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a6cf4-159">-Tag</span></span>
<span data-ttu-id="a6cf4-160">Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-160">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="a6cf4-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="a6cf4-162">Komut dosyası işleyicisinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-162">Specifies the version of the script handler.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6cf4-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6cf4-163">-Confirm</span></span>
<span data-ttu-id="a6cf4-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6cf4-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6cf4-165">-WhatIf</span></span>
<span data-ttu-id="a6cf4-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6cf4-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6cf4-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6cf4-168">CommonParameters</span></span>
<span data-ttu-id="a6cf4-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6cf4-170">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6cf4-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6cf4-171">INPUTS</span></span>

### <span data-ttu-id="a6cf4-172">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a6cf4-172">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

### <span data-ttu-id="a6cf4-173">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Iconnectedmachineıdentity</span><span class="sxs-lookup"><span data-stu-id="a6cf4-173">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="a6cf4-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6cf4-174">OUTPUTS</span></span>

### <span data-ttu-id="a6cf4-175">Microsoft. Azure. PowerShell. cmdlet. ConnectedMachine. modeller. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="a6cf4-175">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="a6cf4-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6cf4-176">NOTES</span></span>

<span data-ttu-id="a6cf4-177">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="a6cf4-177">ALIASES</span></span>

<span data-ttu-id="a6cf4-178">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="a6cf4-178">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a6cf4-179">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-179">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a6cf4-180">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-180">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a6cf4-181">EXTENSIONPARAMETER <IMachineExtension> : bir makine uzantısını açıklar.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-181">EXTENSIONPARAMETER <IMachineExtension>: Describes a Machine Extension.</span></span>
  - <span data-ttu-id="a6cf4-182">`Location <String>`: Kaynağın yaşadığı coğrafi konum</span><span class="sxs-lookup"><span data-stu-id="a6cf4-182">`Location <String>`: The geo-location where the resource lives</span></span>
  - <span data-ttu-id="a6cf4-183">`[Tag <ITrackedResourceTags>]`: Kaynak etiketleri.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-183">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="a6cf4-184">`[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-184">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="a6cf4-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Dağıtım zamanında uzantının kullanılabiliyorsa, uzantının daha yeni bir alt sürüm kullanması gerekip gerekmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-185">`[AutoUpgradeMinorVersion <Boolean?>]`: Indicates whether the extension should use a newer minor version if one is available at deployment time.</span></span> <span data-ttu-id="a6cf4-186">Ancak dağıtıldıktan sonra, bu özellik doğru olarak dağıtılmadıkça, uzantı ikincil sürümleri yükseltmez.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-186">Once deployed, however, the extension will not upgrade minor versions unless redeployed, even with this property set to true.</span></span>
  - <span data-ttu-id="a6cf4-187">`[ForceUpdateTag <String>]`: Uzantı yapılandırması değişmemiş olsa bile, uzantı işleyicisinin güncelleştirmeye zorlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-187">`[ForceUpdateTag <String>]`: How the extension handler should be forced to update even if the extension configuration has not changed.</span></span>
  - <span data-ttu-id="a6cf4-188">`[MachineExtensionType <String>]`: Uzantının türünü belirtir; Örneğin, "CustomScriptExtension".</span><span class="sxs-lookup"><span data-stu-id="a6cf4-188">`[MachineExtensionType <String>]`: Specifies the type of the extension; an example is "CustomScriptExtension".</span></span>
  - <span data-ttu-id="a6cf4-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Uzantı, protectedSettings veya Protectedsettingsfromkeykasası içerebilir veya hiç korumalı ayar içermez.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-189">`[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: The extension can contain either protectedSettings or protectedSettingsFromKeyVault or no protected settings at all.</span></span>
  - <span data-ttu-id="a6cf4-190">`[Publisher <String>]`: Uzantı işleyicisi yayımcısı adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-190">`[Publisher <String>]`: The name of the extension handler publisher.</span></span>
  - <span data-ttu-id="a6cf4-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Uzantı için JSON olarak biçimlendirilmiş genel ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-191">`[Setting <IMachineExtensionPropertiesSettings>]`: Json formatted public settings for the extension.</span></span>
  - <span data-ttu-id="a6cf4-192">`[TypeHandlerVersion <String>]`: Betik işleyicisinin sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-192">`[TypeHandlerVersion <String>]`: Specifies the version of the script handler.</span></span>

<span data-ttu-id="a6cf4-193">INPUTOBJECT <IConnectedMachineIdentity> : IDENTITY parametresi</span><span class="sxs-lookup"><span data-stu-id="a6cf4-193">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a6cf4-194">`[ExtensionName <String>]`: Makine uzantısının adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-194">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="a6cf4-195">`[Id <String>]`: Kaynak kimliği yolu</span><span class="sxs-lookup"><span data-stu-id="a6cf4-195">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a6cf4-196">`[Name <String>]`: Karma makinenin adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-196">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="a6cf4-197">`[ResourceGroupName <String>]`: Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-197">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a6cf4-198">`[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanıtan abonelik kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-198">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a6cf4-199">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a6cf4-199">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a6cf4-200">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6cf4-200">RELATED LINKS</span></span>

