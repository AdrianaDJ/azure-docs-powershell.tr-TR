---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d9ff0746de44d2e5c3c67ea95b66dd3bd3902ca
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934856"
---
# <span data-ttu-id="9a1ce-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="9a1ce-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="9a1ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="9a1ce-103">Blob hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9a1ce-103">Returns the blob service.</span></span>

## <span data-ttu-id="9a1ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a1ce-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="9a1ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a1ce-105">DESCRIPTION</span></span>
<span data-ttu-id="9a1ce-106">Blob hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="9a1ce-106">Returns the blob service.</span></span>

## <span data-ttu-id="9a1ce-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a1ce-107">EXAMPLES</span></span>

### <span data-ttu-id="9a1ce-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9a1ce-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="9a1ce-109">Blob hizmetini edinin.</span><span class="sxs-lookup"><span data-stu-id="9a1ce-109">Get the blob service.</span></span>

## <span data-ttu-id="9a1ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a1ce-110">PARAMETERS</span></span>

### <span data-ttu-id="9a1ce-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9a1ce-111">-FarmName</span></span>
<span data-ttu-id="9a1ce-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="9a1ce-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1ce-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a1ce-113">-ResourceGroupName</span></span>
<span data-ttu-id="9a1ce-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9a1ce-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a1ce-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a1ce-115">CommonParameters</span></span>
<span data-ttu-id="9a1ce-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a1ce-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a1ce-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a1ce-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a1ce-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a1ce-118">INPUTS</span></span>

## <span data-ttu-id="9a1ce-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a1ce-119">OUTPUTS</span></span>

### <span data-ttu-id="9a1ce-120">Microsoft. AzureStack. Management. Storage. admin. modeller. BlobService</span><span class="sxs-lookup"><span data-stu-id="9a1ce-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="9a1ce-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a1ce-121">NOTES</span></span>

## <span data-ttu-id="9a1ce-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a1ce-122">RELATED LINKS</span></span>

