---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a75fafa646839375bf9dc7f1a64b3084fd31ee4
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93935052"
---
# <span data-ttu-id="5a915-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="5a915-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="5a915-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a915-102">SYNOPSIS</span></span>
<span data-ttu-id="5a915-103">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5a915-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5a915-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a915-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a915-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a915-105">DESCRIPTION</span></span>
<span data-ttu-id="5a915-106">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="5a915-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5a915-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a915-107">EXAMPLES</span></span>

### <span data-ttu-id="5a915-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="5a915-108">EXAMPLE 1</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="5a915-109">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="5a915-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="5a915-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a915-110">PARAMETERS</span></span>

### <span data-ttu-id="5a915-111">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="5a915-111">-SourceShareName</span></span>
<span data-ttu-id="5a915-112">Geçirilecek kapsayıcıları tutan paylaşımın adı.</span><span class="sxs-lookup"><span data-stu-id="5a915-112">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="5a915-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5a915-113">-FarmName</span></span>
<span data-ttu-id="5a915-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="5a915-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a915-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a915-115">-ResourceGroupName</span></span>
<span data-ttu-id="5a915-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="5a915-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a915-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a915-117">CommonParameters</span></span>
<span data-ttu-id="5a915-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a915-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a915-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a915-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a915-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a915-120">INPUTS</span></span>

## <span data-ttu-id="5a915-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a915-121">OUTPUTS</span></span>

## <span data-ttu-id="5a915-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a915-122">NOTES</span></span>

## <span data-ttu-id="5a915-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a915-123">RELATED LINKS</span></span>