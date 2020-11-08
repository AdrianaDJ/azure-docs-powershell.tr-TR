---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278635"
---
# <span data-ttu-id="9b567-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="9b567-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="9b567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b567-102">SYNOPSIS</span></span>
<span data-ttu-id="9b567-103">Koruma kapsayıcısı eşlemesi oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="9b567-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="9b567-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9b567-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9b567-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9b567-105">DESCRIPTION</span></span>
<span data-ttu-id="9b567-106">Koruma kapsayıcısı eşlemesi oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="9b567-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="9b567-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9b567-107">EXAMPLES</span></span>

### <span data-ttu-id="9b567-108">Örnek 1: eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b567-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="9b567-109">Eşleme oluşturma</span><span class="sxs-lookup"><span data-stu-id="9b567-109">Create a mapping</span></span>

## <span data-ttu-id="9b567-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9b567-110">PARAMETERS</span></span>

### <span data-ttu-id="9b567-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="9b567-111">-AsJob</span></span>
<span data-ttu-id="9b567-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="9b567-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9b567-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b567-113">-DefaultProfile</span></span>
<span data-ttu-id="9b567-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9b567-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b567-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="9b567-115">-FabricName</span></span>
<span data-ttu-id="9b567-116">Doku adı.</span><span class="sxs-lookup"><span data-stu-id="9b567-116">Fabric name.</span></span>

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

### <span data-ttu-id="9b567-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="9b567-117">-MappingName</span></span>
<span data-ttu-id="9b567-118">Koruma kapsayıcısı eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="9b567-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="9b567-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9b567-119">-NoWait</span></span>
<span data-ttu-id="9b567-120">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="9b567-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9b567-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="9b567-121">-PolicyId</span></span>
<span data-ttu-id="9b567-122">İlgili ilke.</span><span class="sxs-lookup"><span data-stu-id="9b567-122">Applicable policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b567-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="9b567-123">-ProtectionContainerName</span></span>
<span data-ttu-id="9b567-124">Koruma kapsayıcısı adı.</span><span class="sxs-lookup"><span data-stu-id="9b567-124">Protection container name.</span></span>

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

### <span data-ttu-id="9b567-125">-Providerspecificınput</span><span class="sxs-lookup"><span data-stu-id="9b567-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="9b567-126">Eşleştirme için sağlayıcıya özgü giriş.</span><span class="sxs-lookup"><span data-stu-id="9b567-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="9b567-127">Oluşturmak için, PROVIDERSPECIFICıNPUT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9b567-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b567-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b567-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b567-129">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="9b567-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="9b567-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9b567-130">-ResourceName</span></span>
<span data-ttu-id="9b567-131">Kurtarma Hizmetleri kasasındaki adı.</span><span class="sxs-lookup"><span data-stu-id="9b567-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="9b567-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="9b567-132">-SubscriptionId</span></span>
<span data-ttu-id="9b567-133">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="9b567-133">The subscription Id.</span></span>

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

### <span data-ttu-id="9b567-134">-Targetprotectioncontainerıd</span><span class="sxs-lookup"><span data-stu-id="9b567-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="9b567-135">Hedef benzersiz koruma kapsayıcısı adı.</span><span class="sxs-lookup"><span data-stu-id="9b567-135">The target unique protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b567-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="9b567-136">-Confirm</span></span>
<span data-ttu-id="9b567-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9b567-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b567-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b567-138">-WhatIf</span></span>
<span data-ttu-id="9b567-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9b567-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b567-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9b567-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b567-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b567-141">CommonParameters</span></span>
<span data-ttu-id="9b567-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9b567-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b567-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="9b567-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b567-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9b567-144">INPUTS</span></span>

## <span data-ttu-id="9b567-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9b567-145">OUTPUTS</span></span>

### <span data-ttu-id="9b567-146">Microsoft. Azure. PowerShell. cmdlet. Api20180110. ıprotectioncontainermapping</span><span class="sxs-lookup"><span data-stu-id="9b567-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="9b567-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9b567-147">NOTES</span></span>

<span data-ttu-id="9b567-148">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="9b567-148">ALIASES</span></span>

<span data-ttu-id="9b567-149">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="9b567-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b567-150">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="9b567-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b567-151">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9b567-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b567-152">PROVIDERSPECIFICıNPUT <IReplicationProviderSpecificContainerMappingInput> : eşleştirme için sağlayıcıya özgü giriş.</span><span class="sxs-lookup"><span data-stu-id="9b567-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="9b567-153">`[InstanceType <String>]`: Sınıf türü.</span><span class="sxs-lookup"><span data-stu-id="9b567-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="9b567-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9b567-154">RELATED LINKS</span></span>

