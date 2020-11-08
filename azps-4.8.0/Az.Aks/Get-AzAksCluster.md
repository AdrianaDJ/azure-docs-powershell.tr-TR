---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268892"
---
# <span data-ttu-id="a36a0-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="a36a0-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="a36a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a36a0-102">SYNOPSIS</span></span>
<span data-ttu-id="a36a0-103">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="a36a0-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="a36a0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a36a0-104">SYNTAX</span></span>

### <span data-ttu-id="a36a0-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a36a0-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a36a0-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="a36a0-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a36a0-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a36a0-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a36a0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a36a0-108">DESCRIPTION</span></span>
<span data-ttu-id="a36a0-109">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="a36a0-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="a36a0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a36a0-110">EXAMPLES</span></span>

### <span data-ttu-id="a36a0-111">Tüm Kubernetes kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="a36a0-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="a36a0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a36a0-112">PARAMETERS</span></span>

### <span data-ttu-id="a36a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a36a0-113">-DefaultProfile</span></span>
<span data-ttu-id="a36a0-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a36a0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a36a0-115">-ID</span><span class="sxs-lookup"><span data-stu-id="a36a0-115">-Id</span></span>
<span data-ttu-id="a36a0-116">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="a36a0-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a36a0-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="a36a0-117">-Name</span></span>
<span data-ttu-id="a36a0-118">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="a36a0-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36a0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a36a0-119">-ResourceGroupName</span></span>
<span data-ttu-id="a36a0-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="a36a0-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a36a0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a36a0-121">CommonParameters</span></span>
<span data-ttu-id="a36a0-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a36a0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a36a0-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a36a0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a36a0-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a36a0-124">INPUTS</span></span>

### <span data-ttu-id="a36a0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a36a0-125">System.String</span></span>

## <span data-ttu-id="a36a0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a36a0-126">OUTPUTS</span></span>

### <span data-ttu-id="a36a0-127">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a36a0-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="a36a0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a36a0-128">NOTES</span></span>

## <span data-ttu-id="a36a0-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a36a0-129">RELATED LINKS</span></span>
