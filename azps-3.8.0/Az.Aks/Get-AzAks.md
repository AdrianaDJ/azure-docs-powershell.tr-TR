---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: d88ac0feab52d5f62a06981d8fa178db6dad9578
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097451"
---
# <span data-ttu-id="6bd4e-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="6bd4e-101">Get-AzAks</span></span>

## <span data-ttu-id="6bd4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="6bd4e-103">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="6bd4e-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6bd4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6bd4e-104">SYNTAX</span></span>

### <span data-ttu-id="6bd4e-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6bd4e-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bd4e-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="6bd4e-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6bd4e-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bd4e-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bd4e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6bd4e-108">DESCRIPTION</span></span>
<span data-ttu-id="6bd4e-109">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="6bd4e-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6bd4e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6bd4e-110">EXAMPLES</span></span>

### <span data-ttu-id="6bd4e-111">Tüm Kubernetes kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="6bd4e-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="6bd4e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6bd4e-112">PARAMETERS</span></span>

### <span data-ttu-id="6bd4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bd4e-113">-DefaultProfile</span></span>
<span data-ttu-id="6bd4e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6bd4e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bd4e-115">-ID</span><span class="sxs-lookup"><span data-stu-id="6bd4e-115">-Id</span></span>
<span data-ttu-id="6bd4e-116">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="6bd4e-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6bd4e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6bd4e-117">-Name</span></span>
<span data-ttu-id="6bd4e-118">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="6bd4e-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6bd4e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bd4e-119">-ResourceGroupName</span></span>
<span data-ttu-id="6bd4e-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6bd4e-120">Resource group name</span></span>

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

### <span data-ttu-id="6bd4e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bd4e-121">CommonParameters</span></span>
<span data-ttu-id="6bd4e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6bd4e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bd4e-123">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bd4e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bd4e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6bd4e-124">INPUTS</span></span>

### <span data-ttu-id="6bd4e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6bd4e-125">System.String</span></span>

## <span data-ttu-id="6bd4e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6bd4e-126">OUTPUTS</span></span>

### <span data-ttu-id="6bd4e-127">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6bd4e-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="6bd4e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6bd4e-128">NOTES</span></span>

## <span data-ttu-id="6bd4e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6bd4e-129">RELATED LINKS</span></span>
