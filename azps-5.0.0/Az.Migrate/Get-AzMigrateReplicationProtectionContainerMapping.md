---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280064"
---
# <span data-ttu-id="27cae-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="27cae-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="27cae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27cae-102">SYNOPSIS</span></span>
<span data-ttu-id="27cae-103">Koruma kapsayıcısı eşlemesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="27cae-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="27cae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27cae-104">SYNTAX</span></span>

### <span data-ttu-id="27cae-105">List1 (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27cae-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27cae-106">Al</span><span class="sxs-lookup"><span data-stu-id="27cae-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="27cae-107">Listeniz</span><span class="sxs-lookup"><span data-stu-id="27cae-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="27cae-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27cae-108">DESCRIPTION</span></span>
<span data-ttu-id="27cae-109">Koruma kapsayıcısı eşlemesinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="27cae-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="27cae-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27cae-110">EXAMPLES</span></span>

### <span data-ttu-id="27cae-111">Örnek 1: belirli bir eşleme alma</span><span class="sxs-lookup"><span data-stu-id="27cae-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="27cae-112">Eşleme ayrıntısı alın.</span><span class="sxs-lookup"><span data-stu-id="27cae-112">Get a mapping detail.</span></span>

## <span data-ttu-id="27cae-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27cae-113">PARAMETERS</span></span>

### <span data-ttu-id="27cae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cae-114">-DefaultProfile</span></span>
<span data-ttu-id="27cae-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27cae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27cae-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="27cae-116">-FabricName</span></span>
<span data-ttu-id="27cae-117">Doku adı.</span><span class="sxs-lookup"><span data-stu-id="27cae-117">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cae-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="27cae-118">-MappingName</span></span>
<span data-ttu-id="27cae-119">Koruma kapsayıcısı eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="27cae-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="27cae-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="27cae-120">-ProtectionContainerName</span></span>
<span data-ttu-id="27cae-121">Koruma kapsayıcısı adı.</span><span class="sxs-lookup"><span data-stu-id="27cae-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27cae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27cae-122">-ResourceGroupName</span></span>
<span data-ttu-id="27cae-123">Kurtarma Hizmetleri kasasındaki kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="27cae-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="27cae-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="27cae-124">-ResourceName</span></span>
<span data-ttu-id="27cae-125">Kurtarma Hizmetleri kasasındaki adı.</span><span class="sxs-lookup"><span data-stu-id="27cae-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="27cae-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="27cae-126">-SubscriptionId</span></span>
<span data-ttu-id="27cae-127">Abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="27cae-127">The subscription Id.</span></span>

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

### <span data-ttu-id="27cae-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cae-128">CommonParameters</span></span>
<span data-ttu-id="27cae-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27cae-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cae-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27cae-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cae-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27cae-131">INPUTS</span></span>

## <span data-ttu-id="27cae-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27cae-132">OUTPUTS</span></span>

### <span data-ttu-id="27cae-133">Microsoft. Azure. PowerShell. cmdlet. Api20180110. ıprotectioncontainermapping</span><span class="sxs-lookup"><span data-stu-id="27cae-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="27cae-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27cae-134">NOTES</span></span>

<span data-ttu-id="27cae-135">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="27cae-135">ALIASES</span></span>

## <span data-ttu-id="27cae-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27cae-136">RELATED LINKS</span></span>

