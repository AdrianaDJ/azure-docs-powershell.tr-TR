---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276669"
---
# <span data-ttu-id="f3c25-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="f3c25-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="f3c25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3c25-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c25-103">Azure SQL örnek havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3c25-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f3c25-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3c25-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c25-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3c25-105">DESCRIPTION</span></span>
<span data-ttu-id="f3c25-106">**New-Azsqlınstancepool** cmdlet 'ı BIR Azure SQL örnek havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3c25-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f3c25-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3c25-107">EXAMPLES</span></span>

### <span data-ttu-id="f3c25-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3c25-108">Example 1</span></span>
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

<span data-ttu-id="f3c25-109">Bu komut yeni bir Azure SQL örneği havuzu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f3c25-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="f3c25-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3c25-110">PARAMETERS</span></span>

### <span data-ttu-id="f3c25-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="f3c25-111">-AsJob</span></span>
<span data-ttu-id="f3c25-112">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="f3c25-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3c25-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="f3c25-113">-ComputeGeneration</span></span>
<span data-ttu-id="f3c25-114">Örnek havuzunun COMPUTE oluşturma işlemi.</span><span class="sxs-lookup"><span data-stu-id="f3c25-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="f3c25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c25-115">-DefaultProfile</span></span>
<span data-ttu-id="f3c25-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3c25-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c25-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="f3c25-117">-Edition</span></span>
<span data-ttu-id="f3c25-118">Örnek havuzunun sürümü.</span><span class="sxs-lookup"><span data-stu-id="f3c25-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="f3c25-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f3c25-119">-LicenseType</span></span>
<span data-ttu-id="f3c25-120">Hangi lisans türünün kullanılacağını belirler.</span><span class="sxs-lookup"><span data-stu-id="f3c25-120">Determines which License Type to use.</span></span>
<span data-ttu-id="f3c25-121">Olası değerler, temel fiyat (AHB indirimi olan) ve License(AHB indirimi olmadan).</span><span class="sxs-lookup"><span data-stu-id="f3c25-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="f3c25-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="f3c25-122">-Location</span></span>
<span data-ttu-id="f3c25-123">Örnek havuzunun oluşturulacağı konum.</span><span class="sxs-lookup"><span data-stu-id="f3c25-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="f3c25-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f3c25-124">-Name</span></span>
<span data-ttu-id="f3c25-125">Örnek havuzunun adı.</span><span class="sxs-lookup"><span data-stu-id="f3c25-125">The name of the instance pool.</span></span>

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

### <span data-ttu-id="f3c25-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c25-126">-ResourceGroupName</span></span>
<span data-ttu-id="f3c25-127">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f3c25-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3c25-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="f3c25-128">-SubnetId</span></span>
<span data-ttu-id="f3c25-129">Örnek havuzu oluşturulurken kullanılacak alt ağ kimliği.</span><span class="sxs-lookup"><span data-stu-id="f3c25-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="f3c25-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f3c25-130">-Tag</span></span>
<span data-ttu-id="f3c25-131">Örnekle ilişkilendirilecek Etiketler</span><span class="sxs-lookup"><span data-stu-id="f3c25-131">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="f3c25-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="f3c25-132">-VCore</span></span>
<span data-ttu-id="f3c25-133">Örnekle ne kadar Vçekirdeğin ilişkilendiyeceğini belirler.</span><span class="sxs-lookup"><span data-stu-id="f3c25-133">Determines how much VCore to associate with instance.</span></span>

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

### <span data-ttu-id="f3c25-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3c25-134">-Confirm</span></span>
<span data-ttu-id="f3c25-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3c25-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c25-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c25-136">-WhatIf</span></span>
<span data-ttu-id="f3c25-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3c25-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3c25-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3c25-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c25-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c25-139">CommonParameters</span></span>
<span data-ttu-id="f3c25-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3c25-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c25-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f3c25-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c25-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3c25-142">INPUTS</span></span>

### <span data-ttu-id="f3c25-143">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f3c25-143">None</span></span>

## <span data-ttu-id="f3c25-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3c25-144">OUTPUTS</span></span>

### <span data-ttu-id="f3c25-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="f3c25-145">System.Object</span></span>
## <span data-ttu-id="f3c25-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3c25-146">NOTES</span></span>

## <span data-ttu-id="f3c25-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3c25-147">RELATED LINKS</span></span>
