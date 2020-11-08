---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: dc0b4ea1616c916edacaf4d5a4a2b431e7f7d113
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278992"
---
# <span data-ttu-id="628c1-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="628c1-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="628c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="628c1-102">SYNOPSIS</span></span>
<span data-ttu-id="628c1-103">Veritabanı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="628c1-103">Creates or updates a database.</span></span>

## <span data-ttu-id="628c1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="628c1-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="628c1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="628c1-105">DESCRIPTION</span></span>
<span data-ttu-id="628c1-106">Veritabanı oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="628c1-106">Creates or updates a database.</span></span>

## <span data-ttu-id="628c1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="628c1-107">EXAMPLES</span></span>

### <span data-ttu-id="628c1-108">Örnek 1: adla yeni bir kusto veritabanı oluşturma</span><span class="sxs-lookup"><span data-stu-id="628c1-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="628c1-109">Yukarıdaki komut, "mykustodatabase" adlı yeni bir kusto veritabanını, "testrg" kaynak grubunda bulunan "testnewkustocluster" adında oluşturur.</span><span class="sxs-lookup"><span data-stu-id="628c1-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="628c1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="628c1-110">PARAMETERS</span></span>

### <span data-ttu-id="628c1-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="628c1-111">-AsJob</span></span>
<span data-ttu-id="628c1-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="628c1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="628c1-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="628c1-113">-ClusterName</span></span>
<span data-ttu-id="628c1-114">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="628c1-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="628c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="628c1-115">-DefaultProfile</span></span>
<span data-ttu-id="628c1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="628c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="628c1-117">-Hotcachedönem</span><span class="sxs-lookup"><span data-stu-id="628c1-117">-HotCachePeriod</span></span>
<span data-ttu-id="628c1-118">Verilerin TimeSpan 'teki hızlı sorgular için önbellekte tutulması gereken süre.</span><span class="sxs-lookup"><span data-stu-id="628c1-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-119">-Tür</span><span class="sxs-lookup"><span data-stu-id="628c1-119">-Kind</span></span>
<span data-ttu-id="628c1-120">Veritabanı türü</span><span class="sxs-lookup"><span data-stu-id="628c1-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="628c1-121">-Location</span></span>
<span data-ttu-id="628c1-122">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="628c1-122">Resource location.</span></span>

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

### <span data-ttu-id="628c1-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="628c1-123">-Name</span></span>
<span data-ttu-id="628c1-124">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="628c1-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="628c1-125">-NoWait</span></span>
<span data-ttu-id="628c1-126">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="628c1-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="628c1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="628c1-127">-ResourceGroupName</span></span>
<span data-ttu-id="628c1-128">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="628c1-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="628c1-129">-Softdeletedönem</span><span class="sxs-lookup"><span data-stu-id="628c1-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="628c1-130">Verilerin TimeSpan 'teki sorguların erişimini durdurmadan önce tutulacağı süre.</span><span class="sxs-lookup"><span data-stu-id="628c1-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-131">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="628c1-131">-SubscriptionId</span></span>
<span data-ttu-id="628c1-132">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="628c1-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="628c1-133">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="628c1-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="628c1-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="628c1-134">-Confirm</span></span>
<span data-ttu-id="628c1-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="628c1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="628c1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="628c1-136">-WhatIf</span></span>
<span data-ttu-id="628c1-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="628c1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="628c1-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="628c1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="628c1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="628c1-139">CommonParameters</span></span>
<span data-ttu-id="628c1-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="628c1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="628c1-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="628c1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="628c1-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="628c1-142">INPUTS</span></span>

## <span data-ttu-id="628c1-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="628c1-143">OUTPUTS</span></span>

### <span data-ttu-id="628c1-144">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="628c1-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="628c1-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="628c1-145">NOTES</span></span>

<span data-ttu-id="628c1-146">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="628c1-146">ALIASES</span></span>

## <span data-ttu-id="628c1-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="628c1-147">RELATED LINKS</span></span>

