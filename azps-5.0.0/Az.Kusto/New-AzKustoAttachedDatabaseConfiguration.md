---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278998"
---
# <span data-ttu-id="64b4f-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="64b4f-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="64b4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64b4f-102">SYNOPSIS</span></span>
<span data-ttu-id="64b4f-103">Eklenmiş veritabanı yapılandırmasını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="64b4f-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="64b4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="64b4f-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="64b4f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="64b4f-105">DESCRIPTION</span></span>
<span data-ttu-id="64b4f-106">Eklenmiş veritabanı yapılandırmasını oluşturur veya güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="64b4f-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="64b4f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="64b4f-107">EXAMPLES</span></span>

### <span data-ttu-id="64b4f-108">Örnek 1: yeni bir AttachedDatabaseConfiguration oluşturma</span><span class="sxs-lookup"><span data-stu-id="64b4f-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="64b4f-109">Yukarıdaki komut "testnewkustoclusterf" kümesinde "mykustodatabase" salt okunur bir veritabanı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="64b4f-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="64b4f-110">"Mykustodatabase" kümesinden "testnewkustocluster" veritabanı</span><span class="sxs-lookup"><span data-stu-id="64b4f-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="64b4f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="64b4f-111">PARAMETERS</span></span>

### <span data-ttu-id="64b4f-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="64b4f-112">-AsJob</span></span>
<span data-ttu-id="64b4f-113">Komutu iş olarak çalıştırmak</span><span class="sxs-lookup"><span data-stu-id="64b4f-113">Run the command as a job</span></span>

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

### <span data-ttu-id="64b4f-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="64b4f-114">-ClusterName</span></span>
<span data-ttu-id="64b4f-115">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="64b4f-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="64b4f-116">-Clusterresourceıd</span><span class="sxs-lookup"><span data-stu-id="64b4f-116">-ClusterResourceId</span></span>
<span data-ttu-id="64b4f-117">İliştirmek istediğiniz veritabanlarının bulunduğu kümenin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="64b4f-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="64b4f-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64b4f-118">-DatabaseName</span></span>
<span data-ttu-id="64b4f-119">Eklemek istediğiniz veritabanının adı tüm geçerli ve gelecekteki veritabanlarını izlemek istiyorsanız \* kullanın.</span><span class="sxs-lookup"><span data-stu-id="64b4f-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="64b4f-120">-Defaultsprincipalsmodificationkind</span><span class="sxs-lookup"><span data-stu-id="64b4f-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="64b4f-121">Varsayılan asıl öğe değiştirme türü</span><span class="sxs-lookup"><span data-stu-id="64b4f-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b4f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64b4f-122">-DefaultProfile</span></span>
<span data-ttu-id="64b4f-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="64b4f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64b4f-124">-Konum</span><span class="sxs-lookup"><span data-stu-id="64b4f-124">-Location</span></span>
<span data-ttu-id="64b4f-125">Kaynak konumu.</span><span class="sxs-lookup"><span data-stu-id="64b4f-125">Resource location.</span></span>

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

### <span data-ttu-id="64b4f-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="64b4f-126">-Name</span></span>
<span data-ttu-id="64b4f-127">Ekli veritabanı yapılandırmasının adı.</span><span class="sxs-lookup"><span data-stu-id="64b4f-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64b4f-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="64b4f-128">-NoWait</span></span>
<span data-ttu-id="64b4f-129">Komutu zaman uyumsuz olarak çalıştırır</span><span class="sxs-lookup"><span data-stu-id="64b4f-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="64b4f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64b4f-130">-ResourceGroupName</span></span>
<span data-ttu-id="64b4f-131">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="64b4f-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="64b4f-132">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="64b4f-132">-SubscriptionId</span></span>
<span data-ttu-id="64b4f-133">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="64b4f-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="64b4f-134">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="64b4f-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="64b4f-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="64b4f-135">-Confirm</span></span>
<span data-ttu-id="64b4f-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="64b4f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64b4f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64b4f-137">-WhatIf</span></span>
<span data-ttu-id="64b4f-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="64b4f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64b4f-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="64b4f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64b4f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64b4f-140">CommonParameters</span></span>
<span data-ttu-id="64b4f-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="64b4f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64b4f-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="64b4f-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64b4f-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="64b4f-143">INPUTS</span></span>

## <span data-ttu-id="64b4f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="64b4f-144">OUTPUTS</span></span>

### <span data-ttu-id="64b4f-145">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıattacheddatabaseconfiguration</span><span class="sxs-lookup"><span data-stu-id="64b4f-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="64b4f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="64b4f-146">NOTES</span></span>

<span data-ttu-id="64b4f-147">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="64b4f-147">ALIASES</span></span>

## <span data-ttu-id="64b4f-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="64b4f-148">RELATED LINKS</span></span>

