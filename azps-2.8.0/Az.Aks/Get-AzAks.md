---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAks.md
ms.openlocfilehash: 34db847ba7a4051efab32a62c667d3d79ad4ac30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753688"
---
# <span data-ttu-id="c80aa-101">Get-AzAks</span><span class="sxs-lookup"><span data-stu-id="c80aa-101">Get-AzAks</span></span>

## <span data-ttu-id="c80aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c80aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c80aa-103">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="c80aa-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c80aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c80aa-104">SYNTAX</span></span>

### <span data-ttu-id="c80aa-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c80aa-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c80aa-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="c80aa-106">IdParameterSet</span></span>
```
Get-AzAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c80aa-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c80aa-107">NameParameterSet</span></span>
```
Get-AzAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c80aa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c80aa-108">DESCRIPTION</span></span>
<span data-ttu-id="c80aa-109">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="c80aa-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="c80aa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c80aa-110">EXAMPLES</span></span>

### <span data-ttu-id="c80aa-111">Tüm Kubernetes kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="c80aa-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzAks
```

## <span data-ttu-id="c80aa-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c80aa-112">PARAMETERS</span></span>

### <span data-ttu-id="c80aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c80aa-113">-DefaultProfile</span></span>
<span data-ttu-id="c80aa-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c80aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c80aa-115">-ID</span><span class="sxs-lookup"><span data-stu-id="c80aa-115">-Id</span></span>
<span data-ttu-id="c80aa-116">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="c80aa-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c80aa-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c80aa-117">-Name</span></span>
<span data-ttu-id="c80aa-118">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="c80aa-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c80aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c80aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="c80aa-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c80aa-120">Resource group name</span></span>

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

### <span data-ttu-id="c80aa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c80aa-121">CommonParameters</span></span>
<span data-ttu-id="c80aa-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c80aa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c80aa-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c80aa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c80aa-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c80aa-124">INPUTS</span></span>

### <span data-ttu-id="c80aa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c80aa-125">System.String</span></span>

## <span data-ttu-id="c80aa-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c80aa-126">OUTPUTS</span></span>

### <span data-ttu-id="c80aa-127">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c80aa-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c80aa-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c80aa-128">NOTES</span></span>

## <span data-ttu-id="c80aa-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c80aa-129">RELATED LINKS</span></span>
