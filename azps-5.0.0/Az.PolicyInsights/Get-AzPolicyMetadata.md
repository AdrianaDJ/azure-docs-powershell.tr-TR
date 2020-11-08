---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276032"
---
# <span data-ttu-id="48c4e-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="48c4e-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="48c4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="48c4e-103">Ilke meta veri kaynaklarını alır</span><span class="sxs-lookup"><span data-stu-id="48c4e-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="48c4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="48c4e-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48c4e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="48c4e-105">DESCRIPTION</span></span>
<span data-ttu-id="48c4e-106">**Get-Azilkedüzeltme** cmdlet 'i tüm ilke meta veri kaynaklarını veya belirli bir ilke meta veri kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="48c4e-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="48c4e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="48c4e-107">EXAMPLES</span></span>

### <span data-ttu-id="48c4e-108">Örnek 1: tüm ilke meta veri kaynaklarını alma</span><span class="sxs-lookup"><span data-stu-id="48c4e-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="48c4e-109">Bu komut tüm ilke meta veri kaynaklarını alır</span><span class="sxs-lookup"><span data-stu-id="48c4e-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="48c4e-110">Örnek 2:10 poliçe meta veri kaynağı topluluğunu alma</span><span class="sxs-lookup"><span data-stu-id="48c4e-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="48c4e-111">Bu komut 10 poliçe meta veri kaynağı koleksiyonunu alır</span><span class="sxs-lookup"><span data-stu-id="48c4e-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="48c4e-112">Örnek 3: ' ACF1348 ' adlı tek bir ilke meta veri kaynağı alma</span><span class="sxs-lookup"><span data-stu-id="48c4e-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="48c4e-113">Bu komut, ' ACF1348 ' adlı tek bir ilke meta veri kaynağı alır</span><span class="sxs-lookup"><span data-stu-id="48c4e-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="48c4e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="48c4e-114">PARAMETERS</span></span>

### <span data-ttu-id="48c4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c4e-115">-DefaultProfile</span></span>
<span data-ttu-id="48c4e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="48c4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48c4e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="48c4e-117">-Name</span></span>
<span data-ttu-id="48c4e-118">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="48c4e-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48c4e-119">-Üst</span><span class="sxs-lookup"><span data-stu-id="48c4e-119">-Top</span></span>
<span data-ttu-id="48c4e-120">Döndürülecek en fazla ilke meta veri kaynağı sayısı.</span><span class="sxs-lookup"><span data-stu-id="48c4e-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48c4e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c4e-121">CommonParameters</span></span>
<span data-ttu-id="48c4e-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="48c4e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c4e-123">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="48c4e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c4e-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="48c4e-124">INPUTS</span></span>

### <span data-ttu-id="48c4e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="48c4e-125">System.String</span></span>

## <span data-ttu-id="48c4e-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="48c4e-126">OUTPUTS</span></span>

### <span data-ttu-id="48c4e-127">Microsoft. Azure. Commands. Policınsi. model. PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="48c4e-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="48c4e-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="48c4e-128">NOTES</span></span>

## <span data-ttu-id="48c4e-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="48c4e-129">RELATED LINKS</span></span>
