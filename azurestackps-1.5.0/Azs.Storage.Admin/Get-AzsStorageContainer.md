---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4847310f65a0b652d15321cd49583212ef5844d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571502"
---
# <span data-ttu-id="40f43-101">Get-AzsStorageContainer</span><span class="sxs-lookup"><span data-stu-id="40f43-101">Get-AzsStorageContainer</span></span>

## <span data-ttu-id="40f43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40f43-102">SYNOPSIS</span></span>
<span data-ttu-id="40f43-103">Belirtilen paylaşıma geçirilebileceğiniz kapsayıcıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="40f43-103">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="40f43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="40f43-104">SYNTAX</span></span>

```
Get-AzsStorageContainer [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-MaxCount] <Int32>] [[-StartIndex] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="40f43-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="40f43-105">DESCRIPTION</span></span>
<span data-ttu-id="40f43-106">Belirtilen paylaşıma geçirilebileceğiniz kapsayıcıların listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="40f43-106">Returns the list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="40f43-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="40f43-107">EXAMPLES</span></span>

### <span data-ttu-id="40f43-108">--------------------------ÖRNEK 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="40f43-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageContainer -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="40f43-109">Belirtilen paylaşıma geçirilebileceğiniz kapsayıcıların listesini edinin.</span><span class="sxs-lookup"><span data-stu-id="40f43-109">Get a list of containers which can be migrated in the specified share.</span></span>

## <span data-ttu-id="40f43-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="40f43-110">PARAMETERS</span></span>

### <span data-ttu-id="40f43-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="40f43-111">-FarmName</span></span>
<span data-ttu-id="40f43-112">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="40f43-112">Farm Id.</span></span>

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

### <span data-ttu-id="40f43-113">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="40f43-113">-MaxCount</span></span>
<span data-ttu-id="40f43-114">En fazla kapsayıcı sayısı.</span><span class="sxs-lookup"><span data-stu-id="40f43-114">The max count of containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100000000
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f43-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40f43-115">-ResourceGroupName</span></span>
<span data-ttu-id="40f43-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="40f43-116">Resource group name.</span></span>

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

### <span data-ttu-id="40f43-117">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="40f43-117">-ShareName</span></span>
<span data-ttu-id="40f43-118">Depolama kapsayıcılarını tutan paylaşım adı.</span><span class="sxs-lookup"><span data-stu-id="40f43-118">Share name which holds the storage containers.</span></span>

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

### <span data-ttu-id="40f43-119">-StartIndex</span><span class="sxs-lookup"><span data-stu-id="40f43-119">-StartIndex</span></span>
<span data-ttu-id="40f43-120">Kapsayıcıları al.</span><span class="sxs-lookup"><span data-stu-id="40f43-120">The start index of get containers.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40f43-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40f43-121">CommonParameters</span></span>
<span data-ttu-id="40f43-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="40f43-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40f43-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40f43-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40f43-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="40f43-124">INPUTS</span></span>

## <span data-ttu-id="40f43-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="40f43-125">OUTPUTS</span></span>

## <span data-ttu-id="40f43-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="40f43-126">NOTES</span></span>

## <span data-ttu-id="40f43-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="40f43-127">RELATED LINKS</span></span>

