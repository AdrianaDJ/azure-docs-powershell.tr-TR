---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47ac85406955592cba566df505900e6c42befb7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933913"
---
# <span data-ttu-id="7da81-101">Get-AzsStorageDestinationShare</span><span class="sxs-lookup"><span data-stu-id="7da81-101">Get-AzsStorageDestinationShare</span></span>

## <span data-ttu-id="7da81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da81-102">SYNOPSIS</span></span>
<span data-ttu-id="7da81-103">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7da81-103">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="7da81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7da81-104">SYNTAX</span></span>

```
Get-AzsStorageDestinationShare [-SourceShareName] <String> [-FarmName] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="7da81-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7da81-105">DESCRIPTION</span></span>
<span data-ttu-id="7da81-106">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7da81-106">Returns a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="7da81-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7da81-107">EXAMPLES</span></span>

### <span data-ttu-id="7da81-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7da81-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageDestinationShare -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -SourceShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="7da81-109">Sistemin geçiş için en iyi aday olarak belirlediği hedef paylaşımların listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="7da81-109">Get a list of destination shares that the system considers as best candidates for migration.</span></span>

## <span data-ttu-id="7da81-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7da81-110">PARAMETERS</span></span>

### <span data-ttu-id="7da81-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="7da81-111">-FarmName</span></span>
<span data-ttu-id="7da81-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="7da81-112">Farm Id.</span></span>

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

### <span data-ttu-id="7da81-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da81-113">-ResourceGroupName</span></span>
<span data-ttu-id="7da81-114">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7da81-114">Resource group name.</span></span>

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

### <span data-ttu-id="7da81-115">-SourceShareName</span><span class="sxs-lookup"><span data-stu-id="7da81-115">-SourceShareName</span></span>
<span data-ttu-id="7da81-116">Geçirilecek kapsayıcıları tutan paylaşımın adı.</span><span class="sxs-lookup"><span data-stu-id="7da81-116">Name of the share which holds containers to be migrated.</span></span>

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

### <span data-ttu-id="7da81-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da81-117">CommonParameters</span></span>
<span data-ttu-id="7da81-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7da81-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da81-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da81-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da81-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7da81-120">INPUTS</span></span>

## <span data-ttu-id="7da81-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7da81-121">OUTPUTS</span></span>

## <span data-ttu-id="7da81-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7da81-122">NOTES</span></span>

## <span data-ttu-id="7da81-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7da81-123">RELATED LINKS</span></span>
