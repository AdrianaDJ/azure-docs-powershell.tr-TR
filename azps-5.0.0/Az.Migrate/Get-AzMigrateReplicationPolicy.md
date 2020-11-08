---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationPolicy.md
ms.openlocfilehash: a5e35096966355a69ad5b363b61ab3cd5d2f0d0b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280068"
---
# <span data-ttu-id="14593-101">Get-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="14593-101">Get-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="14593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14593-102">SYNOPSIS</span></span>
<span data-ttu-id="14593-103">Çoğaltma ilkesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="14593-103">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="14593-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14593-104">SYNTAX</span></span>

### <span data-ttu-id="14593-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="14593-105">List (Default)</span></span>
```
Get-AzMigrateReplicationPolicy -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="14593-106">Al</span><span class="sxs-lookup"><span data-stu-id="14593-106">Get</span></span>
```
Get-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="14593-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="14593-107">DESCRIPTION</span></span>
<span data-ttu-id="14593-108">Çoğaltma ilkesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="14593-108">Gets the details of a replication policy.</span></span>

## <span data-ttu-id="14593-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14593-109">EXAMPLES</span></span>

### <span data-ttu-id="14593-110">Örnek 1: kasaya tüm ilkeleri alma</span><span class="sxs-lookup"><span data-stu-id="14593-110">Example 1: Get all policies in a vault</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

Location Name                                Type
-------- ----                                ----
         samplepolicy2                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplepolicy1                       Microsoft.RecoveryServices/vaults/replicationPolicies
         samplePolicy3                       Microsoft.RecoveryServices/vaults/replicationPolicies
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="14593-111">Tüm ilkelere ulaşın.</span><span class="sxs-lookup"><span data-stu-id="14593-111">Get all policies.</span></span>

### <span data-ttu-id="14593-112">Örnek 2: belirli bir ilke edinin</span><span class="sxs-lookup"><span data-stu-id="14593-112">Example 2: Get a specific policy</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationPolicy -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -PolicyName  migrateAzMigratePWSHTc8d1sitepolicy

Location Name                                Type
-------- ----                                ----
         migrateAzMigratePWSHTc8d1sitepolicy Microsoft.RecoveryServices/vaults/replicationPolicies
```

<span data-ttu-id="14593-113">Belirli bir.</span><span class="sxs-lookup"><span data-stu-id="14593-113">Get a specific one.</span></span>

## <span data-ttu-id="14593-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14593-114">PARAMETERS</span></span>

### <span data-ttu-id="14593-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14593-115">-DefaultProfile</span></span>
<span data-ttu-id="14593-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14593-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14593-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="14593-117">-PolicyName</span></span>
<span data-ttu-id="14593-118">Çoğaltma ilkesi adı.</span><span class="sxs-lookup"><span data-stu-id="14593-118">Replication policy name.</span></span>

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

### <span data-ttu-id="14593-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14593-119">-ResourceGroupName</span></span>
<span data-ttu-id="14593-120">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="14593-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="14593-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="14593-121">-ResourceName</span></span>
<span data-ttu-id="14593-122">Kurtarma Hizmetleri kasasındaki adı.</span><span class="sxs-lookup"><span data-stu-id="14593-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="14593-123">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="14593-123">-SubscriptionId</span></span>
<span data-ttu-id="14593-124">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="14593-124">The subscription Id.</span></span>

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

### <span data-ttu-id="14593-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14593-125">CommonParameters</span></span>
<span data-ttu-id="14593-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14593-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14593-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="14593-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14593-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14593-128">INPUTS</span></span>

## <span data-ttu-id="14593-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14593-129">OUTPUTS</span></span>

### <span data-ttu-id="14593-130">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180110. ıpolicy</span><span class="sxs-lookup"><span data-stu-id="14593-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="14593-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14593-131">NOTES</span></span>

<span data-ttu-id="14593-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="14593-132">ALIASES</span></span>

## <span data-ttu-id="14593-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14593-133">RELATED LINKS</span></span>

