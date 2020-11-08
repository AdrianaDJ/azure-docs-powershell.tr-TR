---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0fb6da4bde577d5a69c5bd85261822e3cf1865d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935071"
---
# <span data-ttu-id="a68ec-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="a68ec-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="a68ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a68ec-102">SYNOPSIS</span></span>
<span data-ttu-id="a68ec-103">Blob hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a68ec-103">Returns the blob service.</span></span>

## <span data-ttu-id="a68ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a68ec-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="a68ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a68ec-105">DESCRIPTION</span></span>
<span data-ttu-id="a68ec-106">Blob hizmetini döndürür.</span><span class="sxs-lookup"><span data-stu-id="a68ec-106">Returns the blob service.</span></span>

## <span data-ttu-id="a68ec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a68ec-107">EXAMPLES</span></span>

### <span data-ttu-id="a68ec-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a68ec-108">EXAMPLE 1</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="a68ec-109">Blob hizmetini edinin.</span><span class="sxs-lookup"><span data-stu-id="a68ec-109">Get the blob service.</span></span>

## <span data-ttu-id="a68ec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a68ec-110">PARAMETERS</span></span>

### <span data-ttu-id="a68ec-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="a68ec-111">-FarmName</span></span>
<span data-ttu-id="a68ec-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="a68ec-112">Farm Id.</span></span>

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

### <span data-ttu-id="a68ec-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a68ec-113">-ResourceGroupName</span></span>
<span data-ttu-id="a68ec-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a68ec-114">Resource group name.</span></span>

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

### <span data-ttu-id="a68ec-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68ec-115">CommonParameters</span></span>
<span data-ttu-id="a68ec-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a68ec-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68ec-117">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68ec-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68ec-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a68ec-118">INPUTS</span></span>

## <span data-ttu-id="a68ec-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a68ec-119">OUTPUTS</span></span>

### <span data-ttu-id="a68ec-120">Microsoft. AzureStack. Management. Storage. admin. modeller. BlobService</span><span class="sxs-lookup"><span data-stu-id="a68ec-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="a68ec-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a68ec-121">NOTES</span></span>

## <span data-ttu-id="a68ec-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a68ec-122">RELATED LINKS</span></span>