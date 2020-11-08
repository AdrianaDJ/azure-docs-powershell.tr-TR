---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277895"
---
# <span data-ttu-id="88030-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="88030-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="88030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88030-102">SYNOPSIS</span></span>
<span data-ttu-id="88030-103">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="88030-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="88030-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="88030-104">SYNTAX</span></span>

### <span data-ttu-id="88030-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="88030-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="88030-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="88030-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88030-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88030-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88030-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="88030-108">DESCRIPTION</span></span>
<span data-ttu-id="88030-109">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="88030-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="88030-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="88030-110">EXAMPLES</span></span>

### <span data-ttu-id="88030-111">Tüm Kubernetes kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="88030-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="88030-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="88030-112">PARAMETERS</span></span>

### <span data-ttu-id="88030-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88030-113">-DefaultProfile</span></span>
<span data-ttu-id="88030-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="88030-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88030-115">-ID</span><span class="sxs-lookup"><span data-stu-id="88030-115">-Id</span></span>
<span data-ttu-id="88030-116">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="88030-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="88030-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="88030-117">-Name</span></span>
<span data-ttu-id="88030-118">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="88030-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="88030-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88030-119">-ResourceGroupName</span></span>
<span data-ttu-id="88030-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="88030-120">Resource group name</span></span>

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

### <span data-ttu-id="88030-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88030-121">CommonParameters</span></span>
<span data-ttu-id="88030-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="88030-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88030-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="88030-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88030-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="88030-124">INPUTS</span></span>

### <span data-ttu-id="88030-125">System. String</span><span class="sxs-lookup"><span data-stu-id="88030-125">System.String</span></span>

## <span data-ttu-id="88030-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="88030-126">OUTPUTS</span></span>

### <span data-ttu-id="88030-127">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="88030-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="88030-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="88030-128">NOTES</span></span>

## <span data-ttu-id="88030-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="88030-129">RELATED LINKS</span></span>
