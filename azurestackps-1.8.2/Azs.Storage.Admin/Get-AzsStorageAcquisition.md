---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a53b5af4cf77ec961e65f8c0c0d84b05b4adfa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94106892"
---
# <span data-ttu-id="85a57-101">Get-AzsStorageAcquisition</span><span class="sxs-lookup"><span data-stu-id="85a57-101">Get-AzsStorageAcquisition</span></span>

## <span data-ttu-id="85a57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85a57-102">SYNOPSIS</span></span>
<span data-ttu-id="85a57-103">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="85a57-103">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="85a57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="85a57-104">SYNTAX</span></span>

```
Get-AzsStorageAcquisition [-FarmName] <String> [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="85a57-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="85a57-105">DESCRIPTION</span></span>
<span data-ttu-id="85a57-106">Blob sonuçları listesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="85a57-106">Returns a list of blob acquistions.</span></span>

## <span data-ttu-id="85a57-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="85a57-107">EXAMPLES</span></span>

### <span data-ttu-id="85a57-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="85a57-108">EXAMPLE 1</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="85a57-109">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="85a57-109">Get the list of blob acquistions.</span></span>

### <span data-ttu-id="85a57-110">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="85a57-110">EXAMPLE 2</span></span>
```
Get-AzsStorageAcquisition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Filter "startswith(properties/Storageaccount, 'Test'"
```

<span data-ttu-id="85a57-111">Blob alma işlemleri listesini alın.</span><span class="sxs-lookup"><span data-stu-id="85a57-111">Get the list of blob acquistions.</span></span>

## <span data-ttu-id="85a57-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="85a57-112">PARAMETERS</span></span>

### <span data-ttu-id="85a57-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="85a57-113">-FarmName</span></span>
<span data-ttu-id="85a57-114">Grup kimliği.</span><span class="sxs-lookup"><span data-stu-id="85a57-114">Farm Id.</span></span>

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

### <span data-ttu-id="85a57-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a57-115">-ResourceGroupName</span></span>
<span data-ttu-id="85a57-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="85a57-116">Resource group name.</span></span>

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

### <span data-ttu-id="85a57-117">-Filtre</span><span class="sxs-lookup"><span data-stu-id="85a57-117">-Filter</span></span>
<span data-ttu-id="85a57-118">Filtre dizesi</span><span class="sxs-lookup"><span data-stu-id="85a57-118">Filter string</span></span>

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

### <span data-ttu-id="85a57-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a57-119">CommonParameters</span></span>
<span data-ttu-id="85a57-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="85a57-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a57-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a57-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a57-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="85a57-122">INPUTS</span></span>

## <span data-ttu-id="85a57-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="85a57-123">OUTPUTS</span></span>

## <span data-ttu-id="85a57-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="85a57-124">NOTES</span></span>

## <span data-ttu-id="85a57-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="85a57-125">RELATED LINKS</span></span>
