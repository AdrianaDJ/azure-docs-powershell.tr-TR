---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSite.md
ms.openlocfilehash: ebea7936483a34d2515c69c416146d07651b396b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278874"
---
# <span data-ttu-id="0be7a-101">Get-AzMigrateSite</span><span class="sxs-lookup"><span data-stu-id="0be7a-101">Get-AzMigrateSite</span></span>

## <span data-ttu-id="0be7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0be7a-102">SYNOPSIS</span></span>
<span data-ttu-id="0be7a-103">Site alma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="0be7a-103">Method to get a site.</span></span>

## <span data-ttu-id="0be7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0be7a-104">SYNTAX</span></span>

```
Get-AzMigrateSite -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0be7a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0be7a-105">DESCRIPTION</span></span>
<span data-ttu-id="0be7a-106">Site alma yöntemi.</span><span class="sxs-lookup"><span data-stu-id="0be7a-106">Method to get a site.</span></span>

## <span data-ttu-id="0be7a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0be7a-107">EXAMPLES</span></span>

### <span data-ttu-id="0be7a-108">Örnek 1: get (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0be7a-108">Example 1: Get (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateSite -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

ETag Location      Name                Type
---- --------      ----                ----
     southeastasia BBVMwareAVScbbcsite Microsoft.OffAzure/VMwareSites

```

<span data-ttu-id="0be7a-109">Siteyi ada göre alma</span><span class="sxs-lookup"><span data-stu-id="0be7a-109">Get site by name</span></span>

## <span data-ttu-id="0be7a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0be7a-110">PARAMETERS</span></span>

### <span data-ttu-id="0be7a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0be7a-111">-DefaultProfile</span></span>
<span data-ttu-id="0be7a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0be7a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0be7a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="0be7a-113">-Name</span></span>
<span data-ttu-id="0be7a-114">Site adı.</span><span class="sxs-lookup"><span data-stu-id="0be7a-114">Site name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0be7a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0be7a-115">-ResourceGroupName</span></span>
<span data-ttu-id="0be7a-116">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0be7a-116">The name of the resource group.</span></span>
<span data-ttu-id="0be7a-117">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0be7a-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0be7a-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0be7a-118">-SubscriptionId</span></span>
<span data-ttu-id="0be7a-119">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0be7a-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0be7a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0be7a-120">CommonParameters</span></span>
<span data-ttu-id="0be7a-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0be7a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0be7a-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0be7a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0be7a-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0be7a-123">INPUTS</span></span>

## <span data-ttu-id="0be7a-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0be7a-124">OUTPUTS</span></span>

### <span data-ttu-id="0be7a-125">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api202001. ıvmwaresite</span><span class="sxs-lookup"><span data-stu-id="0be7a-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareSite</span></span>

## <span data-ttu-id="0be7a-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0be7a-126">NOTES</span></span>

<span data-ttu-id="0be7a-127">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0be7a-127">ALIASES</span></span>

## <span data-ttu-id="0be7a-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0be7a-128">RELATED LINKS</span></span>

