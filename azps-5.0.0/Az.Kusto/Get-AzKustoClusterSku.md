---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclustersku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterSku.md
ms.openlocfilehash: 88b3104512b1cad4cddf98f521b44c6b638c05b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279016"
---
# <span data-ttu-id="ccd98-101">Get-AzKustoClusterSku</span><span class="sxs-lookup"><span data-stu-id="ccd98-101">Get-AzKustoClusterSku</span></span>

## <span data-ttu-id="ccd98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccd98-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd98-103">Kusto kaynak sağlayıcısı için uygun SKU 'Ları listeler.</span><span class="sxs-lookup"><span data-stu-id="ccd98-103">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="ccd98-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccd98-104">SYNTAX</span></span>

### <span data-ttu-id="ccd98-105">Liste (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ccd98-105">List (Default)</span></span>
```
Get-AzKustoClusterSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ccd98-106">List1</span><span class="sxs-lookup"><span data-stu-id="ccd98-106">List1</span></span>
```
Get-AzKustoClusterSku -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ccd98-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccd98-107">DESCRIPTION</span></span>
<span data-ttu-id="ccd98-108">Kusto kaynak sağlayıcısı için uygun SKU 'Ları listeler.</span><span class="sxs-lookup"><span data-stu-id="ccd98-108">Lists eligible SKUs for Kusto resource provider.</span></span>

## <span data-ttu-id="ccd98-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccd98-109">EXAMPLES</span></span>

### <span data-ttu-id="ccd98-110">Örnek 1: uygun SKU 'Ları listeler</span><span class="sxs-lookup"><span data-stu-id="ccd98-110">Example 1: Lists eligible SKUs</span></span>
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

<span data-ttu-id="ccd98-111">Yukarıdaki komut uygun SKU 'Ları listeler.</span><span class="sxs-lookup"><span data-stu-id="ccd98-111">The above command lists eligible SKUs.</span></span>

### <span data-ttu-id="ccd98-112">Örnek 2: belirli küme için uygun SKU 'Ları listeler</span><span class="sxs-lookup"><span data-stu-id="ccd98-112">Example 2: Lists eligible SKUs for specific cluster</span></span>
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

<span data-ttu-id="ccd98-113">Yukarıdaki komut, belirli küme için uygun SKU 'Ları listeler</span><span class="sxs-lookup"><span data-stu-id="ccd98-113">The above command lists eligible SKUs for specific cluster</span></span>

## <span data-ttu-id="ccd98-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccd98-114">PARAMETERS</span></span>

### <span data-ttu-id="ccd98-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ccd98-115">-ClusterName</span></span>
<span data-ttu-id="ccd98-116">Kusto kümesinin adı.</span><span class="sxs-lookup"><span data-stu-id="ccd98-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="ccd98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd98-117">-DefaultProfile</span></span>
<span data-ttu-id="ccd98-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ccd98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccd98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd98-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccd98-120">Kusto kümesini içeren kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="ccd98-120">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="ccd98-121">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ccd98-121">-SubscriptionId</span></span>
<span data-ttu-id="ccd98-122">Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ccd98-122">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ccd98-123">Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ccd98-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ccd98-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd98-124">CommonParameters</span></span>
<span data-ttu-id="ccd98-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccd98-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd98-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ccd98-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd98-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccd98-127">INPUTS</span></span>

## <span data-ttu-id="ccd98-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccd98-128">OUTPUTS</span></span>

### <span data-ttu-id="ccd98-129">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IAzureResourceSku</span><span class="sxs-lookup"><span data-stu-id="ccd98-129">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAzureResourceSku</span></span>

### <span data-ttu-id="ccd98-130">Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. ıskudescription</span><span class="sxs-lookup"><span data-stu-id="ccd98-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ISkuDescription</span></span>

## <span data-ttu-id="ccd98-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccd98-131">NOTES</span></span>

<span data-ttu-id="ccd98-132">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="ccd98-132">ALIASES</span></span>

## <span data-ttu-id="ccd98-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccd98-133">RELATED LINKS</span></span>

