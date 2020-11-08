---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclustername
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Test-AzKustoClusterName.md
ms.openlocfilehash: c6b2f462ac66ab48b50e7555a3b5bf7c844aae3a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096593"
---
# <span data-ttu-id="72b7e-101">Test-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="72b7e-101">Test-AzKustoClusterName</span></span>

## <span data-ttu-id="72b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="72b7e-103">Verilen bir kusto küme adının olup olmadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="72b7e-103">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="72b7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="72b7e-104">SYNTAX</span></span>

```
Test-AzKustoClusterName -Location <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="72b7e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="72b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="72b7e-106">Verilen bir kusto küme adının olup olmadığını denetleyin.</span><span class="sxs-lookup"><span data-stu-id="72b7e-106">Check if a given Kusto cluster name is available.</span></span>

## <span data-ttu-id="72b7e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="72b7e-107">EXAMPLES</span></span>

### <span data-ttu-id="72b7e-108">Örnek 1-kullanımda olan bir kusto küme adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="72b7e-108">Example 1 - Check the availability of a Kusto cluster name which is in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
False                   mykustocluster      Name 'mykustocluster' with type Engine is already taken. Please specify a different name
```

<span data-ttu-id="72b7e-109">Yukarıdaki komut, "mykustocluster" adlı kusto kümesinin "Merkezi ABD" bölgesinde bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="72b7e-109">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

### <span data-ttu-id="72b7e-110">Örnek 2-kullanımda olmayan bir kusto küme adının kullanılabilirliğini denetleme</span><span class="sxs-lookup"><span data-stu-id="72b7e-110">Example 2 - Check the availability of a Kusto cluster name which is not in use</span></span>

```
PS C:\> Test-AzKustoClusterName -Location 'Central US' -Name mykustocluster

NameAvailable       Name                        Message
-------------           ----                            -------
 True                   mykustocluster
```

<span data-ttu-id="72b7e-111">Yukarıdaki komut, "mykustocluster" adlı kusto kümesinin "Merkezi ABD" bölgesinde bulunup bulunmadığını döndürür.</span><span class="sxs-lookup"><span data-stu-id="72b7e-111">The above command returns whether or not a Kusto cluster named "mykustocluster" exists in the "Central US" region.</span></span>

## <span data-ttu-id="72b7e-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="72b7e-112">PARAMETERS</span></span>

### <span data-ttu-id="72b7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b7e-113">-DefaultProfile</span></span>
<span data-ttu-id="72b7e-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="72b7e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72b7e-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="72b7e-115">-Location</span></span>
<span data-ttu-id="72b7e-116">Denetlenecek konum.</span><span class="sxs-lookup"><span data-stu-id="72b7e-116">The location where to check.</span></span>

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

### <span data-ttu-id="72b7e-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="72b7e-117">-Name</span></span>
<span data-ttu-id="72b7e-118">Belirli bir kümenin adı.</span><span class="sxs-lookup"><span data-stu-id="72b7e-118">Name of a specific cluster.</span></span>

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

### <span data-ttu-id="72b7e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b7e-119">CommonParameters</span></span>
<span data-ttu-id="72b7e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="72b7e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b7e-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72b7e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b7e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="72b7e-122">INPUTS</span></span>

### <span data-ttu-id="72b7e-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="72b7e-123">None</span></span>

## <span data-ttu-id="72b7e-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="72b7e-124">OUTPUTS</span></span>

### <span data-ttu-id="72b7e-125">Microsoft. Azure. Commands. kusto. modeller. Pskustoclusternameuygunluk</span><span class="sxs-lookup"><span data-stu-id="72b7e-125">Microsoft.Azure.Commands.Kusto.Models.PSKustoClusterNameAvailability</span></span>

## <span data-ttu-id="72b7e-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="72b7e-126">NOTES</span></span>

## <span data-ttu-id="72b7e-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="72b7e-127">RELATED LINKS</span></span>
