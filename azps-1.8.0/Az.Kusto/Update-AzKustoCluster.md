---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Update-AzKustoCluster.md
ms.openlocfilehash: 890ec07cecd46badaccc1c2140290fd8042d319b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916127"
---
# <span data-ttu-id="3df80-101">Update-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3df80-101">Update-AzKustoCluster</span></span>

## <span data-ttu-id="3df80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3df80-102">SYNOPSIS</span></span>
<span data-ttu-id="3df80-103">Var olan bir kusto kümesini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="3df80-103">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="3df80-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3df80-104">SYNTAX</span></span>

### <span data-ttu-id="3df80-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3df80-105">ByNameAndResourceGroup (Default)</span></span>
```
Update-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>] [-Capacity <Int32>]
 [-Tier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df80-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="3df80-106">ByResourceId</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3df80-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3df80-107">ByInputObject</span></span>
```
Update-AzKustoCluster [-SkuName <String>] [-Capacity <Int32>] [-Tier <String>] [-InputObject] <PSKustoCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3df80-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3df80-108">DESCRIPTION</span></span>
<span data-ttu-id="3df80-109">Var olan bir kusto kümesini güncelleştirme.</span><span class="sxs-lookup"><span data-stu-id="3df80-109">Update an existing Kusto cluster.</span></span>

## <span data-ttu-id="3df80-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3df80-110">EXAMPLES</span></span>

### <span data-ttu-id="3df80-111">Örnek 1-varolan kümeyi adıyla güncelleyin</span><span class="sxs-lookup"><span data-stu-id="3df80-111">Example 1 - Update an existing cluster by name</span></span>

```
PS C:\> Update-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Sku D14_v2

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Sku               : D14_v2
Capacity          : 5
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="3df80-112">Yukarıdaki komut, "mykustocluster" kaynak grubunda bulunan "" kusto kümesinin katmanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3df80-112">The above command updates the tier of the Kusto cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="3df80-113">Örnek 2-varolan kümeyi boru ile güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3df80-113">Example 2 - Update an existing cluster by piping</span></span>

```
PS C:\> PS C:\> Get-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster | Update-AzKustoCluster -Sku D14_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D14_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster1.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster1.centralus.kusto.windows.net
```

<span data-ttu-id="3df80-114">Yukarıdaki komut, cmdlet 'i kullanarak "testrg" kaynak grubunda bulunan "mykustocluster" kusto kümesini alır `Get-AzKustoCluster` ve sonra da `Update-AzKustoCluster` kümenin katmanını "standart" olarak güncellemesine yol gösterir.</span><span class="sxs-lookup"><span data-stu-id="3df80-114">The above command gets the Kusto cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoCluster` cmdlet, and then pipes the result to `Update-AzKustoCluster` to update the cluster's tier to "standard".</span></span>

## <span data-ttu-id="3df80-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3df80-115">PARAMETERS</span></span>

### <span data-ttu-id="3df80-116">-Kapasite</span><span class="sxs-lookup"><span data-stu-id="3df80-116">-Capacity</span></span>
<span data-ttu-id="3df80-117">VM 'nin örnek numarası.</span><span class="sxs-lookup"><span data-stu-id="3df80-117">The instance number of the VM.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df80-118">-DefaultProfile</span></span>
<span data-ttu-id="3df80-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3df80-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df80-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3df80-120">-InputObject</span></span>
<span data-ttu-id="3df80-121">Kusto küme nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3df80-121">Kusto cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3df80-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="3df80-122">-Name</span></span>
<span data-ttu-id="3df80-123">Güncelleştirilecek kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="3df80-123">Name of cluster to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df80-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df80-124">-ResourceGroupName</span></span>
<span data-ttu-id="3df80-125">Kümenin bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="3df80-125">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3df80-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3df80-126">-ResourceId</span></span>
<span data-ttu-id="3df80-127">Kusto küme RESOURCEID.</span><span class="sxs-lookup"><span data-stu-id="3df80-127">Kusto cluster ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3df80-128">-SkuName</span><span class="sxs-lookup"><span data-stu-id="3df80-128">-SkuName</span></span>
<span data-ttu-id="3df80-129">Kümeyi oluşturmak için kullanılan SKU adı</span><span class="sxs-lookup"><span data-stu-id="3df80-129">Name of the Sku used to create the cluster</span></span>

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

### <span data-ttu-id="3df80-130">Katmanlı</span><span class="sxs-lookup"><span data-stu-id="3df80-130">-Tier</span></span>
<span data-ttu-id="3df80-131">Kümeyi oluşturmak için kullanılan katmanın adı</span><span class="sxs-lookup"><span data-stu-id="3df80-131">Name of the Tier used to create the cluster</span></span>

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

### <span data-ttu-id="3df80-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="3df80-132">-Confirm</span></span>
<span data-ttu-id="3df80-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3df80-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3df80-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3df80-134">-WhatIf</span></span>
<span data-ttu-id="3df80-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3df80-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3df80-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3df80-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3df80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df80-137">CommonParameters</span></span>
<span data-ttu-id="3df80-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3df80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df80-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3df80-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df80-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3df80-140">INPUTS</span></span>

### <span data-ttu-id="3df80-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3df80-141">System.String</span></span>

### <span data-ttu-id="3df80-142">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3df80-142">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="3df80-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3df80-143">OUTPUTS</span></span>

### <span data-ttu-id="3df80-144">Microsoft. Azure. Commands. kusto. modeller. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="3df80-144">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="3df80-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3df80-145">NOTES</span></span>

## <span data-ttu-id="3df80-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3df80-146">RELATED LINKS</span></span>
