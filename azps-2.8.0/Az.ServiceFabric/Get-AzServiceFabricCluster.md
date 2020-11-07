---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: fca4b226dbb265c0aa86147430b6f91e9cc4f326
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933196"
---
# <span data-ttu-id="4a26c-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="4a26c-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="4a26c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a26c-102">SYNOPSIS</span></span>
<span data-ttu-id="4a26c-103">Küme kaynağı ayrıntılarını edinin.</span><span class="sxs-lookup"><span data-stu-id="4a26c-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="4a26c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a26c-104">SYNTAX</span></span>

### <span data-ttu-id="4a26c-105">BySubscription (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a26c-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a26c-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4a26c-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a26c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4a26c-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a26c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a26c-108">DESCRIPTION</span></span>
<span data-ttu-id="4a26c-109">**Get-AzServiceFabricCluster** , küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4a26c-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="4a26c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a26c-110">EXAMPLES</span></span>

### <span data-ttu-id="4a26c-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4a26c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="4a26c-112">Bu komut, ' myCluster ' kümesi için küme kaynağı ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="4a26c-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="4a26c-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a26c-113">PARAMETERS</span></span>

### <span data-ttu-id="4a26c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a26c-114">-DefaultProfile</span></span>
<span data-ttu-id="4a26c-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a26c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a26c-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a26c-116">-Name</span></span>
<span data-ttu-id="4a26c-117">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="4a26c-117">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a26c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a26c-118">-ResourceGroupName</span></span>
<span data-ttu-id="4a26c-119">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4a26c-119">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a26c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a26c-120">CommonParameters</span></span>
<span data-ttu-id="4a26c-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a26c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a26c-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a26c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a26c-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a26c-123">INPUTS</span></span>

### <span data-ttu-id="4a26c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4a26c-124">System.String</span></span>

## <span data-ttu-id="4a26c-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a26c-125">OUTPUTS</span></span>

### <span data-ttu-id="4a26c-126">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="4a26c-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4a26c-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a26c-127">NOTES</span></span>

## <span data-ttu-id="4a26c-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a26c-128">RELATED LINKS</span></span>
