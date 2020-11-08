---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277315"
---
# <span data-ttu-id="df61e-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="df61e-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="df61e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df61e-102">SYNOPSIS</span></span>
<span data-ttu-id="df61e-103">Çoğaltma ilkesi oluşturma işlemi</span><span class="sxs-lookup"><span data-stu-id="df61e-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="df61e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df61e-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df61e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df61e-105">DESCRIPTION</span></span>
<span data-ttu-id="df61e-106">Çoğaltma ilkesi oluşturma işlemi</span><span class="sxs-lookup"><span data-stu-id="df61e-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="df61e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df61e-107">EXAMPLES</span></span>

### <span data-ttu-id="df61e-108">Örnek 1: çoğaltma ilkesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="df61e-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="df61e-109">VmWare CBT için ilke oluşturur</span><span class="sxs-lookup"><span data-stu-id="df61e-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="df61e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df61e-110">PARAMETERS</span></span>

### <span data-ttu-id="df61e-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="df61e-111">-AsJob</span></span>
<span data-ttu-id="df61e-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="df61e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="df61e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df61e-113">-DefaultProfile</span></span>
<span data-ttu-id="df61e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="df61e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df61e-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="df61e-115">-NoWait</span></span>
<span data-ttu-id="df61e-116">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="df61e-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="df61e-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="df61e-117">-PolicyName</span></span>
<span data-ttu-id="df61e-118">Çoğaltma ilkesi adı</span><span class="sxs-lookup"><span data-stu-id="df61e-118">Replication policy name</span></span>

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

### <span data-ttu-id="df61e-119">-Providerspecificınput</span><span class="sxs-lookup"><span data-stu-id="df61e-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="df61e-120">ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="df61e-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="df61e-121">Oluşturmak için, PROVIDERSPECIFICıNPUT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="df61e-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df61e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df61e-122">-ResourceGroupName</span></span>
<span data-ttu-id="df61e-123">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="df61e-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="df61e-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="df61e-124">-ResourceName</span></span>
<span data-ttu-id="df61e-125">Kurtarma Hizmetleri kasasındaki adı.</span><span class="sxs-lookup"><span data-stu-id="df61e-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="df61e-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="df61e-126">-SubscriptionId</span></span>
<span data-ttu-id="df61e-127">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="df61e-127">The subscription Id.</span></span>

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

### <span data-ttu-id="df61e-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="df61e-128">-Confirm</span></span>
<span data-ttu-id="df61e-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="df61e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df61e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df61e-130">-WhatIf</span></span>
<span data-ttu-id="df61e-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="df61e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df61e-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="df61e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df61e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df61e-133">CommonParameters</span></span>
<span data-ttu-id="df61e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df61e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df61e-135">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="df61e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df61e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df61e-136">INPUTS</span></span>

## <span data-ttu-id="df61e-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df61e-137">OUTPUTS</span></span>

### <span data-ttu-id="df61e-138">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıpolicy</span><span class="sxs-lookup"><span data-stu-id="df61e-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="df61e-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df61e-139">NOTES</span></span>

<span data-ttu-id="df61e-140">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="df61e-140">ALIASES</span></span>

<span data-ttu-id="df61e-141">KARMAŞıK PARAMETRE ÖZELLIKLERI</span><span class="sxs-lookup"><span data-stu-id="df61e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df61e-142">Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun.</span><span class="sxs-lookup"><span data-stu-id="df61e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df61e-143">Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df61e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df61e-144">PROVIDERSPECIFICıNPUT <IPolicyProviderSpecificInput> : ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="df61e-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="df61e-145">`[InstanceType <String>]`: Sınıf türü.</span><span class="sxs-lookup"><span data-stu-id="df61e-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="df61e-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df61e-146">RELATED LINKS</span></span>

