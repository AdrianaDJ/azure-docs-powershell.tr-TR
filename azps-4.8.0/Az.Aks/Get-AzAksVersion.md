---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268890"
---
# <span data-ttu-id="b626f-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="b626f-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="b626f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b626f-102">SYNOPSIS</span></span>
<span data-ttu-id="b626f-103">Yönetilen Kubernetes kümesi oluşturmak için kullanılabilir sürümü listeleyin.</span><span class="sxs-lookup"><span data-stu-id="b626f-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="b626f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b626f-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b626f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b626f-105">DESCRIPTION</span></span>
<span data-ttu-id="b626f-106">Yönetilen Kubernetes kümesi oluşturmak için kullanılabilir sürümü listeleyin.</span><span class="sxs-lookup"><span data-stu-id="b626f-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="b626f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b626f-107">EXAMPLES</span></span>

### <span data-ttu-id="b626f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b626f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="b626f-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b626f-109">PARAMETERS</span></span>

### <span data-ttu-id="b626f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b626f-110">-DefaultProfile</span></span>
<span data-ttu-id="b626f-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b626f-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b626f-112">-Konum</span><span class="sxs-lookup"><span data-stu-id="b626f-112">-Location</span></span>
<span data-ttu-id="b626f-113">Kümenin Azure konumu.</span><span class="sxs-lookup"><span data-stu-id="b626f-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="b626f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b626f-114">CommonParameters</span></span>
<span data-ttu-id="b626f-115">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b626f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b626f-116">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b626f-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b626f-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b626f-117">INPUTS</span></span>

### <span data-ttu-id="b626f-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b626f-118">None</span></span>

## <span data-ttu-id="b626f-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b626f-119">OUTPUTS</span></span>

### <span data-ttu-id="b626f-120">Microsoft. Azure. Commands. aks. modeller. PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="b626f-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="b626f-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b626f-121">NOTES</span></span>

## <span data-ttu-id="b626f-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b626f-122">RELATED LINKS</span></span>
