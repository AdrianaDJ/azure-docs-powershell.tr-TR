---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/get-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Get-AzureRmAks.md
ms.openlocfilehash: d30d9858a3050864f5cc86601adf6b598be8c54d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592835"
---
# <span data-ttu-id="6932d-101">Get-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="6932d-101">Get-AzureRmAks</span></span>

## <span data-ttu-id="6932d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6932d-102">SYNOPSIS</span></span>
<span data-ttu-id="6932d-103">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="6932d-103">List Kubernetes managed clusters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6932d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6932d-104">SYNTAX</span></span>

### <span data-ttu-id="6932d-105">ResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6932d-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmAks [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6932d-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="6932d-106">IdParameterSet</span></span>
```
Get-AzureRmAks [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6932d-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6932d-107">NameParameterSet</span></span>
```
Get-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6932d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6932d-108">DESCRIPTION</span></span>
<span data-ttu-id="6932d-109">Liste Kubernetes yönetilen kümeler.</span><span class="sxs-lookup"><span data-stu-id="6932d-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="6932d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6932d-110">EXAMPLES</span></span>

### <span data-ttu-id="6932d-111">Tüm Kubernetes kümelerini listeler</span><span class="sxs-lookup"><span data-stu-id="6932d-111">List all Kubernetes clusters</span></span>
```
PS C:\> Get-AzureRmAks
```

## <span data-ttu-id="6932d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6932d-112">PARAMETERS</span></span>

### <span data-ttu-id="6932d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6932d-113">-DefaultProfile</span></span>
<span data-ttu-id="6932d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6932d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6932d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="6932d-115">-Id</span></span>
<span data-ttu-id="6932d-116">Yönetilen Kubernetes kümesinin kimliği</span><span class="sxs-lookup"><span data-stu-id="6932d-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6932d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6932d-117">-Name</span></span>
<span data-ttu-id="6932d-118">Yönetilen Kubernetes kümeniz adı</span><span class="sxs-lookup"><span data-stu-id="6932d-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="6932d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6932d-119">-ResourceGroupName</span></span>
<span data-ttu-id="6932d-120">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6932d-120">Resource group name</span></span>

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

### <span data-ttu-id="6932d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6932d-121">CommonParameters</span></span>
<span data-ttu-id="6932d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6932d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6932d-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6932d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6932d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6932d-124">INPUTS</span></span>

### <span data-ttu-id="6932d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6932d-125">System.String</span></span>

## <span data-ttu-id="6932d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6932d-126">OUTPUTS</span></span>

### <span data-ttu-id="6932d-127">Microsoft. Azure. Commands. aks. modeller. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="6932d-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="6932d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6932d-128">NOTES</span></span>

## <span data-ttu-id="6932d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6932d-129">RELATED LINKS</span></span>
