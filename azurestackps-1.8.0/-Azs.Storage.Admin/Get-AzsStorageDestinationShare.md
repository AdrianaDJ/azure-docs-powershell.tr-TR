---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93934835"
---
# <span data-ttu-id="83b36-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="83b36-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="83b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83b36-102">SYNOPSIS</span></span>
<span data-ttu-id="83b36-103">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="83b36-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="83b36-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="83b36-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="83b36-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="83b36-105">DESCRIPTION</span></span>
<span data-ttu-id="83b36-106">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="83b36-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="83b36-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="83b36-107">EXAMPLES</span></span>

### <span data-ttu-id="83b36-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="83b36-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="83b36-109">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="83b36-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="83b36-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="83b36-110">PARAMETERS</span></span>

### <span data-ttu-id="83b36-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="83b36-111">-FarmName</span></span>
<span data-ttu-id="83b36-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="83b36-112">Farm Id.</span></span>

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

### <span data-ttu-id="83b36-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b36-113">-ResourceGroupName</span></span>
<span data-ttu-id="83b36-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="83b36-114">Resource group name.</span></span>

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

### <span data-ttu-id="83b36-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="83b36-115">-SourceShareName</span></span>
<span data-ttu-id="83b36-116">Geçirilecek kapsayıcıları tutan paylaşımın adı.</span><span class="sxs-lookup"><span data-stu-id="83b36-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="83b36-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b36-117">CommonParameters</span></span>
<span data-ttu-id="83b36-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="83b36-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b36-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b36-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b36-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="83b36-120">INPUTS</span></span>

## <span data-ttu-id="83b36-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="83b36-121">OUTPUTS</span></span>

## <span data-ttu-id="83b36-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="83b36-122">NOTES</span></span>

## <span data-ttu-id="83b36-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="83b36-123">RELATED LINKS</span></span>

