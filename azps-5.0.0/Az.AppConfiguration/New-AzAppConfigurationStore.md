---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/new-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/New-AzAppConfigurationStore.md
ms.openlocfilehash: 20f3985553a3fc7a993480bdf154a7f8e6776bf6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276449"
---
# <span data-ttu-id="5c2af-101">New-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="5c2af-101">New-AzAppConfigurationStore</span></span>

## <span data-ttu-id="5c2af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c2af-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2af-103">Belirtilen parametrelerle birlikte yapılandırma deposu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c2af-103">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="5c2af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c2af-104">SYNTAX</span></span>

```
New-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> -Location <String> -Sku <String>
 [-SubscriptionId <String>] [-IdentityType <IdentityType>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5c2af-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c2af-105">DESCRIPTION</span></span>
<span data-ttu-id="5c2af-106">Belirtilen parametrelerle birlikte yapılandırma deposu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c2af-106">Creates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="5c2af-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c2af-107">EXAMPLES</span></span>

### <span data-ttu-id="5c2af-108">Örnek 1: uygulama yapılandırma deposu oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c2af-108">Example 1: Create an app configuration store</span></span>
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku free

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="5c2af-109">Bu komut, uygulama yapılandırma deposu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c2af-109">This command creates an app configuration store.</span></span>

### <span data-ttu-id="5c2af-110">Örnek 2: IdentityType "Useratandı" olarak ayarlanmış bir uygulama yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c2af-110">Example 2: Create an app configuration with the IdentityType set to "UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test03 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="5c2af-111">Bu komut bir uygulama yapılandırması oluşturur ve kullanıcıya atanmış bir yönetilen kimliği atar.</span><span class="sxs-lookup"><span data-stu-id="5c2af-111">This command creates an app configuration and assign a user-assigned managed identity to it.</span></span>
<span data-ttu-id="5c2af-112">`Update-AzAppConfigurationStore`CMK 'i (cusomer yönetilen anahtarı) etkinleştirmek için aşağıdaki adımların örneğe bakın.</span><span class="sxs-lookup"><span data-stu-id="5c2af-112">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="5c2af-113">Örnek 3: IdentityType "SystemAssigned" olarak ayarlanmış bir uygulama yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c2af-113">Example 3: Create an app configuration with the IdentityType set to "SystemAssigned"</span></span> 
```powershell
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned"

Location Name             Type
-------- ----             ----
eastus   appconfig-test11 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="5c2af-114">Bu komut, uygulama yapılandırması oluşturur ve kaynakla ilişkili sistem tarafından atanan yönetilen kimliği oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c2af-114">This command creates an app configuration and enables the system-assigned managed identity associated with the resource.</span></span>
<span data-ttu-id="5c2af-115">`Update-AzAppConfigurationStore`CMK 'i (cusomer yönetilen anahtarı) etkinleştirmek için aşağıdaki adımların örneğe bakın.</span><span class="sxs-lookup"><span data-stu-id="5c2af-115">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

