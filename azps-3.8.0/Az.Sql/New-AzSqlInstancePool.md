---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097942"
---
# <span data-ttu-id="5752d-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="5752d-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="5752d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5752d-102">SYNOPSIS</span></span>
<span data-ttu-id="5752d-103">Azure SQL örnek havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5752d-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="5752d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5752d-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5752d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5752d-105">DESCRIPTION</span></span>
<span data-ttu-id="5752d-106">**New-Azsqlınstancepool** cmdlet 'ı BIR Azure SQL örnek havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5752d-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="5752d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5752d-107">EXAMPLES</span></span>

### <span data-ttu-id="5752d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="5752d-108">Example 1</span></span>
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

<span data-ttu-id="5752d-109">Bu komut yeni bir Azure SQL örneği havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5752d-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="5752d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5752d-110">PARAMETERS</span></span>

### <span data-ttu-id="5752d-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="5752d-111">-AsJob</span></span>
<span data-ttu-id="5752d-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="5752d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5752d-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5752d-113">-ComputeGeneration</span></span>
<span data-ttu-id="5752d-114">Örnek havuzunun COMPUTE oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="5752d-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="5752d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5752d-115">-DefaultProfile</span></span>
<span data-ttu-id="5752d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5752d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5752d-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="5752d-117">-Edition</span></span>
<span data-ttu-id="5752d-118">Örnek havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="5752d-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="5752d-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5752d-119">-LicenseType</span></span>
<span data-ttu-id="5752d-120">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="5752d-120">Determines which License Type to use.</span></span>
<span data-ttu-id="5752d-121">Olası değerler, temel fiyat (AHB indirimi olan) ve License(AHB indirimi olmadan).</span><span class="sxs-lookup"><span data-stu-id="5752d-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="5752d-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="5752d-122">-Location</span></span>
<span data-ttu-id="5752d-123">Örnek havuzunun oluşturulacağı konum.</span><span class="sxs-lookup"><span data-stu-id="5752d-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="5752d-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="5752d-124">-Name</span></span>
<span data-ttu-id="5752d-125">Örnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="5752d-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="5752d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5752d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5752d-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5752d-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="5752d-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="5752d-128">-SubnetId</span></span>
<span data-ttu-id="5752d-129">Örnek havuzu oluşturulurken kullanılacak alt ağ kimliği.</span><span class="sxs-lookup"><span data-stu-id="5752d-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="5752d-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5752d-130">-Tag</span></span>
<span data-ttu-id="5752d-131">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="5752d-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="5752d-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="5752d-132">-VCore</span></span>
<span data-ttu-id="5752d-133">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="5752d-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="5752d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="5752d-134">-Confirm</span></span>
<span data-ttu-id="5752d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5752d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5752d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5752d-136">-WhatIf</span></span>
<span data-ttu-id="5752d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5752d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5752d-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5752d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5752d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5752d-139">CommonParameters</span></span>
<span data-ttu-id="5752d-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5752d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5752d-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5752d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5752d-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5752d-142">INPUTS</span></span>

### <span data-ttu-id="5752d-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="5752d-143">None</span></span>

## <span data-ttu-id="5752d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5752d-144">OUTPUTS</span></span>

### <span data-ttu-id="5752d-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="5752d-145">System.Object</span></span>
## <span data-ttu-id="5752d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5752d-146">NOTES</span></span>

## <span data-ttu-id="5752d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5752d-147">RELATED LINKS</span></span>
