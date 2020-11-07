---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: d65e32992b113dfb587b68dd3fcdc1701b291ad4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933837"
---
# <span data-ttu-id="ffcbb-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="ffcbb-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="ffcbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffcbb-102">SYNOPSIS</span></span>
<span data-ttu-id="ffcbb-103">Azure SQL örnek havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ffcbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ffcbb-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffcbb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ffcbb-105">DESCRIPTION</span></span>
<span data-ttu-id="ffcbb-106">**New-Azsqlınstancepool** cmdlet 'ı BIR Azure SQL örnek havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ffcbb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ffcbb-107">EXAMPLES</span></span>

### <span data-ttu-id="ffcbb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ffcbb-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
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

<span data-ttu-id="ffcbb-109">Bu komut yeni bir Azure SQL örneği havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ffcbb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ffcbb-110">PARAMETERS</span></span>

### <span data-ttu-id="ffcbb-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="ffcbb-111">-AsJob</span></span>
<span data-ttu-id="ffcbb-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ffcbb-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffcbb-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ffcbb-113">-ComputeGeneration</span></span>
<span data-ttu-id="ffcbb-114">Örnek havuzunun COMPUTE oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="ffcbb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffcbb-115">-DefaultProfile</span></span>
<span data-ttu-id="ffcbb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffcbb-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="ffcbb-117">-Edition</span></span>
<span data-ttu-id="ffcbb-118">Örnek havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="ffcbb-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ffcbb-119">-LicenseType</span></span>
<span data-ttu-id="ffcbb-120">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-120">Determines which License Type to use.</span></span>
<span data-ttu-id="ffcbb-121">Olası değerler, temel fiyat (AHB indirimi olan) ve License(AHB indirimi olmadan).</span><span class="sxs-lookup"><span data-stu-id="ffcbb-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="ffcbb-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="ffcbb-122">-Location</span></span>
<span data-ttu-id="ffcbb-123">Örnek havuzunun oluşturulacağı konum.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="ffcbb-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="ffcbb-124">-Name</span></span>
<span data-ttu-id="ffcbb-125">Örnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcbb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffcbb-126">-ResourceGroupName</span></span>
<span data-ttu-id="ffcbb-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcbb-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ffcbb-128">-SubnetId</span></span>
<span data-ttu-id="ffcbb-129">Örnek havuzu oluşturulurken kullanılacak alt ağ kimliği.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="ffcbb-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="ffcbb-130">-Tag</span></span>
<span data-ttu-id="ffcbb-131">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="ffcbb-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="ffcbb-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="ffcbb-132">-VCore</span></span>
<span data-ttu-id="ffcbb-133">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffcbb-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="ffcbb-134">-Confirm</span></span>
<span data-ttu-id="ffcbb-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffcbb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffcbb-136">-WhatIf</span></span>
<span data-ttu-id="ffcbb-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffcbb-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffcbb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffcbb-139">CommonParameters</span></span>
<span data-ttu-id="ffcbb-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffcbb-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ffcbb-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffcbb-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ffcbb-142">INPUTS</span></span>

### <span data-ttu-id="ffcbb-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ffcbb-143">None</span></span>

## <span data-ttu-id="ffcbb-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ffcbb-144">OUTPUTS</span></span>

### <span data-ttu-id="ffcbb-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="ffcbb-145">System.Object</span></span>
## <span data-ttu-id="ffcbb-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ffcbb-146">NOTES</span></span>

## <span data-ttu-id="ffcbb-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ffcbb-147">RELATED LINKS</span></span>
