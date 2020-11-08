---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: 336360c3c7aac901ae90ea02f4832a066c6fff12
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278905"
---
# <span data-ttu-id="5d675-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="5d675-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="5d675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d675-102">SYNOPSIS</span></span>
<span data-ttu-id="5d675-103">Verilen sunucunun tüm çoğaltmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="5d675-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="5d675-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d675-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5d675-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d675-105">DESCRIPTION</span></span>
<span data-ttu-id="5d675-106">Verilen sunucunun tüm çoğaltmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="5d675-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="5d675-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d675-107">EXAMPLES</span></span>

### <span data-ttu-id="5d675-108">Örnek 1: bir Mari</span><span class="sxs-lookup"><span data-stu-id="5d675-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="5d675-109">Bu komut, bir MariaDB altındaki tüm çoğaltma VERITABANıNı listeler.</span><span class="sxs-lookup"><span data-stu-id="5d675-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="5d675-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d675-110">PARAMETERS</span></span>

### <span data-ttu-id="5d675-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d675-111">-DefaultProfile</span></span>
<span data-ttu-id="5d675-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d675-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d675-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d675-113">-ResourceGroupName</span></span>
<span data-ttu-id="5d675-114">Kaynağı içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5d675-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5d675-115">Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5d675-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5d675-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5d675-116">-ServerName</span></span>
<span data-ttu-id="5d675-117">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="5d675-117">The name of the server.</span></span>

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

### <span data-ttu-id="5d675-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="5d675-118">-SubscriptionId</span></span>
<span data-ttu-id="5d675-119">Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="5d675-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5d675-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d675-120">CommonParameters</span></span>
<span data-ttu-id="5d675-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d675-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d675-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5d675-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d675-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d675-123">INPUTS</span></span>

## <span data-ttu-id="5d675-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d675-124">OUTPUTS</span></span>

### <span data-ttu-id="5d675-125">Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="5d675-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5d675-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d675-126">NOTES</span></span>

<span data-ttu-id="5d675-127">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="5d675-127">ALIASES</span></span>

## <span data-ttu-id="5d675-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d675-128">RELATED LINKS</span></span>

