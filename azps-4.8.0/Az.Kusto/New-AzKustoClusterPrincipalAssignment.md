---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273548"
---
# <span data-ttu-id="5f308-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f308-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="5f308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f308-102">SYNOPSIS</span></span>
<span data-ttu-id="5f308-103">Kusto küme principalAssignment oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5f308-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="5f308-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5f308-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5f308-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5f308-105">DESCRIPTION</span></span>
<span data-ttu-id="5f308-106">Kusto küme principalAssignment oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5f308-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="5f308-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5f308-107">EXAMPLES</span></span>

### <span data-ttu-id="5f308-108">Örnek 1: kusto kümesi oluşturma principalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f308-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="5f308-109">Yukarıdaki komut kusto kümesi oluşturur principalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f308-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="5f308-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5f308-110">PARAMETERS</span></span>

### <span data-ttu-id="5f308-111">-Iş</span><span class="sxs-lookup"><span data-stu-id="5f308-111">-AsJob</span></span>
<span data-ttu-id="5f308-112">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="5f308-112">Run the command as a job</span></span>

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

### <span data-ttu-id="5f308-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5f308-113">-ClusterName</span></span>
<span data-ttu-id="5f308-114">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="5f308-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5f308-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f308-115">-DefaultProfile</span></span>
<span data-ttu-id="5f308-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5f308-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f308-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5f308-117">-NoWait</span></span>
<span data-ttu-id="5f308-118">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="5f308-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5f308-119">-Princıpalassignmentname</span><span class="sxs-lookup"><span data-stu-id="5f308-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="5f308-120">Kusto principalAssignment adı.</span><span class="sxs-lookup"><span data-stu-id="5f308-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="5f308-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="5f308-121">-PrincipalId</span></span>
<span data-ttu-id="5f308-122">Küme sorumlusuna atanan sorumlu KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5f308-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="5f308-123">Bir kullanıcı e-postası, uygulama KIMLIĞI veya güvenlik grubu adı olabilir.</span><span class="sxs-lookup"><span data-stu-id="5f308-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="5f308-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="5f308-124">-PrincipalType</span></span>
<span data-ttu-id="5f308-125">Anapara türü.</span><span class="sxs-lookup"><span data-stu-id="5f308-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f308-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f308-126">-ResourceGroupName</span></span>
<span data-ttu-id="5f308-127">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5f308-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5f308-128">-Role</span><span class="sxs-lookup"><span data-stu-id="5f308-128">-Role</span></span>
<span data-ttu-id="5f308-129">Küme sorumlusu rolü.</span><span class="sxs-lookup"><span data-stu-id="5f308-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f308-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5f308-130">-SubscriptionId</span></span>
<span data-ttu-id="5f308-131">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="5f308-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5f308-132">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5f308-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5f308-133">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="5f308-133">-TenantId</span></span>
<span data-ttu-id="5f308-134">Anaparanın Kiracı kimliği</span><span class="sxs-lookup"><span data-stu-id="5f308-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="5f308-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="5f308-135">-Confirm</span></span>
<span data-ttu-id="5f308-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5f308-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f308-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f308-137">-WhatIf</span></span>
<span data-ttu-id="5f308-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5f308-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f308-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5f308-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f308-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f308-140">CommonParameters</span></span>
<span data-ttu-id="5f308-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5f308-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f308-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5f308-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f308-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5f308-143">INPUTS</span></span>

## <span data-ttu-id="5f308-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5f308-144">OUTPUTS</span></span>

### <span data-ttu-id="5f308-145">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="5f308-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="5f308-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5f308-146">NOTES</span></span>

<span data-ttu-id="5f308-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5f308-147">ALIASES</span></span>

## <span data-ttu-id="5f308-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5f308-148">RELATED LINKS</span></span>

