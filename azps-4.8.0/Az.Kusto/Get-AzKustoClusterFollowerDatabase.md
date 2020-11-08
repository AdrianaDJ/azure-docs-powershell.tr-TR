---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109970"
---
# <span data-ttu-id="cec90-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="cec90-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="cec90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cec90-102">SYNOPSIS</span></span>
<span data-ttu-id="cec90-103">Bu kümenin sahip olduğu veritabanlarının listesini ve ardından başka bir kümeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="cec90-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="cec90-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cec90-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cec90-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cec90-105">DESCRIPTION</span></span>
<span data-ttu-id="cec90-106">Bu kümenin sahip olduğu veritabanlarının listesini ve ardından başka bir kümeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="cec90-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="cec90-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cec90-107">EXAMPLES</span></span>

### <span data-ttu-id="cec90-108">Örnek 1: tüm izlenen veritabanlarını listeler</span><span class="sxs-lookup"><span data-stu-id="cec90-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="cec90-109">Yukarıdaki komut, bu kümenin sahip olduğu tüm veritabanlarını ve ardından başka bir kümeyi listeler.</span><span class="sxs-lookup"><span data-stu-id="cec90-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="cec90-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cec90-110">PARAMETERS</span></span>

### <span data-ttu-id="cec90-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cec90-111">-ClusterName</span></span>
<span data-ttu-id="cec90-112">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="cec90-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="cec90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec90-113">-DefaultProfile</span></span>
<span data-ttu-id="cec90-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cec90-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cec90-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cec90-115">-ResourceGroupName</span></span>
<span data-ttu-id="cec90-116">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="cec90-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="cec90-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="cec90-117">-SubscriptionId</span></span>
<span data-ttu-id="cec90-118">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="cec90-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cec90-119">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="cec90-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cec90-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="cec90-120">-Confirm</span></span>
<span data-ttu-id="cec90-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cec90-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cec90-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cec90-122">-WhatIf</span></span>
<span data-ttu-id="cec90-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cec90-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cec90-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cec90-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cec90-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec90-125">CommonParameters</span></span>
<span data-ttu-id="cec90-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cec90-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec90-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cec90-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec90-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cec90-128">INPUTS</span></span>

## <span data-ttu-id="cec90-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cec90-129">OUTPUTS</span></span>

### <span data-ttu-id="cec90-130">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıfolaldatabasedatabasedefinition</span><span class="sxs-lookup"><span data-stu-id="cec90-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="cec90-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cec90-131">NOTES</span></span>

<span data-ttu-id="cec90-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="cec90-132">ALIASES</span></span>

## <span data-ttu-id="cec90-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cec90-133">RELATED LINKS</span></span>

