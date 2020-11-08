---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280070"
---
# <span data-ttu-id="22cd2-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="22cd2-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="22cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="22cd2-103">Proje geçirme yöntemi.</span><span class="sxs-lookup"><span data-stu-id="22cd2-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="22cd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22cd2-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="22cd2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22cd2-105">DESCRIPTION</span></span>
<span data-ttu-id="22cd2-106">Proje geçirme yöntemi.</span><span class="sxs-lookup"><span data-stu-id="22cd2-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="22cd2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22cd2-107">EXAMPLES</span></span>

### <span data-ttu-id="22cd2-108">Örnek 1: Get</span><span class="sxs-lookup"><span data-stu-id="22cd2-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="22cd2-109">Proje geçirme yöntemi.</span><span class="sxs-lookup"><span data-stu-id="22cd2-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="22cd2-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22cd2-110">PARAMETERS</span></span>

### <span data-ttu-id="22cd2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cd2-111">-DefaultProfile</span></span>
<span data-ttu-id="22cd2-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22cd2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cd2-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="22cd2-113">-Name</span></span>
<span data-ttu-id="22cd2-114">Azure geçiş projesi adı.</span><span class="sxs-lookup"><span data-stu-id="22cd2-114">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22cd2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cd2-115">-ResourceGroupName</span></span>
<span data-ttu-id="22cd2-116">Project 'in parçası olduğu Azure Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="22cd2-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="22cd2-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="22cd2-117">-SubscriptionId</span></span>
<span data-ttu-id="22cd2-118">Yükseltme projesinin oluşturulduğu Azure abonelik kimliği.</span><span class="sxs-lookup"><span data-stu-id="22cd2-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="22cd2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cd2-119">CommonParameters</span></span>
<span data-ttu-id="22cd2-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22cd2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cd2-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="22cd2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cd2-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22cd2-122">INPUTS</span></span>

## <span data-ttu-id="22cd2-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22cd2-123">OUTPUTS</span></span>

### <span data-ttu-id="22cd2-124">Microsoft. Azure. PowerShell. cmdlet. Api20180901Preview.</span><span class="sxs-lookup"><span data-stu-id="22cd2-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="22cd2-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22cd2-125">NOTES</span></span>

<span data-ttu-id="22cd2-126">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="22cd2-126">ALIASES</span></span>

## <span data-ttu-id="22cd2-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22cd2-127">RELATED LINKS</span></span>

