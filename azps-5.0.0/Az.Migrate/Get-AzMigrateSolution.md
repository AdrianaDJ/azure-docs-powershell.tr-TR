---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278871"
---
# <span data-ttu-id="e88c6-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="e88c6-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="e88c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e88c6-102">SYNOPSIS</span></span>
<span data-ttu-id="e88c6-103">Geçirme projesinde bir çözüm alır.</span><span class="sxs-lookup"><span data-stu-id="e88c6-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="e88c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e88c6-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e88c6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e88c6-105">DESCRIPTION</span></span>
<span data-ttu-id="e88c6-106">Geçirme projesinde bir çözüm alır.</span><span class="sxs-lookup"><span data-stu-id="e88c6-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="e88c6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e88c6-107">EXAMPLES</span></span>

### <span data-ttu-id="e88c6-108">Örnek 1: Get</span><span class="sxs-lookup"><span data-stu-id="e88c6-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="e88c6-109">Proje çözümünü ada göre geçirme.</span><span class="sxs-lookup"><span data-stu-id="e88c6-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="e88c6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e88c6-110">PARAMETERS</span></span>

### <span data-ttu-id="e88c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88c6-111">-DefaultProfile</span></span>
<span data-ttu-id="e88c6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e88c6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88c6-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="e88c6-113">-MigrateProjectName</span></span>
<span data-ttu-id="e88c6-114">Azure geçiş projesi adı.</span><span class="sxs-lookup"><span data-stu-id="e88c6-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="e88c6-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e88c6-115">-Name</span></span>
<span data-ttu-id="e88c6-116">Geçiş projesi içinde geçiş çözümünün benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="e88c6-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e88c6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88c6-117">-ResourceGroupName</span></span>
<span data-ttu-id="e88c6-118">Project 'in parçası olduğu Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e88c6-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="e88c6-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e88c6-119">-SubscriptionId</span></span>
<span data-ttu-id="e88c6-120">Yükseltme projesinin oluşturulduğu Azure abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="e88c6-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="e88c6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88c6-121">CommonParameters</span></span>
<span data-ttu-id="e88c6-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e88c6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88c6-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e88c6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88c6-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e88c6-124">INPUTS</span></span>

## <span data-ttu-id="e88c6-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e88c6-125">OUTPUTS</span></span>

### <span data-ttu-id="e88c6-126">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api20180901Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="e88c6-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="e88c6-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e88c6-127">NOTES</span></span>

<span data-ttu-id="e88c6-128">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e88c6-128">ALIASES</span></span>

## <span data-ttu-id="e88c6-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e88c6-129">RELATED LINKS</span></span>

