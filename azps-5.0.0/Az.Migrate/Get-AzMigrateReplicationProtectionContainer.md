---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280067"
---
# <span data-ttu-id="21e90-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="21e90-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="21e90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21e90-102">SYNOPSIS</span></span>
<span data-ttu-id="21e90-103">Koruma kapsayıcısının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="21e90-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="21e90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21e90-104">SYNTAX</span></span>

### <span data-ttu-id="21e90-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="21e90-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="21e90-106">Al</span><span class="sxs-lookup"><span data-stu-id="21e90-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="21e90-107">List1</span><span class="sxs-lookup"><span data-stu-id="21e90-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="21e90-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="21e90-108">DESCRIPTION</span></span>
<span data-ttu-id="21e90-109">Koruma kapsayıcısının ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="21e90-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="21e90-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21e90-110">EXAMPLES</span></span>

### <span data-ttu-id="21e90-111">Örnek 1: kasa ve dokudaki tüm koruma kapsayıcılarını Listele</span><span class="sxs-lookup"><span data-stu-id="21e90-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="21e90-112">Tümünü listeler.</span><span class="sxs-lookup"><span data-stu-id="21e90-112">Lists all.</span></span>

### <span data-ttu-id="21e90-113">Örnek 2: belirli bir kapsayıcıyı alma</span><span class="sxs-lookup"><span data-stu-id="21e90-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="21e90-114">Belirli bir.</span><span class="sxs-lookup"><span data-stu-id="21e90-114">Gets a specific one.</span></span>

## <span data-ttu-id="21e90-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21e90-115">PARAMETERS</span></span>

### <span data-ttu-id="21e90-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e90-116">-DefaultProfile</span></span>
<span data-ttu-id="21e90-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21e90-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21e90-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="21e90-118">-FabricName</span></span>
<span data-ttu-id="21e90-119">Doku adı.</span><span class="sxs-lookup"><span data-stu-id="21e90-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e90-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="21e90-120">-ProtectionContainerName</span></span>
<span data-ttu-id="21e90-121">Koruma kapsayıcısı adı.</span><span class="sxs-lookup"><span data-stu-id="21e90-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e90-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21e90-122">-ResourceGroupName</span></span>
<span data-ttu-id="21e90-123">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="21e90-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="21e90-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="21e90-124">-ResourceName</span></span>
<span data-ttu-id="21e90-125">Kurtarma Hizmetleri kasasındaki adı.</span><span class="sxs-lookup"><span data-stu-id="21e90-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="21e90-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="21e90-126">-SubscriptionId</span></span>
<span data-ttu-id="21e90-127">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="21e90-127">The subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21e90-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e90-128">CommonParameters</span></span>
<span data-ttu-id="21e90-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="21e90-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e90-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="21e90-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e90-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21e90-131">INPUTS</span></span>

## <span data-ttu-id="21e90-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21e90-132">OUTPUTS</span></span>

### <span data-ttu-id="21e90-133">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıprotectioncontainer</span><span class="sxs-lookup"><span data-stu-id="21e90-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="21e90-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21e90-134">NOTES</span></span>

<span data-ttu-id="21e90-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="21e90-135">ALIASES</span></span>

## <span data-ttu-id="21e90-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21e90-136">RELATED LINKS</span></span>

