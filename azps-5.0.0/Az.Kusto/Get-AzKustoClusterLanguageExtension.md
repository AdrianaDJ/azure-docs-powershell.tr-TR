---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279018"
---
# <span data-ttu-id="b283e-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="b283e-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="b283e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b283e-102">SYNOPSIS</span></span>
<span data-ttu-id="b283e-103">KQL sorgularında çalıştırılabilecek dil uzantılarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b283e-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b283e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b283e-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b283e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b283e-105">DESCRIPTION</span></span>
<span data-ttu-id="b283e-106">KQL sorgularında çalıştırılabilecek dil uzantılarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b283e-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b283e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b283e-107">EXAMPLES</span></span>

### <span data-ttu-id="b283e-108">Örnek 1: kümenin tüm dil uzantılarını listeleme</span><span class="sxs-lookup"><span data-stu-id="b283e-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="b283e-109">Yukarıdaki komut, KQL sorgularında çalıştırılabilecek dil uzantılarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b283e-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="b283e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b283e-110">PARAMETERS</span></span>

### <span data-ttu-id="b283e-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b283e-111">-ClusterName</span></span>
<span data-ttu-id="b283e-112">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="b283e-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="b283e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b283e-113">-DefaultProfile</span></span>
<span data-ttu-id="b283e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b283e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b283e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b283e-115">-ResourceGroupName</span></span>
<span data-ttu-id="b283e-116">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="b283e-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="b283e-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b283e-117">-SubscriptionId</span></span>
<span data-ttu-id="b283e-118">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="b283e-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b283e-119">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="b283e-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b283e-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="b283e-120">-Confirm</span></span>
<span data-ttu-id="b283e-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b283e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b283e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b283e-122">-WhatIf</span></span>
<span data-ttu-id="b283e-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b283e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b283e-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b283e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b283e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b283e-125">CommonParameters</span></span>
<span data-ttu-id="b283e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b283e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b283e-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b283e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b283e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b283e-128">INPUTS</span></span>

## <span data-ttu-id="b283e-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b283e-129">OUTPUTS</span></span>

### <span data-ttu-id="b283e-130">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ılanguageextension</span><span class="sxs-lookup"><span data-stu-id="b283e-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="b283e-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b283e-131">NOTES</span></span>

<span data-ttu-id="b283e-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="b283e-132">ALIASES</span></span>

## <span data-ttu-id="b283e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b283e-133">RELATED LINKS</span></span>

