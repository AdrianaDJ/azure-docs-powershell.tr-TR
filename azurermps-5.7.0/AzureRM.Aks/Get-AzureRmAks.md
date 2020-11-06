---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: ee8420a8869e1056dc0ee3d942b811c3f70d545d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592137"
---
# <span data-ttu-id="27a2a-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="27a2a-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="27a2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="27a2a-103">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="27a2a-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27a2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27a2a-104">SYNTAX</span></span>

### <span data-ttu-id="27a2a-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27a2a-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27a2a-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="27a2a-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27a2a-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="27a2a-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="27a2a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27a2a-108">DESCRIPTION</span></span>
<span data-ttu-id="27a2a-109">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="27a2a-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="27a2a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27a2a-110">EXAMPLES</span></span>

### <span data-ttu-id="27a2a-111">Tüm Kubernetes kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="27a2a-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="27a2a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27a2a-112">PARAMETERS</span></span>

### <span data-ttu-id="27a2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a2a-113">-DefaultProfile</span></span>
<span data-ttu-id="27a2a-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27a2a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a2a-115">-ID</span><span class="sxs-lookup"><span data-stu-id="27a2a-115">-Id</span></span>
<span data-ttu-id="27a2a-116">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="27a2a-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a2a-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="27a2a-117">-Name</span></span>
<span data-ttu-id="27a2a-118">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="27a2a-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a2a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a2a-119">-ResourceGroupName</span></span>
<span data-ttu-id="27a2a-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="27a2a-120">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a2a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a2a-121">CommonParameters</span></span>
<span data-ttu-id="27a2a-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27a2a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a2a-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27a2a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a2a-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27a2a-124">INPUTS</span></span>

### <span data-ttu-id="27a2a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="27a2a-125">System.String</span></span>

## <span data-ttu-id="27a2a-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27a2a-126">OUTPUTS</span></span>

### <span data-ttu-id="27a2a-127">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="27a2a-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="27a2a-128">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster, Microsoft. Azure. Commands. aks, Version = 0.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="27a2a-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster, Microsoft.Azure.Commands.Aks, Version=0.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="27a2a-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27a2a-129">NOTES</span></span>

## <span data-ttu-id="27a2a-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27a2a-130">RELATED LINKS</span></span>
