---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109965"
---
# <span data-ttu-id="e657f-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="e657f-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="e657f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e657f-102">SYNOPSIS</span></span>
<span data-ttu-id="e657f-103">Verilen kusto kümesi ve veritabanının veritabanı sorumluları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e657f-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="e657f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e657f-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e657f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e657f-105">DESCRIPTION</span></span>
<span data-ttu-id="e657f-106">Verilen kusto kümesi ve veritabanının veritabanı sorumluları listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e657f-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="e657f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e657f-107">EXAMPLES</span></span>

### <span data-ttu-id="e657f-108">Örnek 1: verilen kusto kümesi ve veritabanının veritabanı sorumlularının listesi</span><span class="sxs-lookup"><span data-stu-id="e657f-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="e657f-109">Yukarıdaki komut, verilen kusto kümesi ve veritabanının veritabanı sorumlularının listesini döndürür</span><span class="sxs-lookup"><span data-stu-id="e657f-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="e657f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e657f-110">PARAMETERS</span></span>

### <span data-ttu-id="e657f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e657f-111">-ClusterName</span></span>
<span data-ttu-id="e657f-112">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="e657f-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e657f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e657f-113">-DatabaseName</span></span>
<span data-ttu-id="e657f-114">Kusto kümesindeki veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="e657f-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="e657f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e657f-115">-DefaultProfile</span></span>
<span data-ttu-id="e657f-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e657f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e657f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e657f-117">-ResourceGroupName</span></span>
<span data-ttu-id="e657f-118">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e657f-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e657f-119">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="e657f-119">-SubscriptionId</span></span>
<span data-ttu-id="e657f-120">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e657f-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e657f-121">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e657f-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e657f-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e657f-122">-Confirm</span></span>
<span data-ttu-id="e657f-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e657f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e657f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e657f-124">-WhatIf</span></span>
<span data-ttu-id="e657f-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e657f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e657f-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e657f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e657f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e657f-127">CommonParameters</span></span>
<span data-ttu-id="e657f-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e657f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e657f-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e657f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e657f-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e657f-130">INPUTS</span></span>

## <span data-ttu-id="e657f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e657f-131">OUTPUTS</span></span>

### <span data-ttu-id="e657f-132">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="e657f-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="e657f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e657f-133">NOTES</span></span>

<span data-ttu-id="e657f-134">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="e657f-134">ALIASES</span></span>

## <span data-ttu-id="e657f-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e657f-135">RELATED LINKS</span></span>

