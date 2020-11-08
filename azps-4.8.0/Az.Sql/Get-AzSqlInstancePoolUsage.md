---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273924"
---
# <span data-ttu-id="da79c-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="da79c-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="da79c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da79c-102">SYNOPSIS</span></span>
<span data-ttu-id="da79c-103">Azure SQL örnek havuzunun kullanımıyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="da79c-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="da79c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="da79c-104">SYNTAX</span></span>

### <span data-ttu-id="da79c-105">InstancePoolUsageDefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="da79c-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da79c-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="da79c-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da79c-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da79c-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da79c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="da79c-108">DESCRIPTION</span></span>
<span data-ttu-id="da79c-109">**Get-Azsqlınstancepoolusage** cmdlet 'ı Azure SQL örnek havuzunun kullanımı hakkında bilgi verir.</span><span class="sxs-lookup"><span data-stu-id="da79c-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="da79c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="da79c-110">EXAMPLES</span></span>

### <span data-ttu-id="da79c-111">Örnek 1: Azure SQL örnek havuzunun kullanımını alır</span><span class="sxs-lookup"><span data-stu-id="da79c-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="da79c-112">Azure SQL örnek havuzu instancepool0 kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="da79c-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="da79c-113">Örnek 2: bir örnek havuz nesnesi kullanarak Azure SQL örnek havuzunun kullanımını alır</span><span class="sxs-lookup"><span data-stu-id="da79c-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="da79c-114">Örnek havuz nesnesi kullanarak Azure SQL örnek havuzu instancepool0 kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="da79c-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="da79c-115">Örnek 3: örnek havuz kaynak kimliği kullanarak Azure SQL örnek havuzunun kullanımını alır</span><span class="sxs-lookup"><span data-stu-id="da79c-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="da79c-116">Örnek havuz kaynak tanımlayıcısını kullanarak Azure SQL örnek havuzu instancepool0 kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="da79c-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="da79c-117">Örnek 3: havuzdaki yönetilen örnek kullanımlarının dökümünü içeren bir Azure SQL örnek havuzunun kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="da79c-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="da79c-118">İnstancepool0 içinde yönetilen örneklerin kullanımıyla birlikte Azure SQL örnek havuzu instancepool0 kullanımını alır.</span><span class="sxs-lookup"><span data-stu-id="da79c-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="da79c-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="da79c-119">PARAMETERS</span></span>

### <span data-ttu-id="da79c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da79c-120">-DefaultProfile</span></span>
<span data-ttu-id="da79c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="da79c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da79c-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="da79c-122">-ExpandChildren</span></span>
<span data-ttu-id="da79c-123">Bu örnek havuzunun kullanımının çocuklarının kullanımıyla genişlemesini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="da79c-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="da79c-124">-Instancepool</span><span class="sxs-lookup"><span data-stu-id="da79c-124">-InstancePool</span></span>
<span data-ttu-id="da79c-125">Üst örnek havuz nesnesi.</span><span class="sxs-lookup"><span data-stu-id="da79c-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da79c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="da79c-126">-Name</span></span>
<span data-ttu-id="da79c-127">Yönetilen örnek havuzu adı.</span><span class="sxs-lookup"><span data-stu-id="da79c-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da79c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da79c-128">-ResourceGroupName</span></span>
<span data-ttu-id="da79c-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="da79c-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da79c-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="da79c-130">-ResourceId</span></span>
<span data-ttu-id="da79c-131">Üst kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="da79c-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da79c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da79c-132">CommonParameters</span></span>
<span data-ttu-id="da79c-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="da79c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da79c-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="da79c-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da79c-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="da79c-135">INPUTS</span></span>

### <span data-ttu-id="da79c-136">Microsoft.Azure.Commands.Sql.Instance_Pools. model. azures, ınstancepoolmodel</span><span class="sxs-lookup"><span data-stu-id="da79c-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="da79c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="da79c-137">System.String</span></span>

## <span data-ttu-id="da79c-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="da79c-138">OUTPUTS</span></span>

### <span data-ttu-id="da79c-139">Microsoft. Azure. Commands. Sql. kullanım. modeller. AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="da79c-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="da79c-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="da79c-140">NOTES</span></span>

## <span data-ttu-id="da79c-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="da79c-141">RELATED LINKS</span></span>
