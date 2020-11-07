---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 8d2d1333a10290c3a321b22cf33b527738d7ecb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933610"
---
# <span data-ttu-id="42c91-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="42c91-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="42c91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c91-102">SYNOPSIS</span></span>
<span data-ttu-id="42c91-103">Azure SQL örnek havuzuyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="42c91-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="42c91-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42c91-104">SYNTAX</span></span>

### <span data-ttu-id="42c91-105">ListBySubOrResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42c91-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42c91-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="42c91-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42c91-107">Getınstancepoolbyınstancepoolresourceıdentifierparameterset</span><span class="sxs-lookup"><span data-stu-id="42c91-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42c91-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="42c91-108">DESCRIPTION</span></span>
<span data-ttu-id="42c91-109">**Get-Azsqlınstancepool** cmdlet 'i, bir veya daha fazla Azure SQL örneği havuzuyla ilgili bilgileri döndürür.</span><span class="sxs-lookup"><span data-stu-id="42c91-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="42c91-110">Yalnızca bu örnek havuzunun bilgilerini görmek için örnek havuzun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="42c91-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="42c91-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42c91-111">EXAMPLES</span></span>

### <span data-ttu-id="42c91-112">Örnek 1: müşteri aboneliği genelinde tüm örnek havuzlarını alma</span><span class="sxs-lookup"><span data-stu-id="42c91-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="42c91-113">Bu komut, müşteri aboneliğindeki tüm örnek havuzlarıyla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="42c91-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="42c91-114">Örnek 2: kaynak grubundaki tüm örnek havuzlarını alma</span><span class="sxs-lookup"><span data-stu-id="42c91-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="42c91-115">Bu komut, kaynak grubu resourcegroup01 içindeki örnek havuzlarıyla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="42c91-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="42c91-116">Örnek 3: örnek havuz hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="42c91-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="42c91-117">Bu komut, örnek havuz instancePool0 hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="42c91-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="42c91-118">Örnek 4: örnek havuz kaynak kimliğini kullanarak örnek havuzu hakkında bilgi alma</span><span class="sxs-lookup"><span data-stu-id="42c91-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="42c91-119">Bu komut, kaynak tanımlayıcısıyla birlikte örnek havuzu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="42c91-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="42c91-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42c91-120">PARAMETERS</span></span>

### <span data-ttu-id="42c91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c91-121">-DefaultProfile</span></span>
<span data-ttu-id="42c91-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42c91-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c91-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="42c91-123">-Name</span></span>
<span data-ttu-id="42c91-124">Örnek havuz adı.</span><span class="sxs-lookup"><span data-stu-id="42c91-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c91-125">-ResourceGroupName</span></span>
<span data-ttu-id="42c91-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="42c91-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42c91-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="42c91-127">-ResourceId</span></span>
<span data-ttu-id="42c91-128">Örnek havuz kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="42c91-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42c91-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c91-129">CommonParameters</span></span>
<span data-ttu-id="42c91-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42c91-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c91-131">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42c91-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c91-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42c91-132">INPUTS</span></span>

### <span data-ttu-id="42c91-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="42c91-133">None</span></span>

## <span data-ttu-id="42c91-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42c91-134">OUTPUTS</span></span>

### <span data-ttu-id="42c91-135">Microsoft.Azure.Commands.Sql.Instance_Pools. model. azures, ınstancepoolmodel</span><span class="sxs-lookup"><span data-stu-id="42c91-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="42c91-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42c91-136">NOTES</span></span>

## <span data-ttu-id="42c91-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42c91-137">RELATED LINKS</span></span>
