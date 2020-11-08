---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109966"
---
# <span data-ttu-id="6ef63-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="6ef63-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="6ef63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef63-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef63-103">Kusto kaynak sağlayıcısı için uygun SKU 'Ları listeler.</span><span class="sxs-lookup"><span data-stu-id="6ef63-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="6ef63-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ef63-104">SYNTAX</span></span>

### <span data-ttu-id="6ef63-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ef63-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ef63-106">List1</span><span class="sxs-lookup"><span data-stu-id="6ef63-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6ef63-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ef63-107">DESCRIPTION</span></span>
<span data-ttu-id="6ef63-108">Kusto kaynak sağlayıcısı için uygun SKU 'Ları listeler.</span><span class="sxs-lookup"><span data-stu-id="6ef63-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="6ef63-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ef63-109">EXAMPLES</span></span>

### <span data-ttu-id="6ef63-110">Örnek 1: uygun SKU 'Ları listeler</span><span class="sxs-lookup"><span data-stu-id="6ef63-110">Example 1: Lists eligible SKUs</span></span>
```powershell
PS C:\> Get-AzKustoClusterSku

Location             Name                        ResourceType Tier
--------             ----                        ------------ ----
{eastus2}            D13_v2                      clusters     Standard
{eastus2}            D14_v2                      clusters     Standard
{eastus2}            L8                          clusters     Standard
{eastus2}            L16                         clusters     Standard
{eastus2}            D11_v2                      clusters     Standard
{eastus2}            D12_v2                      clusters     Standard
{eastus2}            L4                          clusters     Standard
{eastus2}            Standard_D13_v2             clusters     Standard
{eastus2}            Standard_D14_v2             clusters     Standard
{eastus2}            Standard_L8s                clusters     Standard
{eastus2}            Standard_L16s               clusters     Standard
{eastus2}            Standard_D11_v2             clusters     Standard
{eastus2}            Standard_D12_v2             clusters     Standard
{eastus2}            Standard_L4s                clusters     Standard
{eastus2}            Standard_DS13_v2+1TB_PS     clusters     Standard
{eastus2}            Standard_DS13_v2+2TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+3TB_PS     clusters     Standard
{eastus2}            Standard_DS14_v2+4TB_PS     clusters     Standard
{eastus2}            Dev(No SLA)_Standard_D11_v2 clusters     Basic
{westcentralus}      D13_v2                      clusters     Standard
{westcentralus}      D14_v2                      clusters     Standard
{westcentralus}      D11_v2                      clusters     Standard
{westcentralus}      D12_v2                      clusters     Standard
{westcentralus}      Standard_D13_v2             clusters     Standard
{westcentralus}      Standard_D14_v2             clusters     Standard
{westcentralus}      Standard_D11_v2             clusters     Standard
{westcentralus}      Standard_D12_v2             clusters     Standard
{westcentralus}      Standard_DS13_v2+1TB_PS     clusters     Standard
{westcentralus}      Standard_DS13_v2+2TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+3TB_PS     clusters     Standard
{westcentralus}      Standard_DS14_v2+4TB_PS     clusters     Standard
...
```

<span data-ttu-id="6ef63-111">Yukarıdaki komut uygun SKU 'Ları listeler.</span><span class="sxs-lookup"><span data-stu-id="6ef63-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="6ef63-112">Örnek 2: belirli küme için uygun SKU 'Ları listeler</span><span class="sxs-lookup"><span data-stu-id="6ef63-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
```powershell
PS C:\>  Get-AzKustoClusterSku -ResourceGroupName testrg -ClusterName testnewkustocluster

ResourceType
------------
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
Microsoft.Kusto/clusters
...
```

<span data-ttu-id="6ef63-113">Yukarıdaki komut, belirli küme için uygun SKU 'Ları listeler</span><span class="sxs-lookup"><span data-stu-id="6ef63-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="6ef63-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ef63-114">PARAMETERS</span></span>

### <span data-ttu-id="6ef63-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6ef63-115">-ClusterName</span></span>
<span data-ttu-id="6ef63-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="6ef63-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ef63-117">-DefaultProfile</span></span>
<span data-ttu-id="6ef63-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ef63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ef63-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef63-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ef63-120">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="6ef63-120">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef63-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6ef63-121">-SubscriptionId</span></span>
<span data-ttu-id="6ef63-122">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6ef63-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6ef63-123">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="6ef63-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6ef63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef63-124">CommonParameters</span></span>
<span data-ttu-id="6ef63-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ef63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef63-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ef63-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef63-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ef63-127">INPUTS</span></span>

## <span data-ttu-id="6ef63-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ef63-128">OUTPUTS</span></span>

### <span data-ttu-id="6ef63-129">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="6ef63-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="6ef63-130">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıskudescription</span><span class="sxs-lookup"><span data-stu-id="6ef63-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="6ef63-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ef63-131">NOTES</span></span>

<span data-ttu-id="6ef63-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="6ef63-132">ALIASES</span></span>

## <span data-ttu-id="6ef63-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ef63-133">RELATED LINKS</span></span>

