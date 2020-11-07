---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938007"
---
# <span data-ttu-id="aac87-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="aac87-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="aac87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aac87-102">SYNOPSIS</span></span>
<span data-ttu-id="aac87-103">Azure SQL örnek havuzunun özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aac87-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="aac87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aac87-104">SYNTAX</span></span>

### <span data-ttu-id="aac87-105">Defaultsetınstancepoolparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aac87-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aac87-106">Inputobjectsetınstancepoolparameterset</span><span class="sxs-lookup"><span data-stu-id="aac87-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aac87-107">Resourceıdsetınstancepoolparameterset</span><span class="sxs-lookup"><span data-stu-id="aac87-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aac87-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="aac87-108">DESCRIPTION</span></span>
<span data-ttu-id="aac87-109">**Set-Azsqlınstancepool** cmdlet 'ı BIR Azure SQL örnek havuzunun özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="aac87-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="aac87-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aac87-110">EXAMPLES</span></span>

### <span data-ttu-id="aac87-111">Örnek 1: örnek havuz lisans türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="aac87-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
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

<span data-ttu-id="aac87-112">Bu komut, instancePool0 adındaki bir örnek havuzunun lisans türü ve/veya etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aac87-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="aac87-113">Örnek 2: örnek havuz nesnesini kullanarak bir örnek havuzu lisans türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="aac87-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
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

<span data-ttu-id="aac87-114">Bu komut, örnek havuz nesnesi kullanarak bir örnek havuzunun lisans türü ve/veya etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aac87-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="aac87-115">Örnek 3: örnek havuz kaynak kimliği kullanarak örnek havuzu lisans türünü ayarlama</span><span class="sxs-lookup"><span data-stu-id="aac87-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
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

<span data-ttu-id="aac87-116">Bu komut, instancePool0 adındaki bir örnek havuzunun lisans türü ve/veya etiketlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="aac87-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="aac87-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aac87-117">PARAMETERS</span></span>

### <span data-ttu-id="aac87-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="aac87-118">-AsJob</span></span>
<span data-ttu-id="aac87-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="aac87-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aac87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aac87-120">-DefaultProfile</span></span>
<span data-ttu-id="aac87-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aac87-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aac87-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aac87-122">-InputObject</span></span>
<span data-ttu-id="aac87-123">Örnek havuz giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="aac87-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aac87-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="aac87-124">-LicenseType</span></span>
<span data-ttu-id="aac87-125">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="aac87-125">Determines which License Type to use.</span></span>
<span data-ttu-id="aac87-126">Olası değerler, temel fiyat (AHB indirimi olan) ve License(AHB indirimi olmadan).</span><span class="sxs-lookup"><span data-stu-id="aac87-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="aac87-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="aac87-127">-Name</span></span>
<span data-ttu-id="aac87-128">Örnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="aac87-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac87-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aac87-129">-ResourceGroupName</span></span>
<span data-ttu-id="aac87-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="aac87-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac87-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="aac87-131">-ResourceId</span></span>
<span data-ttu-id="aac87-132">Örnek havuz kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="aac87-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aac87-133">Etiketli</span><span class="sxs-lookup"><span data-stu-id="aac87-133">-Tag</span></span>
<span data-ttu-id="aac87-134">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="aac87-134">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aac87-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="aac87-135">-Confirm</span></span>
<span data-ttu-id="aac87-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aac87-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aac87-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aac87-137">-WhatIf</span></span>
<span data-ttu-id="aac87-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aac87-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aac87-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aac87-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aac87-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aac87-140">CommonParameters</span></span>
<span data-ttu-id="aac87-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aac87-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aac87-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aac87-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aac87-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aac87-143">INPUTS</span></span>

### <span data-ttu-id="aac87-144">Microsoft.Azure.Commands.Sql.Instance_Pools. model. azures, ınstancepoolmodel</span><span class="sxs-lookup"><span data-stu-id="aac87-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="aac87-145">System. String</span><span class="sxs-lookup"><span data-stu-id="aac87-145">System.String</span></span>

## <span data-ttu-id="aac87-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aac87-146">OUTPUTS</span></span>

### <span data-ttu-id="aac87-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="aac87-147">System.Object</span></span>
## <span data-ttu-id="aac87-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aac87-148">NOTES</span></span>

## <span data-ttu-id="aac87-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aac87-149">RELATED LINKS</span></span>