### <span data-ttu-id="5c2af-116">Örnek 4: IdentityType "SystemAssigned, Useratandı" olarak ayarlanmış bir uygulama yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="5c2af-116">Example 4: Create an app configuration with the IdentityType set to "SystemAssigned, UserAssigned"</span></span>
```powershell
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test10 -ResourceGroupName azpwsh-manual-test -Location eastus -Sku standard -IdentityType "SystemAssigned, UserAssigned" -UserAssignedIdentity $assignedIdentity.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="5c2af-117">Sistem tarafından atanan yönetilen kimliği etkinleştirebilir ve aynı anda kullanıcıya atanan kimlikler verebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c2af-117">You can enable system-assigned managed identity and give user-assigned identities at the same time.</span></span>
<span data-ttu-id="5c2af-118">`Update-AzAppConfigurationStore`CMK 'i (cusomer yönetilen anahtarı) etkinleştirmek için aşağıdaki adımların örneğe bakın.</span><span class="sxs-lookup"><span data-stu-id="5c2af-118">See the example of `Update-AzAppConfigurationStore` for the following steps to enable CMK (cusomer managed key).</span></span>

## <span data-ttu-id="5c2af-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c2af-119">PARAMETERS</span></span>

### <span data-ttu-id="5c2af-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="5c2af-120">-AsJob</span></span>
<span data-ttu-id="5c2af-121">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="5c2af-121">Run the command as a job</span></span>

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

### <span data-ttu-id="5c2af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2af-122">-DefaultProfile</span></span>
<span data-ttu-id="5c2af-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c2af-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c2af-124">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5c2af-124">-IdentityType</span></span>
<span data-ttu-id="5c2af-125">Kullanılan yönetilen kimliğin türü.</span><span class="sxs-lookup"><span data-stu-id="5c2af-125">The type of managed identity used.</span></span>
<span data-ttu-id="5c2af-126">' Systemassignedancıuseratandı ' türü, örtülü olarak oluşturulmuş bir kimliği ve Kullanıcı tarafından atanan kimlikler kümesini içerir.</span><span class="sxs-lookup"><span data-stu-id="5c2af-126">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="5c2af-127">' None ' türü tüm kimlikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5c2af-127">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2af-128">-Konum</span><span class="sxs-lookup"><span data-stu-id="5c2af-128">-Location</span></span>
<span data-ttu-id="5c2af-129">Kaynağın konumu.</span><span class="sxs-lookup"><span data-stu-id="5c2af-129">The location of the resource.</span></span>
<span data-ttu-id="5c2af-130">Kaynak oluşturulduktan sonra bu değiştirilemez.</span><span class="sxs-lookup"><span data-stu-id="5c2af-130">This cannot be changed after the resource is created.</span></span>

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

### <span data-ttu-id="5c2af-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="5c2af-131">-Name</span></span>
<span data-ttu-id="5c2af-132">Yapılandırma deposu adı.</span><span class="sxs-lookup"><span data-stu-id="5c2af-132">The name of the configuration store.</span></span>

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

### <span data-ttu-id="5c2af-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5c2af-133">-NoWait</span></span>
<span data-ttu-id="5c2af-134">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="5c2af-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5c2af-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2af-135">-ResourceGroupName</span></span>
<span data-ttu-id="5c2af-136">Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5c2af-136">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="5c2af-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="5c2af-137">-Sku</span></span>
<span data-ttu-id="5c2af-138">Yapılandırma deposu SKU adı.</span><span class="sxs-lookup"><span data-stu-id="5c2af-138">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="5c2af-139">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5c2af-139">-SubscriptionId</span></span>
<span data-ttu-id="5c2af-140">Microsoft Azure abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5c2af-140">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="5c2af-141">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5c2af-141">-Tag</span></span>
<span data-ttu-id="5c2af-142">Kaynağın etiketleri.</span><span class="sxs-lookup"><span data-stu-id="5c2af-142">The tags of the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2af-143">-Useratandidentity</span><span class="sxs-lookup"><span data-stu-id="5c2af-143">-UserAssignedIdentity</span></span>
<span data-ttu-id="5c2af-144">Kaynakla ilişkili kullanıcı tarafından atanan kimliklerin listesi.</span><span class="sxs-lookup"><span data-stu-id="5c2af-144">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="5c2af-145">Kullanıcı tarafından atanan kimlik sözlüğü anahtarları şu formda ARM kaynak kimlikleri olacaktır: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} '.</span><span class="sxs-lookup"><span data-stu-id="5c2af-145">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2af-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c2af-146">-Confirm</span></span>
<span data-ttu-id="5c2af-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c2af-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c2af-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c2af-148">-WhatIf</span></span>
<span data-ttu-id="5c2af-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c2af-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c2af-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c2af-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c2af-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2af-151">CommonParameters</span></span>
<span data-ttu-id="5c2af-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c2af-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2af-153">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5c2af-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2af-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c2af-154">INPUTS</span></span>

## <span data-ttu-id="5c2af-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c2af-155">OUTPUTS</span></span>

### <span data-ttu-id="5c2af-156">Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. Api20200601. Iconationstore</span><span class="sxs-lookup"><span data-stu-id="5c2af-156">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="5c2af-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c2af-157">NOTES</span></span>

<span data-ttu-id="5c2af-158">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5c2af-158">ALIASES</span></span>

## <span data-ttu-id="5c2af-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c2af-159">RELATED LINKS</span></span>



[<span data-ttu-id="5c2af-160">New-Azuseratanandentity</span><span class="sxs-lookup"><span data-stu-id="5c2af-160">New-AzUserAssignedIdentity</span></span>](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)

