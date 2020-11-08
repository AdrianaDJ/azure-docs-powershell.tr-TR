---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigraterunasaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateRunAsAccount.md
ms.openlocfilehash: 6f78a326efc29e3ba89f774575df1c4b7472e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278877"
---
# <span data-ttu-id="0e5ad-101">Get-AzMigrateRunAsAccount</span><span class="sxs-lookup"><span data-stu-id="0e5ad-101">Get-AzMigrateRunAsAccount</span></span>

## <span data-ttu-id="0e5ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5ad-103">Farklı Run as hesabı.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-103">Method to get run as account.</span></span>

## <span data-ttu-id="0e5ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0e5ad-104">SYNTAX</span></span>

### <span data-ttu-id="0e5ad-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0e5ad-105">List (Default)</span></span>
```
Get-AzMigrateRunAsAccount -ResourceGroupName <String> -SiteName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0e5ad-106">Al</span><span class="sxs-lookup"><span data-stu-id="0e5ad-106">Get</span></span>
```
Get-AzMigrateRunAsAccount -AccountName <String> -ResourceGroupName <String> -SiteName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0e5ad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0e5ad-107">DESCRIPTION</span></span>
<span data-ttu-id="0e5ad-108">Farklı Run as hesabı.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-108">Method to get run as account.</span></span>

## <span data-ttu-id="0e5ad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0e5ad-109">EXAMPLES</span></span>

### <span data-ttu-id="0e5ad-110">Örnek 1: liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0e5ad-110">Example 1: List (Default)</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="0e5ad-111">Sitedeki tüm farklı çalışma hesapları listesini listeleyin.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-111">List all run as accounts in a site.</span></span>

### <span data-ttu-id="0e5ad-112">Örnek 2: Get</span><span class="sxs-lookup"><span data-stu-id="0e5ad-112">Example 2: Get</span></span>
```powershell
PS C:\> Get-AzMigrateRunAsAccount  -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -SiteName BBVMwareAVScbbcsite -AccountName b090bef3-b733-5e34-bc8f-eb6f2701432a

Name                                 Type
----                                 ----
b090bef3-b733-5e34-bc8f-eb6f2701432a Microsoft.OffAzure/VMwareSites/runasaccounts
```

<span data-ttu-id="0e5ad-113">Ada göre farklı farklı hesapla hesabı alın.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-113">Get Run as account by name.</span></span>

## <span data-ttu-id="0e5ad-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0e5ad-114">PARAMETERS</span></span>

### <span data-ttu-id="0e5ad-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0e5ad-115">-AccountName</span></span>
<span data-ttu-id="0e5ad-116">Farklı bir hesap kolu adı.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-116">Run as account ARM name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5ad-117">-DefaultProfile</span></span>
<span data-ttu-id="0e5ad-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e5ad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e5ad-119">-ResourceGroupName</span></span>
<span data-ttu-id="0e5ad-120">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-120">The name of the resource group.</span></span>
<span data-ttu-id="0e5ad-121">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-121">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0e5ad-122">-SiteName</span><span class="sxs-lookup"><span data-stu-id="0e5ad-122">-SiteName</span></span>
<span data-ttu-id="0e5ad-123">Site adı.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-123">Site name.</span></span>

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

### <span data-ttu-id="0e5ad-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0e5ad-124">-SubscriptionId</span></span>
<span data-ttu-id="0e5ad-125">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0e5ad-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5ad-126">CommonParameters</span></span>
<span data-ttu-id="0e5ad-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5ad-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0e5ad-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5ad-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0e5ad-129">INPUTS</span></span>

## <span data-ttu-id="0e5ad-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0e5ad-130">OUTPUTS</span></span>

### <span data-ttu-id="0e5ad-131">Microsoft. Azure. PowerShell. cmdlet. geçir. modeller. Api202001. ıvmwarerunaşama ccount</span><span class="sxs-lookup"><span data-stu-id="0e5ad-131">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api202001.IVMwareRunAsAccount</span></span>

## <span data-ttu-id="0e5ad-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0e5ad-132">NOTES</span></span>

<span data-ttu-id="0e5ad-133">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0e5ad-133">ALIASES</span></span>

## <span data-ttu-id="0e5ad-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0e5ad-134">RELATED LINKS</span></span>

